---
title: 附件
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Attachments
api_type:
- schema
ms.assetid: b470e614-34bb-44f0-8790-7ddbdcbbd29d
description: "\"附件\" 元素包含附加到 Exchange 存储中的项目的项目或文件。"
ms.openlocfilehash: a9f79cd79f19e6226703c99c53c91efed600f495
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461532"
---
# <a name="attachments"></a>附件

"**附件**" 元素包含附加到 Exchange 存储中的项目的项目或文件。 
  
```xml
<Attachments>
   <ItemAttachment/>
   <FileAttachment/>
</Attachments>
```

 **ArrayOfAttachmentsType**和**NonEmptyArrayOfAttachmentsType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ItemAttachment](itemattachment.md) <br/> |表示附加到另一个 Exchange 项目的 Exchange 项目。  <br/> |
|[FileAttachment](fileattachment.md) <br/> |代表附加到 Exchange 存储中的项目的文件。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CreateAttachment](createattachment.md) <br/> |定义在 Exchange 存储区中创建项目附件的请求。<br/><br/> 下面是此元素的 XPath 表达式:  `/CreateAttachment` <br/> |
|[AcceptItem](acceptitem.md) <br/> | 表示接受答复会议要求。<br/><br/>下面是此元素的一些 XPath 表达式：<ul><li>`/CreateItem/Items`</li><li>`/MeetingRequest/ConflictingMeetings` </li><li>`/SetItemField/CalendarItem/ConflictingMeetings`</li><li>`/AppendToItemField/CalendarItem/ConflictingMeetings`</li><li>`/AcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings`</li><li>`/DeclineItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings`</li><li>`/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/AdjacentMeetings`</li><li>`/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings`</li><li>`/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings`</li></ul> |
|[DeclineItem](declineitem.md) <br/> |表示谢绝答复会议要求。  <br/> |
|[TentativelyAcceptItem](tentativelyacceptitem.md) <br/> |表示一个暂定答复会议要求。  <br/> |
|[RemoveItem](removeitem.md) <br/> |从 Exchange 存储中删除一个项目。  <br/> |
|[项](item.md) <br/> |表示通用 Exchange 项。  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |表示 Exchange 存储中的会议。  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |表示 Exchange 存储中的会议请求。  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |表示 Exchange 存储中的会议响应。  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |表示 Exchange 存储中的会议取消。  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |表示 Exchange 电子邮件。  <br/> |
|[任务](task.md) <br/> |表示 Exchange 存储中的任务。  <br/> |
|[CalendarItem](calendaritem.md) <br/> |表示 Exchange 日历项。  <br/> |
|[Contact](contact.md) <br/> |表示 Exchange 联系人项目。  <br/> |
|[DistributionList](distributionlist.md) <br/> |表示通讯组列表。  <br/> |
|[CreateAttachmentResponseMessage](createattachmentresponsemessage.md) <br/> |包含单个 CreateAttachment 请求的状态和结果。  <br/> |
|[GetAttachmentResponseMessage](getattachmentresponsemessage.md) <br/> |包含 GetAttachment 请求的状态和结果。  <br/> |
   
## <a name="remarks"></a>备注

**附件**元素具有相同的子元素，但它们基于不同的类型： **ArrayOfAttachmentsType**和**NonEmptyArrayOfAttachmentsType**。 这些类型定义是否需要子元素。 **ArrayOfAttachmentsType**仅在响应消息中使用。 此外，请务必注意，这些元素在消息和类型命名空间中都出现。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

