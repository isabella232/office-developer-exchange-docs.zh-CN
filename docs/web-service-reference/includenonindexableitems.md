---
title: IncludeNonIndexableItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: af7f202b-2889-447e-bdeb-aaad18ce6b46
description: IncludeNonIndexableItems 元素包含一个布尔值，用于指示是否包括无法编制索引的项目。
ms.openlocfilehash: 33ff8c59c3ef1d9a91f87870e0a876c5a39ce795
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514597"
---
# <a name="includenonindexableitems"></a>IncludeNonIndexableItems

**IncludeNonIndexableItems** 元素包含 **一个布尔** 值，用于指示是否包括无法编制索引的项目。 
  
```XML
<IncludeNonIndexableItems>true | false</IncludeNonIndexableItems>
```

 **Boolean**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[SetHoldOnMailboxes](setholdonmailboxes.md)
  
## <a name="text-value"></a>文本值

**IncludeNonIndexableItems** 元素的文本值 **true** 指示无法编制索引的项目包含在邮箱保留中。 false **值表示** 无法编制索引的项目不包含在邮箱保留中。 
  
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |false  <br/> |
   

