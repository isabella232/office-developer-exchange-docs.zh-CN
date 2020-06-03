---
title: EcpUrl-extinstall （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f81807e6-93de-4e47-afee-1e1ae6a85054
description: EcpUrl-extinstall 元素指定一个部分 URL，该 URL 可以与 EcpUrl （POX）元素的值结合使用，以生成可用于查看或更改当前安装在用户邮箱中的邮件应用程序的 URL。
ms.openlocfilehash: 889e0ca3bdcdce4b557fe066db2918fde4abaa9b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461301"
---
# <a name="ecpurl-extinstall-pox"></a>EcpUrl-extinstall （POX）

**EcpUrl-extinstall**元素指定一个部分 url，该 url 可以与[EcpUrl （POX）](ecpurl-pox.md)元素的值结合使用，以生成可用于查看或更改当前安装在用户邮箱中的邮件应用程序的 url。 
  
[自动发现（POX）](autodiscover-pox.md)
  
[响应（POX）](response-pox.md)
  
[帐户（POX）](account-pox.md)
  
[协议（POX）](protocol-pox.md)
  
[EcpUrl-extinstall （POX）](ecpurl-extinstall-pox.md)
  
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
|[协议（POX）](protocol-pox.md) <br/> |包含将客户端连接到运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的规范。  <br/> |
   
## <a name="text-value"></a>文本值

Text 值代表可与[EcpUrl （POX）](ecpurl-pox.md)元素的值结合使用的部分 url，以生成可用于查看或更改当前安装在用户邮箱中的邮件应用程序的 url。 
  
## <a name="remarks"></a>备注

**EcpUrl-extinstall**元素是**Protocol**元素的可选子元素。 
  
## <a name="see-also"></a>另请参阅



[Exchange 的 POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

