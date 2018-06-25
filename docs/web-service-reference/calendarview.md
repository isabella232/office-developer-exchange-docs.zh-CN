---
title: CalendarView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarView
api_type:
- schema
ms.assetid: a4a953b8-0710-416c-95ef-59e51eba9982
description: CalendarView 元素定义为显示日历中一组中返回日历项 FindItem 操作。
ms.openlocfilehash: 79b5ad268a8013092c1122c99bdcd10d876abf2c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753427"
---
# <a name="calendarview"></a>CalendarView

**CalendarView**元素定义为显示日历中一组中返回日历项[FindItem 操作](finditem-operation.md)。 
  
[FindItem](finditem.md)
  
[CalendarView](calendarview.md)
  
```XML
<CalendarView MaxEntriesReturned="" StartDate="" EndDate="" />
```

**CalendarView**

## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|**MaxEntriesReturned** <br/> |最大个数要 FindItem 响应中返回的结果。  <br/> |
|**StartDate** <br/> |标识查询的日历项目的时间范围内的开始。 具有之前不会返回**StartDate**结束时间的所有日历项。 可以采用协调世界时 (UTC) 格式，如 2006年中所示指定的**起始日期**值-01-02T12:00:00Z，或格式为本地时间和时区偏移指定的位置，如所示 2006年-01-02T04:00:00-08:00。  <br/><br/>此属性是必需的。  <br/> |
|**EndDate** <br/> |标识查询日历项目的时间范围的末尾。 不会返回所有已是或**结束日期**之后的开始时间的日历项目。 **EndDate**的值可以指定以 UTC 格式，如下所示 2006年-02-02T12:00:00Z，或格式为本地时间和时区偏移指定的位置，如所示 2006年-02-02T04:00:00-08:00。  <br/><br/>**EndDate**必须大于或等于**StartDate**;否则将返回错误。 此属性是必需的。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |定义查找邮箱中的项目的请求。<br/><br/> 以下是此元素的 XPath 表达式：  <br/>  `/FindItem` <br/> |
   
## <a name="remarks"></a>注解

如果 FindItem 请求中指定的**CalendarView**元素，则 Web 服务返回的单个日历项和匹配项的**StartDate**和**EndDate**指定的范围内的定期日历项目的列表。
  
如果未在 FindItem 请求中指定的**CalendarView**元素，Web 服务返回的单个日历项和定期母版日历项目的列表。 不展开定期日历项目的日历发生次数。 
  
应只进行 CalendarView 查询使用下列属性之一，因为它们支持更快的日历查询。
  
### <a name="recurrence-blob-properties"></a>定期 blob 属性
  
- MapiStartTime
    
- MapiEndTime
    
- SubjectPrefixInternal
    
- NormalizedSubjectInternal
    
- MapiSubject
    
- 位置
    
- AppointmentColor
    
- MapiIsAllDayEvent
    
- MapiHasAttachment
    
- FreeBusyStatus
    
- ReminderIsSetInternal
    
- ReminderMinutesBeforeStartInternal
    
- AppointmentState
    
- AllAttachmentsHidden
    
- ChangeHighlight
    
### <a name="calculated-from-the-primary-recurrence-blob-or-master"></a>从主定期 blob 或主控形状计算
  
- ItemId
    
- IsRecurring
    
- IsException
    
- AppointmentRecurring
    
- MapiStartTime
    
- MapiPRStartDate
    
- MapiEndTime
    
- MapiPREndDate
    
- CalendarItemType
    
- GlobalObjectId
    
- TimeZoneDefinitionStart
    
- TimeZoneDefinitionEnd
    
### <a name="master-calendar-item-properties"></a>母版日历项目属性
  
- EntryId
    
- 更改密钥
    
- ItemClass
    
- SentRepresentingEmailAddress
    
- SentRepresentingDisplayName
    
- SentRepresentingEntryId
    
- AppointmentRecurrenceBlob
    
- TimeZone
    
- TimeZoneBlob
    
- TimeZoneDefinitionRecurring
    
- CleanGlobalObjectId
    
- AppointmentRecurring
    
- IsException
    
- IsRecurring
    
- MapiSensitivity
    
- ContainerClass
    
- MapiPRStartDate
    
- MapiPREndDate
    
- 类别
    
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="example"></a>示例

下面的示例演示一个 FindItem 请求。 成功的请求返回一个响应，其中包括在 2006年启动的日历项目-05-18T00:00:00-08:00 或之后和已结束之前 2006年-05-19T00:00:00-08:00。
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem Traversal="Shallow" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="calendar:Start"/>
          <t:FieldURI FieldURI="calendar:End"/>
          <t:FieldURI FieldURI="item:Subject"/>
        </t:AdditionalProperties>
      </ItemShape>
      <CalendarView MaxEntriesReturned="2" StartDate="2006-05-18T00:00:00-08:00" EndDate="2006-05-19T00:00:00-08:00"/>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="calendar"/>
      </ParentFolderIds>
    </FindItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [FindItem 操作](finditem-operation.md)
- [查找项目](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

