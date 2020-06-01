---
title: DeliveryStatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeliveryStatus
api_type:
- schema
ms.assetid: eab55db3-affb-42be-a586-5caa04052433
description: DeliveryStatus 元素指定邮件的状态。
ms.openlocfilehash: ae32202284d3dd272f693fbb7b76070cb6019d28
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461399"
---
# <a name="deliverystatus"></a>DeliveryStatus

**DeliveryStatus**元素指定邮件的状态。 
  
```XML
<DeliveryStatus>Unsuccessful | Pending | Delivered | Transferred | Read</DeliveryStatus>
```

 **MessageTrackingDeliveryStatusType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**描述**|
|:-----|:-----|
|[RecipientTrackingEvent](recipienttrackingevent.md) <br/> |包含收件人的单个事件的信息。  <br/> |
   
## <a name="text-value"></a>文本值

下表列出了**DeliveryStatus**元素的可能的文本值。 
  
**DeliveryStatus 元素值**

|**值**|**说明**|
|:-----|:-----|
|多次  <br/> |指定邮件未送达。  <br/> |
|Pending  <br/> |指定邮件正在等待来自审阅者的审批。  <br/> |
|附带  <br/> |指定邮件已传递给所有指定的收件人。  <br/> |
|传递  <br/> |指定将邮件传输到搜索范围之外的服务器。  <br/> |
|阅读  <br/> |指定邮件已被收件人传递和读取。  <br/> |
   
## <a name="remarks"></a>备注

**DeliveryStatus**元素为 Exchange Server 2010 中的**MessageTrackingDeliveryStatusType**类型。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

