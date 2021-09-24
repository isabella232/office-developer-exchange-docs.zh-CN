---
title: FindMessageTrackingReport
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FindMessageTrackingReport
api_type:
- schema
ms.assetid: 7ca6e2f7-aae1-4920-b839-73513ba8d4d8
description: FindMessageTrackingReport 元素指定要查找的邮件类型的条件。
ms.openlocfilehash: ec2ab16c6649d85edd86b9438e00ea7cfb9841ef
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513687"
---
# <a name="findmessagetrackingreport"></a>FindMessageTrackingReport

**FindMessageTrackingReport** 元素指定要查找的邮件类型的条件。 
  
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

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Scope (NonEmptyStringType)](scope-nonemptystringtype.md) <br/> |表示邮件跟踪报告应具有的范围。  <br/> |
|[Domain (Message Tracking)](domain-message-tracking.md) <br/> |包含执行邮件跟踪的域的名称。  <br/> |
|[Sender (EmailAddressType)](sender-emailaddresstype.md) <br/> |包含电子邮件发件人的联系人信息。  <br/> |
|[PurportedSender](purportedsender.md) <br/> |包含电子邮件的发件人的联系信息。  <br/> |
|[收件人](recipient.md) <br/> |包含邮件收件人的电子邮件地址。  <br/> |
|[主题](subject.md) <br/> |包含电子邮件的主题。  <br/> |
|[StartDateTime](startdatetime.md) <br/> |包含搜索的开始日期和时间。  <br/> |
|[EndDateTime](enddatetime.md) <br/> |包含搜索的结束日期和时间。  <br/> |
|[MessageId](messageid.md) <br/> |包含搜索的邮件标识符。  <br/> |
|[FederatedDeliveryMailbox](federateddeliverymailbox.md) <br/> |包含发送跨界邮件的邮箱的名称。  <br/> |
|[DiagnosticsLevel](diagnosticslevel.md) <br/> |表示诊断报告的详细信息级别。  <br/> |
|[ServerHint](serverhint.md) <br/> |代表跟踪远程站点或林中的邮件的起点。  <br/> |
|[Properties (ArrayOfTrackingPropertiesType)](properties-arrayoftrackingpropertiestype.md) <br/> |包含一个或多个跟踪属性的列表。 此元素为可选。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>注解

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[FindMessageTrackingReport 操作](findmessagetrackingreport-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

