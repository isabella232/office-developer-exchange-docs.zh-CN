---
title: RedirectAddr （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 0e9fa6b6-7991-4dc1-a59a-48e5f8e041e4
description: RedirectAddr 元素指定应用于后续自动发现请求的电子邮件地址。
ms.openlocfilehash: 6bff28001851f421b4c7429770185401f2f0a743
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529873"
---
# <a name="redirectaddr-pox"></a>RedirectAddr （POX）

**RedirectAddr**元素指定应用于后续自动发现请求的电子邮件地址。 
  
[自动发现（POX）](autodiscover-pox.md)
  
[响应（POX）](response-pox.md)
  
[帐户（POX）](account-pox.md)
  
[RedirectAddr （POX）](redirectaddr-pox.md)
  
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
|[帐户（POX）](account-pox.md) <br/> |指定用户的帐户设置。  <br/> |
   
## <a name="text-value"></a>文本值

该文本值表示应用于后续自动发现请求的电子邮件地址。
  
## <a name="remarks"></a>备注

如果此元素存在于自动发现响应中，请使用**RedirectAddr**元素的文本值进行另一个请求。 
  
## <a name="see-also"></a>另请参阅



[Exchange 的 POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

