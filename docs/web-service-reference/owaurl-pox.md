---
title: OWAUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 450b86a1-1722-49f5-b541-16c1edc3db7a
description: OWAUrl 元素描述 URL 和身份验证架构，该架构用于访问运行 Microsoft Exchange Server 2007 且安装了客户端访问服务器角色且承载 Outlook Web Access 的特定计算机。
ms.openlocfilehash: fbd61eb75018c57dada40f5ed7472379d365e752
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59534889"
---
# <a name="owaurl-pox"></a>OWAUrl (POX)

**OWAUrl** 元素描述 URL 和身份验证架构，该架构用于访问运行 Microsoft Exchange Server 2007 的特定计算机，该计算机安装了承载 Outlook Web Access 的客户端访问服务器角色。 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
[Internal (POX)](internal-pox.md)
  
[OWAUrl (POX)](owaurl-pox.md)
  
```xml
<OWAUrl AuthenticationMethod=""/>
```

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**AuthenticationMethod** <br/> |介绍用于访问 Web Access Outlook方法。  <br/> |
   
#### <a name="authenticationmethod-attribute"></a>AuthenticationMethod 属性

|**值**|**说明**|
|:-----|:-----|
|WindowsIntegrated  <br/> |集成Windows身份验证。  <br/> |
|FBA  <br/> |基于表单的身份验证。  <br/> |
|NTLM  <br/> |NTLM 身份验证。  <br/> |
|摘要  <br/> |摘要式身份验证。  <br/> |
|基本  <br/> |基本身份验证。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Internal (POX)](internal-pox.md) <br/> |包含客户端Outlook防火墙内时可连接到的 Web Access URL 的集合。  <br/> |
   
## <a name="text-value"></a>文本值

文本值表示客户端访问Outlook Web Access 服务的 URL。
  
## <a name="see-also"></a>另请参阅



[用于存储的 POX 自动发现 XML Exchange](pox-autodiscover-xml-elements-for-exchange.md)

