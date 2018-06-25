---
title: RetentionAction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3bdf5955-1212-48a1-b3b5-743086866c91
description: RetentionAction 元素指定与保留标记的项上执行的操作。
ms.openlocfilehash: 54a1038f2e56aad66f89522423ccfbd69dc44a80
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827215"
---
# <a name="retentionaction"></a>RetentionAction

**RetentionAction**元素指定与保留标记的项上执行的操作。 
  
```XML
<RetentionAction> None | MoveToDeletedItems | MoveToFolder | DeleteAndAllowRecovery | PermanentlyDelete | MarkAsPastRetentionLimit | MoveToArchive <RetentionAction>
```

 **RetentionActionType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[RetentionPolicyTag](retentionpolicytag.md)
  
## <a name="text-value"></a>文本值

**RetentionAction**元素的文本值是在项目上执行的操作。 下面的列表包含**RetentionAction**元素的文本值。 
  
> 项目上执行**无**-任何操作。 
    
> **MoveToDeletedItems** -项目移动到默认删除邮件文件夹。 
    
> **MoveToFolder** -项目移动到指定的文件夹。 
    
> **DeleteAndAllowRecovery** -项目被删除，并置于转储程序。 
    
> 从邮箱永久删除**PermanentlyDelete** -项目。 
    
> **MarkAsPastRetentionLimit** -项目标记为具有超过保留时间限制。 
    
> **MoveToArchive** -项目移动到存档邮箱。 
    
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> ||
   

