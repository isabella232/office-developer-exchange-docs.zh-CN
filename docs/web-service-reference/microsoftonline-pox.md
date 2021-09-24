---
title: MicrosoftOnline (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 0b88f02a-9c50-44b3-841b-560b24e37af5
description: MicrosoftOnline 元素包含一个值，该值指示用户的邮箱是托管在 Exchange Online 中Exchange Online还是作为 Office 365 的一Office 365。
ms.openlocfilehash: fbf230df18ca488babb1523cc7f689923eaeb55b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510943"
---
# <a name="microsoftonline-pox"></a>MicrosoftOnline (POX)

**MicrosoftOnline** 元素包含一个值，该值指示用户的邮箱是托管在 Exchange Online 中Exchange Online还是作为 Office 365 的一Office 365。 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[MicrosoftOnline (POX)](microsoftonline-pox.md)
  
```XML
<MicrosoftOnline/>
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
|[Account (POX)](account-pox.md) <br/> |指定用户的帐户设置或包含错误响应。  <br/> |
   
## <a name="remarks"></a>注解

文本值指示用户的邮箱是否托管在 Exchange Online。 如果用户的邮箱托管在邮箱中，则值为 **true;** 如果用户的邮箱位于 Exchange Online;否则为 **false**。
  
## <a name="see-also"></a>另请参阅



[用于存储的 POX 自动发现 XML Exchange](pox-autodiscover-xml-elements-for-exchange.md)

