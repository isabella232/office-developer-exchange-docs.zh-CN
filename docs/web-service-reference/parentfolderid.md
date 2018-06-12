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
description: ParentFolderId 元素均表示包含的项目或文件夹的父文件夹的标识符。
ms.openlocfilehash: 3f60e8adb62fbf464a58af4169fbcd83910877cc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826687"
---
# <a name="parentfolderid"></a>ParentFolderId

**ParentFolderId**元素均表示包含的项目或文件夹的父文件夹的标识符。 
  
```XML
<ParentFolderId Id="" ChangeKey=""/>
```

**FolderIdType**

## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|
  **Id** <br/> |包含一个字符串，标识 Exchange 存储中的文件夹。 此属性是必需的。  <br/> |
|**更改密钥** <br/> |包含一个字符串，标识的文件夹的**Id**属性标识的版本。 此属性是可选的。 使用此属性以确保正确版本的文件夹使用。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CalendarFolder](calendarfolder.md) <br/> |表示邮箱中的日历文件夹。  <br/> |
|[日历项目](calendaritem.md) <br/> |表示邮箱中的日历项目。  <br/> |
|[Contact](contact.md) <br/> |表示邮箱中的联系人项目。  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |表示邮箱中的联系人文件夹。  <br/> |
|[CopiedEvent](copiedevent.md) <br/> |表示复制的项或文件夹的事件。  <br/> |
|[CreatedEvent](createdevent.md) <br/> |表示在其中创建项目或文件夹的事件。  <br/> |
|[DeletedEvent](deletedevent.md) <br/> |表示删除项或文件夹的事件。  <br/> |
|[DistributionList](distributionlist.md) <br/> |表示邮箱中的私人通讯组列表。  <br/> |
|[Folder](folder.md) <br/> |表示邮箱中的文件夹。  <br/> |
|[Item](item.md) <br/> |表示的泛型 Exchange 项目。  <br/> |
|[项目 (UploadItemType)](item-uploaditemtype.md) <br/> |代表单个项目上载到邮箱。  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |表示邮箱中的取消会议。  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |表示邮箱中的会议消息。  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |表示邮箱中的会议请求。  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |代表邮箱中的会议响应。  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |表示邮箱中的电子邮件。  <br/> |
|[ModifiedEvent](modifiedevent.md) <br/> |表示在其中修改项目或文件夹的事件。  <br/> |
|[MovedEvent](movedevent.md) <br/> |表示在其中项目或文件夹从一个父文件夹移到另一个父文件夹的事件。  <br/> |
|[NewMailEvent](newmailevent.md) <br/> |表示由邮箱中的一个新的邮件项目触发的事件。  <br/> |
|[AcceptItem](acceptitem.md) <br/> |表示接受答复会议要求。  <br/> |
|[TentativelyAcceptItem](tentativelyacceptitem.md) <br/> |表示一个暂定答复会议要求。  <br/> |
|[DeclineItem](declineitem.md) <br/> |表示谢绝答复会议要求。  <br/> |
|[RemoveItem](removeitem.md) <br/> |从 Exchange 存储中删除一个项目。  <br/> |
|[任务](task.md) <br/> |表示邮箱中的任务项。  <br/> |
|[ReplyToItem](replytoitem.md) <br/> |包含对 Exchange 存储中的项的创建者的答复。  <br/> |
|[ReplyAllToItem](replyalltoitem.md) <br/> |包含对所有确定收件人的 Exchange 存储中的项的答复。  <br/> |
|[ForwardItem](forwarditem.md) <br/> |包含要转发给收件人的 Exchange 存储区项。  <br/> |
|[CancelCalendarItem](cancelcalendaritem.md) <br/> |表示用于取消会议的响应对象。  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |表示邮箱中的任务文件夹。  <br/> |
|[SearchFolder](searchfolder.md) <br/> |表示邮箱中的搜索文件夹。  <br/> |
   
## <a name="remarks"></a>备注

描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

