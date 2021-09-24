---
title: NewReminderTime
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: ff1b6b1c-3557-41d4-8aa6-9528fdb3a21a
description: NewReminderTime 元素指定提醒的新时间。
ms.openlocfilehash: 9e6cb75396f35f606bcd974e374f24957ee5d1ec
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515444"
---
# <a name="newremindertime"></a>NewReminderTime

**NewReminderTime** 元素指定提醒的新时间。 
  
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

**NewReminderTime** 元素的文本值是提醒的新时间。 **NewReminderTime** 元素在 [ActionType](actiontype-reminderactiontype.md)元素设置为 **Snooze** 时使用，以便延迟提醒。 **NewReminderTime** 的值必须大于 [GetReminders](getreminders-operation.md)操作返回的 [ReminderTime。](remindertime.md)
  
## <a name="remarks"></a>注解

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

