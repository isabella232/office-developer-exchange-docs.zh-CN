---
title: Status (HoldStatusType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: fee3f1f9-e868-49fa-a554-7ff096964718
description: Status 元素指定邮箱的保留状态。
ms.openlocfilehash: a055dde61ae52c266f2349036c881d2b00557171
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521233"
---
# <a name="status-holdstatustype"></a>Status (HoldStatusType)

**Status** 元素指定邮箱的保留状态。 
  
```XML
<Status> NotOnHold | Pending | OnHold | PartialHold | Failed </Status>
```

 **HoldStatusType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[MailboxHoldStatus](mailboxholdstatus.md)
  
## <a name="text-value"></a>文本值

**Status** 元素的文本值是邮箱的保留状态。 **Status** 元素具有以下列表中的值。 
  
> NotOnHold - 邮箱未置于保留状态。
    
> Pending - 邮箱处于待定状态，或处于保留状态。 
    
> OnHold - 已成功将保留应用于邮箱。 
    
> PartialHold - 保留已成功应用于某些邮箱，而不是所有邮箱。
    
> 失败 - 无法将保留应用于邮箱。
    
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
   

