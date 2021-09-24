---
title: POX 自动发现请求Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 75671b1d-f35b-497b-8d8c-706f3f2535fd
description: 自动发现请求包含用户的客户端访问配置的查询。
ms.openlocfilehash: 8a0960dcff21276baf723512befacc4eca35950f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523864"
---
# <a name="pox-autodiscover-request-for-exchange"></a>POX 自动发现请求Exchange

自动发现请求包含用户的客户端访问配置的查询。
  
## <a name="autodiscover-request-example"></a>自动发现请求示例

### <a name="description"></a>Description

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

发送自动发现请求时，以下 HTTP 标头是可选的。
  
**表 1.HTTP 请求标头**

|**Header**|**说明**|
|:-----|:-----|
|X-MapiHttpCapability  <br/> |如果存在并设置为"1"，则指示客户端请求的信息可用于使用 MAPI/HTTP 协议连接到服务器。 此标头适用于实现 MAPI/HTTP 协议的客户端。  <br/> |
|X-ClientCanHandle  <br/> |此标头包含客户端支持的功能的逗号分隔列表。 可能的值在表 2 中指定。  <br/> |
   
**表 2.X-ClientCanHandle 标头值**

|**X-ClientCanHandle (不区分大小写)**|**最低服务器版本**|**说明**|
|:-----|:-----|:-----|
|协商  <br/> |15.00.0995.014  <br/> |如果存在此值，则服务器将在 [AuthPackage (POX) ](authpackage-pox.md) 元素中返回值"Negotiate"（如果服务器配置为接受协商身份验证）。 如果此值不存在，则服务器不会在 AuthPackage 元素中返回值 **"Negotiate"。**  <br/> |
|ExHttpInfo  <br/> |15.00.0995.014  <br/> |如果存在此值，则服务器将返回 [Protocol (POX) ](protocol-pox.md) 元素，如果服务器配置为接受 RPC/HTTP 连接，则 Type ([POX) ](type-pox.md) 元素设置为"EXHTTP"。 如果此值不存在，则服务器不会返回 Type 元素设置为"EXHTTP"的 **Protocol** 元素。   <br/> |
   
### <a name="request-elements"></a>请求元素

请求正文中会使用下列元素：
  
- [AutoDiscover (POX)](autodiscover-pox.md)
    
- [Request (POX)](request-pox.md)
    
- [AcceptableResponseSchema (POX)](acceptableresponseschema-pox.md)
    
- [EMailAddress (POX)](emailaddress-pox.md)
    
> [!NOTE]
> LegacyDN [ (POX) ](legacydn-pox.md) 元素可用于将 [EMailAddress ](emailaddress-pox.md) (POX) 元素。 
  
### <a name="version-differences"></a>版本差异

从内部版本 15.00.0847.032 (Exchange Server 2013 SP1) 开始，X-MapiHttpCapability 标头在 Office 365、Exchange Online 和本地 Exchange 版本中可用。
  
从内部版本 15.00.0995.014 开始，X-ClientCanHandle 标头在 Office 365、Exchange Online 和本地 Exchange 版本中可用。
  
## <a name="see-also"></a>另请参阅



[POX 自动发现响应Exchange](pox-autodiscover-response-for-exchange.md)


[POX 自动发现 Web 服务参考Exchange](pox-autodiscover-web-service-reference-for-exchange.md)
  
[用于存储的 POX 自动发现 XML Exchange](pox-autodiscover-xml-elements-for-exchange.md)

