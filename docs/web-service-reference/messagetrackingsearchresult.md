---
title: MessageTrackingSearchResult
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MessageTrackingSearchResult
api_type:
- schema
ms.assetid: 8ea77aa8-b93f-4287-be36-0a9da06e0946
description: MessageTrackingSearchResult 元素包含 FindMessageTrackingReportResponse 元素的单个邮件结果。
ms.openlocfilehash: ad4fb9d9e2266222303bd2015a7afba0bb46721b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826460"
---
# <a name="messagetrackingsearchresult"></a>MessageTrackingSearchResult

**MessageTrackingSearchResult**元素包含[FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md)元素的单个邮件结果。 
  
```xml
<MessageTrackingSearchResult>
   <Subject/>
   <Sender/>
   <PurportedSender/>
   <Recipients/>
   <SubmittedTime/>
   <MessageTrackingReportId/>
   <PreviousHopServer/>
   <FirstHopServer/>
   <Properties/>
</MessageTrackingSearchResult>
```

 **FindMessageTrackingSearchResultType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Subject](subject.md) <br/> |包含电子邮件主题。  <br/> |
|[发件人 (EmailAddressType)](sender-emailaddresstype.md) <br/> |包含电子邮件发件人的地址。  <br/> |
|[PurportedSender](purportedsender.md) <br/> |包含声称的发件人的电子邮件的联系人信息。  <br/> |
|[收件人 (ArrayOfRecipientsType)](recipients-arrayofrecipientstype.md) <br/> |包含的电子邮件地址收到此消息的列表。  <br/> |
|[SubmittedTime](submittedtime.md) <br/> |包含已提交提交邮件的时间。  <br/> |
|[MessageTrackingReportId](messagetrackingreportid.md) <br/> |包含内部 ID 标识的传输数据库中的消息。  <br/> |
|[PreviousHopServer](previoushopserver.md) <br/> |包含林中的以前接受邮件服务器的名称。  <br/> |
|[FirstHopServer](firsthopserver.md) <br/> |包含林中的先接受邮件服务器的名称。  <br/> |
|[属性 (ArrayOfTrackingPropertiesType)](properties-arrayoftrackingpropertiestype.md) <br/> |包含一个或多个跟踪属性的列表。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[MessageTrackingSearchResults](messagetrackingsearchresults.md) <br/> |包含与搜索条件匹配的邮件的列表。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>备注

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[FindMessageTrackingReport 操作](findmessagetrackingreport-operation.md)


- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

