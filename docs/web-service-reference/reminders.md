---
title: Reminders
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 19294300-ab84-4784-8aa7-3395a08de640
description: Reminders 元素指定响应 GetReminders 请求时返回的提醒。
ms.openlocfilehash: 0b760e93bf27f0fdaad9464580fad924367dea32
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513407"
---
# <a name="reminders"></a>Reminders

**Reminders** 元素指定响应 **GetReminders** 请求时返回的提醒。 
  
```XML
<Reminders>
   <Reminder></Reminder>
</Reminders>
```

 **ArrayOfRemindersType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

[提醒](reminder.md)
  
### <a name="parent-elements"></a>父元素

[GetRemindersResponse](getremindersresponse.md)
  
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



[GetRemindersResponse](getremindersresponse.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

