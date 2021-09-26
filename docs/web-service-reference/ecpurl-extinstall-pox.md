---
title: EcpUrl-extinstall (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: f81807e6-93de-4e47-afee-1e1ae6a85054
description: EcpUrl-extinstall 元素指定可以与 EcpUrl (POX) 元素的值组合的部分 URL，以生成可用于查看或更改用户邮箱中当前安装的邮件应用程序的 URL。
ms.openlocfilehash: bf91b12cbcff3b08b3b13569eac9c957dea12757
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541418"
---
# <a name="ecpurl-extinstall-pox"></a>EcpUrl-extinstall (POX)

**EcpUrl-extinstall** 元素指定可以与 [EcpUrl (POX)](ecpurl-pox.md)元素的值组合的部分 URL，以生成可用于查看或更改用户邮箱中当前安装的邮件应用程序的 URL。 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
[EcpUrl-extinstall (POX)](ecpurl-extinstall-pox.md)
  
```XML
<EcpUrl-extinstall/>
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

文本值表示可以与 [EcpUrl (POX) ](ecpurl-pox.md) 元素的值组合的部分 URL，以生成可用于查看或更改当前安装在用户邮箱中的邮件应用程序的 URL。 
  
## <a name="remarks"></a>注解

**EcpUrl-extinstall** 元素是 Protocol 元素的可选 **子** 元素。 
  
## <a name="see-also"></a>另请参阅



[用于存储的 POX 自动发现 XML Exchange](pox-autodiscover-xml-elements-for-exchange.md)

