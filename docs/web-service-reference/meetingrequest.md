---
title: MeetingRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MeetingRequest
api_type:
- schema
ms.assetid: c44f8804-a355-473d-a837-48cc91617251
description: MeetingRequest 元素表示 Exchange 存储中的会议请求。
ms.openlocfilehash: 3e290613293cb6ad1563912e5015742ffc503d08
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826450"
---
# <a name="meetingrequest"></a>MeetingRequest

**MeetingRequest**元素表示 Exchange 存储中的会议请求。 
  
```xml
<MeetingRequest>
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
   <Importance/>
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
   <Sender/>
   <ToRecipients/>
   <CcRecipients/>
   <BccRecipients/>
   <IsReadReceiptRequested/>
   <IsDeliveryReceiptRequested/>
   <ConversationIndex/>
   <ConversationTopic/>
   <From/>
   <InternetMessageId/>
   <IsRead/>
   <IsResponseRequested/>
   <References/>
   <ReplyTo/>
   <AssociatedCalendarItemId/>
   <IsDelegated/>
   <IsOutOfDate/>
   <HasBeenProcessed/>
   <ResponseType/>
   <MeetingRequestType/>
   <IntendedFreeBusyStatus/>
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
</MeetingRequest>
```

 **MeetingRequestMessageType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[MimeContent](mimecontent.md) <br/> |包含 base64Binary 格式表示的对象的本机多用途 Internet 邮件扩展 (MIME) 流。  <br/> |
