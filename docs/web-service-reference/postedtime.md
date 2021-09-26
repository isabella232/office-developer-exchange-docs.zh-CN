---
title: PostedTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PostedTime
api_type:
- schema
ms.assetid: e8b3813c-fc7e-4674-a4c6-6818c13d2bcf
description: PostedTime 元素表示发布 PostItem 的时间。 此元素是只读的。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: 9aba5d0c8fad521e54ee4c8f9d877d17607d0dd0
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543105"
---
# <a name="postedtime"></a>PostedTime

**PostedTime** 元素表示发布 [PostItem](postitem.md)的时间。 此元素是只读的。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。 
  
```xml
<PostedTime/>
```

 **dateTime**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[PostItem](postitem.md) <br/> |代表应用商店中的一Exchange PostItem。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
   
## <a name="text-value"></a>文本值

文本值是一个 dateTime，表示 **发布 PostItem** 的时间。 此属性是只读的。 
  
## <a name="remarks"></a>说明

描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

