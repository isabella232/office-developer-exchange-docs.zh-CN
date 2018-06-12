---
title: Exchange POX 自动发现请求
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 75671b1d-f35b-497b-8d8c-706f3f2535fd
description: 自动发现请求包含用户的客户端访问配置的查询。
ms.openlocfilehash: 48d6c30946e75936ed93a6f4507d8a8d3ae47d40
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826865"
---
# <a name="pox-autodiscover-request-for-exchange"></a>Exchange POX 自动发现请求

自动发现请求包含用户的客户端访问配置的查询。
  
## <a name="autodiscover-request-example"></a>自动发现请求示例

### <a name="description"></a>说明

下面的 XML 示例演示了自动发现请求正文。
  
### <a name="code"></a>代码

```XML
<Autodiscover xmlns="http://schemas.microsoft.com/exchange/autodiscover/outlook/requestschema/2006">
   <Request>
     <EMailAddress>user@contoso.com</EMailAddress>
     <AcceptableResponseSchema>http://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a</AcceptableResponseSchema>
   </Request>
 </Autodiscover>
```

### <a name="request-headers"></a>请求标头

发送自动发现请求时，以下 HTTP 标头是可选的。
  
**表 1。HTTP 请求标头**

|**Header**|**说明**|
|:-----|:-----|
|X MapiHttpCapability  <br/> |如果存在此参数，并且已设置为"1"，指示客户端的请求可用于连接到服务器使用 MAPI/HTTP 协议的信息。 适用于客户端实现 MAPI/HTTP 协议的此标头。  <br/> |
|X ClientCanHandle  <br/> |此标头中包含客户端支持的功能的以逗号分隔列表。 表 2 中指定的可能值。  <br/> |
   
**表 2。X ClientCanHandle 标头值**

|**X ClientCanHandle 值 （不区分大小写）**|**服务器的最低版本**|**说明**|
|:-----|:-----|:-----|
|协商  <br/> |15.00.0995.014  <br/> |如果存在此值时，服务器将[AuthPackage (POX)](authpackage-pox.md)元素中返回的值为"协商"，如果服务器配置为接受协商身份验证。 如果此值不存在，则服务器不会**AuthPackage**元素中返回的值为"协商"。  <br/> |
|ExHttpInfo  <br/> |15.00.0995.014  <br/> |如果存在此值时，服务器将返回与[类型 (POX)](type-pox.md)元素设置为"EXHTTP"，如果将服务器配置为接受 RPC/HTTP 连接[协议 (POX)](protocol-pox.md)元素。 如果此值不存在，则服务器不会返回**协议**具有元素的**类型**元素设置为"EXHTTP"。  <br/> |
   
### <a name="request-elements"></a>请求元素

在请求正文中使用以下元素：
  
- [自动发现 (POX)](autodiscover-pox.md)
    
- [请求 (POX)](request-pox.md)
    
- [AcceptableResponseSchema (POX)](acceptableresponseschema-pox.md)
    
- [EMailAddress (POX)](emailaddress-pox.md)
    
> [!NOTE]
> [LegacyDN (POX)](legacydn-pox.md)元素可用于代替的[电子邮件地址 (POX)](emailaddress-pox.md)元素。 
  
### <a name="version-differences"></a>版本差异

X MapiHttpCapability 标头位于 Office 365，Exchange Online 和本地开头的 Exchange 版本生成 15.00.0847.032 (Exchange Server 2013 SP1)。
  
X ClientCanHandle 标头位于 Office 365，Exchange Online 和本地开头的 Exchange 版本生成 15.00.0995.014。
  
## <a name="see-also"></a>另请参阅



[Exchange POX 自动发现响应](pox-autodiscover-response-for-exchange.md)


[Exchange POX 自动发现 web 服务引用](pox-autodiscover-web-service-reference-for-exchange.md)
  
[Exchange POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

