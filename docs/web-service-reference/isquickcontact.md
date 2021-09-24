---
title: IsQuickContact
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 1c9542d6-ef72-4743-828a-bb671e783836
description: IsQuickContact 元素指定一个布尔值，该值指示基础联系人是否是快速联系人。
ms.openlocfilehash: 7821332e685b44983787ce05cc6b6ef4250ee01d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59509684"
---
# <a name="isquickcontact"></a>IsQuickContact

**IsQuickContact** 元素指定一个布尔值，该值指示基础联系人是否是快速联系人。 
  
```XML
<IsQuickContact>true | false</IsQuickContact>
```

 **boolean**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Attribution (PersonaAttributionType)](attribution-personaattributiontype.md) <br/> |指定 **Persona** 元素的属性数组中的实例。  <br/> |
   
## <a name="text-value"></a>文本值

**IsQuickContact** 元素的文本值 **true** 指示联系人是快速联系人。 false **值表示** 该联系人不是快速联系人。 
  
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |types.xsd  <br/> |
|可以为空  <br/> |false  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

