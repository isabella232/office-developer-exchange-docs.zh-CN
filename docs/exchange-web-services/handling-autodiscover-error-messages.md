---
title: 处理自动发现错误消息
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: e5939ec2-1100-4174-8a88-5a6e09b60b23
description: 了解不同类型的自动发现错误以及如何处理它们。
localization_priority: Priority
ms.openlocfilehash: 0cba7e54cb251a9775e0971826560e277dcd9d2d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455959"
---
# <a name="handling-autodiscover-error-messages"></a>处理自动发现错误消息

了解不同类型的自动发现错误以及如何处理它们。
  
自动发现使您的应用程序能够自动检索配置信息，并且运行良好。 但是，有些事情并不总是根据计划进行。 我们来看看可能发生的常见错误，以及如何处理这些错误，以最大限度地减少提示用户手动配置客户端的需求。
  
## <a name="http-status-errors"></a>HTTP 状态错误
<a name="bk_HttpErrors"> </a>

发送自动发现请求时，您可能会遇到的第一种错误类型是 HTTP 状态。 如果响应中的 HTTP 状态是200（OK）之外的任何内容，响应有效负载将不包含您要查找的自动发现响应。 为简单起见，我们可以将非200状态代码分组为三个类别。
  
**表1。HTTP 状态代码**

