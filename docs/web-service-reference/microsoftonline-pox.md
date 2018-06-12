---
title: MicrosoftOnline (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0b88f02a-9c50-44b3-841b-560b24e37af5
description: MicrosoftOnline 元素包含一个值，指示是否在用户邮箱位于 Exchange Online 或 Exchange Online 作为 Office 365 的一部分。
ms.openlocfilehash: b952bfda17b30dcf29812697d225db32718d9781
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826458"
---
# <a name="microsoftonline-pox"></a>MicrosoftOnline (POX)

**MicrosoftOnline**元素包含一个值，指示是否在用户邮箱位于 Exchange Online 或 Exchange Online 作为 Office 365 的一部分。 
  
[自动发现 (POX)](autodiscover-pox.md)
  
[响应 (POX)](response-pox.md)
  
[帐户 (POX)](account-pox.md)
  
[MicrosoftOnline (POX)](microsoftonline-pox.md)
  
```XML
<MicrosoftOnline/>
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
|[帐户 (POX)](account-pox.md) <br/> |指定用户帐户设置，或包含错误响应。  <br/> |
   
## <a name="remarks"></a>备注

文本值指示是否在用户邮箱位于 Exchange Online 中。 值是**true**如果用户的邮箱位于承载在 Exchange Online;否则为**false**。
  
## <a name="see-also"></a>另请参阅



[Exchange POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

