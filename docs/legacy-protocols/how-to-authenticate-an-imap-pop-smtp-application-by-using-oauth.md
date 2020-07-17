---
title: 使用 OAuth 对 IMAP、POP 或 SMTP 连接进行身份验证
description: 了解如何对 IMAP、POP 和 SMTP 应用程序使用 OAuth 身份验证。
author: svpsiva
ms.date: 02/19/2020
ms.audience: Developer
ms.openlocfilehash: f83a932790cde558e741ece1e87403103aff18fd
ms.sourcegitcommit: eeda51cb037aa25566adb293f25574674fdb2d9e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/01/2020
ms.locfileid: "45012557"
---
# <a name="authenticate-an-imap-pop-or-smtp-connection-using-oauth"></a>使用 OAuth 对 IMAP、POP 或 SMTP 连接进行身份验证

了解如何使用 OAuth 身份验证连接 IMAP、POP 或 SMTP 协议以及访问 Office 365 用户的电子邮件数据。

> Outlook.com 用户不支持 OAuth2 支持 IMAP、POP、SMTP 协议（如下所述）。

如果你不熟悉 OAuth 2.0，请先阅读[Microsoft identity platform （2.0）概述](/azure/active-directory/develop/v2-overview)。 该文档向你介绍 Microsoft identity platform 的不同组件，包括 Sdk。

您可以使用 Azure Active Directory 提供的 OAuth 身份验证服务，使应用程序能够与 IMAP、POP 或 SMTP 协议连接，以便在 Office 365 中访问 Exchange Online。 若要将 OAuth 与应用程序一起使用，您需要执行以下操作：

