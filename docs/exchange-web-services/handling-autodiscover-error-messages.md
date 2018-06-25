---
title: 处理自动发现的错误消息
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: e5939ec2-1100-4174-8a88-5a6e09b60b23
description: 了解不同类型的自动发现错误和如何处理它们。
ms.openlocfilehash: fcafc799f4d35e92159d2913845474ecf7bc5657
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752724"
---
# <a name="handling-autodiscover-error-messages"></a>处理自动发现的错误消息

了解不同类型的自动发现错误和如何处理它们。
  
自动发现，您的应用程序可以自动检索配置信息和它棒。 但是，操作并不总是会根据计划。 让我们看一下，可能出现的常见错误和如何处理这些大程度地减少需要提示用户手动配置您的客户端。
  
## <a name="http-status-errors"></a>HTTP 状态错误
<a name="bk_HttpErrors"> </a>

发送自动发现请求时可能会遇到的第一种是错误的 HTTP 状态。 如果您的响应中的 HTTP 状态 200 (OK) 之外的任何内容，则响应负载不包含您要寻找的自动发现响应。 为了简单起见，我们可以分为三个类别分组非 200 状态代码。
  
**表 1。HTTP 状态代码**

|**状态代码**|**错误的类型**|**处理...**|
|:-----|:-----|:-----|
|301 或 302  <br/> |重定向错误  <br/> |重新您的请求发送到"位置"HTTP 响应标头中包含的 URI。 有关详细信息，请参阅[处理重定向错误](#bk_HandlingRedirects)。  <br/> |
|401  <br/> |未经授权的错误  <br/> |[自动发现过程](autodiscover-for-exchange.md)涉及尝试多个潜在的 Url，因为您无法获取此个 URL 仅具有下一个接受您的凭据。 因此，您不应考虑单个 401 错误以指示的凭据是无效。 但是，如果您收到 401 错误来自多个 Url，您可能希望提示用户重新输入自己的密码 （如果可能）。  <br/> |
|任何其他非 200 状态  <br/> |无效的自动发现终结点错误  <br/> |请考虑返回任何其他非 200 状态代码无效，URL 并继续尝试在列表中的下一个 URL。  <br/> |
   
## <a name="autodiscover-errors"></a>自动发现错误
<a name="bk_AutodiscoverErrors"> </a>

即使您获得 200 (OK) 状态代码后发送的自动发现请求时，不意味着服务器发送所需的信息。 200 状态仅意味着您具有自动发现响应，且该响应可能包含内负载错误。 根据格式是否为 SOAP 或 POX 不同错误信息的位置。
  
### <a name="soap-autodiscover-errors"></a>SOAP 自动发现错误

对于 SOAP 自动发现响应可包含一个或多个[错误代码 (SOAP)](http://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx)元素，在不同的位置。 通常您可以在响应中预期一个作为[响应 (SOAP)](http://msdn.microsoft.com/library/4c2bcdeb-95ce-4ffa-bd83-118af53b534f%28Office.15%29.aspx)元素的子元素，另一个作为每个[用户回音 (SOAP)](http://msdn.microsoft.com/library/5007b1ba-bfcc-40d7-b1cb-e32fbaf54ffd%28Office.15%29.aspx)元素的子元素。 此外可能会遇到一个作为子元素的[UserSettingError (SOAP)](http://msdn.microsoft.com/library/abb175c5-4f38-4dcc-81e3-b511686862eb%28Office.15%29.aspx)元素，如果存在此参数。 错误的上下文取决于**ErrorCode**元素的位置，，如下所示： 
  
- 作为**响应**元素的子元素， **ErrorCode**元素均表示一条错误，适用于整个请求。 
    
- 作为**用户回音**元素的子元素，它代表适用于特定用户的只是一个错误。 
    
- 作为**UserSettingError**元素的子元素，它表示一条错误，适用于所请求的特定设置。 
    
让我们看看的响应的示例。 本示例中，**响应**元素下的**ErrorCode**元素的值为"NoError"，指示总体成功。 但是，**用户回音**元素下的**ErrorCode**元素的值为"RedirectAddress"，指示该特定用户的发生了错误。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/" 
    xmlns:a="http://www.w3.org/2005/08/addressing">
  <s:Header>
    <a:Action s:mustUnderstand="1">http://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettingsResponse</a:Action>
    <h:ServerVersionInfo xmlns:h="http://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
      <h:MajorVersion>14</h:MajorVersion>
      <h:MinorVersion>3</h:MinorVersion>
      <h:MajorBuildNumber>136</h:MajorBuildNumber>
      <h:MinorBuildNumber>1</h:MinorBuildNumber>
      <h:Version>Exchange2010_SP2</h:Version>
    </h:ServerVersionInfo>
  </s:Header>
  <s:Body>
    <GetUserSettingsResponseMessage xmlns="http://schemas.microsoft.com/exchange/2010/Autodiscover">
      <Response xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
        <ErrorCode>NoError</ErrorCode>
        <ErrorMessage />
        <UserResponses>
          <UserResponse>
            <ErrorCode>RedirectAddress</ErrorCode>
            <ErrorMessage>Redirection address.</ErrorMessage>
            <RedirectTarget>elvin@mail.contoso.com</RedirectTarget>
            <UserSettingErrors />
            <UserSettings />
          </UserResponse>
        </UserResponses>
      </Response>
    </GetUserSettingsResponseMessage>
  </s:Body>
</s:Envelope>
```

[ErrorCode (SOAP)](http://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx)本文包含可能出现的错误的完整列表。 大部分这些指示不可恢复的错误，但一些保证特殊处理。 
  
**表 2。SOAP Autodisover ErrorCode 值**

|**ErrorCode 值**|**处理...**|
|:-----|:-----|
|RedirectAddress  <br/> |与[RedirectTarget (SOAP)](http://msdn.microsoft.com/library/f8162724-cf9a-4543-a1ad-5846c8b10bfa%28Office.15%29.aspx)元素中的电子邮件地址，[重新启动与新的电子邮件地址的自动发现](#bk_RestartAutodiscover)。  <br/> |
|RedirectUrl  <br/> |**RedirectTarget**元素中的 url 的[重新发送您的请求指向新 URL](#bk_ResendRequest) 。  <br/> |
|ServerBusy  <br/> |在小型延迟后重试此 URL。 您可能等待的时间设置，或只是将此 URL 移动到的尝试的 Url 列表末尾。 如果从 URL 多次收到此错误，则应考虑的 URL 无效。  <br/> |
   
### <a name="pox-autodiscover-errors"></a>POX 自动发现错误

POX 自动发现服务略有不同报告的错误。 [错误 (POX)](http://msdn.microsoft.com/library/91c63b62-ab68-4c32-a2f7-5a87c188335b%28Office.15%29.aspx)元素中包含非恢复错误。 [ErrorCode (POX)](http://msdn.microsoft.com/library/064d73e4-45b7-4797-828e-9df590830db8%28Office.15%29.aspx)本文包含可能错误代码的完整列表。 
  
[操作 (POX)](http://msdn.microsoft.com/library/a3462c6b-453c-462a-830d-f29ee4a2babb%28Office.15%29.aspx)元素中包含重定向错误。 **Action**元素"设置"之外的任何值指示重定向错误。 
  
**表 3。POX Autodisover ErrorCode 值**

|**Action 值**|**处理...**|
|:-----|:-----|
|redirectAddr  <br/> |与[RedirectAddr (POX)](http://msdn.microsoft.com/library/0e9fa6b6-7991-4dc1-a59a-48e5f8e041e4%28Office.15%29.aspx)元素中的电子邮件地址，[重新启动与新的电子邮件地址的自动发现](#bk_RestartAutodiscover)。  <br/> |
|redirectUrl  <br/> |[RedirectUrl (POX)](http://msdn.microsoft.com/library/c54f310f-8c99-4c37-8e73-ac87722b6229%28Office.15%29.aspx)元素中的 url 的[重新发送您的请求指向新 URL](#bk_ResendRequest) 。  <br/> |
   
本示例中，为**Action**元素的值为"redirectAddr"，指示应将新的请求发送**RedirectAddr**元素中包含的新电子邮件地址。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="http://schemas.microsoft.com/exchange/autodiscover/responseschema/2006">
  <Response xmlns="http://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a">
    <Account>
      <Action>redirectAddr</Action>
      <RedirectAddr>elvin@mail.contoso.com</RedirectAddr>
    </Account>
  </Response>
</Autodiscover>
```

## <a name="handling-redirect-errors"></a>处理重定向错误
<a name="bk_HandlingRedirects"> </a>

您可以处理以下两种方式重定向错误方案：
  
- 通过使用新的电子邮件地址，重新启动自动发现。
    
- 通过重新您的请求发送到新 URL。
    
这两种方案需要一些然后再继续验证。
  
### <a name="restarting-autodiscover-with-a-new-email-address"></a>使用新的电子邮件地址重新启动自动发现
<a name="bk_RestartAutodiscover"> </a>

当您获取中自动发现新的电子邮件地址重定向响应，首先验证重定向错误响应中提供的新电子邮件地址不是导致此错误的请求中发送相同的地址。 如果是，您不应重新启动自动发现和改为考虑生成响应无效的 URL。
  
如果不同的新电子邮件地址，放弃的潜在的自动发现终结点 Url 现有列表，并生成新的电子邮件地址所基于的新列表。
  
### <a name="resending-your-request-to-a-new-url"></a>重新您的请求发送到新 URL
<a name="bk_ResendRequest"> </a>

自动发现重定向响应中收到新 URL，您首先应，如下所示验证 URL:
  
- 验证 URL 是 HTTPS URL。
    
- 确认您未从之前的当前电子邮件地址与此 URL 中收到了错误。
    
- 如果适用于您的应用程序，告知用户重定向并获取其权限遵循重定向。
    
- 将请求发送到 URL 和[验证服务器提供的 SSL 证书有效](how-to-validate-a-server-certificate-for-the-ews-managed-api.md)。
    
如果 URL 通过验证，则重新请求发送到此新的 URL。
  
## <a name="see-also"></a>另请参阅


- [Exchange 自动发现](autodiscover-for-exchange.md)
    
- [在 Exchange 使用 SCP 查找来查找自动发现终结点](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md)
    
- [ErrorCode (SOAP)](http://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx)
    
- [ErrorCode (POX)](http://msdn.microsoft.com/library/064d73e4-45b7-4797-828e-9df590830db8%28Office.15%29.aspx)
    

