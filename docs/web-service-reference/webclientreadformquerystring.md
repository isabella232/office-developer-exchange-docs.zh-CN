---
title: WebClientReadFormQueryString
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- WebClientReadFormQueryString
api_type:
- schema
ms.assetid: 13e8871a-32a6-4bb9-9493-864c4c07efff
description: WebClientReadFormQueryString 元素表示要连接到 Outlook Web App 终结点以读取项目在Outlook Web App。
ms.openlocfilehash: 10035aa001c74926ae36e96e09b5b2995844cb68
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59538469"
---
# <a name="webclientreadformquerystring"></a>WebClientReadFormQueryString

**WebClientReadFormQueryString** 元素表示连接到 Outlook Web App 终结点以读取项目在Outlook Web App。 
  
```XML
<WebClientReadFormQueryString/>
```

 **string**
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
|[PostItem](postitem.md) <br/> |代表应用商店中的Exchange项。  <br/> |
|[RemoveItem](removeitem.md) <br/> |从 Exchange 存储中删除一个项目。  <br/> |
|[任务](task.md) <br/> |表示 Exchange 存储中的任务。  <br/> |
   
## <a name="text-value"></a>文本值

如果使用此元素，则代表字符串的文本值是必需的。
  
## <a name="remarks"></a>注解

项目 URL 的项目标识符Outlook Web App项的 EWS 标识符。 您可以对 EWS 项标识符进行 URL 编码，并将其追加到查询字符串，Outlook Web App项的 URL。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
### <a name="version-differences"></a>版本差异

Exchange 版本从主要版本 15 开始到 Exchange Server 2013 内部版本 15.0.775.38 (CU3) 和 Exchange Online 版本 15.00.0775.009，不会在 **WebClientReadFormQueryString** 元素中返回正确的查询字符串片段。 
  
在主要Exchange 15 之前的版本版本中，Outlook Web App URL 的项目标识符是Outlook Web App标识符。 如果要面向主要版本 15 Exchange版本，您必须使用[ConvertId](convertid-operation.md)操作转换标识符。 
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

