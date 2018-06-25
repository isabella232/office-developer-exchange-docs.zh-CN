---
title: 状态 (TeamMailboxLifecycleStateType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3b1bc531-6988-41c3-9aad-3f5ad5b732a9
description: 状态元素包含对网站邮箱设置的生命周期状态。
ms.openlocfilehash: accd70d36cc34e7364387b98a2e94c56b91f012f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827571"
---
# <a name="state-teammailboxlifecyclestatetype"></a>状态 (TeamMailboxLifecycleStateType)

**状态**元素包含对网站邮箱设置的生命周期状态。 
  
```XML
<State> Active | Closed | Unlinked | PendingDelete </State>
```

**TeamMailboxLifecycleStateType**

## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[SetTeamMailbox](setteammailbox.md)
  
## <a name="text-value"></a>文本值

**状态**元素的文本值是站点邮箱设置的生命周期状态。 **活动**的文本值指示站点邮箱正在使用中。 **已关闭**文本值表示的站点邮箱已关闭，并不是正在使用中。 **未链接**文本值表示的站点邮箱不链接到的基于 web 的协作环境。 **活动**、**已关闭**，和**PendingDelete**值都是互斥的但**未链接**值不互相互斥其他值。 **PendingDelete**文本值指示站点邮箱当前删除未决。 站点邮箱具有要关闭之前可以将其设置为**PendingDelete**。
  
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> ||
   

