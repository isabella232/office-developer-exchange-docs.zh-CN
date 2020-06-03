---
title: GroupingInformation （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d8a007f-d79c-43c8-90e3-2c6d883f3a7c
description: GroupingInformation 元素包含一个值，用于对用户的邮箱进行分组，以便在通过多个邮箱订阅通知时保持相关性。
ms.openlocfilehash: 7cab5d68f7dd5ec1f6caded5b9da6cfee03f3a67
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530076"
---
# <a name="groupinginformation-pox"></a>GroupingInformation （POX）

**GroupingInformation**元素包含一个值，用于对用户的邮箱进行分组，以便在通过多个邮箱订阅通知时[保持相关性](https://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx)。 
  
[自动发现（POX）](autodiscover-pox.md)
  
[响应（POX）](response-pox.md)
  
[帐户（POX）](account-pox.md)
  
[协议（POX）](protocol-pox.md)
  
[GroupingInformation （POX）](groupinginformation-pox.md)
  
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
|[协议（POX）](protocol-pox.md) <br/> |包含用于将客户端连接到 Exchange 服务器的规范。  <br/> |
   
## <a name="text-value"></a>文本值

将文本值与其他邮箱的**GroupingInformation**元素的值进行比较。 具有相同值并使用相同的 Exchange Web 服务（EWS）终结点的邮箱可以组合在一起以保持相关性。 有关更多详细信息，请参阅[维护 Exchange 中的一组订阅和邮箱服务器之间的相关性](https://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx)。
  
## <a name="remarks"></a>备注

**GroupingInformation**元素仅适用于具有值为 "EXPR" 的[类型（POX）](type-pox.md)子元素的**协议**元素。 
  
## <a name="see-also"></a>另请参阅

- [Exchange 的 POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)
- [维护 Exchange 中的一组订阅和邮箱服务器之间的相关性](https://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx)

