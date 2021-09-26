---
title: Timeout (duration)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: bb15f9a7-8ea5-4765-9877-762c3f98bf50
description: Timeout 元素指定服务器超时拉订阅之前的时间长度。
ms.openlocfilehash: a5a9e094c25f609c0bcfa207ab96ae7f0877f43f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59545767"
---
# <a name="timeout-duration"></a>Timeout (duration)

**Timeout** 元素指定服务器超时拉订阅之前的时间长度。 
  
```XML
<Timeout></Timeout>
```

 **SubscriptionTimeoutType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[PullSubscriptionRequest](pullsubscriptionrequest.md)
  
## <a name="text-value"></a>文本值

**Timeout** 元素的文本值是服务器超时拉订阅之前的时间长度（分钟）。 最小值为 1;最大值为 1440。 
  
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> ||
   

