---
title: CalendarEventDetails
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CalendarEventDetails
api_type:
- schema
ms.assetid: 2dca0192-b91b-4154-aa09-84da74e875e9
description: CalendarEventDetails 元素提供有关日历事件的其他信息。
ms.openlocfilehash: c332d17b1bb630b9635e64c484b4c5fd989f9845
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516088"
---
# <a name="calendareventdetails"></a>CalendarEventDetails

**CalendarEventDetails** 元素提供有关日历事件的其他信息。 
  
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
|[ID](id.md) <br/> |表示日历项目的条目 ID。  <br/> |
|[Subject (CalendarEventDetails)](subject-calendareventdetails.md) <br/> |表示日历项目的主题。  <br/> |
|[Location (CalendarEventDetails)](location-calendareventdetails.md) <br/> |表示日历项目的位置字段。  <br/> |
|[IsMeeting (CalendarEventDetails)](ismeeting-calendareventdetails.md) <br/> |指示日历事件是会议还是约会。  <br/> |
|[IsRecurring (CalendarEventDetails)](isrecurring-calendareventdetails.md) <br/> |指示日历事件是定期日历项目的实例还是单个日历项目的实例。  <br/> |
|[IsException](isexception.md) <br/> |指示是否从主控对象更改了定期日历项目的实例。  <br/> |
|[IsReminderSet](isreminderset.md) <br/> |指示是否已为日历事件设置提醒。  <br/> |
|[IsPrivate](isprivate.md) <br/> |指示日历项目是否私有。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CalendarEvent](calendarevent.md) <br/> |表示唯一的日历项目事件。  <br/> 下面是此元素的 XPath 2.0 表达式：  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## <a name="remarks"></a>注解

所有子元素都按其发生顺序列出。 
  
如果 [IsPrivate](isprivate.md) 元素 **为 true，** 则响应中不会返回 [CalendarEventDetails](calendareventdetails.md) 元素中的所有其他元素。 
  
GetUserAvailability 操作不会返回详细的呼叫者信息，除非呼叫者对目标用户的日历具有读取访问权限。 可以使用命令行管理程序设置Exchange权限。
  
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

