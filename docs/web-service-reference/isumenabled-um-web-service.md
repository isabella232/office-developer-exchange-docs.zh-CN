---
title: IsUMEnabled （UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- IsUMEnabled
api_type:
- schema
ms.assetid: 33810bbd-837f-4a71-9ed9-cb4b8c52186d
description: IsUMEnabled 元素指示是否为邮箱启用统一消息。
ms.openlocfilehash: ea5bde677c62664acad8afd5c8142e96d82b7a74
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458227"
---
# <a name="isumenabled-um-web-service"></a>IsUMEnabled （UM web 服务）

**IsUMEnabled**元素指示是否为邮箱启用统一消息。 
  
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

如果包含此元素，则需要一个表示布尔值的文本值。 **如果值为 true** ，则表示已为邮箱启用统一消息。 **如果值为 false** ，则表示没有为邮箱启用统一消息。 
  
## <a name="remarks"></a>备注

若要确定是否为统一消息启用了邮箱，请使用[IsUMEnabled 操作（UM web 服务）](isumenabled-operation-um-web-service.md)。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |邮件  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[IsUMEnabled 操作（UM web 服务）](isumenabled-operation-um-web-service.md)


[Exchange 的统一消息 web 服务 XML 元素](unified-messaging-web-service-xml-elements-for-exchange.md)

