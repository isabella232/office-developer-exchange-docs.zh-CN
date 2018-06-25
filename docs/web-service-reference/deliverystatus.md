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
description: DeliveryStatus 元素指定一条消息的状态。
ms.openlocfilehash: 4e6f31e8ef4f98d8e838ba91167c7dd5d6ab2590
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753832"
---
# <a name="deliverystatus"></a>DeliveryStatus

**DeliveryStatus**元素指定一条消息的状态。 
  
```XML
<DeliveryStatus>Unsuccessful | Pending | Delivered | Transferred | Read</DeliveryStatus>
```

 **MessageTrackingDeliveryStatusType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[RecipientTrackingEvent](recipienttrackingevent.md) <br/> |包含收件人为一个事件的信息。  <br/> |
   
## <a name="text-value"></a>文本值

下表列出了**DeliveryStatus**元素的可能的文本值。 
  
**DeliveryStatus 元素的值**

|**值**|**说明**|
|:-----|:-----|
|失败  <br/> |指定一条消息未送达。  <br/> |
|挂起  <br/> |指定邮件正等待审阅者的批准。  <br/> |
|传送  <br/> |指定邮件已送达所有指定的收件人。  <br/> |
|转接  <br/> |指定邮件已转接到的搜索范围之外的服务器。  <br/> |
|已阅读  <br/> |指定邮件已发送和读取的收件人。  <br/> |
   
## <a name="remarks"></a>注解

**DeliveryStatus**元素是类型**MessageTrackingDeliveryStatusType**在 Exchange Server 2010。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

