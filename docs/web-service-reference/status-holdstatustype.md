---
title: 状态（HoldStatusType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fee3f1f9-e868-49fa-a554-7ff096964718
description: Status 元素指定邮箱的保留状态。
ms.openlocfilehash: cecfdfaf67b00b6f8cf02188e7a4df7062a732e4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459985"
---
# <a name="status-holdstatustype"></a>状态（HoldStatusType）

**Status**元素指定邮箱的保留状态。 
  
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

**Status**元素的文本值是邮箱的保留状态。 **Status**元素的值可以是下表中的值。 
  
> NotOnHold-邮箱未处于保留状态。
    
> 待处理-邮箱挂起或处于保留状态。 
    
> OnHold-已成功将保留应用到邮箱。 
    
> PartialHold-已成功将保留应用于某些邮箱，而不是所有邮箱。
    
> 失败-保留无法应用于邮箱。
    
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
   

