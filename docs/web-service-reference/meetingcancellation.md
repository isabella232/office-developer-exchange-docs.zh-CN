---
title: MeetingCancellation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MeetingCancellation
api_type:
- schema
ms.assetid: a9c61f7f-2ecd-4b21-9dce-24d9f61aeeea
description: MeetingCancellation 元素表示会议存储区中的Exchange取消。
ms.openlocfilehash: 979db9af3092247fe09775fb2d7a43394a09925c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523970"
---
# <a name="meetingcancellation"></a>MeetingCancellation

**MeetingCancellation** 元素表示会议存储区中的Exchange取消。 
  
```xml
<MeetingCancellation>
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
   <EffectiveRights/>
   <LastModifiedName/>
   <LastModifiedTime/>
   <IsAssociated/>
   <WebClientReadFormQueryString/>
   <WebClientEditFormQueryString/>
   <ConversationId/>
   <UniqueBody/>
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
</MeetingCancellation>
```

 **MeetingCancellationMessageType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[MimeContent](mimecontent.md) <br/> |包含以 base64Binary 格式表示的对象的本机 MIME 流。  <br/> |
|[ItemId](itemid.md) <br/> |包含项目存储中项的唯一标识符Exchange项。 此属性是只读的。  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |表示包含项目或文件夹的父文件夹的标识符。 此属性是只读的。  <br/> |
|[ItemClass](itemclass.md) <br/> |表示项目的邮件类。  <br/> |
|[主题](subject.md) <br/> |表示用于存储Exchange响应对象的主题。 主题限制为 255 个字符。  <br/> |
|[Sensitivity](sensitivity.md) <br/> |指示项目的敏感度级别。  <br/> |
|[正文](body.md) <br/> |表示邮件的实际正文内容。  <br/> |
|[附件](attachments-ex15websvcsotherref.md) <br/> |包含附加到项目存储中的项目或Exchange文件。  <br/> |
|[DateTimeReceived](datetimereceived.md) <br/> |表示接收邮箱中的项目的日期和时间。  <br/> |
|[尺寸](size.md) <br/> |表示项目的大小（以字节为单位）。 此属性是只读的。  <br/> |
|[Categories](categories-ex15websvcsotherref.md) <br/> |表示标识邮箱中项目属于哪些类别的字符串集合。  <br/> |
|[Importance](importance.md) <br/> |描述项目的重要性。  <br/> |
|[InReplyTo](inreplyto.md) <br/> |表示此项是答复项的标识符。  <br/> |
|[IsSubmitted](issubmitted.md) <br/> |指示项目是否已提交到发件箱默认文件夹。  <br/> |
|[IsDraft](isdraft.md) <br/> |表示项目尚未发送。  <br/> |
|[IsFromMe](isfromme.md) <br/> |指示用户是否向自己发送了项目。  <br/> |
|[IsResend](isresend.md) <br/> |指示项目先前是否已发送。  <br/> |
|[IsUnmodified](isunmodified.md) <br/> |指示项目是否已修改。  <br/> |
|[InternetMessageHeaders](internetmessageheaders.md) <br/> |表示包含在邮箱中的项目内的所有 Internet 邮件头的集合。  <br/> |
|[DateTimeSent](datetimesent.md) <br/> |表示邮箱中项目的发送日期和时间。  <br/> |
|[DateTimeCreated](datetimecreated.md) <br/> |表示邮箱中给定项目的创建日期和时间。  <br/> |
|[ResponseObjects](responseobjects.md) <br/> |包含与项目存储中的项目关联的所有响应Exchange的集合。  <br/> |
|[ReminderDueBy](reminderdueby.md) <br/> |表示事件发生的日期和时间。 [ReminderMinutesBeforeStart](reminderminutesbeforestart.md)元素使用此功能来确定何时显示提醒。  <br/> |
|[ReminderIsSet](reminderisset.md) <br/> |指示是否已为应用商店中的项目设置Exchange提醒。  <br/> |
|[ReminderMinutesBeforeStart](reminderminutesbeforestart.md) <br/> |表示显示提醒的事件前的分钟数。  <br/> |
|[DisplayCc](displaycc.md) <br/> |表示用于"抄送"框内容的显示字符串。 这是所有"抄送"收件人显示名称的串联字符串。  <br/> |
|[DisplayTo](displayto.md) <br/> |表示用于"To"框内容的显示字符串。 这是所有"收件人"收件人显示名称的串联字符串。  <br/> |
|[HasAttachments](hasattachments.md) <br/> |表示一个属性 **，如果项目** 具有至少一个可见附件，则该属性设置为 true。 此属性是只读的。  <br/> |
|[ExtendedProperty](extendedproperty.md) <br/> |标识文件夹和项目的扩展属性。  <br/> |
|[Culture](culture.md) <br/> |表示邮箱中给定项目的区域性。  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |包含客户端的权利基础的项或文件夹的权限设置。此元素是只读的。  <br/> |
|[LastModifiedName](lastmodifiedname.md) <br/> |包含显示名称用户修改项目的详细信息。  <br/> |
|[LastModifiedTime](lastmodifiedtime.md) <br/> |指示项目的上次修改时间。  <br/> |
|[IsAssociated](isassociated.md) <br/> |指示项目是否与文件夹关联。  <br/> |
|[WebClientReadFormQueryString](webclientreadformquerystring.md) <br/> |表示连接到 Web App 终结点以读取Microsoft Office Outlook Web App 终结点的 URL Outlook Web App。  <br/> |
|[WebClientEditFormQueryString](webclienteditformquerystring.md) <br/> |表示要连接到 Outlook Web App 终结点以编辑 Outlook Web App 中的项目的 URL。  <br/> |
|[ConversationId](conversationid.md) <br/> |包含项目或对话的标识符。  <br/> |
|[UniqueBody](uniquebody.md) <br/> |表示 HTML 片段或纯文本，表示此对话的唯一正文。  <br/> |
|[发件人](sender.md) <br/> |标识项目的发件人。  <br/> |
|[ToRecipients](torecipients.md) <br/> |包含邮件的一组收件人。  <br/> |
|[CcRecipients](ccrecipients.md) <br/> |表示将收到邮件副本的收件人集合。  <br/> |
|[BccRecipients](bccrecipients.md) <br/> |表示接收电子邮件的密件抄送 (Bcc) 的收件人集合。  <br/> |
|[IsReadReceiptRequested](isreadreceiptrequested.md) <br/> |指示项目的发件人是否请求已读回执。  <br/> |
|[IsDeliveryReceiptRequested](isdeliveryreceiptrequested.md) <br/> |指示项目的发件人是否请求送达回执。  <br/> |
|[ConversationIndex](conversationindex.md) <br/> |包含二进制 ID，表示此消息所属的线程。  <br/> |
|[ConversationTopic](conversationtopic.md) <br/> |表示对话标识符。  <br/> |
|[发件人](from.md) <br/> |表示邮件发件人的地址。  <br/> |
|[InternetMessageId](internetmessageid.md) <br/> |表示项目的 Internet 邮件标识符。  <br/> |
|[IsRead](isread.md) <br/> |指示是否已阅读邮件。  <br/> |
|[IsResponseRequested](isresponserequested.md) <br/> |指示是否请求对电子邮件的响应。  <br/> |
|[References](references.md) <br/> |代表用于将答复与其原始邮件关联的 Usenet 头。  <br/> |
|[ReplyTo](replyto.md) <br/> |标识答复应发送到的一组地址。  <br/> |
|[AssociatedCalendarItemId](associatedcalendaritemid.md) <br/> |表示与 [MeetingMessage 关联的日历项目](meetingmessage.md)。  <br/> |
|[IsDelegated](isdelegated.md) <br/> |指示会议是否由具有委派访问权限的帐户处理。  <br/> |
|[IsOutOfDate](isoutofdate.md) <br/> |指示会议邮件是否过期。  <br/> |
|[HasBeenProcessed](hasbeenprocessed.md) <br/> |指示是否已处理会议邮件项目。  <br/> |
|[ResponseType](responsetype.md) <br/> |表示为会议收到的收件人响应类型。  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |包含客户端的权利基础的项或文件夹的权限设置。 此元素是只读的。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。  <br/> |
|[ReceivedBy](receivedby.md) <br/> |标识委派访问方案中的代理。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
|[ReceivedRepresenting](receivedrepresenting.md) <br/> |标识委派访问方案中的主体。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
|[UID](uid.md) <br/> |标识日历项目。  <br/> |
|[RecurrenceId](recurrenceid.md) <br/> |用于标识定期日历项目的特定实例。  <br/> |
|[DateTimeStamp](datetimestamp.md) <br/> |指示创建 iCalendar 对象实例的日期和时间。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[AdjacentMeetings](adjacentmeetings.md) <br/> |标识与会议时间相邻的所有日历项目。  <br/> |
|[AppendToItemField](appendtoitemfield.md) <br/> |标识要追加到 [UpdateItem](updateitem-operation.md)操作期间项的单个属性的数据。  <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> |标识与会议时间冲突的所有项目。  <br/> |
|[Create (ItemSync)](create-itemsync.md) <br/> |标识要在本地客户端存储中创建的单个项目。  <br/> |
|[Items](items.md) <br/> |包含项目数组。  <br/> |
|[Items (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |包含要创建的项数组。  <br/> |
|[ItemAttachment](itemattachment.md) <br/> |代表Exchange附加到其他项目的项目Exchange项。  <br/> |
|[SetItemField](setitemfield.md) <br/> |表示对 [UpdateItem](updateitem-operation.md)操作中某个项目的单个属性的更新。  <br/> |
|[Update (ItemSync)](update-itemsync.md) <br/> |标识要在本地客户端存储中更新的单个项目。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>注解

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

