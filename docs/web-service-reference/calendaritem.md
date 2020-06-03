---
title: CalendarItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarItem
api_type:
- schema
ms.assetid: b0c1fd27-b6da-46e5-88b8-88f00c71ba80
description: CalendarItem 元素表示 Exchange 日历项目。
ms.openlocfilehash: b29141470d157ef5bd67be06a1e1fa1c9536b042
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529481"
---
# <a name="calendaritem"></a>CalendarItem

**CalendarItem**元素表示 Exchange 日历项目。 
  
```XML
<CalendarItem>
   <MimeContent/>
   <ItemId/>
   <ParentFolderId/>
   <ItemClass/>
   <Subject/>
   <Sensitivity/>
   <Body/>
   <Attachments/>
   <DateTimeReceived/>
   <Size/>
   <Categories/>
   <InReplyTo/>
   <IsSubmitted/>
   <IsDraft/>
   <IsFromMe/>
   <IsResend/>
   <IsUnmodified/>
   <InternetMessageHeaders/>
   <DateTimeSent/>
   <DateTimeCreated/>
   <ResponseObjects/>
   <ReminderDueBy/>
   <ReminderIsSet/>
   <ReminderMinutesBeforeStart/>
   <DisplayCc/>
   <DisplayTo/>
   <HasAttachments/>
   <ExtendedProperty/>
   <Culture/>
   <Start/>
   <End/>
   <OriginalStart/>
   <IsAllDayEvent/>
   <LegacyFreeBusyStatus/>
   <Location/>
   <When/>
   <IsMeeting/>
   <IsCancelled/>
   <IsRecurring/>
   <MeetingRequestWasSent/>
   <IsResponseRequested/>
   <CalendarItemType/>
   <MyResponseType/>
   <Organizer/>
   <RequiredAttendees/>
   <OptionalAttendees/>
   <Resources/>
   <ConflictingMeetingCount/>
   <AdjacentMeetingCount/>
   <ConflictingMeetings/>
   <AdjacentMeetings/>
   <Duration/>
   <TimeZone/>
   <AppointmentReplyTime/>
   <AppointmentSequenceNumber/>
   <AppointmentState/>
   <Recurrence/>
   <FirstOccurrence/>
   <LastOccurrence/>
   <ModifiedOccurrences/>
   <DeletedOccurrences/>
   <MeetingTimeZone/>
   <StartTimeZone/>
   <EndTimeZone/>
   <ConferenceType/>
   <AllowNewTimeProposal/>
   <IsOnlineMeeting/>
   <MeetingWorkspaceUrl/>
   <NetShowUrl/>
   <EffectiveRights/>
   <LastModifiedName/>
   <LastModifiedTime/>
   <IsAssociated/>
   <WebClientReadFormQueryString/>
   <WebClientEditFormQueryString/>
   <ConversationId/>
   <UniqueBody/>
</CalendarItem>
```

 **CalendarItemType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[MimeContent](mimecontent.md) <br/> |包含以 base64Binary 格式表示的对象的本机多用途 Internet 邮件扩展（MIME）流。  <br/> |
