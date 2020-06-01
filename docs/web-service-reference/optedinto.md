---
title: OptedInto
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 083a23d9-acc3-4c15-9d30-c20bf7e6808d
description: OptedInto 元素指定一个布尔值，该值指示用户是否选择保留策略。
ms.openlocfilehash: 1095a8c2527546b8c945dd7efb5c0218f9a151c8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468766"
---
# <a name="optedinto"></a>OptedInto

**OptedInto**元素指定一个布尔值，该值指示用户是否选择保留策略。 
  
```XML
<OptedInto>true | false</OptedInto>
```

 **Boolean**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[Get-retentionpolicytag](retentionpolicytag.md)
  
## <a name="text-value"></a>文本值

如果**OptedInto**元素的文本值为**true** ，则指示用户选择保留策略。 **如果值为 false** ，则表示用户未选择保留策略。 
  
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> ||
   

