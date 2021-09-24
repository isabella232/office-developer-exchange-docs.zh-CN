---
title: ReminderType
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: bfaf84eb-271a-4728-84fc-a20205a100bd
description: ReminderType 元素指定要返回的提醒的类型。
ms.openlocfilehash: ab10db372efb935b335868f5d212ded84b29e6eb
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517999"
---
# <a name="remindertype"></a>ReminderType

**ReminderType** 元素指定要返回的提醒的类型。 
  
```XML
<ReminderType> All | Current | Old </ReminderType>
```

 **string**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[GetReminders](getreminders.md)
  
## <a name="text-value"></a>文本值

**ReminderType** 元素的文本值是要返回的提醒类型，**即 All、Current** 或 **Old。** **All** 是此元素的建议值。 有关 **ReminderType** 元素与 [BeginTime](begintime.md) 和 [EndTime](endtime-remindermessagedatatype.md) 元素之间的关系详细信息，请参阅 [GetReminders 操作](getreminders-operation.md)。
  
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetReminders](getreminders.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

