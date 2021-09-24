---
title: MessageTrackingSearchResult
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MessageTrackingSearchResult
api_type:
- schema
ms.assetid: 8ea77aa8-b93f-4287-be36-0a9da06e0946
description: MessageTrackingSearchResult 元素包含 FindMessageTrackingReportResponse 元素的单个邮件结果。
ms.openlocfilehash: 2bd70461b2896d0204b163365d525f76d42bb213
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523878"
---
# <a name="messagetrackingsearchresult"></a>MessageTrackingSearchResult

**MessageTrackingSearchResult** 元素包含 [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md)元素的单个邮件结果。 
  
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

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[主题](subject.md) <br/> |包含电子邮件主题。  <br/> |
|[Sender (EmailAddressType)](sender-emailaddresstype.md) <br/> |包含电子邮件发件人的地址。  <br/> |
|[PurportedSender](purportedsender.md) <br/> |包含电子邮件的发件人的联系信息。  <br/> |
|[Recipients (ArrayOfRecipientsType)](recipients-arrayofrecipientstype.md) <br/> |包含收到此邮件的电子邮件地址列表。  <br/> |
|[SubmittedTime](submittedtime.md) <br/> |包含邮件的提交时间。  <br/> |
|[MessageTrackingReportId](messagetrackingreportid.md) <br/> |包含标识传输数据库中的邮件的内部 ID。  <br/> |
|[PreviousHopServer](previoushopserver.md) <br/> |包含林中先前接受邮件的服务器的名称。  <br/> |
|[FirstHopServer](firsthopserver.md) <br/> |包含林中第一次接受邮件的服务器的名称。  <br/> |
|[Properties (ArrayOfTrackingPropertiesType)](properties-arrayoftrackingpropertiestype.md) <br/> |包含一个或多个跟踪属性的列表。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[MessageTrackingSearchResults](messagetrackingsearchresults.md) <br/> |包含匹配搜索条件的邮件列表。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>注解

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[FindMessageTrackingReport 操作](findmessagetrackingreport-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

