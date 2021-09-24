---
title: EcpUrl-tmHiding (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 9b9ae15b-3ac1-45ac-85ba-38c7231fe508
description: EcpUrl-tmHiding 元素指定一个部分 URL，该 URL 可以与 EcpUrl (POX) 元素的值结合使用，以生成可用于从网站邮箱取消订阅用户的 URL。
ms.openlocfilehash: d8e8ced554b96f1a0cd554d3d601970d5f47019b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514730"
---
# <a name="ecpurl-tmhiding-pox"></a>EcpUrl-tmHiding (POX)

**EcpUrl-tmHiding** 元素指定可以与 [EcpUrl (POX)](ecpurl-pox.md)元素的值组合的部分 URL，以生成可用于从网站邮箱取消订阅用户的 URL。 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
[EcpUrl-tmHiding (POX)](ecpurl-tmhiding-pox.md)
  
```XML
<EcpUrl-tmHiding/>
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

文本值表示可以与 [EcpUrl (POX) ](ecpurl-pox.md) 元素的值组合的部分 URL，以生成可用于从网站邮箱取消订阅用户的 URL。 **EcpUrl-tmHiding** 元素的值包含由客户端替代的"<"和">"字符中包含的参数，如下表所示。 
  
|**Parameter**|**替换为**|
|:-----|:-----|
| _Id_ <br/> |站点邮箱的 SMTP 电子邮件地址或 X500 可分辨名称。  <br/> |
   
## <a name="remarks"></a>注解

**EcpUrl-tmHiding** 元素是 Protocol 元素的可选 **子** 元素。 
  
## <a name="see-also"></a>另请参阅



[用于存储的 POX 自动发现 XML Exchange](pox-autodiscover-xml-elements-for-exchange.md)

