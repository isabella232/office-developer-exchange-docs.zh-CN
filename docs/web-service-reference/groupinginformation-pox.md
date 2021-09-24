---
title: GroupingInformation (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 2d8a007f-d79c-43c8-90e3-2c6d883f3a7c
description: GroupingInformation 元素包含一个值，该值用于对用户邮箱进行分组，以在订阅多个邮箱的通知时保持相关性。
ms.openlocfilehash: 14e751adcd0b966907ce495a2753b2b26d812a86
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59525882"
---
# <a name="groupinginformation-pox"></a>GroupingInformation (POX)

**GroupingInformation** 元素包含一个值，该值用于对用户邮箱进行分组，以在 [](https://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx)跨多个邮箱订阅通知时保持相关性。 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
[GroupingInformation (POX)](groupinginformation-pox.md)
  
```XML
<GroupingInformation/>
```

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Protocol (POX)](protocol-pox.md) <br/> |包含用于将客户端连接到 Exchange 服务器的规范。  <br/> |
   
## <a name="text-value"></a>文本值

文本值与其他邮箱的 **GroupingInformation** 元素的值进行比较。 可以将具有相同值并使用相同值Exchange EWS (EWS) 终结点的邮箱组合在一起以保持相关性。 有关更多详细信息，请参阅在订阅组中保持一组订阅与邮箱服务器之间的[关联Exchange。](https://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx)
  
## <a name="remarks"></a>注解

**GroupingInformation** 元素仅适用于 Type ([POX](type-pox.md)) 值为"EXPR"的子元素的 **Protocol** 元素。 
  
## <a name="see-also"></a>另请参阅

- [用于存储的 POX 自动发现 XML Exchange](pox-autodiscover-xml-elements-for-exchange.md)
- [在 Exchange 中保持一组订阅和邮箱服务器之间的相关性](https://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx)

