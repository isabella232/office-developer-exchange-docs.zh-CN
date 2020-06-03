---
title: EcpUrl-tmEditing （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1fbc2ea9-3f94-441b-ab42-647326bf0021
description: EcpUrl-tmEditing 元素指定一个可与 EcpUrl （POX）元素的值结合使用的部分 URL，以生成可用于编辑现有网站邮箱的 URL。
ms.openlocfilehash: 5d6c6b8e8f73d113cfde3570065435927ffbae05
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463536"
---
# <a name="ecpurl-tmediting-pox"></a>EcpUrl-tmEditing （POX）

**EcpUrl-tmEditing**元素指定一个可与[EcpUrl （POX）](ecpurl-pox.md)元素的值结合使用的部分 url，以生成可用于编辑现有网站邮箱的 url。 
  
[自动发现（POX）](autodiscover-pox.md)
  
[响应（POX）](response-pox.md)
  
[帐户（POX）](account-pox.md)
  
[协议（POX）](protocol-pox.md)
  
[EcpUrl-tmEditing （POX）](ecpurl-tmediting-pox.md)
  
```XML
<EcpUrl-tmEditing/>
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

Text 值表示一个可与[EcpUrl （POX）](ecpurl-pox.md)元素的值结合使用的部分 url，以生成可用于编辑现有网站邮箱的 URL。 **EcpUrl-tmEditing**元素的值包含在 "<" 和 ">" 字符中包含的参数，这些参数由客户端替换，如下表所示。 
  
|**参数**|**替换为**|
|:-----|:-----|
| _Id_ <br/> |网站邮箱的 SMTP 电子邮件地址或 X500 可分辨名称。  <br/> |
   
## <a name="remarks"></a>备注

**EcpUrl-tmEditing**元素是**Protocol**元素的可选子元素。 
  
## <a name="see-also"></a>另请参阅



[Exchange 的 POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

