---
title: HasAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de152be6-fc2f-48bc-a05d-1211935da20a
description: HasAttachment 元素指定一个布尔值，以指示该项目是否具有附件。
ms.openlocfilehash: c6bc0932a08a1bbec215bb8a974ed746d2961123
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530259"
---
# <a name="hasattachment"></a>HasAttachment

**HasAttachment**元素指定一个布尔值，以指示该项目是否具有附件。 
  
```XML
<HasAttachment> true | false </HasAttachment
```

 **Boolean**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[SearchPreviewItem](searchpreviewitem.md) <br/> |指定在不打开项目的情况下预览邮箱项目的前256个字符。  <br/> |
   
## <a name="text-value"></a>文本值

如果**HasAttachment**元素的文本值为**true** ，则表示该项目具有附件。 **如果值为 false** ，则表示该项目没有附件。 
  
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

