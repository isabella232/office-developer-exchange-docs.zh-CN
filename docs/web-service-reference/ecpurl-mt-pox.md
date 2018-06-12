---
title: EcpUrl 黑 (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5221745b-572c-44a5-afdb-41b58af44971
description: EcpUrl 黑元素指定可以结合使用 EcpUrl (POX) 元素的值生成一个 URL，可用于访问电子邮件跟踪已启用邮件的用户设置的部分 URL。
ms.openlocfilehash: 13954a4dab8e81f4ba75b3578e6ba7f67f4b8b96
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754002"
---
# <a name="ecpurl-mt-pox"></a>EcpUrl 黑 (POX)

**EcpUrl 黑**元素指定可以结合使用[EcpUrl (POX)](ecpurl-pox.md)元素的值生成一个 URL，可用于访问电子邮件跟踪已启用邮件的用户设置的部分 URL。 
  
[自动发现 (POX)](autodiscover-pox.md)
  
[响应 (POX)](response-pox.md)
  
[帐户 (POX)](account-pox.md)
  
[协议 (POX)](protocol-pox.md)
  
[EcpUrl 黑 (POX)](ecpurl-mt-pox.md)
  
```XML
<EcpUrl-mt/>
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
|[协议 (POX)](protocol-pox.md) <br/> |包含客户端连接到运行 Microsoft Exchange Server 已安装了客户端访问服务器角色的计算机的规格。  <br/> |
   
## <a name="text-value"></a>文本值

文本值表示可以结合使用[EcpUrl (POX)](ecpurl-pox.md)元素的值生成一个 URL，可用于访问电子邮件跟踪的用户设置的部分 URL。 **EcpUrl 黑**元素的值包含参数中包含 < 和 > 下表中所示，客户端会替换的字符。 
  
|**参数**|**用替代**|
|:-----|:-----|
| _IsOwa_ <br/> |n  <br/> |
| _邮件 Id_ <br/> |Internet 消息标识符的邮件跟踪所指定的邮件 ID 标头。  <br/> |
| _Mbx_ <br/> |邮箱所有者的 SMTP 地址。  <br/> |
| _发件人_ <br/> |发件人 SMTP 地址。  <br/> |
   
## <a name="remarks"></a>备注

**EcpUrl 黑**元素是**协议**元素的可选子元素。 
  
## <a name="see-also"></a>另请参阅



[Exchange POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

