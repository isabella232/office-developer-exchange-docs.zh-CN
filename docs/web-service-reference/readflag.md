---
title: ReadFlag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 9d91aa89-9f9f-4877-846d-aaf48bbeec7c
description: ReadFlag 元素指示对文件夹中的项目设置的读取状态。
ms.openlocfilehash: ac079f6adbdb2686221dd52d748b05ac4141d6c6
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523648"
---
# <a name="readflag"></a>ReadFlag

**ReadFlag** 元素指示对文件夹中的项目设置的读取状态。 
  
```XML
<ReadFlag>true | false</ReadFlag>
```

 **Boolean**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[MarkAllItemsAsRead](markallitemsasread.md)
  
## <a name="text-value"></a>文本值

**ReadFlag** 元素的文本值 **true** 指示文件夹中的项目将被标记为已读。 false **值表示** 文件夹中的项目将被标记为未读。 
  
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> ||
   

