---
title: 内部 (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 69c22546-ebd6-4a03-b0b4-bbac72ec5551
description: 内部元素包含客户端可以使用连接到从 Exchange 组织的网络内的 Url 的集合。
ms.openlocfilehash: 0dc5b679af98b52f15ef3b40181c2d97f102f373
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825946"
---
# <a name="internal-pox"></a>内部 (POX)

**内部**元素包含客户端可以使用连接到从 Exchange 组织的网络内的 Url 的集合。 
  
[自动发现 (POX)](autodiscover-pox.md)
  
[响应 (POX)](response-pox.md)
  
[帐户 (POX)](account-pox.md)
  
[协议 (POX)](protocol-pox.md)
  
[内部 (POX)](internal-pox.md)
  
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

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[OWAUrl (POX)](owaurl-pox.md) <br/> |介绍 URL 并用于访问特定的正在运行 Microsoft Exchange Server 的计算机的身份验证架构了客户端访问服务器角色安装承载 Outlook Web Access。  <br/> |
|[协议 (POX)](protocol-pox.md) <br/> |包含客户端连接到运行 Microsoft Exchange Server 已安装了客户端访问服务器角色的计算机的规格。 此**协议**元素具有仅两个子元素： 指定的连接协议，[类型 (POX)](type-pox.md)元素和[ASUrl (POX)](asurl-pox.md)元素，指定的 EWS 终结点的可用性 web 服务。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[协议 (POX)](protocol-pox.md) <br/> |包含客户端连接到运行 Microsoft Exchange Server 已安装了客户端访问服务器角色的计算机的规格。  <br/> |
   
## <a name="remarks"></a>注解

**内部**元素是**协议**元素的可选子元素。 
  
## <a name="see-also"></a>另请参阅



[Exchange POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

