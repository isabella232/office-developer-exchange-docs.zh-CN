---
title: RetentionAction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 3bdf5955-1212-48a1-b3b5-743086866c91
description: RetentionAction 元素指定对具有保留标记的项目执行的操作。
ms.openlocfilehash: ecea4326f0e50460635966991cd55badf8946993
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517943"
---
# <a name="retentionaction"></a>RetentionAction

**RetentionAction** 元素指定对具有保留标记的项目执行的操作。 
  
```XML
<RetentionAction> None | MoveToDeletedItems | MoveToFolder | DeleteAndAllowRecovery | PermanentlyDelete | MarkAsPastRetentionLimit | MoveToArchive <RetentionAction>
```

 **RetentionActionType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[RetentionPolicyTag](retentionpolicytag.md)
  
## <a name="text-value"></a>文本值

**RetentionAction** 元素的文本值是项目上执行的操作。 下面的列表包含 **RetentionAction** 元素的文本值。 
  
> **无** - 不对项目执行任何操作。 
    
> **MoveToDeletedItems** - 项目移至默认"已删除邮件"文件夹。 
    
> **MoveToFolder** - 项目移动到指定文件夹。 
    
> **DeleteAndAllowRecovery** - 项目被删除并放入垃圾站中。 
    
> **PermanentlyDelete** - 从邮箱中永久删除项目。 
    
> **MarkAsPastRetentionLimit** - 项目标记为已超出保留时间限制。 
    
> **MoveToArchive** - 项目已移动到存档邮箱。 
    
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> ||
   

