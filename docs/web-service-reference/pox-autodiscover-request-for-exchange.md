---
title: Exchange 的 POX 自动发现请求
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 75671b1d-f35b-497b-8d8c-706f3f2535fd
description: 自动发现请求包含对用户的客户端访问配置的查询。
ms.openlocfilehash: b2138f9813c7b75aef9afb90089b9b874aac7532
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461665"
---
# <a name="pox-autodiscover-request-for-exchange"></a>Exchange 的 POX 自动发现请求

自动发现请求包含对用户的客户端访问配置的查询。
  
## <a name="autodiscover-request-example"></a>自动发现请求示例

### <a name="description"></a>说明

以下 XML 示例显示了自动发现请求正文。
  
### <a name="code"></a>代码

```XML
<Autodiscover xmlns="https://schemas.microsoft.com/exchange/autodiscover/outlook/requestschema/2006">
   <Request>
     <EMailAddress>user@contoso.com</EMailAddress>
     <AcceptableResponseSchema>https://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a</AcceptableResponseSchema>
   </Request>
 </Autodiscover>
```

### <a name="request-headers"></a>请求标头

在发送自动发现请求时，以下 HTTP 标头是可选的。
  
**表1。HTTP 请求标头**

|**Header**|**说明**|
|:-----|:-----|
|X-MapiHttpCapability  <br/> |如果存在并设置为 "1"，则指示客户端正在请求可用于通过使用 MAPI/HTTP 协议连接到服务器的信息。 此标头适用于实现 MAPI/HTTP 协议的客户端。  <br/> |
|X-ClientCanHandle  <br/> |此标头包含客户端支持的功能的逗号分隔列表。 表2中指定了可能的值。  <br/> |
   
**表2。ClientCanHandle 标头值**

|**X-ClientCanHandle 值（不区分大小写）**|**最低服务器版本**|**说明**|
|:-----|:-----|:-----|
|沟通  <br/> |15.00.0995.014  <br/> |如果此值存在，如果服务器配置为接受协商身份验证，则服务器将在[AuthPackage （POX）](authpackage-pox.md)元素中返回值 "Negotiate"。 如果此值不存在，则服务器将不会在**AuthPackage**元素中返回 "Negotiate" 值。  <br/> |
|ExHttpInfo  <br/> |15.00.0995.014  <br/> |如果此值存在，则服务器将返回一个[Protocol （POX）](protocol-pox.md)元素，其中如果将服务器配置为接受 RPC/HTTP 连接，则该服务器会将[类型（POX）](type-pox.md)元素设置为 "EXHTTP"。 如果不存在此值，则服务器将不会返回**Type**元素设置为 "EXHTTP" 的**协议**元素。  <br/> |
   
### <a name="request-elements"></a>Request 元素

请求正文中使用以下元素：
  
- [自动发现（POX）](autodiscover-pox.md)
    
- [请求（POX）](request-pox.md)
    
- [AcceptableResponseSchema （POX）](acceptableresponseschema-pox.md)
    
- [EMailAddress （POX）](emailaddress-pox.md)
    
> [!NOTE]
> 可以使用[LegacyDN （POX）](legacydn-pox.md)元素代替[EMailAddress （POX）](emailaddress-pox.md)元素。 
  
### <a name="version-differences"></a>版本差异

在 Office 365、Exchange Online 和内部部署版本中，MapiHttpCapability 标头适用于以 build 15.00.0847.032 （Exchange Server 2013 SP1）开头的 Exchange Online 和内部部署版本。
  
在 Office 365、Exchange Online 和内部部署版本中，ClientCanHandle 标头可从生成15.00.0995.014 开始。
  
## <a name="see-also"></a>另请参阅



[Exchange 的 POX 自动发现响应](pox-autodiscover-response-for-exchange.md)


[Exchange 的 POX 自动发现 web 服务参考](pox-autodiscover-web-service-reference-for-exchange.md)
  
[Exchange 的 POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

