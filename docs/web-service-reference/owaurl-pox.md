---
title: OWAUrl （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 450b86a1-1722-49f5-b541-16c1edc3db7a
description: OWAUrl 元素描述用于访问运行 Microsoft Exchange Server 2007 的特定计算机的 URL 和身份验证架构，该计算机安装了承载 Outlook Web Access 的客户端访问服务器角色。
ms.openlocfilehash: c0728af063cfbf1353eb7d3b81f5fcfe8b398f7d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457261"
---
# <a name="owaurl-pox"></a>OWAUrl （POX）

**OWAUrl**元素描述用于访问运行 Microsoft Exchange server 2007 的特定计算机的 URL 和身份验证架构，该计算机安装了承载 Outlook Web Access 的客户端访问服务器角色。 
  
[自动发现（POX）](autodiscover-pox.md)
  
[响应（POX）](response-pox.md)
  
[帐户（POX）](account-pox.md)
  
[协议（POX）](protocol-pox.md)
  
[Internal （POX）](internal-pox.md)
  
[OWAUrl （POX）](owaurl-pox.md)
  
```xml
<OWAUrl AuthenticationMethod=""/>
```

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**AuthenticationMethod** <br/> |介绍用于访问 Outlook Web Access 的身份验证方法。  <br/> |
   
#### <a name="authenticationmethod-attribute"></a>AuthenticationMethod 属性

|**值**|**说明**|
|:-----|:-----|
|WindowsIntegrated  <br/> |集成的 Windows 身份验证。  <br/> |
|FBA  <br/> |基于表单的身份验证。  <br/> |
|NTLM  <br/> |NTLM 身份验证。  <br/> |
|Digest  <br/> |摘要式身份验证。  <br/> |
|基本  <br/> |基本身份验证。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**描述**|
|:-----|:-----|
|[Internal （POX）](internal-pox.md) <br/> |包含当客户端在防火墙内部时可连接到的 Outlook Web Access Url 的集合。  <br/> |
   
## <a name="text-value"></a>文本值

该文本值表示客户端访问服务器上的 Outlook Web Access 服务的 URL。
  
## <a name="see-also"></a>另请参阅



[Exchange 的 POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

