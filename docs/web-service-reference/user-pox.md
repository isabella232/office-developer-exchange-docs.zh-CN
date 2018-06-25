---
title: 用户 (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 7c42b516-77f6-4aee-99d8-b866d82d793a
description: User 元素提供特定于用户的信息。
ms.openlocfilehash: 3f90ff0cc00170170c7304f2a19fe1d7abd9d1bc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838456"
---
# <a name="user-pox"></a>用户 (POX)

**User**元素提供特定于用户的信息。 
  
[自动发现 (POX)](autodiscover-pox.md)
  
[响应 (POX)](response-pox.md)
  
[用户 (POX)](user-pox.md)
  
```xml
<User>
   <DisplayName/>
   <LegacyDN/>
   <DeploymentId/>
   <AutoDiscoverSMTPAddress/>
</User>
```

## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[显示名称 (字符串)](displayname-string.md) <br/> |代表用户的显示名称。  <br/> |
|[LegacyDN (POX)](legacydn-pox.md) <br/> |通过旧的可分辨名称标识用户的邮箱。  <br/> |
|[DeploymentId (POX)](deploymentid-pox.md) <br/> |唯一标识 Exchange 林。  <br/> |
|[AutoDiscoverSMTPAddress (POX)](autodiscoversmtpaddress-pox.md) <br/> |包含用于自动发现过程的用户的 SMTP 地址。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[响应 (POX)](response-pox.md) <br/> |包含来自自动发现服务的响应。  <br/> |
   
## <a name="remarks"></a>注解

自动发现请求和响应必须为 utf-8 编码。
  
## <a name="see-also"></a>另请参阅



[Exchange POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

