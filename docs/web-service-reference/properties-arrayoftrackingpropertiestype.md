---
title: Properties (ArrayOfTrackingPropertiesType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Properties
api_type:
- schema
ms.assetid: 175566d2-fd62-45a2-8518-2827912cec88
description: Properties 元素包含一个或多个跟踪属性的列表。
ms.openlocfilehash: 8232b94effe3aae5b07be12bdaf1b5e85331938f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542979"
---
# <a name="properties-arrayoftrackingpropertiestype"></a>Properties (ArrayOfTrackingPropertiesType)

Properties 元素包含一个或多个跟踪属性的列表。 
  
- [FindMessageTrackingReport](findmessagetrackingreport.md)
  
- [Properties (ArrayOfTrackingPropertiesType)](properties-arrayoftrackingpropertiestype.md)
  
```xml
<Properties>
   <TrackingPropertyType/>
</Properties>
```

**ArrayOfTrackingPropertiesType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[TrackingPropertyType](trackingpropertytype.md) <br/> |表示用于创建邮件跟踪报告的属性的字符串的名称和值对。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FindMessageTrackingReport](findmessagetrackingreport.md) <br/> |指定要查找的邮件类型的条件。  <br/> |
|[FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) <br/> |包含单个 [FindMessageTrackingReport](findmessagetrackingreport-operation.md) 操作请求的状态和结果。  <br/> |
|[GetMessageTrackingReport](getmessagetrackingreport.md) <br/> |包含 [GetMessageTrackingReport](getmessagetrackingreport-operation.md) 操作的请求，以检索指定 ID 的完整邮件跟踪报告。  <br/> |
|[GetMessageTrackingReportResponse](getmessagetrackingreportresponse.md) <br/> |包含单个 [GetMessageTrackingReport 操作请求](getmessagetrackingreport-operation.md) 的结果。  <br/> |
|[RecipientTrackingEvent](recipienttrackingevent.md) <br/> |包含收件人的单个事件的信息。  <br/> |
|[MessageTrackingReport](messagetrackingreport.md) <br/> |包含在[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)中返回一条消息。  <br/> |
|[MessageTrackingSearchResult](messagetrackingsearchresult.md) <br/> |包含 [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) 元素的单个邮件结果。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>注解

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [FindMessageTrackingReport 操作](findmessagetrackingreport-operation.md)
- [GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

