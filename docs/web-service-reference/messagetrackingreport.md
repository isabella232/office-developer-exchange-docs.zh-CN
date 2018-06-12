---
title: MessageTrackingReport
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MessageTrackingReport
api_type:
- schema
ms.assetid: 2740bcf6-f86d-4756-a0f2-24ed6e9b75f7
description: MessageTrackingReport 元素包含 GetMessageTrackingReport 操作中返回的单个消息。
ms.openlocfilehash: d01e0fbf099d096c7f255a8e94070e330577e6ca
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826457"
---
# <a name="messagetrackingreport"></a>MessageTrackingReport

**MessageTrackingReport**元素包含在[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)中返回单个邮件。
  
```XML
<MessageTrackingReport>
   <Sender/>
   <PurportedSender/>
   <Subject/>
   <SubmitTime/>
   <OriginalRecipients/>
   <RecipientTrackingEvents/>
   <Properties/>
</MessageTrackingReport>
```

 **MessageTrackingReportType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[发件人 (EmailAddressType)](sender-emailaddresstype.md) <br/> |包含发件人的电子邮件的联系人信息。  <br/> |
|[PurportedSender](purportedsender.md) <br/> |包含声称的发件人的电子邮件的联系人信息。  <br/> |
|[Subject](subject.md) <br/> |包含电子邮件的主题。  <br/> |
|[SubmitTime](submittime.md) <br/> |包含已提交的电子邮件的一天的时间。  <br/> |
|[OriginalRecipients](originalrecipients.md) <br/> |包含电子邮件收件人的列表。  <br/> |
|[RecipientTrackingEvents](recipienttrackingevents.md) <br/> |包含一个或多个跟踪事件的列表的收件人。  <br/> |
|[属性 (ArrayOfTrackingPropertiesType)](properties-arrayoftrackingpropertiestype.md) <br/> |包含一个或多个跟踪属性的列表。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetMessageTrackingReportResponse](getmessagetrackingreportresponse.md) <br/> |包含结果的单个[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)请求。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>备注

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[FindMessageTrackingReport 操作](findmessagetrackingreport-operation.md)
  
[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)


- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)
  
- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

