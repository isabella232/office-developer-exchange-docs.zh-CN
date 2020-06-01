---
title: ActionType （ReminderActionType）
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0ffcdcf4-8ea3-483c-bb7f-0cd84126120c
description: ActionType 元素指定要对提醒执行的操作。
ms.openlocfilehash: 5c62b2dd945b23a5ff2bb824385c45dbc617a5a5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465056"
---
# <a name="actiontype-reminderactiontype"></a>ActionType （ReminderActionType）

**ActionType**元素指定要对提醒执行的操作。 
  
```XML
<ActionType> Dismiss | Snooze </ActionType>
```

 **ReminderActionType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[ReminderItemAction](reminderitemaction.md)
  
## <a name="text-value"></a>文本值

**ActionType**元素的文本值指定要对提醒执行的操作。 "**取消**" 文本值表示应消除提醒。 "**推迟**" 的文本值表示提醒应延迟到[NewReminderTime](newremindertime.md)元素指定的时间。 
  
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [ReminderItemAction](reminderitemaction.md)
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

