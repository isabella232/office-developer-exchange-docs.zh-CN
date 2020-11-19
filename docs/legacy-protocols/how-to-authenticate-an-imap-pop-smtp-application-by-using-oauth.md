---
title: 使用 OAuth 对 IMAP、POP 或 SMTP 连接进行身份验证
description: 了解如何对 IMAP、POP 和 SMTP 应用程序使用 OAuth 身份验证。
author: svpsiva
ms.date: 02/19/2020
ms.audience: Developer
ms.openlocfilehash: 4662aa904ed162edcced6c096eac8cf636180f6a
ms.sourcegitcommit: 37d4ecd4f469690ba1de87baad2f2f58c40c96ba
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49348813"
---
# <a name="authenticate-an-imap-pop-or-smtp-connection-using-oauth"></a><span data-ttu-id="01d83-103">使用 OAuth 对 IMAP、POP 或 SMTP 连接进行身份验证</span><span class="sxs-lookup"><span data-stu-id="01d83-103">Authenticate an IMAP, POP or SMTP connection using OAuth</span></span>

<span data-ttu-id="01d83-104">了解如何使用 OAuth 身份验证连接 IMAP、POP 或 SMTP 协议以及访问 Office 365 用户的电子邮件数据。</span><span class="sxs-lookup"><span data-stu-id="01d83-104">Learn how to use OAuth authentication to connect with IMAP, POP or SMTP protocols and access email data for Office 365 users.</span></span>

> <span data-ttu-id="01d83-105">OAuth2 支持 IMAP、POP、SMTP 协议（如下面所述）对 Microsoft 365 (（包括 web 上的 Office) 和 Outlook.com 用户）都受支持。</span><span class="sxs-lookup"><span data-stu-id="01d83-105">OAuth2 support for IMAP, POP, SMTP protocols as described below is supported for both Microsoft 365 (which includes Office on the web) and Outlook.com users.</span></span>

<span data-ttu-id="01d83-106">如果你不熟悉 OAuth 2.0 协议，请先阅读 [Microsoft identity platform 概述中的 OAuth 2.0 协议](/azure/active-directory/develop/active-directory-v2-protocols)。</span><span class="sxs-lookup"><span data-stu-id="01d83-106">If you're not familiar with the OAuth 2.0 protocol, start by reading the [OAuth 2.0 protocol on Microsoft identity platform overview](/azure/active-directory/develop/active-directory-v2-protocols).</span></span> <span data-ttu-id="01d83-107">若要了解有关 Microsoft 身份验证 Libariers (MSAL) 的详细信息，该协议可实施 OAuth 2.0 协议以对用户进行身份验证并访问安全 Api，请阅读 [MSAL 概述](/azure/active-directory/develop/msal-overview)。</span><span class="sxs-lookup"><span data-stu-id="01d83-107">To learn more about the Microsoft Authentication Libariers (MSAL), which implement the OAuth 2.0 protocol to authenticate users and access secure APIs, read the [MSAL overview](/azure/active-directory/develop/msal-overview).</span></span>

<span data-ttu-id="01d83-108">您可以使用 Azure Active Directory 提供的 OAuth 身份验证服务，使应用程序能够与 IMAP、POP 或 SMTP 协议连接，以便在 Office 365 中访问 Exchange Online。</span><span class="sxs-lookup"><span data-stu-id="01d83-108">You can use the OAuth authentication service provided by Azure Active Directory to enable your application to connect with IMAP, POP or SMTP protocols to access Exchange Online in Office 365.</span></span> <span data-ttu-id="01d83-109">若要将 OAuth 与应用程序一起使用，您需要执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="01d83-109">To use OAuth with your application you need to:</span></span>

