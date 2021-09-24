---
title: EcpUrl-tmEditing (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 1fbc2ea9-3f94-441b-ab42-647326bf0021
description: EcpUrl-tmEditing 元素指定一个部分 URL，该 URL 可以与 EcpUrl (POX) 元素的值结合使用，以生成可用于编辑现有网站邮箱的 URL。
ms.openlocfilehash: e615e8ae09c3a9422f753a71070917a41f40741b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59531090"
---
# <a name="ecpurl-tmediting-pox"></a>EcpUrl-tmEditing (POX)

**EcpUrl-tmEditing** 元素指定一个部分 URL，该 URL 可以与 [EcpUrl (POX)](ecpurl-pox.md)元素的值结合使用，以生成可用于编辑现有网站邮箱的 URL。 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
[EcpUrl-tmEditing (POX)](ecpurl-tmediting-pox.md)
  
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
|[Protocol (POX)](protocol-pox.md) <br/> |包含用于将客户端连接到运行已安装客户端访问服务器角色Microsoft Exchange Server的计算机的规范。  <br/> |
   
## <a name="text-value"></a>文本值

文本值表示可以与 [EcpUrl (POX) ](ecpurl-pox.md) 元素的值组合的部分 URL，以生成可用于编辑现有网站邮箱的 URL。 **EcpUrl-tmEditing** 元素的值包含"<"和">"字符中包含的参数，这些参数由客户端替代，如下表所示。 
  
|**Parameter**|**替换为**|
|:-----|:-----|
| _Id_ <br/> |站点邮箱的 SMTP 电子邮件地址或 X500 可分辨名称。  <br/> |
   
## <a name="remarks"></a>注解

**EcpUrl-tmEditing** 元素是 Protocol 元素的可选 **子** 元素。 
  
## <a name="see-also"></a>另请参阅



[用于存储的 POX 自动发现 XML Exchange](pox-autodiscover-xml-elements-for-exchange.md)

