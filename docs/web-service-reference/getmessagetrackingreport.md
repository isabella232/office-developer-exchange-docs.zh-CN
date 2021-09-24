---
title: GetMessageTrackingReport
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GetMessageTrackingReport
api_type:
- schema
ms.assetid: b6ffa8ef-90f6-402d-afac-c3f5ee55cf49
description: GetMessageTrackingReport 元素包含 GetMessageTrackingReport 操作的请求，以检索指定 ID 的完整邮件跟踪报告。
ms.openlocfilehash: cdf4e2c0f17c7d723dc56f30c445bfd527f891a3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516977"
---
# <a name="getmessagetrackingreport"></a>GetMessageTrackingReport

**GetMessageTrackingReport** 元素包含 [GetMessageTrackingReport](getmessagetrackingreport-operation.md)操作的请求，以检索指定 ID 的完整邮件跟踪报告。 
  
```XML
<GetMessageTrackingReport>
   <Scope/>
   <ReportTemplate/>
   <RecipientFilter/>
   <MessageTrackingReportId/>
   <ReturnQueueEvents/>
   <DiagnosticsLevel/>
   <Properties/>
</GetMessageTrackingReport>
```

 **GetMessageTrackingReportRequestType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Scope (NonEmptyStringType)](scope-nonemptystringtype.md) <br/> |指定在何处执行搜索。 此元素是必需的。  <br/> |
|[ReportTemplate](reporttemplate.md) <br/> |指定要检索的跟踪报告的类型。 此元素是必需的。  <br/> |
|[RecipientFilter](recipientfilter.md) <br/> |指定要用于指定跟踪报告的收件人地址。 此元素为可选。  <br/> |
|[MessageTrackingReportId](messagetrackingreportid.md) <br/> |指定从 **FindMessageTrackingReport** 操作获取的标识字符串。 此元素是必需的。  <br/> |
|[ReturnQueueEvents](returnqueueevents.md) <br/> |指定运行该任务的人具有特权角色。 此元素为可选。  <br/> |
|[DiagnosticsLevel](diagnosticslevel.md) <br/> |指定将用于派生跟踪报告的计时和性能信息。 此元素为可选。  <br/> |
|[Properties (ArrayOfTrackingPropertiesType)](properties-arrayoftrackingpropertiestype.md) <br/> |指定一个或多个跟踪属性的列表。 此元素为可选。  <br/> |
   
### <a name="parent-elements"></a>父元素

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



[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

