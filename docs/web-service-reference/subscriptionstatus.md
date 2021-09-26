---
title: SubscriptionStatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SubscriptionStatus
api_type:
- schema
ms.assetid: 2d64ebb7-f26a-4d02-b7ef-d9d7da75f0c3
description: SubscriptionStatus 元素描述推送订阅的状态。
ms.openlocfilehash: 6918a4965da2c075341c99581c3bd06c93da35fa
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546929"
---
# <a name="subscriptionstatus"></a>SubscriptionStatus

**SubscriptionStatus** 元素描述推送订阅的状态。 
  
```xml
<SubscriptionStatus>OK or Unsubscribe</SubscriptionStatus>
```

 **SubscriptionStatusType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[SendNotificationResult](sendnotificationresult.md) <br/> |包含客户端应用程序对推送通知的响应。  <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。 以下是此元素的可能文本值：
  
- 确定
    
- Unsubscribe
    
## <a name="remarks"></a>注解

此元素描述订阅的状态。 推送订阅客户端应用程序将状态发送回运行 Exchange 2007 的计算机，该计算机在每个推送通知后安装了客户端访问服务器角色。 如果 **SubscriptionStatus** 值等于 **Unsubscribe，** 客户端访问服务器将停止发送通知并结束订阅。 如果 **SubscriptionStatus** 值等于 **OK，** 则客户端访问服务器将继续发送通知。
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

