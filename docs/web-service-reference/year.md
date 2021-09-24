---
title: Year
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Year
api_type:
- schema
ms.assetid: 93bf2847-53fa-496c-9a1e-dc9a9ffd0b9f
description: Year 元素用于定义根据年份更改的时区。 此元素为可选。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: 80b4ce642a7a08631140e583fb9d92143f485ea3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59509278"
---
# <a name="year"></a>Year

**Year** 元素用于定义根据年份更改的时区。 此元素为可选。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。 
  
```xml
<Year/>
```

**string**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[StandardTime](standardtime.md) <br/> |表示相对于与协调世界时 (UTC) ，由 偏置 ([UTC ](bias-utc.md)) 元素的时间偏移。  <br/> |
|[DaylightTime](daylighttime.md) <br/> |表示相对于协调世界时 (UTC) 的时差，该时间由观测到夏令时的区域中的 [Bias (UTC) ](bias-utc.md) 元素表示。  <br/> |
   
## <a name="text-value"></a>文本值

Year 元素接受表示年份的字符串。 年格式为 YYYY。
  
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

