---
title: EndTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- EndTime
api_type:
- schema
ms.assetid: 82e4ef4f-a557-4044-b9b7-d91622f4ac55
description: EndTime 元素表示时间跨度的结束。
ms.openlocfilehash: 9b7dde6c318bb198e1ec25df19cf3a053feff5cf
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540053"
---
# <a name="endtime"></a>EndTime

**EndTime** 元素表示时间跨度的结束。 
  
```xml
<EndTime>dateTime</EndTime>
```

 **dateTime**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[TimeWindow](timewindow.md) <br/> |标识查询用户可用性信息的时间跨度。<br/><br/> 下面是此元素的 XPath 表达式： <br/><br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions/TimeWindow` <br/> |
|[DetailedSuggestionsWindow](detailedsuggestionswindow.md) <br/> |标识查询有关建议的会议时间的详细信息的时间跨度。<br/><br/> 下面是此元素的 XPath 表达式： <br/><br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions/DetailedSuggestionsWindow`.  <br/> |
|[Duration (UserOofSettings)](duration-useroofsettings.md) <br/> | 指定在 [OofState](oofstate.md)元素设置为 scheduled Office (OOF) 启用的 **持续时间**。  <br/><br/>  以下是此元素的可能 XPath 表达式：<br/><br/>  `/SetUserOofSettingsRequest/UserOofSettings/Duration` <br/><br/>  `/GetUserOofSettingsResponse/OofSettings/Duration` <br/> |
|[Occurrence](occurrence.md) <br/> |表示定期日历项目的单个修改事件。  <br/> |
|[CalendarEvent](calendarevent.md) <br/> |表示唯一的日历项目事件。 这用于可用性查询。 **EndTime** 元素是 **CalendarEvent** 元素中的必需元素。 **CalendarEvent** 元素中的 **EndTime** 元素对于 **CalendarEvent** 类型是唯一的。<br/><br/> 下面是此元素的 XPath 表达式： <br/><br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。
  
## <a name="remarks"></a>说明

[StartTime](starttime.md)元素表示时间跨度的开始。 
  
结束时间表示客户端的时间。
  
该架构包括许多 [EndTime](endtime.md) 元素。 
  
> [!NOTE]
> 描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。 
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [GetUserAvailability 操作](getuseravailability-operation.md)
- [获取用户可用性](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

