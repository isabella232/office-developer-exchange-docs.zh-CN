---
title: State （TeamMailboxLifecycleStateType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3b1bc531-6988-41c3-9aad-3f5ad5b732a9
description: State 元素包含在网站邮箱上设置的生命周期状态。
ms.openlocfilehash: 597946b48649d997f8dd57823b4e0fcc091a6f84
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465161"
---
# <a name="state-teammailboxlifecyclestatetype"></a>State （TeamMailboxLifecycleStateType）

**State**元素包含在网站邮箱上设置的生命周期状态。 
  
```XML
<State> Active | Closed | Unlinked | PendingDelete </State>
```

**TeamMailboxLifecycleStateType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[SetTeamMailbox](setteammailbox.md)
  
## <a name="text-value"></a>文本值

**State**元素的文本值是在网站邮箱上设置的生命周期状态。 **活动**的文本值表示网站邮箱处于活动使用状态。 "**已关闭**" 文本值表示网站邮箱已关闭，未处于活动使用状态。 未**链接**的文本值表示网站邮箱未链接到基于 web 的协作环境。 **活动**、**闭合**和**PendingDelete**值是互斥的，但未**链接**的值不与其他值互斥。 文本值为**PendingDelete**表示网站邮箱正在等待删除。 必须先关闭网站邮箱，然后才能将其设置为**PendingDelete**。
  
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> ||
   

