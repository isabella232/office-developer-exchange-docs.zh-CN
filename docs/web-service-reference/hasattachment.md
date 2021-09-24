---
title: HasAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: de152be6-fc2f-48bc-a05d-1211935da20a
description: HasAttachment 元素指定一个布尔值，以指示项目是否具有附件。
ms.openlocfilehash: c3d153e86a9d170c69e74bdc08a3bdedfa5e1220
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516795"
---
# <a name="hasattachment"></a>HasAttachment

**HasAttachment** 元素指定一个布尔值，以指示项目是否具有附件。 
  
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
|[SearchPreviewItem](searchpreviewitem.md) <br/> |指定用于预览的邮箱项目的前 256 个字符，而无需打开该项目。  <br/> |
   
## <a name="text-value"></a>文本值

**HasAttachment** 元素的文本值 **true** 指示项目具有附件。 false **值表示** 项目没有附件。 
  
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |types.xsd  <br/> |
|可以为空  <br/> ||
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