1. 向 Azure Active Directory[注册应用程序](#register-your-application)。
1. 在 Azure Active Directory 中[配置应用程序](#configure-your-application)。
1. 从令牌服务器[获取访问令牌](#get-an-access-token)。
1. 使用访问令牌[对连接请求进行身份验证](#authenticate-connection-requests)。

## <a name="register-your-application"></a>注册应用程序

若要使用 OAuth，必须向 Azure Active Directory 注册应用程序。

按照在[Microsoft identity platform 中注册应用程序](/azure/active-directory/develop/quickstart-register-app)中列出的说明创建新的应用程序。

## <a name="configure-your-application"></a>配置应用程序

按照[Configure a client application to access Web api](/azure/active-directory/develop/quickstart-configure-app-access-web-apis)中列出的说明操作。

确保添加以下一个或多个与要与之集成的协议对应的权限范围。 在 "**添加权限**向导" 中，选择 " **Microsoft Graph** "，然后选择 "**委派权限**" 以查找列出的以下权限范围。

| 协议  | 权限范围        |
|-----------|-------------------------|
| IMAP      | `IMAP.AccessAsUser.All` |
| 弹出式       | `POP.AccessAsUser.All`  |
| SMTP 身份验证 | `SMTP.Send`             |

## <a name="get-an-access-token"></a>获取访问令牌

您可以使用我们的[MSAL 客户端库](/azure/active-directory/develop/msal-overview)之一从客户端应用程序中获取访问令牌。

或者，也可以从以下列表中选择一个合适的流，并按照相应的步骤调用基础标识平台 REST Api 并检索访问令牌。

1. [OAuth2 授权代码流](/azure/active-directory/develop/v2-oauth2-auth-code-flow)
1. [OAuth2 设备授权授予流](/azure/active-directory/develop/v2-oauth2-device-code)

不支持通过 OAuth2 客户端凭据授予流的对 IMAP、POP、SMTP 身份验证协议的 OAuth 访问权限。 如果您的应用程序需要对 Microsoft 365 组织中的所有邮箱具有持久访问权限，我们建议您使用 Microsoft Graph Api，这些 Api 允许没有用户的访问，启用粒度权限，并允许管理员将此类访问权限限定为特定的一组邮箱。

在授权应用程序和请求访问令牌时，请确保指定完整的作用域（包括 Outlook 资源 Url）。

| 协议  | 权限范围字符串 |
|-----------|-------------------------|
| IMAP      | `https://outlook.office.com/IMAP.AccessAsUser.All` |
| 弹出式       | `https://outlook.office.com/POP.AccessAsUser.All`  |
| SMTP 身份验证 | `https://outlook.office.com/SMTP.Send`             |

此外，还可以请求[offline_access](/azure/active-directory/develop/v2-permissions-and-consent#offline_access)范围。 当用户批准 offline_access 范围时，您的应用程序可以从 Microsoft identity platform 令牌终结点接收刷新令牌。 刷新令牌的生存期较长。 您的应用程序可以将新的访问令牌作为旧令牌过期。

## <a name="authenticate-connection-requests"></a>对连接请求进行身份验证

您可以使用[适用于 office 365 的 IMAP 和 POP 电子邮件设置](https://support.office.com/article/pop-and-imap-email-settings-for-outlook-8361e398-8af4-4e97-b147-6c6c4ac95353)，启动到 office 365 邮件服务器的连接。

### <a name="sasl-xoauth2"></a>SASL XOAUTH2

与的 OAuth 集成要求您的应用程序使用 SASL XOAUTH2 格式编码和传输访问令牌。 SASL XOAUTH2 将用户名、访问令牌按以下格式进行编码：

```text
base64("user=" + userName + "^Aauth=Bearer " + accessToken + "^A^A")
```

`^A`代表 a**控件**  +  **A** （ `%x01` ）。

例如，使用 access 令牌访问的 SASL XOAUTH2 格式 `test@contoso.onmicrosoft.com` `EwBAAl3BAAUFFpUAo7J3Ve0bjLBWZWCclRC3EoAA` 为：

```text
base64("user=test@contoso.onmicrosoft.com^Aauth=Bearer EwBAAl3BAAUFFpUAo7J3Ve0bjLBWZWCclRC3EoAA^A^A")
```

在 base64 编码之后，这会转换为以下字符串。 请注意，插入换行符的目的是为了提高可读性。

```text
dXNlcj10ZXN0QGNvbnRvc28ub25taWNyb3NvZnQuY29tAWF1dGg9QmVhcmVy
IEV3QkFBbDNCQUFVRkZwVUFvN0ozVmUwYmpMQldaV0NjbFJDM0VvQUEBAQ==
```

### <a name="sasl-xoauth2-authentication-for-shared-mailboxes-in-office-365"></a>Office 365 中的共享邮箱的 SASL XOAUTH2 身份验证

如果使用 OAuth 的共享邮箱访问，应用程序需要代表用户获取访问令牌，而将 SASL XOAUTH2 编码字符串中的 userName 字段替换为共享邮箱的电子邮件地址。 

### <a name="imap-protocol-exchange"></a>IMAP 协议交换

若要对 IMAP 服务器连接进行身份验证，客户端将必须使用 `AUTHENTICATE` 以下格式的命令进行响应：

```text
AUTHENTICATE XOAUTH2 <base64 string in XOAUTH2 format>
```

导致身份验证成功的示例客户端/服务器消息交换：

```text
[connection begins]
C: C01 CAPABILITY
S: * CAPABILITY … AUTH=XOAUTH2
S: C01 OK Completed
C: A01 AUTHENTICATE XOAUTH2 dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlYXJlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMjl0Q2cBAQ==
S: A01 OK AUTHENTICATE completed.
```

导致身份验证失败的示例客户端/服务器消息交换：

```text
[connection begins]
S: * CAPABILITY … AUTH=XOAUTH2
S: C01 OK Completed
C: A01 AUTHENTICATE XOAUTH2 dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlYXJlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMjl0Q2cBAQ==
S: A01 NO AUTHENTICATE failed.
```

### <a name="pop-protocol-exchange"></a>POP 协议交换

若要对 POP 服务器连接进行身份验证，客户端必须使用 `AUTH` 以下格式的命令拆分成两行：    

```text 
AUTH XOAUTH2 
<base64 string in XOAUTH2 format>   
``` 

导致身份验证成功的示例客户端/服务器消息交换：    

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

导致身份验证失败的示例客户端/服务器消息交换：    

```text 
[connection begins] 
C: AUTH XOAUTH2     
S: +    
C: dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlY    
XJlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMj   
l0Q2cBAQ=   
S: -ERR Authentication failure: unknown user name or bad password.  
```

### <a name="smtp-protocol-exchange"></a>SMTP 协议交换

若要对 SMTP 服务器连接进行身份验证，客户端将必须使用 `AUTH` 以下格式的命令进行响应：

```text
AUTH XOAUTH2 <base64 string in XOAUTH2 format>
```

导致身份验证成功的示例客户端/服务器消息交换：

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

导致身份验证失败的示例客户端/服务器消息交换：

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

- [Exchange 中的身份验证和 EWS](../exchange-web-services/authentication-and-ews-in-exchange.md)
- [IMAP、POP 连接设置](https://support.office.com/article/pop-and-imap-email-settings-for-outlook-8361e398-8af4-4e97-b147-6c6c4ac95353)
- [Internet 邮件访问协议](https://tools.ietf.org/html/rfc3501)
- [邮局协议](https://tools.ietf.org/html/rfc1081)
- [SMTP 服务扩展以进行身份验证](https://tools.ietf.org/html/rfc4954)
