---
title: IsRecurring
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IsRecurring
api_type:
- schema
ms.assetid: f4df6997-8d5b-4893-a4a5-fc7047e0a9c3
description: IsRecurring 元素指示日历项目、会议请求或任务是否是定期项目的一部分。 此元素是只读的。
ms.openlocfilehash: ea910b78e962906285a73c869e394147c324372c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59532724"
---
# <a name="isrecurring"></a>IsRecurring

**IsRecurring** 元素指示日历项目、会议请求或任务是否是定期项目的一部分。 此元素是只读的。 
  
```xml
<IsRecurring/>
```

 **Boolean**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |表示 Exchange 日历项。  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |表示 Exchange 存储中的会议请求。  <br/> |
|[任务](task.md) <br/> |表示 Exchange 存储中的任务。  <br/> |
   
## <a name="text-value"></a>文本值

表示一个布尔值的文本值是必需的。
  
## <a name="remarks"></a>注解

下表显示了如何为组织者和与会者的不同日历项目类型以及会议请求和更新设置 **IsRecurring** 属性。 
  
|**CalendarItem 类型**|**组织者  <br/> (IsRecurring)**|**<br/>IsRecurring (Attendee)**|**<br/>IsRecurring (会议请求/)**|
|:-----|:-----|:-----|:-----|
|单次出现  <br/> |**FALSE** <br/> |**FALSE** <br/> |**FALSE** <br/> |
|定期母版  <br/> |**FALSE** <br/> |**TRUE** <br/> |**TRUE** <br/> |
|定期异常  <br/> |**TRUE** <br/> |**TRUE** <br/> |**TRUE** <br/> |
   
为组织者的定期主日历项目设置的 **IsRecurring** 属性值不正确;此值应设置为 **TRUE**。 
  
> [!NOTE]
> GetUserAvailability 操作还具有一个 [IsRecurring (CalendarEventDetails) ](isrecurring-calendareventdetails.md) 元素。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[TaskType.IsRecurring](https://msdn.microsoft.com/library/ExchangeWebServices.TaskType.IsRecurring.aspx)
  
[CalendarEventDetails.IsRecurring](https://msdn.microsoft.com/library/ExchangeWebServices.CalendarEventDetails.IsRecurring.aspx)
  
[CalendarItemType.IsRecurring](https://msdn.microsoft.com/library/ExchangeWebServices.CalendarItemType.IsRecurring.aspx)
  
[MeetingRequestMessageType.IsRecurring](https://msdn.microsoft.com/library/ExchangeWebServices.MeetingRequestMessageType.IsRecurring.aspx)
  
[CalendarItemType.IsRecurringSpecified](https://msdn.microsoft.com/library/ExchangeWebServices.CalendarItemType.IsRecurringSpecified.aspx)
  
[MeetingRequestMessageType.IsRecurringSpecified](https://msdn.microsoft.com/library/ExchangeWebServices.MeetingRequestMessageType.IsRecurringSpecified.aspx)
  
[TaskType.IsRecurringSpecified](https://msdn.microsoft.com/library/ExchangeWebServices.TaskType.IsRecurringSpecified.aspx)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

