---
title: 开始
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Start
api_type:
- schema
ms.assetid: 7cfe9979-c893-4f9b-b3a1-8f9e17515a4b
description: Start 元素表示持续时间的开始。
ms.openlocfilehash: 7342e285e57a165ec4a9ba0b8551bfbe045d3b9c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521268"
---
# <a name="start"></a>开始

**Start** 元素表示持续时间的开始。 
  
```xml
<Start/>
```

**DateTime**

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
|[DeletedOccurrence](deletedoccurrence.md) <br/> |表示定期日历项目的已删除匹配项。  <br/> |
|[FirstOccurrence](firstoccurrence.md) <br/> |表示第一次出现的定期日历项目。  <br/> |
|[LastOccurrence](lastoccurrence.md) <br/> |表示最后一次出现的定期日历项目。  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |表示 Exchange 存储中的会议请求。  <br/> |
|[Occurrence](occurrence.md) <br/> |表示定期日历项目的单个修改事件。  <br/> |
   
## <a name="text-value"></a>文本值

文本值表示持续时间的开始。
  
## <a name="remarks"></a>注解

UpdateItem 操作[可以设置](start.md)Exchange[](end-ex15websvcsotherref.md)存储项目的开始时间和结束时间。 在 UpdateItem 请求中， **可以** 设置开始时间，而无需同时设置 **结束** 时间。 如果开始时间晚于结束 **时间** ， **这可能会导致错误** 。 请注意，客户端应用程序必须在更改"开始时间"时对"结束时间"执行调整以保留持续时间。 
  
> [!NOTE]
> 如果定期主项目的开始日期和结束日期的日期不[](start.md)等于每周[](end-ex15websvcsotherref.md)日历的第一次发生日期，则时区偏移定期模式。 
  
描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [WeeklyRecurrence](weeklyrecurrence.md)
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

