---
title: User (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 7c42b516-77f6-4aee-99d8-b866d82d793a
description: User 元素提供特定于用户的信息。
ms.openlocfilehash: 832e0a63e75a08406b3aa397ac29ad5aa300cfe0
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522403"
---
# <a name="user-pox"></a>User (POX)

**User** 元素提供特定于用户的信息。 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[User (POX)](user-pox.md)
  
```xml
<User>
   <DisplayName/>
   <LegacyDN/>
   <DeploymentId/>
   <AutoDiscoverSMTPAddress/>
</User>
```

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[显示名称 (字符串)](displayname-string.md) <br/> |表示用户的显示名称。  <br/> |
|[LegacyDN (POX)](legacydn-pox.md) <br/> |按旧版可分辨名称标识用户的邮箱。  <br/> |
|[DeploymentId (POX)](deploymentid-pox.md) <br/> |唯一标识Exchange林。  <br/> |
|[AutoDiscoverSMTPAddress (POX)](autodiscoversmtpaddress-pox.md) <br/> |包含用于自动发现过程的用户的 SMTP 地址。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Response (POX)](response-pox.md) <br/> |包含来自自动发现服务的响应。  <br/> |
   
## <a name="remarks"></a>注解

自动发现请求和响应必须经过 UTF-8 编码。
  
## <a name="see-also"></a>另请参阅



[用于存储的 POX 自动发现 XML Exchange](pox-autodiscover-xml-elements-for-exchange.md)

