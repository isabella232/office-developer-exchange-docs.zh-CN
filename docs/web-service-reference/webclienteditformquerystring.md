---
title: WebClientEditFormQueryString
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- WebClientEditFormQueryString
api_type:
- schema
ms.assetid: 9e571021-d58f-424b-8db2-48cf683533dc
description: WebClientEditFormQueryString 元素表示要连接到 Outlook Web App 中编辑项目的 Outlook Web App 终结点的 URL。
ms.openlocfilehash: a7503c3896899e8d2da6aced7b8d259f9b8aaceb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838541"
---
# <a name="webclienteditformquerystring"></a>WebClientEditFormQueryString

**WebClientEditFormQueryString**元素表示要连接到 Outlook Web App 中编辑项目的 Outlook Web App 终结点的 URL。 
  
```XML
<WebClientEditFormQueryString/>
```

 **string**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[日历项目](calendaritem.md) <br/> |表示 Exchange 日历项。  <br/> |
|[联系人](contact.md) <br/> |表示 Exchange 联系人项目。  <br/> |
|[DistributionList](distributionlist.md) <br/> |表示通讯组列表。  <br/> |
|[项目](item.md) <br/> |表示 Exchange 存储中的项。  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |表示 Exchange 存储中的会议取消。  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |表示 Exchange 存储中的会议。  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |表示 Exchange 存储中的会议请求。  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |表示 Exchange 存储中的会议响应。  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |表示 Exchange 电子邮件。  <br/> |
|[PostItem](postitem.md) <br/> |代表一个 Exchange 存储中的公告项目。  <br/> |
|[任务](task.md) <br/> |表示 Exchange 存储中的任务。  <br/> |
   
## <a name="text-value"></a>文本值

如果使用此元素，则需要用于表示字符串的文本值。
  
## <a name="remarks"></a>注解

启动与 Exchange Server 2013，包括 Exchange Online 的 Exchange 版本使用来自[WebClientReadFormQueryString](webclientreadformquerystring.md)元素的信息来打开 Outlook Web App 中的草稿项，然后使用 UI 编辑草稿项目。 **WebClientEditFormQueryString**元素不适用于启动与 Exchange Server 2013，包括 Exchange Online 的 Exchange 版本。 
  
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

