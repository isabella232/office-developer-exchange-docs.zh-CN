---
title: MeetingWorkspaceUrl
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MeetingWorkspaceUrl
api_type:
- schema
ms.assetid: 0ca942fe-8f57-4065-93ad-65790f9a04c3
description: MeetingWorkspaceUrl 元素包含日历项目中包含的会议工作区的 URL。 "会议工作区" 是用于规划会议和跟踪结果的共享网站。
ms.openlocfilehash: cd4396e590ab1471278bd44b9a4e0009fe326eaf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466281"
---
# <a name="meetingworkspaceurl"></a>MeetingWorkspaceUrl

**MeetingWorkspaceUrl**元素包含日历项目中包含的会议工作区的 URL。 "会议工作区" 是用于规划会议和跟踪结果的共享网站。 
  
```xml
<MeetingWorkspaceUrl/>
```

 **string**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[MeetingRequest](meetingrequest.md) <br/> |表示 Exchange 存储中的会议。  <br/> |
|[CalendarItem](calendaritem.md) <br/> |表示 Exchange 日历项。  <br/> |
   
## <a name="text-value"></a>文本值

如果使用此元素，则需要一个表示 URL 的文本值。
  
## <a name="remarks"></a>备注

对于组织者的日历项目，MeetingWorkspaceUrl 属性是可读写的。 对于会议请求和与会者的日历项目，它是只读的。
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

