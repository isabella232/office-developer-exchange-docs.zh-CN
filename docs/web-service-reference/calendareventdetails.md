---
title: CalendarEventDetails
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarEventDetails
api_type:
- schema
ms.assetid: 2dca0192-b91b-4154-aa09-84da74e875e9
description: CalendarEventDetails 元素提供有关日历事件的其他信息。
ms.openlocfilehash: 3e1dbba00bce4a1fdc53f3330527764c516890ab
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459067"
---
# <a name="calendareventdetails"></a>CalendarEventDetails

**CalendarEventDetails**元素提供有关日历事件的其他信息。 
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)
  
[FreeBusyResponseArray](freebusyresponsearray.md)
  
[FreeBusyResponse](freebusyresponse.md)
  
[FreeBusyView](freebusyview.md)
  
[CalendarEventArray](calendareventarray.md)
  
[CalendarEvent](calendarevent.md)
  
[CalendarEventDetails](calendareventdetails.md)
  
```xml
<CalendarEventDetails>
   <ID/>
   <Subject/>
   <Location/>
   <IsMeeting/>
   <IsRecurring/>
   <IsException/>
   <IsReminderSet/>
   <IsPrivate/>
</CalendarEventDetails>
```

 **CalendarEventDetails**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ID](id.md) <br/> |代表日历项目的条目 ID。  <br/> |
|[Subject （CalendarEventDetails）](subject-calendareventdetails.md) <br/> |代表 "日历" 项目的主题。  <br/> |
|[Location （CalendarEventDetails）](location-calendareventdetails.md) <br/> |代表 "日历" 项目的 "位置" 字段。  <br/> |
|[IsMeeting (CalendarEventDetails)](ismeeting-calendareventdetails.md) <br/> |指示日历事件是否为会议或约会。  <br/> |
|[IsRecurring （CalendarEventDetails）](isrecurring-calendareventdetails.md) <br/> |指示日历事件是定期日历项目的实例还是单个日历项目。  <br/> |
|[IsException](isexception.md) <br/> |指示定期日历项目的实例是否已从主控形状更改。  <br/> |
|[IsReminderSet](isreminderset.md) <br/> |指示是否已为日历事件设置提醒。  <br/> |
|[IsPrivate](isprivate.md) <br/> |指示日历项目是否为私有。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CalendarEvent](calendarevent.md) <br/> |代表唯一的日历项目事件。  <br/> 以下是此元素的 XPath 2.0 表达式：  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## <a name="remarks"></a>备注

所有子元素都按它们出现的顺序列出。 
  
如果[IsPrivate](isprivate.md)元素为**true**，则不会在响应中返回[CalendarEventDetails](calendareventdetails.md)元素中的所有其他元素。 
  
除非呼叫者拥有对目标用户日历的读取访问权限，否则 GetUserAvailability 操作不会返回详细的呼叫者信息。 您可以使用 Exchange 命令行管理程序设置访问权限。
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetUserAvailability 操作](getuseravailability-operation.md)
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)


[Getting User Availability](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

