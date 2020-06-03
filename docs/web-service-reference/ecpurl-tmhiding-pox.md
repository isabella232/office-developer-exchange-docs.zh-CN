---
title: EcpUrl-tmHiding （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b9ae15b-3ac1-45ac-85ba-38c7231fe508
description: EcpUrl-tmHiding 元素指定一个部分 URL，该 URL 可以与 EcpUrl （POX）元素的值结合使用，以生成可用于从网站邮箱取消订阅用户的 URL。
ms.openlocfilehash: 68b949db8b8d98caddbac3b9f96c5d5e55b104b7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463529"
---
# <a name="ecpurl-tmhiding-pox"></a>EcpUrl-tmHiding （POX）

**EcpUrl-tmHiding**元素指定一个部分 url，该 url 可以与[EcpUrl （POX）](ecpurl-pox.md)元素的值结合使用，以生成可用于从网站邮箱取消订阅用户的 URL。 
  
[自动发现（POX）](autodiscover-pox.md)
  
[响应（POX）](response-pox.md)
  
[帐户（POX）](account-pox.md)
  
[协议（POX）](protocol-pox.md)
  
[EcpUrl-tmHiding （POX）](ecpurl-tmhiding-pox.md)
  
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
|[协议（POX）](protocol-pox.md) <br/> |包含将客户端连接到运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的规范。  <br/> |
   
## <a name="text-value"></a>文本值

Text 值代表可与[EcpUrl （POX）](ecpurl-pox.md)元素的值结合使用的部分 url，以生成可用于从网站邮箱取消订阅用户的 URL。 **EcpUrl-tmHiding**元素的值包含在 "<" 和 ">" 字符中包含的参数，这些参数由客户端替换，如下表所示。 
  
|**参数**|**替换为**|
|:-----|:-----|
| _Id_ <br/> |网站邮箱的 SMTP 电子邮件地址或 X500 可分辨名称。  <br/> |
   
## <a name="remarks"></a>备注

**EcpUrl-tmHiding**元素是**Protocol**元素的可选子元素。 
  
## <a name="see-also"></a>另请参阅



[Exchange 的 POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

