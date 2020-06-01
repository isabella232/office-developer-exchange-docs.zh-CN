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
description: CalendarView 元素将 FindItem 操作定义为返回日历中显示的日历项目。
ms.openlocfilehash: e547a4b2db5c09ebefd9a072da6cc4733818002e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462260"
---
# <a name="calendarview"></a>CalendarView

**CalendarView**元素将[FindItem 操作](finditem-operation.md)定义为返回日历中显示的日历项目。 
  
[FindItem](finditem.md)
  
[CalendarView](calendarview.md)
  
```XML
<CalendarView MaxEntriesReturned="" StartDate="" EndDate="" />
```

**CalendarView**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**MaxEntriesReturned** <br/> |描述在 FindItem 响应中返回的最大结果数。  <br/> |
|**StartDate** <br/> |标识为日历项目查询的时间范围的开始时间。 将不返回开始**日期**前结束时间的所有日历项目。 开始**日期**值可以指定为协调世界时（UTC）格式，如 2006-01-02T12：00：00Z，或以指定本地时间和时区偏移量的格式（如 2006-01-02T04：00：00：00：00：00：00：00：00：00：00）。  <br/><br/>此特性是必需的。  <br/> |
|**EndDate** <br/> |标识为日历项目查询的时间范围的结束时间。 将不返回开始时间或**结束时间结束**的所有日历项目。 **结束**日期的值可以指定为 UTC 格式，如 2006-02-02T12：00：00Z，或以指定本地时间和时区偏移量的格式（如 2006-02-02T04：00： 00-08：00中所示）。  <br/><br/>**结束**日期必须大于或等于开始**日期**;否则，将返回错误。 此特性是必需的。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |定义在邮箱中查找项目的请求。<br/><br/> 下面是此元素的 XPath 表达式：   <br/>  `/FindItem` <br/> |
   
## <a name="remarks"></a>备注

如果在 FindItem 请求中指定了**CalendarView**元素，则 Web 服务将在**起始日期**和**结束**日期指定的范围内返回单个日历项目和定期日历项目的匹配项的列表。
  
如果 FindItem 请求中未指定**CalendarView**元素，则 Web 服务将返回单个日历项目和定期主日历项目的列表。 不展开定期日历项目的日历事件。 
  
CalendarView 查询应仅使用下列属性，因为它们支持更快的日历查询。
  
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
    
### <a name="calculated-from-the-primary-recurrence-blob-or-master"></a>通过主定期 blob 或主机计算
  
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
    
### <a name="master-calendar-item-properties"></a>主日历项目属性
  
- EntryId
    
- ChangeKey
    
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

下面的示例展示了一个 FindItem 请求。 成功的请求将返回一个响应，其中包括在2006年-18T00：00：00：00：00：00：00：00：00：00：00：00：00：00：00： 00-08：00之前开始的日历项目。
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem Traversal="Shallow" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [FindItem 操作](finditem-operation.md)
- [查找项目](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

