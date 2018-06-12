---
title: SubscriptionStatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SubscriptionStatus
api_type:
- schema
ms.assetid: 2d64ebb7-f26a-4d02-b7ef-d9d7da75f0c3
description: SubscriptionStatus 元素描述推送订阅的状态。
ms.openlocfilehash: 1f6de15f7a3b07714899aef2ff74a8d556f8ca1d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838155"
---
# <a name="subscriptionstatus"></a>SubscriptionStatus

**SubscriptionStatus**元素描述推送订阅的状态。 
  
```xml
<SubscriptionStatus>OK or Unsubscribe</SubscriptionStatus>
```

 **SubscriptionStatusType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[SendNotificationResult](sendnotificationresult.md) <br/> |包含客户端应用程序的响应推送通知。  <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。 此元素的可能的文本值如下：
  
- 确定
    
- 取消订阅
    
## <a name="remarks"></a>备注

此元素描述订阅的状态。 推送订阅客户端应用程序发送回运行 Exchange 2007 的计算机的状态具有每个推送通知之后安装了客户端访问服务器角色。 如果**SubscriptionStatus**值等于**取消订阅**，客户端访问服务器将停止发送通知，并结束订阅。 如果**SubscriptionStatus**值等于**确定**，则客户端访问服务器将继续发送通知。
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

