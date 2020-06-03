---
title: NewReminderTime
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ff1b6b1c-3557-41d4-8aa6-9528fdb3a21a
description: NewReminderTime 元素指定提醒的新时间。
ms.openlocfilehash: a10f7e481b474501f33dba4c09060766568952b0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465952"
---
# <a name="newremindertime"></a>NewReminderTime

**NewReminderTime**元素指定提醒的新时间。 
  
```XML
<NewReminderTime/>
```

 **string**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[ReminderItemAction](reminderitemaction.md)
  
## <a name="text-value"></a>文本值

**NewReminderTime**元素的文本值是提醒的新时间。 当[ActionType](actiontype-reminderactiontype.md)元素设置为 "**暂停**" 时，将使用**NewReminderTime**元素，以便延迟提醒。 **NewReminderTime**的值必须大于[GetReminders 操作](getreminders-operation.md)返回的[ReminderTime](remindertime.md) 。
  
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



[ReminderItemAction](reminderitemaction.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

