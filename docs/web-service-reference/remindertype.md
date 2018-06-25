---
title: ReminderType
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfaf84eb-271a-4728-84fc-a20205a100bd
description: ReminderType 元素指定的提醒，以便在返回的类型。
ms.openlocfilehash: 11739d2068a1009b2840b2169e86b113151cbfa9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827077"
---
# <a name="remindertype"></a>ReminderType

**ReminderType**元素指定的提醒，以便在返回的类型。 
  
```XML
<ReminderType> All | Current | Old </ReminderType>
```

 **string**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[GetReminders](getreminders.md)
  
## <a name="text-value"></a>文本值

**ReminderType**元素的文本值的提醒，以便返回，**所有**、**当前**，或**旧**的类型。 **所有**是此元素的建议的值。 有关**ReminderType**元素和[BeginTime](begintime.md)和[EndTime](endtime-remindermessagedatatype.md)元素之间的关系的详细信息，请参阅[GetReminders 操作](getreminders-operation.md)。
  
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetReminders](getreminders.md)


- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

