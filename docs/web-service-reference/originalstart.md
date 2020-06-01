---
title: OriginalStart
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OriginalStart
api_type:
- schema
ms.assetid: 4599dd34-15ee-4d57-b886-732081b50784
description: OriginalStart 元素表示日历项目的原始开始时间。
ms.openlocfilehash: 5346a65c432b8e96cb95e412e3e88fbc40ce36e8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462365"
---
# <a name="originalstart"></a>OriginalStart

**OriginalStart**元素表示日历项目的原始开始时间。 
  
```xml
<OriginalStart/>
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
|[CalendarItem](calendaritem.md) <br/> |表示 Exchange 存储中的日历项目。  <br/> |
|[FirstOccurrence](firstoccurrence.md) <br/> |表示定期日历项目的第一个匹配项。  <br/> |
|[LastOccurrence](lastoccurrence.md) <br/> |表示定期日历项目的最后一个事件。  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |表示 Exchange 存储中的会议请求。  <br/> |
|[重复](occurrence.md) <br/> |代表定期日历项目的单个修改事件。  <br/> |
   
## <a name="text-value"></a>文本值

如果使用此元素，则表示日期和时间的文本值是必需的。
  
## <a name="remarks"></a>说明

描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

