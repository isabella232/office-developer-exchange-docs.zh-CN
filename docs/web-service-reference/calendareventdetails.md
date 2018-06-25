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
description: CalendarEventDetails 元素提供了有关日历事件的其他信息。
ms.openlocfilehash: 8df4f3ed4f66c7dcba00e1f0c5b0c383075da0a0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753407"
---
# <a name="calendareventdetails"></a>CalendarEventDetails

**CalendarEventDetails**元素提供了有关日历事件的其他信息。 
  
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

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[标识](id.md) <br/> |代表日历项目的条目 ID。  <br/> |
|[主题 (CalendarEventDetails)](subject-calendareventdetails.md) <br/> |代表日历项目的主题。  <br/> |
|[位置 (CalendarEventDetails)](location-calendareventdetails.md) <br/> |代表位置字段中的日历项目。  <br/> |
|[IsMeeting (CalendarEventDetails)](ismeeting-calendareventdetails.md) <br/> |指示日历事件是会议或约会。  <br/> |
|[IsRecurring (CalendarEventDetails)](isrecurring-calendareventdetails.md) <br/> |指示日历事件是否定期日历项目或单个日历项目的实例。  <br/> |
|[IsException](isexception.md) <br/> |指示是否将定期日历项实例更改从母版。  <br/> |
|[IsReminderSet](isreminderset.md) <br/> |指示是否已设置日历事件提醒。  <br/> |
|[IsPrivate](isprivate.md) <br/> |指示日历项目是否为私有。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CalendarEvent](calendarevent.md) <br/> |代表独特的日历项匹配项。  <br/> 以下是此元素的 XPath 2.0 表达式：  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## <a name="remarks"></a>注解

中发生的顺序排列的所有子元素。 
  
[IsPrivate](isprivate.md)元素为**true**，如果不在响应中返回[CalendarEventDetails](calendareventdetails.md)元素中的所有其他元素。 
  
除非将呼叫者在目标用户的日历上具有读取权限，GetUserAvailability 操作不会返回详细呼叫者信息。 您可以通过使用 Exchange 命令行管理程序设置的访问权限。
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetUserAvailability 操作](getuseravailability-operation.md)
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)


[Getting User Availability](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

