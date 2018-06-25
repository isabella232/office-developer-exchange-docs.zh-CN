---
title: 状态 (HoldStatusType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fee3f1f9-e868-49fa-a554-7ff096964718
description: Status 元素指定邮箱的保留状态。
ms.openlocfilehash: c40dc865d2b305ac86fa40d536e2d516a14260ab
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827579"
---
# <a name="status-holdstatustype"></a>状态 (HoldStatusType)

**Status**元素指定邮箱的保留状态。 
  
```XML
<Status> NotOnHold | Pending | OnHold | PartialHold | Failed </Status>
```

 **HoldStatusType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[MailboxHoldStatus](mailboxholdstatus.md)
  
## <a name="text-value"></a>文本值

**Status**元素的文本值是邮箱的保留状态。 **Status**元素可以具有以下列表中的值。 
  
> NotOnHold-邮箱不是置于保持状态。
    
> 挂起的邮箱是挂起正在发出或发布置于保持状态。 
    
> OnHold-保留已成功应用于邮箱。 
    
> PartialHold-保留已成功应用到某些邮箱而不是为所有邮箱。
    
> 保留项失败-未能应用于邮箱。
    
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
   

