---
title: EcpUrl tmHiding (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b9ae15b-3ac1-45ac-85ba-38c7231fe508
description: EcpUrl tmHiding 元素指定可以结合使用 EcpUrl (POX) 元素的值生成一个 URL，可用来取消订阅的站点邮箱用户的部分 URL。
ms.openlocfilehash: 461e9780dbd657ba0ba8b9ce9ea4fe902cba9698
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754016"
---
# <a name="ecpurl-tmhiding-pox"></a>EcpUrl tmHiding (POX)

**EcpUrl tmHiding**元素指定可以结合使用[EcpUrl (POX)](ecpurl-pox.md)元素的值生成一个 URL，可用来取消订阅的站点邮箱用户的部分 URL。 
  
[自动发现 (POX)](autodiscover-pox.md)
  
[响应 (POX)](response-pox.md)
  
[帐户 (POX)](account-pox.md)
  
[协议 (POX)](protocol-pox.md)
  
[EcpUrl tmHiding (POX)](ecpurl-tmhiding-pox.md)
  
```XML
<EcpUrl-tmHiding/>
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

文本值表示可以结合使用[EcpUrl (POX)](ecpurl-pox.md)元素的值生成一个 URL，可用来取消订阅的站点邮箱用户的部分 URL。 **EcpUrl tmHiding**元素的值包含参数中包含 < 和 > 下表中所示，客户端会替换的字符。 
  
|**参数**|**用替代**|
|:-----|:-----|
| 
  _Id_ <br/> |SMTP 电子邮件地址或 X500 可分辨名称的站点邮箱。  <br/> |
   
## <a name="remarks"></a>注解

**EcpUrl tmHiding**元素是**协议**元素的可选子元素。 
  
## <a name="see-also"></a>另请参阅



[Exchange POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

