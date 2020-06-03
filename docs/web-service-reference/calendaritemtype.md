---
title: CalendarItemType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarItemType
api_type:
- schema
ms.assetid: 1feb0788-adf7-4a7c-830c-005214ad930f
description: CalendarItemType 元素表示日历项目的类型。
ms.openlocfilehash: 05e93b6db3ae574c03f6e43c5ebec2288edec3e5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527192"
---
# <a name="calendaritemtype"></a>CalendarItemType

**CalendarItemType**元素表示日历项目的类型。 
  
```xml
<CalendarItemType/>
```

 **CalendarItemTypeType**
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

如果使用此元素，则需要一个 text 值。 以下是此元素的可能值：
  
- **单一**项目不与定期日历项目相关联。 
    
- **事件**项目是定期日历项的发生。 
    
- **异常**项目是定期日历项目的例外。 
    
- **RecurringMaster**项目是一组定期日历项目的主控形状。 
    
## <a name="remarks"></a>说明

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

