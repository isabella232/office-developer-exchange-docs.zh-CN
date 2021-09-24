---
title: RootAddress
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RootAddress
api_type:
- schema
ms.assetid: 1dbb130a-e4eb-4baf-ae07-2568a8375bff
description: RootAddress 元素表示启动 RecipientTrackingEvent 事件事件的第一个地址。
ms.openlocfilehash: 8e9ad87889fa2cd02dee7b4b7c16d36862d4becd
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59525573"
---
# <a name="rootaddress"></a>RootAddress

**RootAddress** 元素表示为 [RecipientTrackingEvent 事件启动事件的第一个](recipienttrackingevent.md)地址。 
  
```xml
<RootAddress/>
```

 **NonEmptyStringType**
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

文本值是启动跟踪事件的地址。
  
## <a name="remarks"></a>注解

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

