---
title: ParentFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ParentFolderId
api_type:
- schema
ms.assetid: 258f4b1f-367e-4c7d-9c29-eb775a2398c7
description: ParentFolderId 元素表示包含项或文件夹的父文件夹的标识符。
ms.openlocfilehash: 3bad638aa21019472df8f487f1e065d2e725e750
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465749"
---
# <a name="parentfolderid"></a>ParentFolderId

**ParentFolderId**元素表示包含项或文件夹的父文件夹的标识符。 
  
```XML
<ParentFolderId Id="" ChangeKey=""/>
```

**FolderIdType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**Id** <br/> |包含标识 Exchange 存储中的文件夹的字符串。 此特性是必需的。  <br/> |
|**ChangeKey** <br/> |包含标识由**Id**属性标识的文件夹版本的字符串。 此特性是可选的。 使用此属性可确保使用的是正确的文件夹版本。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CalendarFolder](calendarfolder.md) <br/> |代表邮箱中的 "日历" 文件夹。  <br/> |
|[CalendarItem](calendaritem.md) <br/> |表示邮箱中的日历项目。  <br/> |
|[联系人](contact.md) <br/> |表示邮箱中的联系人项目。  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |表示邮箱中的 "联系人" 文件夹。  <br/> |
|[CopiedEvent](copiedevent.md) <br/> |表示在其中复制项目或文件夹的事件。  <br/> |
|[CreatedEvent](createdevent.md) <br/> |代表在其中创建项目或文件夹的事件。  <br/> |
|[DeletedEvent](deletedevent.md) <br/> |代表在其中删除项目或文件夹的事件。  <br/> |
|[DistributionList](distributionlist.md) <br/> |表示邮箱中的专用通讯组列表。  <br/> |
|[Folder](folder.md) <br/> |表示邮箱中的文件夹。  <br/> |
|[项](item.md) <br/> |表示通用 Exchange 项。  <br/> |
|[Item （UploadItemType）](item-uploaditemtype.md) <br/> |代表要上传到邮箱中的单个项目。  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |表示邮箱中的会议取消。  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |表示邮箱中的会议邮件。  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |表示邮箱中的会议请求。  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |表示邮箱中的会议响应。  <br/> |
|[邮件](message-ex15websvcsotherref.md) <br/> |表示邮箱中的电子邮件。  <br/> |
|[ModifiedEvent](modifiedevent.md) <br/> |表示在其中修改项或文件夹的事件。  <br/> |
|[MovedEvent](movedevent.md) <br/> |代表将项目或文件夹从一个父文件夹移动到另一个父文件夹的事件。  <br/> |
|[NewMailEvent](newmailevent.md) <br/> |代表由邮箱中的新邮件项目触发的事件。  <br/> |
|[AcceptItem](acceptitem.md) <br/> |表示接受答复会议要求。  <br/> |
|[TentativelyAcceptItem](tentativelyacceptitem.md) <br/> |表示一个暂定答复会议要求。  <br/> |
|[DeclineItem](declineitem.md) <br/> |表示谢绝答复会议要求。  <br/> |
|[RemoveItem](removeitem.md) <br/> |从 Exchange 存储中删除一个项目。  <br/> |
|[Task](task.md) <br/> |表示邮箱中的任务项。  <br/> |
|[ReplyToItem](replytoitem.md) <br/> |包含对 Exchange 存储中的项的创建者的答复。  <br/> |
|[ReplyAllToItem](replyalltoitem.md) <br/> |包含对所有确定收件人的 Exchange 存储中的项的答复。  <br/> |
|[ForwardItem](forwarditem.md) <br/> |包含要转发给收件人的 Exchange 存储区项。  <br/> |
|[CancelCalendarItem](cancelcalendaritem.md) <br/> |表示用于取消会议的响应对象。  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |表示邮箱中的任务文件夹。  <br/> |
|[SearchFolder](searchfolder.md) <br/> |表示邮箱中的搜索文件夹。  <br/> |
   
## <a name="remarks"></a>说明

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

