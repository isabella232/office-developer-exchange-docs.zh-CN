---
title: TokenIssuer （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d7be675-626c-4173-89e9-e32beef81ad5
description: TokenIssuer 元素指定安全令牌服务的 Uri （SOAP）和终结点（SOAP）。
ms.openlocfilehash: e9c0b4140de26c7ff05daf4e863b3e8a17fedc62
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526324"
---
# <a name="tokenissuer-soap"></a>TokenIssuer （SOAP）

**TokenIssuer**元素指定安全令牌服务的[Uri （Soap）](uri-soap.md)和[终结点（soap）](endpoint-soap.md) 。 
  
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
|[Uri （SOAP）](uri-soap.md) <br/> |颁发安全令牌的 security token service 的 URI。  <br/> |
|[终结点（SOAP）](endpoint-soap.md) <br/> |Web 服务终结点 URI。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[TokenIssuers （SOAP）](tokenissuers-soap.md) <br/> |表示安全令牌服务[Uri （soap）](uri-soap.md)和[终结点（soap）](endpoint-soap.md)的集合。  <br/> |
   
## <a name="remarks"></a>备注

使用**TokenIssuer**元素来指定安全令牌在使用安全令牌时的服务。 
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|架构名称  <br/> |自动发现架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[Exchange 的自动发现 web 服务参考](autodiscover-web-service-reference-for-exchange.md)
  
[Exchange 2013 的 SOAP 自动发现 XML 元素](soap-autodiscover-xml-elements-for-exchange-2013.md)

