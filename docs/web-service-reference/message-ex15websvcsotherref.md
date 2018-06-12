---
title: 邮件
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Message
api_type:
- schema
ms.assetid: 2400b33c-43b2-4fc2-b6fb-275a99e0e810
description: 消息元素均表示一个 Microsoft Exchange 电子邮件。
ms.openlocfilehash: 388b944cfa16899cb2376320882f5087396d7b82
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826474"
---
# <a name="message"></a>邮件

**消息**元素均表示一个 Microsoft Exchange 电子邮件。 
  
```xml
<Message>
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
   <EffectiveRights/>
   <ReceivedBy/>
   <ReceivedRepresenting/>
   <LastModifiedName/>
   <LastModifiedTime/>
   <IsAssociated/>
   <WebClientReadFormQueryString/>
   <WebClientEditFormQueryString/>
   <ConversationId/>
   <UniqueBody/>
   <ReminderMessageData/>
</Message>
```

 **MessageType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[MimeContent](mimecontent.md) <br/> |包含一个对象，表示 base64Binary 格式的本机多用途 Internet 邮件扩展 (MIME) 流。  <br/> |
|[ItemId](itemid.md) <br/> |包含在 Exchange 存储中的项目的唯一标识符和更改的键。 此属性是只读的。  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |表示包含的项目或文件夹的父文件夹的标识符。 此属性是只读的。  <br/> |
|[ItemClass](itemclass.md) <br/> |表示项目的消息类。  <br/> |
|[Subject](subject.md) <br/> |代表 Exchange 存储项和响应对象主题。 主题被限制为 255 个字符。  <br/> |
|[Sensitivity](sensitivity.md) <br/> |指示项目的敏感度级别。  <br/> |
|[Body](body.md) <br/> |表示一条消息的实际正文内容。  <br/> |
|[附件](attachments-ex15websvcsotherref.md) <br/> |包含的项或附加到 Exchange 存储中的项目文件。  <br/> |
|[DateTimeReceived](datetimereceived.md) <br/> |表示的日期和接收邮箱中的项目的时间。  <br/> |
|[Size](size.md) <br/> |表示以字节为单位的项目的大小。 此属性是只读的。  <br/> |
|[类别](categories-ex15websvcsotherref.md) <br/> |表示标识的邮箱中项目所属的类别的字符串的集合。  <br/> |
|[Importance](importance.md) <br/> |描述项目的重要性。  <br/> |
|[InReplyTo](inreplyto.md) <br/> |表示此项将答复到项目的标识符。  <br/> |
|[IsSubmitted](issubmitted.md) <br/> |指示项目是否已提交到默认发件箱文件夹。  <br/> |
|[IsDraft](isdraft.md) <br/> |表示是否尚未发送项目。  <br/> |
|[IsFromMe](isfromme.md) <br/> |指示用户是否发送到他或她自己的项目。  <br/> |
|[IsResend](isresend.md) <br/> |指示是否已以前被发送项目。  <br/> |
|[IsUnmodified](isunmodified.md) <br/> |指示是否已修改项目。  <br/> |
|[InternetMessageHeaders](internetmessageheaders.md) <br/> |代表包含在邮箱中项目的所有 Internet 邮件头的集合。  <br/> |
|[DateTimeSent](datetimesent.md) <br/> |表示的日期和时间发送邮箱中的项目。  <br/> |
|[DateTimeCreated](datetimecreated.md) <br/> |表示的日期和给定的邮箱中项目的创建时间。  <br/> |
|[ResponseObjects](responseobjects.md) <br/> |包含与 Exchange 存储中的项相关联的所有响应对象的集合。  <br/> |
|[ReminderDueBy](reminderdueby.md) <br/> |表示的日期和时间事件发生。 这使用[ReminderMinutesBeforeStart](reminderminutesbeforestart.md)元素以确定其何时在显示提醒。  <br/> |
|[ReminderIsSet](reminderisset.md) <br/> |指示是否已设置提醒的项在 Exchange 存储中。  <br/> |
|[ReminderMinutesBeforeStart](reminderminutesbeforestart.md) <br/> |表示事件时显示提醒前的分钟数。  <br/> |
|[DisplayCc](displaycc.md) <br/> |表示用于 CC 行的内容显示字符串。 这是连接的所有抄送收件人的显示名称的字符串。  <br/> |
|[DisplayTo](displayto.md) <br/> |表示用于收件人框的内容显示字符串。 这是连接的所有收件人的显示名称的字符串。  <br/> |
|[HasAttachments](hasattachments.md) <br/> |表示如果项目具有至少一个可见的附件设置为**true**的属性。 此属性是只读的。  <br/> |
|[ExtendedProperty](extendedproperty.md) <br/> |标识文件夹和项扩展的属性。  <br/> |
|[区域性](culture.md) <br/> |表示给定邮箱中项目的区域性。  <br/> |
|[发件人](sender.md) <br/> |标识项目的发件人。  <br/> |
|[ToRecipients](torecipients.md) <br/> |包含邮件收件人的一组。  <br/> |
|[CcRecipients](ccrecipients.md) <br/> |表示将收到邮件副本的收件人集合。  <br/> |
|[BccRecipients](bccrecipients.md) <br/> |表示要接收的电子邮件的密件抄送 (Bcc) 收件人的集合。  <br/> |
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
|[EffectiveRights](effectiverights.md) <br/> |包含客户端的权利基础的项或文件夹的权限设置。此元素是只读的。  <br/> |
|[ReceivedBy](receivedby.md) <br/> |标识委派访问方案中的委托。  <br/> |
|[ReceivedRepresenting](receivedrepresenting.md) <br/> |标识委派访问方案中的主体。  <br/> |
|[LastModifiedName](lastmodifiedname.md) <br/> |包含要修改的项目的最后一个用户的显示名称。  <br/> |
|[LastModifiedTime](lastmodifiedtime.md) <br/> |指示上次修改的项。  <br/> |
|[IsAssociated](isassociated.md) <br/> |指示项目是否与文件夹关联。  <br/> |
|[WebClientReadFormQueryString](webclientreadformquerystring.md) <br/> |表示要连接到 Microsoft Office Outlook Web App 终结点读取 Outlook Web App 中的项目的 URL。  <br/> |
|[WebClientEditFormQueryString](webclienteditformquerystring.md) <br/> |表示要连接到 Outlook Web App 中编辑项目的 Outlook Web App 终结点的 URL。  <br/> |
|[ConversationId](conversationid.md) <br/> |包含项目或会话的标识符。  <br/> |
|[UniqueBody](uniquebody.md) <br/> |代表一个 HTML 片段或代表此对话的唯一正文的纯文本。  <br/> |
|[ReminderMessageData](remindermessagedata.md) <br/> |包含提醒消息的数据。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[AdjacentMeetings](adjacentmeetings.md) <br/> |介绍所有彼此相邻的会议时间的日历项目。  <br/> |
|[AppendToItemField](appendtoitemfield.md) <br/> |标识要追加到的项目的单个属性[UpdateItem 操作](updateitem-operation.md)期间数据。  <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> |标识与会议时间冲突的所有项目。  <br/> |
|[创建 (ItemSync)](create-itemsync.md) <br/> |标识在本地客户端库中创建的单个项。  <br/> |
|[ItemAttachment](itemattachment.md) <br/> |代表附加到另一个 Exchange 项目的 Exchange 项目。  <br/> |
|[Items](items.md) <br/> |包含项的数组。  <br/> |
|[项目 (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |包含由[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md)元素的文件夹中创建的项的数组。  <br/> |
|[SetItemField](setitemfield.md) <br/> |表示更新到单个[UpdateItem 操作](updateitem-operation.md)中的项目的属性。  <br/> |
|[更新 (ItemSync)](update-itemsync.md) <br/> |标识要更新本地客户端存储中的单个项。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>备注

可用性操作使用另一个**邮件**元素，[邮件 （可用性）](message-availability.md)可返回 OOF 邮件。 
  
[消息](message-ex15websvcsotherref.md)元素表示电子邮件和非 Exchange Web Services (EWS) 架构的强类型的所有其他项目。 如 IPM 的项目。共享和**消息**元素以返回 IPM.InfoPath。 Exchange 2010 不在响应中返回基本的**Item**元素。 
  
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

