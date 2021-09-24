---
title: IsUMEnabled（UM Web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- IsUMEnabled
api_type:
- schema
ms.assetid: 33810bbd-837f-4a71-9ed9-cb4b8c52186d
description: IsUMEnabled 元素指示邮箱是否启用了统一消息。
ms.openlocfilehash: 43632c28c5fb0c526dcf2ad936784953b00cc14a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524117"
---
# <a name="isumenabled-um-web-service"></a>IsUMEnabled（UM Web 服务）

**IsUMEnabled** 元素指示邮箱是否启用了统一消息。 
  
```xml
<IsUMEnabled/>
```

 **Boolean**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

无。
  
## <a name="text-value"></a>文本值

如果包含此元素，则代表布尔值的文本值是必需的。 值为 **true** 表示邮箱已启用统一消息。 false **值表示** 邮箱未启用统一消息。 
  
## <a name="remarks"></a>注解

若要确定是否为邮箱启用了统一消息，请使用 [IsUMEnabled ](isumenabled-operation-um-web-service.md)操作 (UM Web 服务) 。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[IsUMEnabled 操作（UM Web 服务）](isumenabled-operation-um-web-service.md)


[统一消息 Web 服务 XML 元素Exchange](unified-messaging-web-service-xml-elements-for-exchange.md)

