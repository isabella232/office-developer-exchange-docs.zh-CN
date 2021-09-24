---
title: State (TeamMailboxLifecycleStateType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 3b1bc531-6988-41c3-9aad-3f5ad5b732a9
description: State 元素包含在站点邮箱上设置的生命周期状态。
ms.openlocfilehash: 5189ee8573fd33d2265fd60c47bb40d17b16b8fe
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59538966"
---
# <a name="state-teammailboxlifecyclestatetype"></a>State (TeamMailboxLifecycleStateType)

**State** 元素包含在站点邮箱上设置的生命周期状态。 
  
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

**State** 元素的文本值是在站点邮箱上设置的生命周期状态。 Active **的文本值表示** 站点邮箱正被使用。 文本值 **Closed** 表示已关闭网站邮箱，并且未在活动使用中。 "未链接 **"的文本** 值表示网站邮箱未链接到基于 Web 的协作环境。 **Active、Closed** 和 **PendingDelete** 值相互排斥，但 **Unlinked** 值不相互排斥其他值。  **PendingDelete 的文本** 值指示网站邮箱正在等待删除。 网站邮箱必须关闭才能设置为 **PendingDelete**。
  
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
   

