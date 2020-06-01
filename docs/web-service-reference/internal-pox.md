---
title: Internal （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 69c22546-ebd6-4a03-b0b4-bbac72ec5551
description: Internal 元素包含客户端可用于从组织的网络内部连接到 Exchange 的 Url 的集合。
ms.openlocfilehash: 8164a018a11f9bae9c3abcbfebf6cf0694ca4183
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465595"
---
# <a name="internal-pox"></a>Internal （POX）

**Internal**元素包含客户端可用于从组织的网络内部连接到 Exchange 的 url 的集合。 
  
[自动发现（POX）](autodiscover-pox.md)
  
[响应（POX）](response-pox.md)
  
[帐户（POX）](account-pox.md)
  
[协议（POX）](protocol-pox.md)
  
[Internal （POX）](internal-pox.md)
  
```xml
<Internal>
   <OWAUrl/>
   <Protocol>
      <Type/>
      <ASUrl/>
   </Protocol>
</Internal>
```

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[OWAUrl （POX）](owaurl-pox.md) <br/> |介绍用于访问运行 Microsoft Exchange Server 的特定计算机的 URL 和身份验证架构，该计算机安装了承载 Outlook Web Access 的客户端访问服务器角色。  <br/> |
|[协议（POX）](protocol-pox.md) <br/> |包含将客户端连接到运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的规范。 此**协议**元素只有两个子元素：一个指定连接协议的[类型（POX）](type-pox.md)元素和一个[ASUrl （POX）](asurl-pox.md)元素，指定了可用性 web 服务的 EWS 终结点。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[协议（POX）](protocol-pox.md) <br/> |包含将客户端连接到运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的规范。  <br/> |
   
## <a name="remarks"></a>备注

**Internal**元素是**Protocol**元素的可选子元素。 
  
## <a name="see-also"></a>另请参阅



[Exchange 的 POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