|**状态代码**|**错误类型**|**处理 .。。**|
|:-----|:-----|:-----|
|301或302  <br/> |重定向错误  <br/> |将您的请求重新发送到包含在 "Location" HTTP 响应头中的 URI。 有关详细信息，请参阅[处理重定向错误](#bk_HandlingRedirects)。  <br/> |
|401  <br/> |未经授权的错误  <br/> |由于[自动发现过程](autodiscover-for-exchange.md)涉及尝试多个可能的 url，因此您可以在一个 URL 上获取此程序，使下一个 url 接受您的凭据。 出于此原因，您不应考虑使用一个401错误来指示凭据无效。 但是，如果收到来自多个 Url 的401错误，您可能希望提示用户重新输入密码（如果可能）。  <br/> |
|任何其他非200状态  <br/> |无效的自动发现终结点错误  <br/> |请考虑返回任何其他非200状态代码为无效的 URL，并继续尝试列表中的下一个 URL。  <br/> |
   
## <a name="autodiscover-errors"></a>自动发现错误
<a name="bk_AutodiscoverErrors"> </a>

即使在发送自动发现请求之后收到200（OK）状态代码，这并不意味着服务器发送了您所需的信息。 200状态仅表示您有一个自动发现响应，并且该响应可能在有效负载中包含一个错误。 错误消息的位置因格式是 SOAP 还是 POX 而异。
  
### <a name="soap-autodiscover-errors"></a>SOAP 自动发现错误

对于 SOAP 自动发现，响应可以包含一个或多个[ErrorCode （SOAP）](https://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx)元素，位于不同的位置。 通常情况下，您可以将一个作为[响应（soap）](https://msdn.microsoft.com/library/4c2bcdeb-95ce-4ffa-bd83-118af53b534f%28Office.15%29.aspx)元素的子元素，另一个作为响应中的每个[UserResponse （soap）](https://msdn.microsoft.com/library/5007b1ba-bfcc-40d7-b1cb-e32fbaf54ffd%28Office.15%29.aspx)元素的子元素。 您可能还会遇到一个[UserSettingError （SOAP）](https://msdn.microsoft.com/library/abb175c5-4f38-4dcc-81e3-b511686862eb%28Office.15%29.aspx)元素的子元素（如果有的话）。 错误的上下文取决于**ErrorCode**元素所在的位置，如下所示： 
  
- 作为**Response**元素的子元素， **ErrorCode**元素表示应用于整个请求的错误。 
    
- 作为**UserResponse**元素的子元素，它表示仅适用于该特定用户的错误。 
    
- 作为**UserSettingError**元素的子元素，它表示应用于所请求的特定设置的错误。 
    
我们来看看响应的一个示例。 在此示例中， **Response**元素下的**ErrorCode**元素的值为 "NoError"，表示整体成功。 但是， **UserResponse**元素下的**ErrorCode**元素的值为 "RedirectAddress"，表示该特定用户发生了错误。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/" 
    xmlns:a="http://www.w3.org/2005/08/addressing">
  <s:Header>
    <a:Action s:mustUnderstand="1">https://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettingsResponse</a:Action>
    <h:ServerVersionInfo xmlns:h="https://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
      <h:MajorVersion>14</h:MajorVersion>
      <h:MinorVersion>3</h:MinorVersion>
      <h:MajorBuildNumber>136</h:MajorBuildNumber>
      <h:MinorBuildNumber>1</h:MinorBuildNumber>
      <h:Version>Exchange2010_SP2</h:Version>
    </h:ServerVersionInfo>
  </s:Header>
  <s:Body>
    <GetUserSettingsResponseMessage xmlns="https://schemas.microsoft.com/exchange/2010/Autodiscover">
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

[ErrorCode （SOAP）](https://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx)文章包含可能的错误的完整列表。 大多数情况下，它们都表示出现不可恢复的错误，但少数是特别的处理保证。 
  
**表2。SOAP Autodisover ErrorCode 值**

|**ErrorCode 值**|**处理 .。。**|
|:-----|:-----|
|RedirectAddress  <br/> |使用[新的电子邮件地址重启](#bk_RestartAutodiscover) [RedirectTarget （SOAP）](https://msdn.microsoft.com/library/f8162724-cf9a-4543-a1ad-5846c8b10bfa%28Office.15%29.aspx)元素中的电子邮件地址的自动发现。  <br/> |
|RedirectUrl  <br/> |将[您的请求重新发送到](#bk_ResendRequest) **RedirectTarget**元素中的 url 的新 url。  <br/> |
|ServerBusy  <br/> |请在短暂延迟后重试此 URL。 您可以等待一段设定的时间，或者只是将此 URL 移到 Url 列表的末尾，以尝试。 如果从某个 URL 多次收到此错误，则应将该 URL 视为无效。  <br/> |
   
### <a name="pox-autodiscover-errors"></a>POX 自动发现错误

POX 自动发现服务以略有不同的方式报告错误。 不可恢复的错误包含在[Error （POX）](https://msdn.microsoft.com/library/91c63b62-ab68-4c32-a2f7-5a87c188335b%28Office.15%29.aspx)元素中。 [ErrorCode （POX）](https://msdn.microsoft.com/library/064d73e4-45b7-4797-828e-9df590830db8%28Office.15%29.aspx)文章包含可能的错误代码的完整列表。 
  
重定向错误包含在[Action （POX）](https://msdn.microsoft.com/library/a3462c6b-453c-462a-830d-f29ee4a2babb%28Office.15%29.aspx)元素中。 除 "设置" 之外的**Action**元素的任何值都表示重定向错误。 
  
**表3。POX Autodisover ErrorCode 值**

|**操作值**|**处理 .。。**|
|:-----|:-----|
|redirectAddr  <br/> |使用[新电子邮件地址重启](#bk_RestartAutodiscover) [RedirectAddr （POX）](https://msdn.microsoft.com/library/0e9fa6b6-7991-4dc1-a59a-48e5f8e041e4%28Office.15%29.aspx)元素中的电子邮件地址的自动发现。  <br/> |
|redirectUrl  <br/> |将[您的请求重新发送到](#bk_ResendRequest) [RedirectUrl （POX）](https://msdn.microsoft.com/library/c54f310f-8c99-4c37-8e73-ac87722b6229%28Office.15%29.aspx)元素中的 url 的新 url。  <br/> |
   
在此示例中， **Action**元素的值为 "redirectAddr"，表示应使用**redirectAddr**元素中包含的新电子邮件地址发送新的请求。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="https://schemas.microsoft.com/exchange/autodiscover/responseschema/2006">
  <Response xmlns="https://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a">
    <Account>
      <Action>redirectAddr</Action>
      <RedirectAddr>elvin@mail.contoso.com</RedirectAddr>
    </Account>
  </Response>
</Autodiscover>
```

## <a name="handling-redirect-errors"></a>处理重定向错误
<a name="bk_HandlingRedirects"> </a>

您可以通过两种方式处理重定向错误方案：
  
- 通过使用新的电子邮件地址重新启动自动发现。
    
- 通过将您的请求重新发送到新的 URL。
    
这两种方案在继续之前都需要进行一些验证。
  
### <a name="restarting-autodiscover-with-a-new-email-address"></a>使用新的电子邮件地址重新启动自动发现
<a name="bk_RestartAutodiscover"> </a>

当您在自动发现重定向响应中获取新的电子邮件地址时，请首先验证重定向错误响应中提供的新电子邮件地址是否与您在导致错误的请求中发送的地址不相同。 如果是，则不应重新启动自动发现，而应考虑生成响应的 URL 是否无效。
  
如果新的电子邮件地址不同，请丢弃现有的潜在自动发现终结点 Url 列表，并根据新的电子邮件地址生成新的列表。
  
### <a name="resending-your-request-to-a-new-url"></a>将请求重新发送到新 URL
<a name="bk_ResendRequest"> </a>

当您在自动发现重定向响应中获取新 URL 时，应首先验证 URL，如下所示：
  
- 验证 URL 是否为 HTTPS URL。
    
- 验证您以前没有收到与当前电子邮件地址在此 URL 中的错误。
    
- 如果适用于你的应用程序，请通知用户重定向，并获取其对重定向的访问权限。
    
- 向 URL 发送请求，并[验证服务器出示的 SSL 证书是否有效](how-to-validate-a-server-certificate-for-the-ews-managed-api.md)。
    
如果 URL 通过验证，请将请求重新发送到此新 URL。
  
## <a name="see-also"></a>另请参阅


- [Exchange 自动发现](autodiscover-for-exchange.md)
    
- [通过使用 Exchange 中的 SCP 查找来找到自动发现终结点](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md)
    
- [ErrorCode （SOAP）](https://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx)
    
- [ErrorCode （POX）](https://msdn.microsoft.com/library/064d73e4-45b7-4797-828e-9df590830db8%28Office.15%29.aspx)
    

