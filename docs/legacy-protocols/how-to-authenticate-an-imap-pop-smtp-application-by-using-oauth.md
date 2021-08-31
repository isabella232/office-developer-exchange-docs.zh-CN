---
title: 使用 OAuth 对 IMAP、POP 或 SMTP 连接进行身份验证
description: 了解如何将 OAuth 身份验证用于 IMAP、POP 和 SMTP 应用程序。
author: svpsiva
ms.date: 07/08/2021
ms.audience: Developer
ms.openlocfilehash: 4a307a6e329d5320b2b304d17a78a61db6d111bd
ms.sourcegitcommit: 357b882a02e37b380a23b8a45b15f9c006a40b02
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/31/2021
ms.locfileid: "58764586"
---
# <a name="authenticate-an-imap-pop-or-smtp-connection-using-oauth"></a>使用 OAuth 对 IMAP、POP 或 SMTP 连接进行身份验证

了解如何使用 OAuth 身份验证与 IMAP、POP 或 SMTP 协议连接以及访问用户的电子邮件Office 365数据。

> 以下所述的 IMAP、POP 和 SMTP 协议的 OAuth2 支持适用于包括 Microsoft 365 (和 Office web 版) Outlook.com 用户的 OAuth2。

如果您不熟悉 OAuth 2.0 协议，请首先阅读有关[OAuth 2.0](/azure/active-directory/develop/active-directory-v2-protocols)协议Microsoft 标识平台概述。 若要了解有关实现 OAuth 2.0 协议以对用户进行身份验证和访问安全 API 的 Microsoft Authentication Libariers (MSAL) ，请阅读 [MSAL 概述](/azure/active-directory/develop/msal-overview)。

您可以使用由 Azure Active Directory 提供的 OAuth 身份验证服务，使您的应用程序能够与 IMAP、POP 或 SMTP 协议连接，以访问 Exchange Online 中的Office 365。 若要将 OAuth 与应用程序一同使用，需要：

