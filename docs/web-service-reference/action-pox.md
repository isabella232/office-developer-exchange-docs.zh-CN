---
title: Action (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: a3462c6b-453c-462a-830d-f29ee4a2babb
description: Action 元素提供用于确定是否需要其他自动发现请求才能返回用户配置信息的信息。
ms.openlocfilehash: b1c07fefc6b8033b9b93bd044c04fb07ba289177
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513855"
---
# <a name="action-pox"></a>Action (POX)

**Action** 元素提供用于确定是否需要其他自动发现请求才能返回用户配置信息的信息。 
  
- [AutoDiscover (POX)](autodiscover-pox.md)
  
- [Response (POX)](response-pox.md)
  
- [Account (POX)](account-pox.md)
  
- [Action (POX)](action-pox.md)
  
```xml
<Action>redirectUrl or redirectAddr or settings</Action>
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
|[Account (POX)](account-pox.md) <br/> |指定用户的帐户设置。  <br/> |
   
## <a name="text-value"></a>文本值

文本值表示是否需要其他自动发现请求来检索用户的配置信息。 下表列出了可能的值。
  
|**值**|**说明**|
|:-----|:-----|
|redirectUrl  <br/> |如果指定此值，则 RedirectUrl ([POX) ](redirecturl-pox.md) 元素将指定在后续自动发现请求中使用的客户端访问服务器 URL。 客户端应用程序应在 10 次重定向后停止重定向。  <br/> |
|redirectAddr  <br/> |如果指定此值， [则 REDIRECTAddr ](redirectaddr-pox.md) (POX) 元素将指定应该用于后续自动发现请求的电子邮件地址。  <br/> |
|设置  <br/> |如果指定此值，则自动发现响应将包含用于配置帐户的设置。 大部分设置将位于 Protocol ([POX) ](protocol-pox.md) 元素中。  <br/> |
   
## <a name="see-also"></a>另请参阅

- [用于存储的 POX 自动发现 XML Exchange](pox-autodiscover-xml-elements-for-exchange.md)

