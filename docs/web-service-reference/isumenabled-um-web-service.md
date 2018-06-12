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
description: IsUMEnabled 元素指示是否将邮箱启用统一消息。
ms.openlocfilehash: 5f4d59c5497158e5afbc8bb5db4900bd129df50b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826113"
---
# <a name="isumenabled-um-web-service"></a>IsUMEnabled （UM web 服务）

**IsUMEnabled**元素指示是否将邮箱启用统一消息。 
  
```xml
<IsUMEnabled/>
```

 **Boolean**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

无。
  
## <a name="text-value"></a>文本值

如果此元素是包含，则需要一个文本值，它代表一个布尔值。 值为**true**指示邮箱启用统一消息。 如果值为**false**意味着邮箱未启用统一消息。 
  
## <a name="remarks"></a>备注

若要确定是否将邮箱启用统一消息，请使用[IsUMEnabled 操作 （UM web 服务）](isumenabled-operation-um-web-service.md)。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |邮件  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[IsUMEnabled 操作 （UM web 服务）](isumenabled-operation-um-web-service.md)


[Exchange 的统一的消息 web 服务 XML 元素](unified-messaging-web-service-xml-elements-for-exchange.md)

