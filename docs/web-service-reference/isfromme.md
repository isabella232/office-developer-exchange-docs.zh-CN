---
title: IsFromMe
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsFromMe
api_type:
- schema
ms.assetid: d3c5fbf0-a95c-46e5-890f-953e50ac49d6
description: IsFromMe 元素指示用户是否向他或她发送了一项。
ms.openlocfilehash: eb69aa493d5ba8b0497fde4c52ad80fe17c92f1c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/01/2020
ms.locfileid: "44468017"
---
# <a name="isfromme"></a>IsFromMe

**IsFromMe**元素指示用户是否向他或她发送了一项。 
  
```xml
<IsFromMe/>
```

 **Boolean**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |表示 Exchange 日历项。  <br/> |
|[Contact](contact.md) <br/> |表示 Exchange 联系人项目。  <br/> |
|[DistributionList](distributionlist.md) <br/> |表示通讯组列表。  <br/> |
|[项目](item.md) <br/> |表示 Exchange 存储中的项。  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |表示 Exchange 存储中的会议取消。  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |表示 Exchange 存储中的会议。  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |表示 Exchange 存储中的会议请求。  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |表示 Exchange 存储中的会议响应。  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |表示 Exchange 电子邮件。  <br/> |
|[RemoveItem](removeitem.md) <br/> |从 Exchange 存储中删除一个项目。  <br/> |
|[任务](task.md) <br/> |表示 Exchange 存储中的任务。  <br/> |
   
## <a name="text-value"></a>文本值

如果文本值为**true** ，则表示该项目已由用户发送给他或她。 如果值为**false** ，则表示该项目未由用户发送给他或她。 
  
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

