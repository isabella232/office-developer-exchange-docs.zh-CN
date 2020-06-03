---
title: IsArchive
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b89d8a78-5c18-4547-aaf4-4b16a93190a7
description: IsArchive 元素指定一个布尔值，该值指示邮箱是否为存档邮箱。
ms.openlocfilehash: 6d0be0eb283de3f4d8f786ff96f4a0d4f49e2009
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526513"
---
# <a name="isarchive"></a>IsArchive

**IsArchive**元素指定一个布尔值，该值指示邮箱是否为存档邮箱。 
  
```XML
<IsArchive>true | false</IsArchive>
```

 **Boolean**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[FailedMailbox](failedmailbox.md)  | [Get-retentionpolicytag](retentionpolicytag.md)
  
## <a name="text-value"></a>文本值

如果**IsArchive**元素的文本值为**true** ，则表示目标邮箱是存档邮箱。 **如果值为 false** ，则表示目标邮箱不是存档邮箱。 
  
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

