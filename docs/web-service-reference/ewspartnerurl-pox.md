---
title: EwsPartnerUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 2ebae21c-3efa-4239-9b49-4a3a8871449b
description: EwsPartnerUrl 元素为启用邮件的用户指定 Exchange Web 服务 (EWS) 的最佳终结点实例的 URL。
ms.openlocfilehash: 88ee0abdc5b8db09a938fc5fdba717a166b42399
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524320"
---
# <a name="ewspartnerurl-pox"></a>EwsPartnerUrl (POX)

**EwsPartnerUrl** 元素为启用邮件的用户指定 Exchange Web 服务 (EWS) 的最佳终结点实例的 URL。 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
[EwsPartnerUrl (POX)](ewspartnerurl-pox.md)
  
```XML
<EwsPartnerUrl/>
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
|[Protocol (POX)](protocol-pox.md) <br/> |包含用于将客户端连接到运行已安装客户端访问服务器角色Microsoft Exchange Server的计算机的规范。  <br/> |
   
## <a name="text-value"></a>文本值

文本值表示用户的 EWS 终结点的 URL。
  
## <a name="remarks"></a>注解

**EwsPartnerUrl** 元素是 Protocol 元素的可选 **子** 元素。 它相当于 [EwsUrl (POX) ](ewsurl-pox.md) 元素。 
  
## <a name="see-also"></a>另请参阅



[用于存储的 POX 自动发现 XML Exchange](pox-autodiscover-xml-elements-for-exchange.md)

