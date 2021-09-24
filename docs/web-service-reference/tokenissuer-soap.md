---
title: TokenIssuer (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 2d7be675-626c-4173-89e9-e32beef81ad5
description: TokenIssuer 元素指定安全令牌服务的 Uri (SOAP) 和 Endpoint (SOAP) 。
ms.openlocfilehash: ea1c93493e4f47a6f2551c24586e54614f4f45e6
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59527263"
---
# <a name="tokenissuer-soap"></a>TokenIssuer (SOAP)

**TokenIssuer** 元素指定 [安全令牌服务的 Uri (SOAP](uri-soap.md)) [和 Endpoint (SOAP](endpoint-soap.md)) 。 
  
```XML
<TokenIssuer>
   <Uri/>
   <Endpoint/>
</TokenIssuer>
```

 **TokenIssuer**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Uri (SOAP)](uri-soap.md) <br/> |颁发安全令牌的安全令牌服务的 URI。  <br/> |
|[Endpoint (SOAP)](endpoint-soap.md) <br/> |Web 服务终结点 URI。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[TokenIssuers (SOAP)](tokenissuers-soap.md) <br/> |表示安全令牌服务 [Uri ](uri-soap.md) (SOAP) [和 Endpoint (SOAP) ](endpoint-soap.md)。  <br/> |
   
## <a name="remarks"></a>注解

使用安全令牌时，使用 **TokenIssuer** 元素指定安全令牌服务。 
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|架构名称  <br/> |自动发现架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[自动发现 Web 服务引用Exchange](autodiscover-web-service-reference-for-exchange.md)
  
[Exchange 2013 的 SOAP 自动发现 XML 元素](soap-autodiscover-xml-elements-for-exchange-2013.md)

