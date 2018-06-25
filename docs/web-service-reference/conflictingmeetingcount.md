---
title: ConflictingMeetingCount
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConflictingMeetingCount
api_type:
- schema
ms.assetid: 11f4d93a-b514-4a27-8d19-f4f0a35a185e
description: ConflictingMeetingCount 元素均表示与日历项目发生冲突的会议数。
ms.openlocfilehash: ace800982c284cf65ff22d92c711197ee5ee1d06
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753478"
---
# <a name="conflictingmeetingcount"></a>ConflictingMeetingCount

**ConflictingMeetingCount**元素均表示与日历项目发生冲突的会议数。 
  
```xml
<ConflictingMeetingCount/>
```

 **int**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[MeetingRequest](meetingrequest.md) <br/> |表示 Exchange 存储中的会议。  <br/> |
|[日历项目](calendaritem.md) <br/> |表示 Exchange 日历项。  <br/> |
   
## <a name="text-value"></a>文本值

文本值表示一个整数。 此属性是只读的。
  
## <a name="remarks"></a>注解

日历项被视为发生时，至少在部件中，为相同的日历文件夹中的另一个日历项同时冲突。 如果日历项目 noncalendar 文件夹中，将与默认的日历文件夹中的日历项目进行比较。 与默认的日历文件夹中的日历项目，会议请求进行比较。
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

