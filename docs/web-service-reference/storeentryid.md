---
title: StoreEntryId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f536e264-8c4d-4cc5-bab8-22a4fa38de39
description: StoreEntryId 元素包含项目的 Exchange 存储标识符。
ms.openlocfilehash: 669ea937da6c08b50877c24aeb450fe975326247
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465154"
---
# <a name="storeentryid"></a>StoreEntryId

**StoreEntryId**元素包含项目的 Exchange 存储标识符。 
  
```XML
<StoreEntryId/>
```

 **xs： base64Binary**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素名**|**说明**|
|:-----|:-----|
|[AcceptItem](acceptitem.md) <br/> |表示接受答复会议要求。  <br/> |
|[CalendarItem](calendaritem.md) <br/> |表示 Exchange 日历项。  <br/> |
|[条件](conditions.md) <br/> |表示履行时将触发规则的规则操作的条件。  <br/> |
|[联系人](contact.md) <br/> |表示对 Exchange 存储中的联系人项目。  <br/> |
|[DeclineItem](declineitem.md) <br/> |表示谢绝答复会议要求。  <br/> |
|[DistributionList](distributionlist.md) <br/> |表示通讯组列表。  <br/> |
|[异常](exceptions.md) <br/> |代表收件箱规则的所有可用的规则例外条件。  <br/> |
|[项](item.md) <br/> |表示通用 Exchange 项。  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |表示 Exchange 存储中的会议取消。  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |表示 Exchange 存储中的会议。  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |表示 Exchange 存储中的会议请求。  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |表示 Exchange 存储中的会议响应。  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |表示 Exchange 电子邮件。  <br/> |
|[RemoveItem](removeitem.md) <br/> |从 Exchange 存储中删除一个项目。  <br/> |
|[任务](task.md) <br/> |表示 Exchange 存储中的任务。  <br/> |
|[TentativelyAcceptItem](tentativelyacceptitem.md) <br/> |表示暂时接受的会议请求答复。  <br/> |
   
## <a name="text-value"></a>文本值

Text 值是一个字符串，表示存储项的标识符。
  
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
Exchange Server 2010 Service Pack 2 (SP2) 中引入了此元素。
  
## <a name="element-information"></a>元素信息

||
|:-----|
|命名空间  <br/> |
|架构名称  <br/> |
|验证文件  <br/> |
|可以为空  <br/> |
   

