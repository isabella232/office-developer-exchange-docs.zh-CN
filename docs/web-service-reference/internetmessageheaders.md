---
title: InternetMessageHeaders
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- InternetMessageHeaders
api_type:
- schema
ms.assetid: 4dcf8671-96df-4a2d-9836-7e8e3a67e0db
description: InternetMessageHeaders 元素包含邮箱中的项目中包含的一些 Internet 邮件头的集合。 若要获取整个 Internet 邮件头集合，请使用 PR_TRANSPORT_MESSAGE_HEADERS 属性。 有关 EWS 和 Internet 邮件头详细信息，请参阅在 EWS、MIME 中获取 Internet 邮件头和缺少的 Internet 邮件头。
ms.openlocfilehash: 1ea49f2d5cc31aef09a9bc6d38dff25652696842
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541077"
---
# <a name="internetmessageheaders"></a>InternetMessageHeaders

**InternetMessageHeaders** 元素包含邮箱中的项目中包含的一些 Internet 邮件头的集合。 若要获取整个 Internet 邮件头集合，请使用 **PR_TRANSPORT_MESSAGE_HEADERS** 属性。 有关 EWS 和 Internet 邮件头的信息，请参阅 [EWS、MIME](https://msdn.microsoft.com/library/exchange/hh545614%28v=exchg.140%29.aspx)中的"获取 Internet 邮件头"和缺少的 Internet 邮件头。
  
```XML
<InternetMessageHeaders>
   <InternetMessageHeader/>
</InternetMessageHeaders>
```

 **NonEmptyArrayOfInternetHeadersType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[InternetMessageHeader](internetmessageheader.md) <br/> |代表 headers 集合中给定邮件头的 Internet 邮件头。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[AcceptItem](acceptitem.md) <br/> |表示接受答复会议要求。  <br/> |
|[CalendarItem](calendaritem.md) <br/> |表示 Exchange 日历项。  <br/> |
|[Contact](contact.md) <br/> |表示 Exchange 联系人项目。  <br/> |
|[DeclineItem](declineitem.md) <br/> |表示谢绝答复会议要求。  <br/> |
|[DistributionList](distributionlist.md) <br/> |表示通讯组列表。  <br/> |
|[项目](item.md) <br/> |表示 Exchange 存储中的项。  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |表示 Exchange 存储中的会议取消。  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |表示 Exchange 存储中的会议。  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |表示 Exchange 存储中的会议请求。  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |表示 Exchange 存储中的会议响应。  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |表示 Exchange 电子邮件。  <br/> |
|[RemoveItem](removeitem.md) <br/> |从 Exchange 存储中删除一个项目。  <br/> |
|[任务](task.md) <br/> |表示 Exchange 存储中的任务。  <br/> |
|[TentativelyAcceptItem](tentativelyacceptitem.md) <br/> |表示暂时接受的会议请求答复。  <br/> |
   
## <a name="remarks"></a>注解

下面是 EWS 托管 API 扩展属性定义的 PR_TRANSPORT_MESSAGE_HEADERS **属性。** 
  
```cs
ExtendedPropertyDefinition transportMsgHdr = new ExtendedPropertyDefinition(0x007D, MapiPropertyType.String);
```

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)


[EWS、MIME 和缺少的 Internet 邮件头](https://msdn.microsoft.com/library/exchange/hh545614%28v=exchg.140%29.aspx)