|[ItemId](itemid.md) <br/> |包含在 Exchange 存储中的项目的唯一标识符和更改的键。 此属性是只读的。  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |表示包含的项目或文件夹的父文件夹的标识符。 此属性是只读的。  <br/> |
|[ItemClass](itemclass.md) <br/> |表示项目的消息类。  <br/> |
|[Subject](subject.md) <br/> |代表 Exchange 存储项和响应对象主题。 主题被限制为 255 个字符。  <br/> |
|[Sensitivity](sensitivity.md) <br/> |指示项目的敏感度级别。  <br/> |
|[Body](body.md) <br/> |表示一条消息的实际正文内容。  <br/> |
|[附件](attachments-ex15websvcsotherref.md) <br/> |包含的项或附加到 Exchange 存储中的项目文件。  <br/> |
|[DateTimeReceived](datetimereceived.md) <br/> |代表的数据和接收邮箱中的项目的时间。  <br/> |
|[Size](size.md) <br/> |表示以字节为单位的项目的大小。 此属性是只读的。  <br/> |
|[类别](categories-ex15websvcsotherref.md) <br/> |表示标识的邮箱中项目所属的类别的字符串的集合。  <br/> |
|[Importance](importance.md) <br/> |描述项目的重要性。  <br/> |
|[InReplyTo](inreplyto.md) <br/> |表示此项将答复到项目的标识符。  <br/> |
|[IsSubmitted](issubmitted.md) <br/> |指示项目是否已提交到默认发件箱文件夹。  <br/> |
|[IsDraft](isdraft.md) <br/> |指示是否项目尚未发送。  <br/> |
|[IsFromMe](isfromme.md) <br/> |指示用户是否发送到其自身的项目。  <br/> |
|[IsResend](isresend.md) <br/> |指示是否已以前被发送项目。  <br/> |
|[IsUnmodified](isunmodified.md) <br/> |指示是否已修改项目。  <br/> |
|[InternetMessageHeaders](internetmessageheaders.md) <br/> |代表邮箱中的一个项内包含的所有 Internet 邮件头的集合。  <br/> |
|[DateTimeSent](datetimesent.md) <br/> |表示的日期和时间发送邮箱中的项目。  <br/> |
|[DateTimeCreated](datetimecreated.md) <br/> |表示的日期和给定的邮箱中项目的创建时间。  <br/> |
|[ResponseObjects](responseobjects.md) <br/> |包含与 Exchange 存储中的项相关联的所有响应对象的集合。  <br/> |
|[ReminderDueBy](reminderdueby.md) <br/> |表示的日期和时间事件发生。 这使用[ReminderMinutesBeforeStart](reminderminutesbeforestart.md)元素以确定其何时在显示提醒。  <br/> |
|[ReminderIsSet](reminderisset.md) <br/> |指示是否已设置提醒的项在 Exchange 存储中。  <br/> |
|[ReminderMinutesBeforeStart](reminderminutesbeforestart.md) <br/> |表示事件时显示提醒前的分钟数。  <br/> |
|[DisplayCc](displaycc.md) <br/> |表示用于 CC 行的内容显示字符串。 这是连接的所有抄送收件人的显示名称的字符串。  <br/> |
|[DisplayTo](displayto.md) <br/> |表示用于 To 行的内容显示字符串。 这是连接的所有收件人的显示名称的字符串。  <br/> |
|[HasAttachments](hasattachments.md) <br/> |表示如果项目具有至少一个可见的附件设置为**true**的属性。 此属性为只读。  <br/> |
|[ExtendedProperty](extendedproperty.md) <br/> |标识文件夹和项扩展的属性。  <br/> |
|[区域性](culture.md) <br/> |表示给定邮箱中项目的区域性。  <br/> |
|[发件人](sender.md) <br/> |标识项目的发件人。  <br/> |
|[ToRecipients](torecipients.md) <br/> |包含邮件收件人的一组。  <br/> |
|[CcRecipients](ccrecipients.md) <br/> |表示将收到邮件副本的收件人集合。  <br/> |
|[BccRecipients](bccrecipients.md) <br/> |表示接收电子邮件的密件抄送 (Bcc) 的收件人集合。  <br/> |
|[IsReadReceiptRequested](isreadreceiptrequested.md) <br/> |指示项目的发件人是否请求已读的回执。  <br/> |
|[IsDeliveryReceiptRequested](isdeliveryreceiptrequested.md) <br/> |指示项目的发件人是否请求回执。  <br/> |
|[ConversationIndex](conversationindex.md) <br/> |包含表示此消息所属的主题的二进制 ID。  <br/> |
|[ConversationTopic](conversationtopic.md) <br/> |表示对话标识符。  <br/> |
|[发件人](from.md) <br/> |表示邮件发件人的地址。  <br/> |
|[InternetMessageId](internetmessageid.md) <br/> |表示项目的 Internet 消息标识符。  <br/> |
|[IsRead](isread.md) <br/> |指示是否已读取一条消息。  <br/> |
|[IsResponseRequested](isresponserequested.md) <br/> |指示是否对电子邮件的响应请求。  <br/> |
|[引用](references.md) <br/> |代表用于将答复其原始消息关联起来新闻标头。  <br/> |
|[回复](replyto.md) <br/> |标识一组地址应向其发送答复。  <br/> |
|[AssociatedCalendarItemId](associatedcalendaritemid.md) <br/> |代表与[MeetingMessage](meetingmessage.md)相关联的日历项目。  <br/> |
|[IsDelegated](isdelegated.md) <br/> |指示是否具有代理访问的帐户已处理的会议。  <br/> |
|[IsOutOfDate](isoutofdate.md) <br/> |指示会议邮件是否过期。  <br/> |
|[HasBeenProcessed](hasbeenprocessed.md) <br/> |指示是否会议邮件项已处理。  <br/> |
|[ResponseType](responsetype.md) <br/> |代表收到会议的收件人响应的类型。  <br/> |
|[MeetingRequestType](meetingrequesttype.md) <br/> |描述将会议请求的类型。  <br/> |
|[IntendedFreeBusyStatus](intendedfreebusystatus.md) <br/> |代表与会议请求相关联的日历项目的预期的状态。  <br/> |
|[Start](start.md) <br/> |表示日历项目的开始。 此元素仅适用于日历项目的一个匹配项。  <br/> |
|[结束](end-ex15websvcsotherref.md) <br/> |代表工期的结束。 此元素仅适用于日历项目的一个匹配项。  <br/> |
|[OriginalStart](originalstart.md) <br/> |代表日历项目的原始开始时间。  <br/> |
|[IsAllDayEvent](isalldayevent.md) <br/> |指示日历项目或会议请求是否表示全天事件。  <br/> |
|[LegacyFreeBusyStatus](legacyfreebusystatus.md) <br/> |代表日历项目的忙/闲状态。  <br/> |
|[位置](location.md) <br/> |表示会议或约会的位置。  <br/> |
|[When](when.md) <br/> |提供会议发生的说明。  <br/> |
|[IsMeeting](ismeeting.md) <br/> |指示日历项目是否会议或约会。  <br/> |
|[IsCancelled](iscancelled.md) <br/> |指示是否已取消约会或会议。  <br/> |
|[IsRecurring](isrecurring.md) <br/> |指示日历项目是否定期项的一部分。 此元素是只读的。  <br/> |
|[MeetingRequestWasSent](meetingrequestwassent.md) <br/> |指示是否已向请求与会者发送会议请求。  <br/> |
|[CalendarItemType](calendaritemtype.md) <br/> |表示日历项目的匹配项的类型。  <br/> |
|[MyResponseType](myresponsetype.md) <br/> |包含的状态或日历项目的响应。  <br/> |
|[Organizer](organizer.md) <br/> |表示会议的组织者。  <br/> |
|[RequiredAttendees](requiredattendees.md) <br/> |代表需要参加会议的与会者。  <br/> |
|[OptionalAttendees](optionalattendees.md) <br/> |表示无需参加会议的与会者。  <br/> |
|[资源](resources.md) <br/> |表示会议的计划的资源。  <br/> |
|[ConflictingMeetingCount](conflictingmeetingcount.md) <br/> |代表与会议请求冲突的会议数。  <br/> |
|[AdjacentMeetingCount](adjacentmeetingcount.md) <br/> |表示相邻的会议时间的日历项目的总数。  <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> |标识与会议时间冲突的所有项目。  <br/> |
|[AdjacentMeetings](adjacentmeetings.md) <br/> |介绍所有彼此相邻的会议时间的日历项目。  <br/> |
|[持续时间 （项）](duration-items.md) <br/> |表示日历项目的持续时间。  <br/> |
|[TimeZone （项）](timezone-item.md) <br/> |提供时区的文本的说明。  <br/> |
|[AppointmentReplyTime](appointmentreplytime.md) <br/> |表示对会议请求的日期和时间与会者的答复。  <br/> |
|[AppointmentSequenceNumber](appointmentsequencenumber.md) <br/> |指定约会的版本的序列号。  <br/> |
|[AppointmentState](appointmentstate.md) <br/> |指定约会的状态。  <br/> |
|[定期 (RecurrenceType)](recurrence-recurrencetype.md) <br/> |包含日历项和会议请求的定期模式。  <br/> |
|[FirstOccurrence](firstoccurrence.md) <br/> |代表定期日历项目的第一个匹配项。  <br/> 此元素是如果[CalendarItemType](calendaritemtype.md) RecurringMaster 值有效。  <br/> |
|[LastOccurrence](lastoccurrence.md) <br/> |代表定期日历项目的最后一个实例。  <br/> 此元素是如果[CalendarItemType](calendaritemtype.md) RecurringMaster 值有效。  <br/> |
|[ModifiedOccurrences](modifiedoccurrences.md) <br/> |包含一个数组，以便它们是不同的定期主项目已修改的定期日历项目事件。  <br/> 此元素是如果[CalendarItemType](calendaritemtype.md) RecurringMaster 值有效。  <br/> |
|[DeletedOccurrences](deletedoccurrences.md) <br/> |包含数组的定期日历项目的已删除匹配项。  <br/> 此元素是如果[CalendarItemType](calendaritemtype.md) RecurringMaster 值有效。  <br/> |
|[MeetingTimeZone](meetingtimezone.md) <br/> |表示时区的会议所在的位置。  <br/> |
|[StartTimeZone](starttimezone.md) <br/> |代表日历项目开始所在的时区。  <br/> |
|[EndTimeZone](endtimezone.md) <br/> |代表最终所在的时区的日历项目。  <br/> |
|[ConferenceType](conferencetype.md) <br/> |描述使用日历项目执行的会议类型。  <br/> |
|[AllowNewTimeProposal](allownewtimeproposal.md) <br/> |表示是否可以为会议建议的新的会议时间。  <br/> |
|[IsOnlineMeeting](isonlinemeeting.md) <br/> |指示是否联机会议。  <br/> |
|[MeetingWorkspaceUrl](meetingworkspaceurl.md) <br/> |包含会议工作区链接到的日历项目的 URL。  <br/> |
|[NetShowUrl](netshowurl.md) <br/> |指定 Microsoft Netshow 联机会议的 URL。  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |包含客户端基于的项目或文件夹的权限设置的权限。 此元素是只读的。  <br/> |
|[LastModifiedName](lastmodifiedname.md) <br/> |包含要修改的项目的最后一个用户的显示名称。  <br/> |
|[LastModifiedTime](lastmodifiedtime.md) <br/> |指示上次修改的项。  <br/> |
|[IsAssociated](isassociated.md) <br/> |指示项目是否与文件夹关联。  <br/> |
|[WebClientReadFormQueryString](webclientreadformquerystring.md) <br/> |表示要连接到 Microsoft Office Outlook Web App 终结点读取 Outlook Web App 中的项目的 URL。  <br/> |
|[WebClientEditFormQueryString](webclienteditformquerystring.md) <br/> |表示要连接到 Outlook Web App 中编辑项目的 Outlook Web App 终结点的 URL。  <br/> |
|[ConversationId](conversationid.md) <br/> |包含项目或会话的标识符。  <br/> |
|[UniqueBody](uniquebody.md) <br/> |代表一个 HTML 片段或代表此对话的唯一正文的纯文本。  <br/> |
|[UID](uid.md) <br/> |标识日历项目。  <br/> |
|[RecurrenceId](recurrenceid.md) <br/> |用于标识定期日历项目的特定实例。  <br/> |
|[DateTimeStamp](datetimestamp.md) <br/> |指示的日期和时间创建 iCalendar 对象的实例。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[AdjacentMeetings](adjacentmeetings.md) <br/> |标识所有彼此相邻的会议时间的日历项目。  <br/> |
|[AppendToItemField](appendtoitemfield.md) <br/> |标识要追加到的项目的单个属性[UpdateItem 操作](updateitem-operation.md)期间数据。  <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> |标识与会议时间冲突的所有项目。  <br/> |
|[创建 (ItemSync)](create-itemsync.md) <br/> |标识在本地客户端库中创建的单个项。  <br/> |
|[Items](items.md) <br/> |包含项的数组。  <br/> |
|[项目 (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |包含项创建的数组。  <br/> |
|[ItemAttachment](itemattachment.md) <br/> |代表附加到另一个 Exchange 项目的 Exchange 项目。  <br/> |
|[SetItemField](setitemfield.md) <br/> |表示更新到单个[UpdateItem 操作](updateitem-operation.md)中的项目的属性。  <br/> |
|[更新 (ItemSync)](update-itemsync.md) <br/> |标识要更新本地客户端存储中的单个项。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>备注

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

