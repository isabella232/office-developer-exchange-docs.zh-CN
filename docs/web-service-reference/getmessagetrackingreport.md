---
title: GetMessageTrackingReport
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetMessageTrackingReport
api_type:
- schema
ms.assetid: b6ffa8ef-90f6-402d-afac-c3f5ee55cf49
description: GetMessageTrackingReport 元素包含要检索完整的邮件跟踪报告的指定 ID 的 GetMessageTrackingReport 操作的请求
ms.openlocfilehash: cb16f6e9d322cefb0d59c962af8e2f60ebae0e90
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754622"
---
# <a name="getmessagetrackingreport"></a>GetMessageTrackingReport

**GetMessageTrackingReport**元素包含[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)以检索完整的邮件跟踪报告的指定 ID 的请求 
  
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

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[范围 (NonEmptyStringType)](scope-nonemptystringtype.md) <br/> |指定用于执行搜索的位置。 此元素是必需的。  <br/> |
|[ReportTemplate](reporttemplate.md) <br/> |指定用于跟踪报告，若要检索的类型。 此元素是必需的。  <br/> |
|[RecipientFilter](recipientfilter.md) <br/> |指定要用于指定的跟踪报告的收件人地址。 此元素是可选的。  <br/> |
|[MessageTrackingReportId](messagetrackingreportid.md) <br/> |指定来自**FindMessageTrackingReport**操作标识字符串。 此元素是必需的。  <br/> |
|[ReturnQueueEvents](returnqueueevents.md) <br/> |指定运行任务的用户具有的特权的角色。 此元素是可选的。  <br/> |
|[DiagnosticsLevel](diagnosticslevel.md) <br/> |指定将用于派生跟踪报告的计时和性能信息。 此元素是可选的。  <br/> |
|[属性 (ArrayOfTrackingPropertiesType)](properties-arrayoftrackingpropertiestype.md) <br/> |指定的一个或多个跟踪属性的列表。 此元素是可选的。  <br/> |
   
### <a name="parent-elements"></a>父元素

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



[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)


- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

