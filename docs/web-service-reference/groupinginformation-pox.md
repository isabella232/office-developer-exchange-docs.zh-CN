---
title: GroupingInformation (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d8a007f-d79c-43c8-90e3-2c6d883f3a7c
description: GroupingInformation 元素包含一个值，用于组跨多个邮箱订阅通知时保持关联的用户的邮箱。
ms.openlocfilehash: bcde002c794ac79d9515befc0755c1f954ee8706
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825781"
---
# <a name="groupinginformation-pox"></a>GroupingInformation (POX)

**GroupingInformation**元素包含一个值，用于跨多个邮箱订阅通知时组[维护关联](http://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx)的用户的邮箱。 
  
[自动发现 (POX)](autodiscover-pox.md)
  
[响应 (POX)](response-pox.md)
  
[帐户 (POX)](account-pox.md)
  
[协议 (POX)](protocol-pox.md)
  
[GroupingInformation (POX)](groupinginformation-pox.md)
  
```XML
<GroupingInformation/>
```

## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[协议 (POX)](protocol-pox.md) <br/> |包含客户端连接到 Exchange 服务器的规范。  <br/> |
   
## <a name="text-value"></a>文本值

其他邮箱的**GroupingInformation**元素的值进行比较的文本值。 具有相同的值，并使用相同的 Exchange Web Services (EWS) 终点的邮箱的组合可以在一起，以维护关联。 有关详细信息，请参阅[在 Exchange 维护一组订阅和邮箱服务器之间的关联](http://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx)。
  
## <a name="remarks"></a>注解

**GroupingInformation**元素仅适用于具有[类型 (POX)](type-pox.md)子元素的值为"EXPR"的**协议**元素。 
  
## <a name="see-also"></a>另请参阅

- [Exchange POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)
- [在 Exchange 维护一组订阅和邮箱服务器之间的关联](http://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx)

