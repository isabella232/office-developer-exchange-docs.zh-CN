---
title: PostReplyItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PostReplyItem
api_type:
- schema
ms.assetid: e5d93d63-0a3b-470f-9a94-2d57284c6745
description: PostReplyItem 元素包含对公告项的答复。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: 4104e79449acc6e358b729cf2de769d28dac52bd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461679"
---
# <a name="postreplyitem"></a>PostReplyItem

**PostReplyItem**元素包含对公告项的答复。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。 
  
```xml
<PostReplyItem>
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
   <NewBodyContent/>
</PostReplyItem>
```

 **PostReplyItemType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[MimeContent](mimecontent.md) <br/> |包含以 base64Binary 格式表示的对象的本机多用途 Internet 邮件扩展（MIME）流。  <br/> |
|[ItemId](itemid.md) <br/> |包含 Exchange 存储中某项的唯一标识符和更改键。 此属性是只读的。  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |表示包含项或文件夹的父文件夹的标识符。 此属性是只读的。  <br/> |
|[ItemClass](itemclass.md) <br/> |表示项目的邮件类。  <br/> |
|[主题](subject.md) <br/> |表示 Exchange 存储项和响应对象的主题。 主题限制为255个字符。  <br/> |
|[Sensitivity](sensitivity.md) <br/> |指示项的敏感度级别。  <br/> |
|[Body](body.md) <br/> |表示邮件的实际正文内容。  <br/> |
|[附件](attachments-ex15websvcsotherref.md) <br/> |包含附加到 Exchange 存储中的项目的项目或文件。  <br/> |
|[DateTimeReceived](datetimereceived.md) <br/> |表示邮箱中的项目的接收日期和时间。  <br/> |
|[大小](size.md) <br/> |表示项的大小（以字节为单位）。 此属性是只读的。  <br/> |
|[类别](categories-ex15websvcsotherref.md) <br/> |表示一个字符串集合，这些字符串标识邮箱中的项目所属的类别。  <br/> |
|[Importance](importance.md) <br/> |介绍项的重要性。  <br/> |
|[InReplyTo](inreplyto.md) <br/> |表示此项是其回复项的标识符。  <br/> |
|[IsSubmitted](issubmitted.md) <br/> |指示是否已将项目提交到 "发件箱" 默认文件夹。  <br/> |
|[IsDraft](isdraft.md) <br/> |表示是否尚未发送某个项目。  <br/> |
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
|[DisplayTo](displayto.md) <br/> |表示用于 "To" 框中的内容的显示字符串。 这是所有收件人显示名称的串联字符串。  <br/> |
|[HasAttachments](hasattachments.md) <br/> |表示一个在项目有附件的情况设置为**true**的属性。 此属性是只读的。  <br/> |
|[ExtendedProperty](extendedproperty.md) <br/> |标识文件夹和项的扩展属性。  <br/> |
|[Culture](culture.md) <br/> |表示邮箱中给定项目的区域性。  <br/> |
|[发件人](sender.md) <br/> |标识项目的发件人。  <br/> |
|[ToRecipients](torecipients.md) <br/> |包含一组邮件的收件人。  <br/> |
|[CcRecipients](ccrecipients.md) <br/> |表示将收到邮件副本的收件人集合。  <br/> |
|[BccRecipients](bccrecipients.md) <br/> |表示接收电子邮件的密件抄送 (Bcc) 的收件人集合。  <br/> |
|[IsReadReceiptRequested](isreadreceiptrequested.md) <br/> |指示项目的发件人是否请求已读回执。  <br/> |
|[IsDeliveryReceiptRequested](isdeliveryreceiptrequested.md) <br/> |指示项目的发件人是否请求送达回执。  <br/> |
|[ConversationIndex](conversationindex.md) <br/> |包含代表此邮件所属线程的二进制 ID。  <br/> |
|[ConversationTopic](conversationtopic.md) <br/> |表示会话标识符。  <br/> |
|[From](from.md) <br/> |表示发送邮件的地址。  <br/> |
|[InternetMessageId](internetmessageid.md) <br/> |表示项目的 Internet 邮件标识符。  <br/> |
|[IsRead](isread.md) <br/> |指示是否已阅读邮件。  <br/> |
|[IsResponseRequested](isresponserequested.md) <br/> |指示是否请求对电子邮件的响应。  <br/> |
|[References](references.md) <br/> |表示用于将答复与原始邮件关联的 Usenet 标头。  <br/> |
|[ReplyTo](replyto.md) <br/> |标识应将答复发送到的一组地址。  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |包含基于项目或文件夹的权限设置的客户端权限。此元素为只读。Exchange 2007 SP1 中引入了此元素。  <br/> |
|[ReceivedBy](receivedby.md) <br/> |标识代理访问方案中的委派。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
|[ReceivedRepresenting](receivedrepresenting.md) <br/> |标识代理访问方案中的主体。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
|[NewBodyContent](newbodycontent.md) <br/> |表示公告项的新正文内容。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[AdjacentMeetings](adjacentmeetings.md) <br/> |描述与会议时间相邻的所有项目。  <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> |描述与会议时间冲突的所有项目。  <br/> |
|[ResponseObjects](responseobjects.md) <br/> |包含与 Exchange 存储中的项目关联的所有响应对象的集合。  <br/> |
|[项目（NonEmptyArrayOfAllItemsType）](items-nonemptyarrayofallitemstype.md) <br/> |包含要在由[ParentFolderId （TargetFolderIdType）](parentfolderid-targetfolderidtype.md)元素标识的文件夹中创建的项的数组。  <br/> |
   
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

