---
title: CalendarView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CalendarView
api_type:
- schema
ms.assetid: a4a953b8-0710-416c-95ef-59e51eba9982
description: CalendarView 元素将 FindItem 操作定义为在日历中显示时返回集合中的日历项目。
ms.openlocfilehash: 5e0180bb5e8a6d9fcbe42380abbe32820117ae29
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518825"
---
# <a name="calendarview"></a>CalendarView

**CalendarView** 元素将 [FindItem 操作](finditem-operation.md)定义为在日历中显示时返回集合中的日历项目。 
  
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
|**StartDate** <br/> |标识查询日历项目的时间跨度的开始时间。 不会返回结束时间在 **StartDate** 之前的所有日历项目。 **StartDate** 的值可以使用协调世界时 (UTC) 格式指定（如 2006-01-02T12：00：00Z 中一样）或指定本地时间和时区偏移的格式（如 2006-01-02T04：00：00-08：00）。  <br/><br/>此特性是必需的。  <br/> |
|**EndDate** <br/> |标识查询日历项目的时间跨度的结束时间。 不会返回开始时间在 **EndDate** 或之后的所有日历项目。 **EndDate** 的值可以使用 UTC 格式指定，如 2006-02-02T12：00：00Z 中一样，也可以采用指定本地时间和时区偏移的格式（如 2006-02-02T04：00：00-08：00 中一样）。  <br/><br/>**EndDate** 必须大于或等于 **StartDate**;否则将返回错误。 此特性是必需的。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |定义查找邮箱中的项目的请求。<br/><br/> 下面是此元素的 XPath 表达式：   <br/>  `/FindItem` <br/> |
   
## <a name="remarks"></a>注解

如果在 FindItem 请求中指定了 **CalendarView** 元素，Web 服务将返回由 **StartDate 和 EndDate** 指定的范围内的单个日历项目和定期日历项目发生 **次数的列表**。
  
如果 **FindItem** 请求中未指定 CalendarView 元素，Web 服务将返回单个日历项目和定期主日历项目的列表。 不展开定期日历项目的日历匹配项。 
  
CalendarView 查询应仅使用以下属性，因为它们支持更快的日历查询。
  
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
    
- freeBusyStatus
    
- ReminderIsSetInternal
    
- ReminderMinutesBeforeStartInternal
    
- AppointmentState
    
- AllAttachmentsHidden
    
- ChangeHighlight
    
### <a name="calculated-from-the-primary-recurrence-blob-or-master"></a>从主定期 blob 或主控点计算
  
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

下面的示例展示了 FindItem 请求。 成功的请求返回响应，其中包括从 2006-05-18T00：00：00-08：00 开始或在 2006-05-19T00：00：00-08：00 之前结束的日历项目。
  
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

