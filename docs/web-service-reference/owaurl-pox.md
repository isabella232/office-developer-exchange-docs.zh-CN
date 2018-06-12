---
title: OWAUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 450b86a1-1722-49f5-b541-16c1edc3db7a
description: OWAUrl 元素描述 URL 并用于访问特定的正在运行 Microsoft Exchange Server 2007 的计算机的身份验证架构了客户端访问服务器角色安装承载 Outlook Web Access。
ms.openlocfilehash: 93d03506e2a74aa1b4ef6d2a49ccbda01cfc1f9a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826673"
---
# <a name="owaurl-pox"></a>OWAUrl (POX)

**OWAUrl**元素描述 URL 并用于访问特定的正在运行 Microsoft Exchange Server 2007 的计算机的身份验证架构了客户端访问服务器角色安装承载 Outlook Web Access。 
  
[自动发现 (POX)](autodiscover-pox.md)
  
[响应 (POX)](response-pox.md)
  
[帐户 (POX)](account-pox.md)
  
[协议 (POX)](protocol-pox.md)
  
[内部 (POX)](internal-pox.md)
  
[OWAUrl (POX)](owaurl-pox.md)
  
```xml
<OWAUrl AuthenticationMethod=""/>
```

## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|**AuthenticationMethod** <br/> |介绍用于访问 Outlook Web Access 的身份验证方法。  <br/> |
   
#### <a name="authenticationmethod-attribute"></a>AuthenticationMethod 属性

|**值**|**说明**|
|:-----|:-----|
|WindowsIntegrated  <br/> |集成的 Windows 身份验证。  <br/> |
|FBA  <br/> |基于表单的身份验证。  <br/> |
|NTLM  <br/> |NTLM 身份验证。  <br/> |
|摘要式  <br/> |摘要式身份验证。  <br/> |
|基本  <br/> |基本身份验证。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[内部 (POX)](internal-pox.md) <br/> |包含客户端可以连接到内部防火墙时的 Outlook Web Access Url 的集合。  <br/> |
   
## <a name="text-value"></a>文本值

文本值表示的客户端访问服务器上的 Outlook Web Access 服务的 URL。
  
## <a name="see-also"></a>另请参阅



[Exchange POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

