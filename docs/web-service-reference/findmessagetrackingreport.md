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
description: FindMessageTrackingReport 元素指定要查找的邮件类型的条件。
ms.openlocfilehash: d30e5391bb4305cae0004a9788df971a57297cae
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462934"
---
# <a name="findmessagetrackingreport"></a>FindMessageTrackingReport

**FindMessageTrackingReport**元素指定要查找的邮件类型的条件。 
  
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
|[范围（NonEmptyStringType）](scope-nonemptystringtype.md) <br/> |表示邮件跟踪报告的范围。  <br/> |
|[域（邮件跟踪）](domain-message-tracking.md) <br/> |包含执行邮件跟踪的域的名称。  <br/> |
|[发件人（EmailAddressType）](sender-emailaddresstype.md) <br/> |包含电子邮件发件人的联系人信息。  <br/> |
|[PurportedSender](purportedsender.md) <br/> |包含所声称的电子邮件发件人的联系人信息。  <br/> |
|[收件人](recipient.md) <br/> |包含邮件收件人的电子邮件地址。  <br/> |
|[主题](subject.md) <br/> |包含电子邮件的主题。  <br/> |
|[StartDateTime](startdatetime.md) <br/> |包含搜索的开始日期和时间。  <br/> |
|[EndDateTime](enddatetime.md) <br/> |包含搜索的结束日期和时间。  <br/> |
|[MessageId](messageid.md) <br/> |包含搜索的邮件标识符。  <br/> |
|[FederatedDeliveryMailbox](federateddeliverymailbox.md) <br/> |包含发送了跨界邮件的邮箱的名称。  <br/> |
|[DiagnosticsLevel](diagnosticslevel.md) <br/> |表示诊断报告的详细程度。  <br/> |
|[ServerHint](serverhint.md) <br/> |表示跟踪远程站点或林中的邮件的起始点。  <br/> |
|[Properties （ArrayOfTrackingPropertiesType）](properties-arrayoftrackingpropertiestype.md) <br/> |包含一个或多个跟踪属性的列表。 此元素为可选。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>说明

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

