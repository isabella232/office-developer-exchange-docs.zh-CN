---
title: StartTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StartTime
api_type:
- schema
ms.assetid: 1fac7937-7a06-4d66-9d2a-14423bcb3b37
description: StartTime 元素均表示的时间跨度。
ms.openlocfilehash: 4346797d755bb6e577e1cacb8bec656a7562bf1f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827560"
---
# <a name="starttime"></a>StartTime

**StartTime**元素均表示的时间跨度。 
  
```xml
<StartTime/
```

**dateTime**

## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[TimeWindow](timewindow.md) <br/> |标识查询的用户的可用性信息的时间跨度。  <br/><br/> 以下是此元素的 XPath 表达式：  <br/><br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions/TimeWindow` <br/> |
|[DetailedSuggestionsWindow](detailedsuggestionswindow.md) <br/> |标识查询建议的会议时间有关的详细信息的时间跨度。  <br/><br/> 以下是此元素的 XPath 表达式： <br/> <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions/DetailedSuggestionsWindow` <br/> |
|[持续时间 (UserOofSettings)](duration-useroofsettings.md) <br/> | 指定如果[OofState](oofstate.md)元素设置为**计划**为其启用 Office 外出 (OOF) 状态的持续时间。  <br/><br/>  以下是此元素可能 XPath 表达式： <br/> <br/>  `/SetUserOofSettingsRequest/UserOofSettings/Duration` <br/><br/>  `/GetUserOofSettingsResponse/OofSettings/Duration` <br/> |
|[CalendarEvent](calendarevent.md) <br/> |代表独特的日历项匹配项。 这用于可用性的查询。 **StartTime**元素需要**CalendarEvent**元素中。 尽管它包含的**持续时间**类型中的**StartTime**元素包含的方面值相同， **CalendarEvent**元素中的**StartTime**元素是唯一的**CalendarEvent**类型。  <br/><br/> 以下是此元素的 XPath 表达式：  <br/> <br/> `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。
  
## <a name="remarks"></a>备注

[EndTime](endtime.md)元素均表示时间范围的末尾。 
  
架构包括许多[StartTime](starttime.md)元素。 
  
> [!NOTE]
> 描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。 
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [GetUserAvailability 操作](getuseravailability-operation.md)
- [Getting User Availability](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

