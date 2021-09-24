---
title: DeletedOccurrences
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DeletedOccurrences
api_type:
- schema
ms.assetid: 736fb305-9528-4be8-ad37-65d7556edbf2
description: DeletedOccurrences 元素包含定期日历项目的已删除事件的数组。
ms.openlocfilehash: b1e60bfee9dbc8e5691db2a13474a945da0484af
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510244"
---
# <a name="deletedoccurrences"></a>DeletedOccurrences

**DeletedOccurrences** 元素包含定期日历项目的已删除事件的数组。 
  
```xml
<DeletedOccurrences>
   <DeletedOccurrence/>
</DeletedOccurrences>
```

 **NonEmptyArrayOfDeletedOccurrencesType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[DeletedOccurrence](deletedoccurrence.md) <br/> |表示定期日历项目的已删除匹配项。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |表示 Exchange 日历项。  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |表示 Exchange 存储中的会议请求。  <br/> |
   
## <a name="remarks"></a>注解

如果 [CalendarItemType](calendaritemtype.md) 元素使用 RecurringMaster 文本值，则此元素有效。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)  
- [Exchange 的 EWS 引用](ews-reference-for-exchange.md)

