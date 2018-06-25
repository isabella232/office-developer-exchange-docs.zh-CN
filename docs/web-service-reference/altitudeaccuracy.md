---
title: AltitudeAccuracy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aadc1f90-e9ab-4411-b51f-2d43e5e22f2a
description: AltitudeAccuracy 元素指定邮政地址的海拔属性的准确性。
ms.openlocfilehash: 09ec86e4913327feb47067f5e5de7a60efc47bc5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753139"
---
# <a name="altitudeaccuracy"></a>AltitudeAccuracy

**AltitudeAccuracy**元素指定邮政地址的海拔属性的准确性。 
  
```XML
<AltitudeAccuracy></AltitudeAccuracy>
```

 **xs:double**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[PostalAddress (PersonaPostalAddressType)](postaladdress-personapostaladdresstype.md) <br/> |指定位置的邮政地址。  <br/> |
   
## <a name="text-value"></a>文本值

**AltitudeAccuracy**元素的文本值是邮寄地址的海拔属性的准确性估计值。 
  
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |types.xsd  <br/> |
|可以为空  <br/> ||
   
## <a name="see-also"></a>另请参阅

- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

