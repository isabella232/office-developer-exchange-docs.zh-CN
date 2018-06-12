---
title: FindMessageTrackingReport
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindMessageTrackingReport
api_type:
- schema
ms.assetid: 7ca6e2f7-aae1-4920-b839-73513ba8d4d8
description: FindMessageTrackingReport 元素指定条件的邮件，以查找的类型。
ms.openlocfilehash: 77545121aa056992248c045af3f3d36566678b94
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754352"
---
# <a name="findmessagetrackingreport"></a>FindMessageTrackingReport

**FindMessageTrackingReport**元素指定条件的邮件，以查找的类型。 
  
```xml
<FindMessageTrackingReport>
   <Scope/>
   <Domain/>
   <Sender/>
   <PurportedSender/>
   <Recipient/>
   <Subject/>
   <StartDateTime/>
   <EndDateTime/>
   <MessageId/>
   <FederatedDeliveryMailbox/>
   <DiagnosticsLevel/>
   <ServerHint/>
   <Properties/>
</FindMessageTrackingReport>
```

 **FindMessageTrackingReportRequestType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[范围 (NonEmptyStringType)](scope-nonemptystringtype.md) <br/> |代表邮件跟踪报告应如何扩展。  <br/> |
|[域 （邮件跟踪）](domain-message-tracking.md) <br/> |包含执行邮件跟踪所在的域的名称。  <br/> |
|[发件人 (EmailAddressType)](sender-emailaddresstype.md) <br/> |包含发件人的电子邮件的联系人信息。  <br/> |
|[PurportedSender](purportedsender.md) <br/> |包含声称的发件人的电子邮件的联系人信息。  <br/> |
|[Recipient](recipient.md) <br/> |包含邮件的收件人的电子邮件地址。  <br/> |
|[Subject](subject.md) <br/> |包含电子邮件的主题。  <br/> |
|[开始日期时间](startdatetime.md) <br/> |包含开始的日期和时间的搜索。  <br/> |
|[EndDateTime](enddatetime.md) <br/> |包含的结束日期和时间搜索。  <br/> |
|[MessageId](messageid.md) <br/> |包含搜索的消息标识符。  <br/> |
|[FederatedDeliveryMailbox](federateddeliverymailbox.md) <br/> |包含其中发送跨内部部署邮件的邮箱的名称。  <br/> |
|[DiagnosticsLevel](diagnosticslevel.md) <br/> |表示的诊断报告的详细信息的级别。  <br/> |
|[ServerHint](serverhint.md) <br/> |代表跟踪远程站点或林的邮件中的起始点。  <br/> |
|[属性 (ArrayOfTrackingPropertiesType)](properties-arrayoftrackingpropertiestype.md) <br/> |包含一个或多个跟踪属性的列表。 此元素是可选的。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>备注

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[FindMessageTrackingReport 操作](findmessagetrackingreport-operation.md)


- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

