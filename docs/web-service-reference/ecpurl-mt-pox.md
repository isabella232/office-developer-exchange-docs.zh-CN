---
title: EcpUrl-mt (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 5221745b-572c-44a5-afdb-41b58af44971
description: EcpUrl-mt 元素指定一个部分 URL，该 URL 可以与 EcpUrl (POX) 元素的值结合使用，以生成可用于访问启用邮件的用户的电子邮件跟踪设置的 URL。
ms.openlocfilehash: bb0a60f3b3a2d65421164e40537e7514df20e357
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520813"
---
# <a name="ecpurl-mt-pox"></a>EcpUrl-mt (POX)

**EcpUrl-mt** 元素指定可以与 [EcpUrl (POX)](ecpurl-pox.md)元素的值组合的部分 URL，以生成可用于访问启用邮件的用户的电子邮件跟踪设置的 URL。 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
[EcpUrl-mt (POX)](ecpurl-mt-pox.md)
  
```XML
<EcpUrl-mt/>
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

文本值表示可以与 [EcpUrl (POX) ](ecpurl-pox.md) 元素的值组合的部分 URL，以生成可用于访问用户的电子邮件跟踪设置的 URL。 **EcpUrl-mt** 元素的值包含由客户端替代的"<"和">"字符中包含的参数，如下表所示。 
  
|**Parameter**|**替换为**|
|:-----|:-----|
| _IsOwa_ <br/> |n  <br/> |
| _MsgID_ <br/> |要跟踪的邮件的 Internet 邮件标识符（由 Message-ID 标头指定）。  <br/> |
| _Mbx_ <br/> |邮箱所有者的 SMTP 地址。  <br/> |
| _Sender_ <br/> |邮件发件人的 SMTP 地址。  <br/> |
   
## <a name="remarks"></a>注解

**EcpUrl-mt** 元素是 Protocol 元素的可选 **子** 元素。 
  
## <a name="see-also"></a>另请参阅



[用于存储的 POX 自动发现 XML Exchange](pox-autodiscover-xml-elements-for-exchange.md)

