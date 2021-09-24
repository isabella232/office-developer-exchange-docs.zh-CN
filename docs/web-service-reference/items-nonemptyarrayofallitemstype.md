---
title: Items (NonEmptyArrayOfAllItemsType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Items
api_type:
- schema
ms.assetid: d61ef1cc-ddfc-480a-9625-7b436cb33ae0
description: Items 元素包含一组要创建的项。
ms.openlocfilehash: a511fa9e81cdfb4d5c84705edb0d37f75eb76049
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524992"
---
# <a name="items-nonemptyarrayofallitemstype"></a>Items (NonEmptyArrayOfAllItemsType)

Items 元素包含一组要创建的项。 
  
```XML
<Items>
   <Item/>
   <Message/>
   <CalendarItem/>
   <Contact/>
   <DistributionList/>
   <MeetingMessage/>
   <MeetingRequest/>
   <MeetingResponse/>
   <MeetingCancellation/>
   <Task/>
   <ReplyToItem/>
   <ForwardItem/>
   <ReplyAllToItem/>
   <AcceptItem/>
   <TentativelyAcceptItem/>
   <DeclineItem/>
   <CancelCalendarItem/>
   <RemoveItem/>
   <PostReplyItem/>
   <SuppressReadReceipt/>
   <AcceptSharingInvitation/>
</Items>
```

 **NonEmptyArrayOfAllItemsType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[项目](item.md) <br/> |表示 Exchange 存储中的项。  <br/> |
|[消息](message-ex15websvcsotherref.md) <br/> |代表Exchange电子邮件。  <br/> |
|[CalendarItem](calendaritem.md) <br/> |表示 Exchange 日历项。  <br/> |
|[Contact](contact.md) <br/> |表示 Exchange 联系人项目。  <br/> |
|[DistributionList](distributionlist.md) <br/> |表示通讯组列表。  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |表示会议存储中的Exchange消息。  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |表示 Exchange 存储中的会议请求。  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |表示 Exchange 存储中的会议响应。  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |表示 Exchange 存储中的会议取消。  <br/> |
|[任务](task.md) <br/> |表示 Exchange 存储中的任务。  <br/> |
|[ReplyToItem](replytoitem.md) <br/> |包含对邮件存储中项目发件人Exchange答复。  <br/> |
|[ForwardItem](forwarditem.md) <br/> |包含要转发给收件人的 Exchange 存储区项。  <br/> |
|[ReplyAllToItem](replyalltoitem.md) <br/> |包含对邮件存储中项目的发件人和所有标识Exchange的答复。  <br/> |
|[AcceptItem](acceptitem.md) <br/> |表示接受答复会议要求。  <br/> |
|[TentativelyAcceptItem](tentativelyacceptitem.md) <br/> |表示一个暂定答复会议要求。  <br/> |
|[DeclineItem](declineitem.md) <br/> |表示谢绝答复会议要求。  <br/> |
|[CancelCalendarItem](cancelcalendaritem.md) <br/> |表示用于取消会议的响应对象。  <br/> |
|[RemoveItem](removeitem.md) <br/> |表示响应对象，该对象用于接收 MeetingCancellation 消息时删除会议项目。  <br/> |
|[PostReplyItem](postreplyitem.md) <br/> |包含对帖子项目的回复。  <br/> |
|[SuppressReadReceipt](suppressreadreceipt.md) <br/> |用于禁止显示已读回执。  <br/> |
|[AcceptSharingInvitation](acceptsharinginvitation.md) <br/> |用于接受允许访问其他用户的日历或联系人数据的邀请。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CreateItem](createitem.md) <br/> |定义在项目存储中创建Exchange请求。  <br/> 下面是此元素的 XPath 表达式:  `/CreateItem` <br/> |
|[ConversationNode](conversationnode.md) <br/> |标识对话中的单个节点。  <br/> |
   
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[CreateFolder 操作](createfolder-operation.md)
  
[CreateItem 操作](createitem-operation.md)


[Creating Folders (Exchange Web Services)](https://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

