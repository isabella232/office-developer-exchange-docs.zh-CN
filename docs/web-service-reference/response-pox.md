---
title: Response (POX)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 002b72f2-f94d-467c-8e6c-b3818f7e51dc
description: 应用于：
ms.openlocfilehash: d613bbb1d8573c1eb60c053ddc064f564676a7c4
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523480"
---
# <a name="response-pox"></a>Response (POX)


  
**Response** 元素包含来自自动发现服务的响应。 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
```xml
<Response>
   <User/>
   <Account/>
</Response>
```

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[User (POX)](user-pox.md) <br/> |提供特定于用户的信息。 此元素为可选。  <br/> |
|[Account (POX)](account-pox.md) <br/> |指定用户的帐户设置。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[AutoDiscover (POX)](autodiscover-pox.md) <br/> |自动发现响应中的根元素。  <br/> |
   
## <a name="see-also"></a>另请参阅



[用于存储的 POX 自动发现 XML Exchange](pox-autodiscover-xml-elements-for-exchange.md)

