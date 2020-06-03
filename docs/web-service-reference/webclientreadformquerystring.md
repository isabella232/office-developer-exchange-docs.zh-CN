---
title: WebClientReadFormQueryString
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- WebClientReadFormQueryString
api_type:
- schema
ms.assetid: 13e8871a-32a6-4bb9-9493-864c4c07efff
description: WebClientReadFormQueryString 元素表示用于连接到 Outlook web App 终结点以在 Outlook Web App 中读取项目的 URL。
ms.openlocfilehash: d7102ef288c0aafa6cdada09eda321b546edddb7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464978"
---
# <a name="webclientreadformquerystring"></a>WebClientReadFormQueryString

**WebClientReadFormQueryString**元素表示用于连接到 Outlook web app 终结点以在 Outlook web app 中读取项目的 URL。 
  
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
|[PostItem](postitem.md) <br/> |表示 Exchange 存储中的公告项。  <br/> |
|[RemoveItem](removeitem.md) <br/> |从 Exchange 存储中删除一个项目。  <br/> |
|[任务](task.md) <br/> |表示 Exchange 存储中的任务。  <br/> |
   
## <a name="text-value"></a>文本值

如果使用此元素，则需要一个表示字符串的文本值。
  
## <a name="remarks"></a>备注

Outlook Web App URL 的项目标识符是项目的 EWS 标识符。 您可以对 EWS 项标识符进行 URL 编码，并将其追加到查询字符串，以获取项目的 Outlook Web App URL。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
### <a name="version-differences"></a>版本差异

Exchange 的版本从主要版本15开始，以 Exchange Server 2013 build 15.0.775.38 （CU3）和 Exchange Online 版本15.00.0775.009 在**WebClientReadFormQueryString**元素中不返回正确的查询字符串片段。 
  
在低于主要版本15的 Exchange 版本中，Outlook Web App Url 的项目标识符是 Outlook Web App 标识符。 如果要将低于主要版本15的 Exchange 作为目标，则必须使用[ConvertId 操作](convertid-operation.md)来转换标识符。 
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