1. 使用 Azure Active Directory [注册应用程序](#register-your-application)。
1. [在应用程序中配置](#configure-your-application)Azure Active Directory。
1. [从令牌服务器](#get-an-access-token) 获取访问令牌。
1. [使用访问令牌](#authenticate-connection-requests) 对连接请求进行身份验证。

## <a name="register-your-application"></a>注册应用程序

若要使用 OAuth，应用程序必须注册到 Azure Active Directory。

按照向[应用程序注册中列出的](/azure/active-directory/develop/quickstart-register-app)Microsoft 标识平台创建新应用程序。

## <a name="get-an-access-token"></a>获取访问令牌

您可以使用我们的 [MSAL 客户端库之](/azure/active-directory/develop/msal-overview) 一从客户端应用程序获取访问令牌。

或者，也可以从以下列表中选择相应的流，并按照相应步骤调用基础标识平台 REST API 并检索访问令牌。

1. [OAuth2 授权代码流](/azure/active-directory/develop/v2-oauth2-auth-code-flow)
1. [OAuth2 设备授权授予流](/azure/active-directory/develop/v2-oauth2-device-code)

不支持通过 OAuth2 客户端凭据授予流对 IMAP、POP、SMTP AUTH 协议的 OAuth 访问。 如果您的应用程序需要永久访问 Microsoft 365 组织的所有邮箱，我们建议您使用 Microsoft Graph API（允许无需用户访问）启用粒度权限，并允许管理员将此类访问范围设定为一组特定的邮箱。

在授权应用程序和请求访问令牌时，Outlook包括资源 URL 的完整范围。

| 协议  | 权限范围字符串 |
|-----------|-------------------------|
| IMAP      | `https://outlook.office.com/IMAP.AccessAsUser.All` |
| POP       | `https://outlook.office.com/POP.AccessAsUser.All`  |
| SMTP AUTH | `https://outlook.office.com/SMTP.Send`             |

此外，还可以 [请求offline_access范围](/azure/active-directory/develop/v2-permissions-and-consent#offline_access) 。 当用户批准此offline_access时，你的应用可以从令牌Microsoft 标识平台刷新令牌。 刷新令牌长期使用。 当较旧的访问令牌过期时，你的应用可以获取新的访问令牌。

## <a name="authenticate-connection-requests"></a>验证连接请求

可以使用邮件服务器的 IMAP Office 365 POP 电子邮件设置启动与邮件[服务器Office 365。](https://support.office.com/article/pop-and-imap-email-settings-for-outlook-8361e398-8af4-4e97-b147-6c6c4ac95353)

### <a name="sasl-xoauth2"></a>SASL XOAUTH2

OAuth 集成要求应用程序使用 SASL XOAUTH2 格式编码和传输访问令牌。 SASL XOAUTH2 将用户名和访问令牌一起编码，格式如下：

```text
base64("user=" + userName + "^Aauth=Bearer " + accessToken + "^A^A")
```

`^A`代表控件  +  **A** `%x01` () 。

例如，使用访问令牌访问的 SASL XOAUTH2 `test@contoso.onmicrosoft.com` 格式 `EwBAAl3BAAUFFpUAo7J3Ve0bjLBWZWCclRC3EoAA` 为：

```text
base64("user=test@contoso.onmicrosoft.com^Aauth=Bearer EwBAAl3BAAUFFpUAo7J3Ve0bjLBWZWCclRC3EoAA^A^A")
```

base64 编码后，将转换为以下字符串。 请注意，插入换行符是为了可读性。

```text
dXNlcj10ZXN0QGNvbnRvc28ub25taWNyb3NvZnQuY29tAWF1dGg9QmVhcmVy
IEV3QkFBbDNCQUFVRkZwVUFvN0ozVmUwYmpMQldaV0NjbFJDM0VvQUEBAQ==
```

### <a name="sasl-xoauth2-authentication-for-shared-mailboxes-in-office-365"></a>OFFICE 365 中的共享邮箱的 SASL XOAUTH2 Office 365

如果使用 OAuth 访问共享邮箱，应用程序需要代表用户获取访问令牌，但需要将 SASL XOAUTH2 编码字符串中的 userName 字段替换为共享邮箱的电子邮件地址。 

### <a name="imap-protocol-exchange"></a>IMAP 协议Exchange

若要对 IMAP 服务器连接进行身份验证，客户端必须采用以下 `AUTHENTICATE` 格式的命令进行响应：

```text
AUTHENTICATE XOAUTH2 <base64 string in XOAUTH2 format>
```

导致身份验证成功的客户端-服务器邮件交换示例：

```text
[connection begins]
C: C01 CAPABILITY
S: * CAPABILITY … AUTH=XOAUTH2
S: C01 OK Completed
C: A01 AUTHENTICATE XOAUTH2 dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlYXJlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMjl0Q2cBAQ==
S: A01 OK AUTHENTICATE completed.
```

导致身份验证失败的客户端-服务器邮件交换示例：

```text
[connection begins]
S: * CAPABILITY … AUTH=XOAUTH2
S: C01 OK Completed
C: A01 AUTHENTICATE XOAUTH2 dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlYXJlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMjl0Q2cBAQ==
S: A01 NO AUTHENTICATE failed.
```

### <a name="pop-protocol-exchange"></a>POP 协议Exchange

若要对 POP 服务器连接进行身份验证，客户端必须按以下格式将命令拆分为两行 `AUTH` 进行响应：    

```text 
AUTH XOAUTH2 
<base64 string in XOAUTH2 format>   
``` 

导致身份验证成功的客户端-服务器邮件交换示例：    

```text 
[connection begins] 
C: AUTH XOAUTH2     
S: +    
C: dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlYX   
JlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMjl0  
Q2cBAQ==    
S: +OK User successfully authenticated. 
[connection continues...]   
``` 

导致身份验证失败的客户端-服务器邮件交换示例：    

```text 
[connection begins] 
C: AUTH XOAUTH2     
S: +    
C: dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlY    
XJlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMj   
l0Q2cBAQ=   
S: -ERR Authentication failure: unknown user name or bad password.  
```

### <a name="smtp-protocol-exchange"></a>SMTP 协议Exchange

若要对 SMTP 服务器连接进行身份验证，客户端必须采用以下 `AUTH` 格式的命令进行响应：

```text
AUTH XOAUTH2 <base64 string in XOAUTH2 format>
```

导致身份验证成功的客户端-服务器邮件交换示例：

```text
[connection begins]
C: auth xoauth2
S: 334
C: dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlY
XJlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMj
l0Q2cBAQ==
S: 235 2.7.0 Authentication successful
[connection continues...]
```

导致身份验证失败的客户端-服务器邮件交换示例：

```text
[connection begins]
C: auth xoauth2
S: 334
C: dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlY
XJlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMj
l0Q2cBAQ==
S: 535 5.7.3 Authentication unsuccessful [SN2PR00CA0018.namprd00.prod.outlook.com]
```

## <a name="see-also"></a>另请参阅

- [在 Exchange 中的身份验证和 EWS](../exchange-web-services/authentication-and-ews-in-exchange.md)
- [IMAP、POP 连接设置](https://support.office.com/article/pop-and-imap-email-settings-for-outlook-8361e398-8af4-4e97-b147-6c6c4ac95353)
- [Internet 邮件访问协议](https://tools.ietf.org/html/rfc3501)
- [后期Office协议](https://tools.ietf.org/html/rfc1081)
- [身份验证的 SMTP 服务扩展](https://tools.ietf.org/html/rfc4954)
