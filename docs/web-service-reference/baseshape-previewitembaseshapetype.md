---
title: BaseShape (PreviewItemBaseShapeType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7b9e2fdd-5678-4178-9297-7f12a3ca9d64
description: BaseShape 元素指定具有返回的所有属性的默认预览或返回较少属性的精简预览。
ms.openlocfilehash: 29f008840d649f97dfb299fee8e7bf5aaa573404
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527416"
---
# <a name="baseshape-previewitembaseshapetype"></a>BaseShape (PreviewItemBaseShapeType)

**BaseShape**元素指定具有返回的所有属性的默认预览或返回较少属性的精简预览。 
  
```XML
<BaseShape> Default | Compact</BaseShape>
```

 **PreviewItemBaseShapeType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**描述**|
|:-----|:-----|
|[PreviewItemResponseShape](previewitemresponseshape.md) <br/> |包含响应的形状。  <br/> |
   
## <a name="text-value"></a>文本值

**BaseShape 元素文本值**

|**值**|**说明**|
|:-----|:-----|
|默认  <br/> |指示显示所有属性。  <br/> |
|紧凑型  <br/> |指示仅显示选定的属性。  <br/> |
   
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |类型 .xsd  <br/> |
|可以为空  <br/> ||
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

