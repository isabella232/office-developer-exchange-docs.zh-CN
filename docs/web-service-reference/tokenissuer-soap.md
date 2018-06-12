---
title: TokenIssuer (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d7be675-626c-4173-89e9-e32beef81ad5
description: TokenIssuer 元素指定安全令牌服务的 Uri (SOAP) 和终结点 (SOAP)。
ms.openlocfilehash: 1c267fc6cbfdadd471c568473cc9aeeafb43ae2d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838244"
---
# <a name="tokenissuer-soap"></a>TokenIssuer (SOAP)

**TokenIssuer**元素指定安全令牌服务的[Uri (SOAP)](uri-soap.md)和[终结点 (SOAP)](endpoint-soap.md) 。 
  
```XML
<TokenIssuer>
   <Uri/>
   <Endpoint/>
</TokenIssuer>
```

 **TokenIssuer**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Uri (SOAP)](uri-soap.md) <br/> |安全令牌颁发的安全令牌服务的 URI。  <br/> |
|[终结点 (SOAP)](endpoint-soap.md) <br/> |Web 服务终结点 URI。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[TokenIssuers (SOAP)](tokenissuers-soap.md) <br/> |表示安全令牌服务[Uri (SOAP)](uri-soap.md)的集合和[终结点 (SOAP)](endpoint-soap.md)。  <br/> |
   
## <a name="remarks"></a>备注

使用**TokenIssuer**元素指定安全令牌服务时使用安全令牌。 
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|架构名称  <br/> |自动发现架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[Exchange 的自动发现 web 服务引用](autodiscover-web-service-reference-for-exchange.md)
  
[SOAP Exchange 2013 自动发现 XML 元素](soap-autodiscover-xml-elements-for-exchange-2013.md)

