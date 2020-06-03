---
title: ErrorSubscriptionIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ErrorSubscriptionIds
api_type:
- schema
ms.assetid: e64e76ff-4d98-4082-9acc-a1114ae45f44
description: ErrorSubscriptionIds 元素包含一个由无效订阅 Id 组成的数组。
ms.openlocfilehash: bdc5c86560800464d677a9043607bed3f7872e32
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526184"
---
# <a name="errorsubscriptionids"></a>ErrorSubscriptionIds

**ErrorSubscriptionIds**元素包含一个由无效订阅 id 组成的数组。 
  
```xml
<ErrorSubscriptionIds>
   <SubscriptionId/>
</ErrorSubscriptionIds>
```

 **NonEmptyArrayOfSubscriptionIdsType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[SubscriptionId （GetEvents）](subscriptionid-getevents.md) <br/> |表示订阅的标识符。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetStreamingEventsResponseMessage](getstreamingeventsresponsemessage.md) <br/> |包含单个[GetStreamingEvents 操作](getstreamingevents-operation.md)请求的状态和结果。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages 和 https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |邮件架构;类型架构  <br/> |
|验证文件  <br/> |消息 .xsd;类型 .xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetStreamingEvents 操作](getstreamingevents-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

