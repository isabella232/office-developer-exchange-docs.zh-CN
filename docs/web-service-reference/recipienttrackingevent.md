---
title: RecipientTrackingEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RecipientTrackingEvent
api_type:
- schema
ms.assetid: 2bffdac7-c2f5-4805-ae7e-bd865301acb6
description: RecipientTrackingEvent 元素包含收件人为一个事件的信息。
ms.openlocfilehash: c5488ba105f9a853a490d6f0f4ff9ff15b537e23
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826989"
---
# <a name="recipienttrackingevent"></a>RecipientTrackingEvent

**RecipientTrackingEvent**元素包含收件人为一个事件的信息。 
  
```XML
<RecipientTrackingEvent>
   <Date/>
   <Recipient/>
   <DeliveryStatus/>
   <EventDescription/>
   <EventData/>
   <Server/>
   <InternalId/>
   <BccRecipient/>
   <HiddenRecipient/>
   <UniquePathId/>
   <RootAddress/>
   <Properties/>
</RecipientTrackingEvent>
```

 **RecipientTrackingEventType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[日期 (MessageTracking)](date-messagetracking.md) <br/> |此元素是必需的。  <br/> |
|[Recipient](recipient.md) <br/> |此元素是必需的。  <br/> |
|[DeliveryStatus](deliverystatus.md) <br/> |此元素是必需的。  <br/> |
|[EventDescription](eventdescription.md) <br/> |此元素是必需的。  <br/> |
|[EventData](eventdata.md) <br/> |此元素是可选的。  <br/> |
|[服务器 (MessageTracking)](server-messagetracking.md) <br/> |此元素是必需的。  <br/> |
|[InternalId](internalid.md) <br/> |此元素是必需的。  <br/> |
|[BccRecipient](bccrecipient.md) <br/> |此元素是可选的。  <br/> |
|[HiddenRecipient](hiddenrecipient.md) <br/> |此元素是可选的。  <br/> |
|[UniquePathId](uniquepathid.md) <br/> |此元素是可选的。  <br/> |
|[RootAddress](rootaddress.md) <br/> |此元素是可选的。  <br/> |
|[属性 (ArrayOfTrackingPropertiesType)](properties-arrayoftrackingpropertiestype.md) <br/> |此元素是可选的。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[RecipientTrackingEvents](recipienttrackingevents.md) <br/> |包含一个或多个跟踪事件的列表的收件人。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>备注

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)


- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

