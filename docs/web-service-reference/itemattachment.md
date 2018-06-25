---
title: ItemAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ItemAttachment
api_type:
- schema
ms.assetid: 089ee599-f45e-46f5-a18a-5cfb3d2851ff
description: ItemAttachment 元素均表示一个 Exchange 项目附加到另一个 Exchange 项目。
ms.openlocfilehash: 87e0331664f1fdf8857afc78500014d138f05401
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826137"
---
# <a name="itemattachment"></a>ItemAttachment

**ItemAttachment**元素均表示一个 Exchange 项目附加到另一个 Exchange 项目。 
  
```xml
<ItemAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <Item/>
</ItemAttachment>
```

 **ItemAttachmentType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[AttachmentId](attachmentid.md) <br/> |标识附件。  <br/> |
|[名称 (AttachmentType)](name-attachmenttype.md) <br/> |表示附件的名称。  <br/> |
|[ContentType](contenttype.md) <br/> |描述附件内容多用途 Internet 邮件扩展 (MIME) 类型。  <br/> |
|[ContentId](contentid.md) <br/> |表示附件的内容的标识符。 [ContentId](contentid.md)可以设置为任何字符串值。 应用程序可以使用[ContentId](contentid.md)来实现自己标识机制。  <br/> |
|[ContentLocation](contentlocation.md) <br/> |包含附件的内容的位置所对应的统一资源标识符 (URI)。  <br/> |
|[Size](size.md) <br/> |表示以字节为单位的附件文件的大小。  <br/> |
|[LastModifiedTime](lastmodifiedtime.md) <br/> |表示上次修改附件时。  <br/> |
|[IsInline](isinline.md) <br/> |表示是否附件显示为内嵌项目中。  <br/> |
|[Item](item.md) <br/> |代表一个通用的 Exchange 项目附件。  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |代表 Exchange 电子邮件附件。  <br/> |
|[日历项目](calendaritem.md) <br/> |代表 Exchange 日历项目附件。  <br/> |
|[Contact](contact.md) <br/> |代表 Exchange 联系人项目附件。  <br/> |
|[任务](task.md) <br/> |代表 Exchange 任务附件。  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |表示 Exchange 存储中的会议。  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |表示 Exchange 存储中的会议请求。  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |表示 Exchange 存储中的会议响应。  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |表示 Exchange 存储中的会议取消。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[附件](attachments-ex15websvcsotherref.md) <br/> |包含项目和/或附加到 Exchange 存储中的项目文件。  <br/> |
   
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