|[ItemId](itemid.md) <br/> |包含 Exchange 存储中某项的唯一标识符和更改键。  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |表示包含项或文件夹的父文件夹的标识符。  <br/> |
|[ItemClass](itemclass.md) <br/> |表示项目的邮件类。  <br/> |
|[主题](subject.md) <br/> |表示 Exchange 存储项和响应对象的主题。  <br/> |
|[Sensitivity](sensitivity.md) <br/> |指示项的敏感度级别。  <br/> |
|[Body](body.md) <br/> |表示邮件的实际正文内容。  <br/> |
|[附件](attachments-ex15websvcsotherref.md) <br/> |包含附加到 Exchange 存储中的项目的项目或文件。  <br/> |
|[DateTimeReceived](datetimereceived.md) <br/> |表示邮箱中的项目的接收日期和时间。  <br/> |
|[大小](size.md) <br/> |表示项的大小（以字节为单位）。 此属性是只读的。  <br/> |
|[类别](categories-ex15websvcsotherref.md) <br/> |表示一个字符串集合，这些字符串标识邮箱中的项目所属的类别。  <br/> |
|[Importance](importance.md) <br/> |介绍项的重要性。  <br/> |
|[InReplyTo](inreplyto.md) <br/> |表示此项是其回复项的标识符。  <br/> |
|[IsSubmitted](issubmitted.md) <br/> |指示是否已将项目提交到 "发件箱" 默认文件夹。  <br/> |
|[IsDraft](isdraft.md) <br/> |指示是否尚未发送项目。  <br/> |
|[IsFromMe](isfromme.md) <br/> |指示用户是否向他或她发送了一项。  <br/> |
|[IsResend](isresend.md) <br/> |指示以前是否已发送过该项目。  <br/> |
|[IsUnmodified](isunmodified.md) <br/> |指示项目是否已被修改。  <br/> |
|[Message](internetmessageheaders.md) <br/> |表示邮箱中的项目所包含的所有 Internet 邮件头的集合。  <br/> |
|[DateTimeSent](datetimesent.md) <br/> |表示邮箱中的项目的发送日期和时间。  <br/> |
|[DateTimeCreated](datetimecreated.md) <br/> |表示邮箱中的给定项目的创建日期和时间。  <br/> |
|[ResponseObjects](responseobjects.md) <br/> |包含与 Exchange 存储中的项目关联的所有响应对象的集合。  <br/> |
|[ReminderDueBy](reminderdueby.md) <br/> |表示事件发生的日期和时间。 [ReminderMinutesBeforeStart](reminderminutesbeforestart.md)元素使用此元素来确定何时显示提醒。  <br/> |
|[ReminderIsSet](reminderisset.md) <br/> |指示是否已为 Exchange 存储中的某个项目设置提醒。  <br/> |
|[ReminderMinutesBeforeStart](reminderminutesbeforestart.md) <br/> |表示在显示提醒时事件之前的分钟数。  <br/> |
|[DisplayCc](displaycc.md) <br/> |代表用于 "抄送" 行内容的显示字符串。 这是所有 Cc 收件人显示名称的串联字符串。  <br/> |
|[DisplayTo](displayto.md) <br/> |表示用于 "To" 行的内容的显示字符串。 这是所有收件人显示名称的串联字符串。  <br/> |
|[HasAttachments](hasattachments.md) <br/> |表示一个属性，如果一个项目至少有一个可见的附件，则设置为**true** 。 此属性是只读的。  <br/> |
|[ExtendedProperty](extendedproperty.md) <br/> |标识文件夹和项的扩展属性。  <br/> |
|[Culture](culture.md) <br/> |表示邮箱中给定项目的区域性。  <br/> |
|[UID](uid.md) <br/> |标识日历项目。  <br/> |
|[RecurrenceId](recurrenceid.md) <br/> |用于标识定期日历项目的特定实例。  <br/> |
|[DateTimeStamp](datetimestamp.md) <br/> |指示 iCalendar 对象的实例的创建日期和时间。  <br/> |
|[开始](start.md) <br/> |代表日历项目的开始。 此元素仅适用于日历项目的一次事件。  <br/> |
|[停止](end-ex15websvcsotherref.md) <br/> |表示持续时间的结束。 此元素仅适用于日历项目的一次事件。  <br/> |
|[OriginalStart](originalstart.md) <br/> |表示日历项目的原始开始时间。  <br/> |
|[IsAllDayEvent](isalldayevent.md) <br/> |指示日历项目或会议请求是否代表全天事件。  <br/> |
|[LegacyFreeBusyStatus](legacyfreebusystatus.md) <br/> |表示日历项目的忙/闲状态。  <br/> |
|[Location](location.md) <br/> |代表会议或约会的位置。  <br/> |
|[When](when.md) <br/> |提供有关何时发生日历项的信息。  <br/> |
|[IsMeeting](ismeeting.md) <br/> |指示日历项目是否为会议或约会。  <br/> |
|[IsCancelled](iscancelled.md) <br/> |指示约会或会议是否已被取消。  <br/> |
|[IsRecurring](isrecurring.md) <br/> |指示日历项目是否是定期项目的一部分。 此元素是只读的。  <br/> |
|[MeetingRequestWasSent](meetingrequestwassent.md) <br/> |指示是否已将会议请求发送到请求的与会者。  <br/> |
|[IsResponseRequested](isresponserequested.md) <br/> |指示是否需要对项目的响应。  <br/> |
|[CalendarItemType](calendaritemtype.md) <br/> |表示日历项的发生类型。  <br/> |
|[MyResponseType](myresponsetype.md) <br/> |包含日历项目的状态或响应。  <br/> |
|[Organizer](organizer.md) <br/> |表示会议的组织者。  <br/> |
|[RequiredAttendees](requiredattendees.md) <br/> |表示参加会议所需的与会者。  <br/> |
|[OptionalAttendees](optionalattendees.md) <br/> |表示参加会议不需要的与会者。  <br/> |
|[资源](resources.md) <br/> |表示会议的计划资源。  <br/> |
|[ConflictingMeetingCount](conflictingmeetingcount.md) <br/> |表示与日历项目相冲突的会议数。  <br/> |
|[AdjacentMeetingCount](adjacentmeetingcount.md) <br/> |表示与会议时间相邻的日历项目的总数。  <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> |标识与会议时间冲突的所有项目。  <br/> |
|[AdjacentMeetings](adjacentmeetings.md) <br/> |介绍与会议时间相邻的所有日历项目。  <br/> |
|[持续时间（项目）](duration-items.md) <br/> |表示日历项的持续时间。  <br/> |
|[时区（项目）](timezone-item.md) <br/> |提供时区的文本说明。  <br/> |
|[AppointmentReplyTime](appointmentreplytime.md) <br/> |表示与会者答复会议请求的日期和时间。  <br/> |
|[AppointmentSequenceNumber](appointmentsequencenumber.md) <br/> |指定约会的一个版本的序列号。  <br/> |
|[AppointmentState](appointmentstate.md) <br/> |指定约会的状态。  <br/> |
|[重复周期（RecurrenceType）](recurrence-recurrencetype.md) <br/> |包含日历项目和会议请求的定期模式。  <br/> 如果[CalendarItemType](calendaritemtype.md)具有 RecurringMaster 值，则此元素有效。  <br/> |
|[FirstOccurrence](firstoccurrence.md) <br/> |表示定期日历项目的第一个匹配项。  <br/> 如果[CalendarItemType](calendaritemtype.md)具有 RecurringMaster 值，则此元素有效。  <br/> |
|[LastOccurrence](lastoccurrence.md) <br/> |表示定期日历项目的最后一个事件。  <br/> 如果[CalendarItemType](calendaritemtype.md)具有 RecurringMaster 值，则此元素有效。  <br/> |
|[ModifiedOccurrences](modifiedoccurrences.md) <br/> |包含已修改的定期日历项目匹配项的数组，以便它们不同于定期主项目。  <br/> 如果[CalendarItemType](calendaritemtype.md)具有 RecurringMaster 值，则此元素有效。  <br/> |
|[DeletedOccurrences](deletedoccurrences.md) <br/> |包含定期日历项目的已删除事件数组。  <br/> 如果[CalendarItemType](calendaritemtype.md)具有 RecurringMaster 值，则此元素有效。  <br/> |
|[MeetingTimeZone](meetingtimezone.md) <br/> |表示时区的会议所在的位置。  <br/> |
|[StartTimeZone](starttimezone.md) <br/> |表示日历项目的起始时区。  <br/> |
|[EndTimeZone](endtimezone.md) <br/> |表示日历项目的结束时区。  <br/> |
|[ConferenceType](conferencetype.md) <br/> |介绍使用日历项目执行的会议的类型。  <br/> |
|[AllowNewTimeProposal](allownewtimeproposal.md) <br/> |指示与会者是否可以为会议建议新的会议时间。  <br/> |
|[IsOnlineMeeting](isonlinemeeting.md) <br/> |指示会议是否处于联机状态。  <br/> |
|[MeetingWorkspaceUrl](meetingworkspaceurl.md) <br/> |包含由日历项目链接到的会议工作区的 URL。  <br/> |
|[NetShowUrl](netshowurl.md) <br/> |指定 Microsoft NetShow online 会议的 URL。  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |包含客户端的权利基础的项或文件夹的权限设置。此元素是只读的。  <br/> |
|[LastModifiedName](lastmodifiedname.md) <br/> |包含上次修改项目的用户的显示名称。  <br/> |
|[LastModifiedTime](lastmodifiedtime.md) <br/> |指示项目的上次修改时间。  <br/> |
|[IsAssociated](isassociated.md) <br/> |指示项目是否与文件夹相关联。  <br/> |
|[WebClientReadFormQueryString](webclientreadformquerystring.md) <br/> |表示连接到 Microsoft Office Outlook Web App 终结点以在 Outlook Web App 中读取项目的 URL。  <br/> |
|[WebClientEditFormQueryString](webclienteditformquerystring.md) <br/> |表示一个用于连接到 Microsoft Office Outlook Web App 终结点以在 Outlook Web App 中编辑项目的 URL。  <br/> |
|[ConversationId](conversationid.md) <br/> |包含项或对话的标识符。  <br/> |
|[UniqueBody](uniquebody.md) <br/> |表示一个 HTML 片段或纯文本，它表示此对话的唯一正文。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[AdjacentMeetings](adjacentmeetings.md) <br/> |介绍与会议时间相邻的所有日历项目。  <br/> |
|[AppendToItemField](appendtoitemfield.md) <br/> |标识在[UpdateItem 操作](updateitem-operation.md)过程中追加到项或文件夹的单个属性的数据。  <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> |标识与会议时间冲突的所有项目。  <br/> |
|[创建（ItemSync）](create-itemsync.md) <br/> |标识要在本地客户端存储中创建一个文件夹。  <br/> |
|[ItemAttachment](itemattachment.md) <br/> |表示附加到另一个 Exchange 项目的 Exchange 项目。  <br/> |
|[Items](items.md) <br/> |包含项的数组。  <br/> |
|[项目（NonEmptyArrayOfAllItemsType）](items-nonemptyarrayofallitemstype.md) <br/> |包含要在由[ParentFolderId （TargetFolderIdType）](parentfolderid-targetfolderidtype.md)元素标识的文件夹中创建的项的数组。  <br/> |
|[SetItemField](setitemfield.md) <br/> |表示对[UpdateItem 操作](updateitem-operation.md)中项的单个属性的更新。  <br/> |
|[Update （ItemSync）](update-itemsync.md) <br/> |标识要在本地客户端存储中更新的单个项目。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>说明

更新单个日历项目以使其成为定期主日历项目时，必须指定[MeetingTimeZone](meetingtimezone.md)元素，以便保留日历项目的原始时区。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)
  
[Exchange 的 EWS 引用](ews-reference-for-exchange.md)