1. <span data-ttu-id="01d83-110">使用 Azure Active Directory [注册应用程序](#register-your-application)。</span><span class="sxs-lookup"><span data-stu-id="01d83-110">[Register your application](#register-your-application) with Azure Active Directory.</span></span>
1. <span data-ttu-id="01d83-111">在 Azure Active Directory 中[配置应用程序](#configure-your-application)。</span><span class="sxs-lookup"><span data-stu-id="01d83-111">[Configure your application](#configure-your-application) in Azure Active Directory.</span></span>
1. <span data-ttu-id="01d83-112">从令牌服务器[获取访问令牌](#get-an-access-token)。</span><span class="sxs-lookup"><span data-stu-id="01d83-112">[Get an access token](#get-an-access-token) from a token server.</span></span>
1. <span data-ttu-id="01d83-113">使用访问令牌[对连接请求进行身份验证](#authenticate-connection-requests)。</span><span class="sxs-lookup"><span data-stu-id="01d83-113">[Authenticate connection requests](#authenticate-connection-requests) with an access token.</span></span>

## <a name="register-your-application"></a><span data-ttu-id="01d83-114">注册应用程序</span><span class="sxs-lookup"><span data-stu-id="01d83-114">Register your application</span></span>

<span data-ttu-id="01d83-115">若要使用 OAuth，必须向 Azure Active Directory 注册应用程序。</span><span class="sxs-lookup"><span data-stu-id="01d83-115">To use OAuth, an application must be registered with Azure Active Directory.</span></span>

<span data-ttu-id="01d83-116">按照在 [Microsoft identity platform 中注册应用程序](/azure/active-directory/develop/quickstart-register-app) 中列出的说明创建新的应用程序。</span><span class="sxs-lookup"><span data-stu-id="01d83-116">Follow the instructions listed in [Register an application with the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app) to create a new application.</span></span>

## <a name="configure-your-application"></a><span data-ttu-id="01d83-117">配置应用程序</span><span class="sxs-lookup"><span data-stu-id="01d83-117">Configure your application</span></span>

<span data-ttu-id="01d83-118">按照[Configure a client application to access Web api](/azure/active-directory/develop/quickstart-configure-app-access-web-apis)中列出的说明操作。</span><span class="sxs-lookup"><span data-stu-id="01d83-118">Follow the instructions listed in [Configure a client application to access web APIs](/azure/active-directory/develop/quickstart-configure-app-access-web-apis)</span></span>

<span data-ttu-id="01d83-119">确保添加以下一个或多个与要与之集成的协议对应的权限范围。</span><span class="sxs-lookup"><span data-stu-id="01d83-119">Make sure to add one or more of the following permission scopes that correspond to the protocols you would like to integrate with.</span></span> <span data-ttu-id="01d83-120">在 " **添加权限** 向导" 中，选择 " **Microsoft Graph** "，然后选择 " **委派权限** " 以查找列出的以下权限范围。</span><span class="sxs-lookup"><span data-stu-id="01d83-120">In the **Add a permission** wizard, select **Microsoft Graph** and then **Delegated permissions** to find the following permission scopes listed.</span></span>

| <span data-ttu-id="01d83-121">协议</span><span class="sxs-lookup"><span data-stu-id="01d83-121">Protocol</span></span>  | <span data-ttu-id="01d83-122">权限范围</span><span class="sxs-lookup"><span data-stu-id="01d83-122">Permission scope</span></span>        |
|-----------|-------------------------|
| <span data-ttu-id="01d83-123">IMAP</span><span class="sxs-lookup"><span data-stu-id="01d83-123">IMAP</span></span>      | `IMAP.AccessAsUser.All` |
| <span data-ttu-id="01d83-124">弹出式</span><span class="sxs-lookup"><span data-stu-id="01d83-124">POP</span></span>       | `POP.AccessAsUser.All`  |
| <span data-ttu-id="01d83-125">SMTP 身份验证</span><span class="sxs-lookup"><span data-stu-id="01d83-125">SMTP AUTH</span></span> | `SMTP.Send`             |

## <a name="get-an-access-token"></a><span data-ttu-id="01d83-126">获取访问令牌</span><span class="sxs-lookup"><span data-stu-id="01d83-126">Get an access token</span></span>

<span data-ttu-id="01d83-127">您可以使用我们的 [MSAL 客户端库](/azure/active-directory/develop/msal-overview) 之一从客户端应用程序中获取访问令牌。</span><span class="sxs-lookup"><span data-stu-id="01d83-127">You can use one of our [MSAL client libraries](/azure/active-directory/develop/msal-overview) to fetch an access token from your client application.</span></span>

<span data-ttu-id="01d83-128">或者，也可以从以下列表中选择一个合适的流，并按照相应的步骤调用基础标识平台 REST Api 并检索访问令牌。</span><span class="sxs-lookup"><span data-stu-id="01d83-128">Alternatively, you can select an appropriate flow from the following list and follow the corresponding steps to call the underlying identity platform REST APIs and retrieve an access token.</span></span>

1. [<span data-ttu-id="01d83-129">OAuth2 授权代码流</span><span class="sxs-lookup"><span data-stu-id="01d83-129">OAuth2 authorization code flow</span></span>](/azure/active-directory/develop/v2-oauth2-auth-code-flow)
1. [<span data-ttu-id="01d83-130">OAuth2 设备授权授予流</span><span class="sxs-lookup"><span data-stu-id="01d83-130">OAuth2 Device authorization grant flow</span></span>](/azure/active-directory/develop/v2-oauth2-device-code)

<span data-ttu-id="01d83-131">不支持通过 OAuth2 客户端凭据授予流的对 IMAP、POP、SMTP 身份验证协议的 OAuth 访问权限。</span><span class="sxs-lookup"><span data-stu-id="01d83-131">OAuth access to IMAP, POP, SMTP AUTH protocols via OAuth2 client credentials grant flow is not supported.</span></span> <span data-ttu-id="01d83-132">如果您的应用程序需要对 Microsoft 365 组织中的所有邮箱具有持久访问权限，我们建议您使用 Microsoft Graph Api，这些 Api 允许没有用户的访问，启用粒度权限，并允许管理员将此类访问权限限定为特定的一组邮箱。</span><span class="sxs-lookup"><span data-stu-id="01d83-132">If your application needs persistent access to all mailboxes in a Microsoft 365 organization, we recommend that you use the Microsoft Graph APIs which allow access without a user, enable granular permissions and let administrators scope such access to a specific set of mailboxes.</span></span>

<span data-ttu-id="01d83-133">在授权应用程序和请求访问令牌时，请确保指定完整的作用域（包括 Outlook 资源 Url）。</span><span class="sxs-lookup"><span data-stu-id="01d83-133">Make sure to specify the full scopes, including Outlook resource URLs, when authorizing your application and requesting an access token.</span></span>

| <span data-ttu-id="01d83-134">协议</span><span class="sxs-lookup"><span data-stu-id="01d83-134">Protocol</span></span>  | <span data-ttu-id="01d83-135">权限范围字符串</span><span class="sxs-lookup"><span data-stu-id="01d83-135">Permission scope string</span></span> |
|-----------|-------------------------|
| <span data-ttu-id="01d83-136">IMAP</span><span class="sxs-lookup"><span data-stu-id="01d83-136">IMAP</span></span>      | `https://outlook.office.com/IMAP.AccessAsUser.All` |
| <span data-ttu-id="01d83-137">弹出式</span><span class="sxs-lookup"><span data-stu-id="01d83-137">POP</span></span>       | `https://outlook.office.com/POP.AccessAsUser.All`  |
| <span data-ttu-id="01d83-138">SMTP 身份验证</span><span class="sxs-lookup"><span data-stu-id="01d83-138">SMTP AUTH</span></span> | `https://outlook.office.com/SMTP.Send`             |

<span data-ttu-id="01d83-139">此外，还可以请求 [offline_access](/azure/active-directory/develop/v2-permissions-and-consent#offline_access) 范围。</span><span class="sxs-lookup"><span data-stu-id="01d83-139">In addition, you can request for [offline_access](/azure/active-directory/develop/v2-permissions-and-consent#offline_access) scope.</span></span> <span data-ttu-id="01d83-140">当用户批准 offline_access 范围时，您的应用程序可以从 Microsoft identity platform 令牌终结点接收刷新令牌。</span><span class="sxs-lookup"><span data-stu-id="01d83-140">When a user approves the offline_access scope, your app can receive refresh tokens from the Microsoft identity platform token endpoint.</span></span> <span data-ttu-id="01d83-141">刷新令牌的生存期较长。</span><span class="sxs-lookup"><span data-stu-id="01d83-141">Refresh tokens are long-lived.</span></span> <span data-ttu-id="01d83-142">您的应用程序可以将新的访问令牌作为旧令牌过期。</span><span class="sxs-lookup"><span data-stu-id="01d83-142">Your app can get new access tokens as older ones expire.</span></span>

## <a name="authenticate-connection-requests"></a><span data-ttu-id="01d83-143">对连接请求进行身份验证</span><span class="sxs-lookup"><span data-stu-id="01d83-143">Authenticate connection requests</span></span>

<span data-ttu-id="01d83-144">您可以使用 [适用于 office 365 的 IMAP 和 POP 电子邮件设置](https://support.office.com/article/pop-and-imap-email-settings-for-outlook-8361e398-8af4-4e97-b147-6c6c4ac95353)，启动到 office 365 邮件服务器的连接。</span><span class="sxs-lookup"><span data-stu-id="01d83-144">You can initiate a connection to Office 365 mail servers using the [IMAP and POP email settings for Office 365](https://support.office.com/article/pop-and-imap-email-settings-for-outlook-8361e398-8af4-4e97-b147-6c6c4ac95353).</span></span>

### <a name="sasl-xoauth2"></a><span data-ttu-id="01d83-145">SASL XOAUTH2</span><span class="sxs-lookup"><span data-stu-id="01d83-145">SASL XOAUTH2</span></span>

<span data-ttu-id="01d83-146">与的 OAuth 集成要求您的应用程序使用 SASL XOAUTH2 格式编码和传输访问令牌。</span><span class="sxs-lookup"><span data-stu-id="01d83-146">OAuth integration with requires your application to use SASL XOAUTH2 format for encoding and transmitting the access token.</span></span> <span data-ttu-id="01d83-147">SASL XOAUTH2 将用户名、访问令牌按以下格式进行编码：</span><span class="sxs-lookup"><span data-stu-id="01d83-147">SASL XOAUTH2 encodes the username, access token together in the following format:</span></span>

```text
base64("user=" + userName + "^Aauth=Bearer " + accessToken + "^A^A")
```

<span data-ttu-id="01d83-148">`^A`表示 **Control**  +  **A** () 的控件 `%x01` 。</span><span class="sxs-lookup"><span data-stu-id="01d83-148">`^A` represents a **Control** + **A** (`%x01`).</span></span>

<span data-ttu-id="01d83-149">例如，使用 access 令牌访问的 SASL XOAUTH2 格式 `test@contoso.onmicrosoft.com` `EwBAAl3BAAUFFpUAo7J3Ve0bjLBWZWCclRC3EoAA` 为：</span><span class="sxs-lookup"><span data-stu-id="01d83-149">For example, the SASL XOAUTH2 format to access `test@contoso.onmicrosoft.com` with access token `EwBAAl3BAAUFFpUAo7J3Ve0bjLBWZWCclRC3EoAA` is:</span></span>

```text
base64("user=test@contoso.onmicrosoft.com^Aauth=Bearer EwBAAl3BAAUFFpUAo7J3Ve0bjLBWZWCclRC3EoAA^A^A")
```

<span data-ttu-id="01d83-150">在 base64 编码之后，这会转换为以下字符串。</span><span class="sxs-lookup"><span data-stu-id="01d83-150">After base64 encoding, this translates to the following string.</span></span> <span data-ttu-id="01d83-151">请注意，插入换行符的目的是为了提高可读性。</span><span class="sxs-lookup"><span data-stu-id="01d83-151">Note that line breaks are inserted for readability.</span></span>

```text
dXNlcj10ZXN0QGNvbnRvc28ub25taWNyb3NvZnQuY29tAWF1dGg9QmVhcmVy
IEV3QkFBbDNCQUFVRkZwVUFvN0ozVmUwYmpMQldaV0NjbFJDM0VvQUEBAQ==
```

### <a name="sasl-xoauth2-authentication-for-shared-mailboxes-in-office-365"></a><span data-ttu-id="01d83-152">Office 365 中的共享邮箱的 SASL XOAUTH2 身份验证</span><span class="sxs-lookup"><span data-stu-id="01d83-152">SASL XOAUTH2 authentication for shared mailboxes in Office 365</span></span>

<span data-ttu-id="01d83-153">如果使用 OAuth 的共享邮箱访问，应用程序需要代表用户获取访问令牌，而将 SASL XOAUTH2 编码字符串中的 userName 字段替换为共享邮箱的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="01d83-153">In case of shared mailbox access using OAuth, application needs to obtain the access token on behalf of a user but replace the userName field in the SASL XOAUTH2 encoded string with the email address of the shared mailbox.</span></span> 

### <a name="imap-protocol-exchange"></a><span data-ttu-id="01d83-154">IMAP 协议交换</span><span class="sxs-lookup"><span data-stu-id="01d83-154">IMAP Protocol Exchange</span></span>

<span data-ttu-id="01d83-155">若要对 IMAP 服务器连接进行身份验证，客户端将必须使用 `AUTHENTICATE` 以下格式的命令进行响应：</span><span class="sxs-lookup"><span data-stu-id="01d83-155">To authenticate a IMAP server connection, the client will have to respond with an `AUTHENTICATE` command in the following format:</span></span>

```text
AUTHENTICATE XOAUTH2 <base64 string in XOAUTH2 format>
```

<span data-ttu-id="01d83-156">导致身份验证成功的示例客户端/服务器消息交换：</span><span class="sxs-lookup"><span data-stu-id="01d83-156">Sample client-server message exchange that results in an authentication success:</span></span>

```text
[connection begins]
C: C01 CAPABILITY
S: * CAPABILITY … AUTH=XOAUTH2
S: C01 OK Completed
C: A01 AUTHENTICATE XOAUTH2 dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlYXJlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMjl0Q2cBAQ==
S: A01 OK AUTHENTICATE completed.
```

<span data-ttu-id="01d83-157">导致身份验证失败的示例客户端/服务器消息交换：</span><span class="sxs-lookup"><span data-stu-id="01d83-157">Sample client-server message exchange that results in an authentication failure:</span></span>

```text
[connection begins]
S: * CAPABILITY … AUTH=XOAUTH2
S: C01 OK Completed
C: A01 AUTHENTICATE XOAUTH2 dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlYXJlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMjl0Q2cBAQ==
S: A01 NO AUTHENTICATE failed.
```

### <a name="pop-protocol-exchange"></a><span data-ttu-id="01d83-158">POP 协议交换</span><span class="sxs-lookup"><span data-stu-id="01d83-158">POP Protocol Exchange</span></span>

<span data-ttu-id="01d83-159">若要对 POP 服务器连接进行身份验证，客户端必须使用 `AUTH` 以下格式的命令拆分成两行：</span><span class="sxs-lookup"><span data-stu-id="01d83-159">To authenticate a POP server connection, the client will have to respond with an `AUTH` command split into two lines in the following format:</span></span>    

```text 
AUTH XOAUTH2 
<base64 string in XOAUTH2 format>   
``` 

<span data-ttu-id="01d83-160">导致身份验证成功的示例客户端/服务器消息交换：</span><span class="sxs-lookup"><span data-stu-id="01d83-160">Sample client-server message exchange that results in an authentication success:</span></span>    

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

<span data-ttu-id="01d83-161">导致身份验证失败的示例客户端/服务器消息交换：</span><span class="sxs-lookup"><span data-stu-id="01d83-161">Sample client-server message exchange that results in an authentication failure:</span></span>    

```text 
[connection begins] 
C: AUTH XOAUTH2     
S: +    
C: dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlY    
XJlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMj   
l0Q2cBAQ=   
S: -ERR Authentication failure: unknown user name or bad password.  
```

### <a name="smtp-protocol-exchange"></a><span data-ttu-id="01d83-162">SMTP 协议交换</span><span class="sxs-lookup"><span data-stu-id="01d83-162">SMTP Protocol Exchange</span></span>

<span data-ttu-id="01d83-163">若要对 SMTP 服务器连接进行身份验证，客户端将必须使用 `AUTH` 以下格式的命令进行响应：</span><span class="sxs-lookup"><span data-stu-id="01d83-163">To authenticate a SMTP server connection, the client will have to respond with an `AUTH` command in the following format:</span></span>

```text
AUTH XOAUTH2 <base64 string in XOAUTH2 format>
```

<span data-ttu-id="01d83-164">导致身份验证成功的示例客户端/服务器消息交换：</span><span class="sxs-lookup"><span data-stu-id="01d83-164">Sample client-server message exchange that results in an authentication success:</span></span>

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

<span data-ttu-id="01d83-165">导致身份验证失败的示例客户端/服务器消息交换：</span><span class="sxs-lookup"><span data-stu-id="01d83-165">Sample client-server message exchange that results in an authentication failure:</span></span>

```text
[connection begins]
C: auth xoauth2
S: 334
C: dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlY
XJlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMj
l0Q2cBAQ==
S: 535 5.7.3 Authentication unsuccessful [SN2PR00CA0018.namprd00.prod.outlook.com]
```

## <a name="see-also"></a><span data-ttu-id="01d83-166">另请参阅</span><span class="sxs-lookup"><span data-stu-id="01d83-166">See also</span></span>

- [<span data-ttu-id="01d83-167">在 Exchange 中的身份验证和 EWS</span><span class="sxs-lookup"><span data-stu-id="01d83-167">Authentication and EWS in Exchange</span></span>](../exchange-web-services/authentication-and-ews-in-exchange.md)
- [<span data-ttu-id="01d83-168">IMAP、POP 连接设置</span><span class="sxs-lookup"><span data-stu-id="01d83-168">IMAP, POP Connection settings</span></span>](https://support.office.com/article/pop-and-imap-email-settings-for-outlook-8361e398-8af4-4e97-b147-6c6c4ac95353)
- [<span data-ttu-id="01d83-169">Internet 邮件访问协议</span><span class="sxs-lookup"><span data-stu-id="01d83-169">Internet Message Access Protocol</span></span>](https://tools.ietf.org/html/rfc3501)
- [<span data-ttu-id="01d83-170">邮局协议</span><span class="sxs-lookup"><span data-stu-id="01d83-170">Post Office Protocol</span></span>](https://tools.ietf.org/html/rfc1081)
- [<span data-ttu-id="01d83-171">SMTP 服务扩展以进行身份验证</span><span class="sxs-lookup"><span data-stu-id="01d83-171">SMTP Service extension for Authentication</span></span>](https://tools.ietf.org/html/rfc4954)
