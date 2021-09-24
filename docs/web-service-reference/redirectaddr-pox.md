---
title: RedirectAddr (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 0e9fa6b6-7991-4dc1-a59a-48e5f8e041e4
description: RedirectAddr 元素指定应用于后续自动发现请求的电子邮件地址。
ms.openlocfilehash: 75db62a84ccce743e73c812082ab9dbbc4fdb1cd
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540592"
---
# <a name="redirectaddr-pox"></a>RedirectAddr (POX)

**RedirectAddr** 元素指定应用于后续自动发现请求的电子邮件地址。 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[RedirectAddr (POX)](redirectaddr-pox.md)
  
```xml
<RedirectAddr/>
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

文本值表示应用于后续自动发现请求的电子邮件地址。
  
## <a name="remarks"></a>注解

如果此元素存在于自动发现响应中，则使用 **RedirectAddr** 元素的文本值提出另一个请求。 
  
## <a name="see-also"></a>另请参阅



[用于存储的 POX 自动发现 XML Exchange](pox-autodiscover-xml-elements-for-exchange.md)

