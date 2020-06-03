---
title: RetentionAction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3bdf5955-1212-48a1-b3b5-743086866c91
description: RetentionAction 元素指定对带有保留标记的项目执行的操作。
ms.openlocfilehash: c16988413e732ddc3cd6ebc355cb73c4d96550c7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465231"
---
# <a name="retentionaction"></a>RetentionAction

**RetentionAction**元素指定对带有保留标记的项目执行的操作。 
  
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

[Get-retentionpolicytag](retentionpolicytag.md)
  
## <a name="text-value"></a>文本值

**RetentionAction**元素的文本值是对项目执行的操作。 以下列表包含**RetentionAction**元素的文本值。 
  
> **无**-对项目不执行任何操作。 
    
> **MoveToDeletedItems** -将项目移动到默认的 "已删除邮件" 文件夹。 
    
> **MoveToFolder** -将项目移动到指定的文件夹。 
    
> **DeleteAndAllowRecovery** -将删除该项目并将其放入转储程序中。 
    
> **PermanentlyDelete** -项目从邮箱中永久删除。 
    
> **MarkAsPastRetentionLimit** -项目被标记为已超过保留时间限制。 
    
> **MoveToArchive** -将项目移动到存档邮箱。 
    
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
   

