---
title: Internal (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 69c22546-ebd6-4a03-b0b4-bbac72ec5551
description: Internal 元素包含一组 URL，客户端可以使用这些 URL Exchange组织网络内部的 URL。
ms.openlocfilehash: f87c5e21eff87965c9b6ff6f3d59e2b3a37b87f1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541117"
---
# <a name="internal-pox"></a>Internal (POX)

**Internal** 元素包含客户端可用于从组织网络Exchange内部连接到客户端的 URL 的集合。 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
[Internal (POX)](internal-pox.md)
  
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
|[OWAUrl (POX)](owaurl-pox.md) <br/> |介绍 URL 和身份验证架构，该架构用于访问运行 Microsoft Exchange Server安装了客户端访问服务器角色且承载 Web Access Outlook的计算机。  <br/> |
|[Protocol (POX)](protocol-pox.md) <br/> |包含用于将客户端连接到运行已安装客户端访问服务器角色Microsoft Exchange Server的计算机的规范。 此 **Protocol** 元素只有两个子元素：一个指定连接协议的 [Type (POX)](type-pox.md) 元素和一个指定可用性 Web 服务的 EWS 终结点的 [ASUrl (POX)](asurl-pox.md) 元素。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Protocol (POX)](protocol-pox.md) <br/> |包含用于将客户端连接到运行已安装客户端访问服务器角色Microsoft Exchange Server的计算机的规范。  <br/> |
   
## <a name="remarks"></a>注解

**Internal** 元素是 Protocol 元素的可选 **子** 元素。 
  
## <a name="see-also"></a>另请参阅



[用于存储的 POX 自动发现 XML Exchange](pox-autodiscover-xml-elements-for-exchange.md)

