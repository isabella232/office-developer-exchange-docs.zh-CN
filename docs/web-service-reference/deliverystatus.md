---
title: DeliveryStatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DeliveryStatus
api_type:
- schema
ms.assetid: eab55db3-affb-42be-a586-5caa04052433
description: DeliveryStatus 元素指定邮件的状态。
ms.openlocfilehash: f11952f401e0d22d780725598bfb32cbd3a8d622
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543385"
---
# <a name="deliverystatus"></a>DeliveryStatus

**DeliveryStatus** 元素指定邮件的状态。 
  
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

|**元素**|**说明**|
|:-----|:-----|
|[RecipientTrackingEvent](recipienttrackingevent.md) <br/> |包含收件人的单个事件的信息。  <br/> |
   
## <a name="text-value"></a>文本值

下表列出了 **DeliveryStatus** 元素的可能文本值。 
  
**DeliveryStatus 元素值**

|**值**|**说明**|
|:-----|:-----|
|不成功  <br/> |指定未传递邮件。  <br/> |
|挂起  <br/> |指定邮件正在等待审阅人审批。  <br/> |
|已传递  <br/> |指定邮件已传递给所有指定的收件人。  <br/> |
|已转移  <br/> |指定邮件已传输到搜索范围之外的服务器。  <br/> |
|读取  <br/> |指定邮件由收件人传递和读取。  <br/> |
   
## <a name="remarks"></a>注解

**DeliveryStatus** 元素的类型为 **MessageTrackingDeliveryStatusType，Exchange Server** 2010 年。 
  
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

