---
title: 操作 (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a3462c6b-453c-462a-830d-f29ee4a2babb
description: Action 元素提供用于确定是否需要返回用户配置信息的另一个自动发现请求的信息。
ms.openlocfilehash: 118bb59f2c929e3c74683dbf3f073da34d67a3e7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754267"
---
# <a name="action-pox"></a>操作 (POX)

**Action**元素提供用于确定是否需要返回用户配置信息的另一个自动发现请求的信息。 
  
- [自动发现 (POX)](autodiscover-pox.md)
  
- [响应 (POX)](response-pox.md)
  
- [帐户 (POX)](account-pox.md)
  
- [操作 (POX)](action-pox.md)
  
```xml
<Action>redirectUrl or redirectAddr or settings</Action>
```

## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[帐户 (POX)](account-pox.md) <br/> |指定用户帐户的设置。  <br/> |
   
## <a name="text-value"></a>文本值

文本值表示另一个自动发现请求是否需要检索用户的配置信息。 下表列出了可能的值。
  
|**值**|**说明**|
|:-----|:-----|
|redirectUrl  <br/> |如果指定此值，则[RedirectUrl (POX)](redirecturl-pox.md)元素将指定在后续的自动发现请求中使用的客户端访问服务器 URL。 客户端应用程序应停止 10 次重定向后重定向。  <br/> |
|redirectAddr  <br/> |如果指定此值，则[RedirectAddr (POX)](redirectaddr-pox.md)元素将指定应用于后续的自动发现请求的电子邮件地址。  <br/> |
|settings  <br/> |如果指定此值，则自动发现响应中包含用于配置帐户的设置。 将[协议 (POX)](protocol-pox.md)元素中找到的大多数设置。  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

