---
title: RequestType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RequestType
api_type:
- schema
ms.assetid: 4e657e57-528f-4250-a99c-f9850bbbcec5
description: RequestType 元素标识代理请求是跨站点请求还是跨林请求。
ms.openlocfilehash: 3390381b903c7a39a1d2ea6cae80b3fbc07eba43
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541852"
---
# <a name="requesttype"></a>RequestType

**RequestType** 元素标识代理请求是跨站点请求还是跨林请求。 
  
```xml
<RequestType>CrossSite or CrossForest</RequestType>
```

 **AvailabilityProxyRequestType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

此元素在架构中没有父级。 此元素在 SOAP 标头中使用。 有关如何使用此元素的信息，请参阅 WSDL 文件。
  
## <a name="text-value"></a>文本值

此元素需要文本值。 以下是可能的值：
  
- CrossSite
    
- CrossForest
    
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

