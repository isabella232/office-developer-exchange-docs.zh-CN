---
title: Name (Message Tracking)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Name
api_type:
- schema
ms.assetid: a1669f6d-53f3-4849-9b30-56909aaeac82
description: Name 元素表示邮件跟踪报告的属性名称。
ms.openlocfilehash: b57c109cfbcb2744ae6854e0afce52e240d22b30
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515451"
---
# <a name="name-message-tracking"></a>Name (Message Tracking)

**Name** 元素表示邮件跟踪报告的属性名称。 
  
```xml
<Name/>
```

**String**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[TrackingPropertyType](trackingpropertytype.md) <br/> |表示用于创建邮件跟踪报告的属性的字符串的名称和值对。  <br/> |
   
## <a name="text-value"></a>文本值

如果此元素已使用，则文本值是必需的。
  
## <a name="remarks"></a>注解

此元素可在 [TrackingPropertyType](trackingpropertytype.md) 元素中最多出现一次。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

