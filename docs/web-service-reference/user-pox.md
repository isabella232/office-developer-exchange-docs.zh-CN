---
title: User （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 7c42b516-77f6-4aee-99d8-b866d82d793a
description: User 元素提供用户特定的信息。
ms.openlocfilehash: 8f53319bcf34595305748adafc9aa1e25283611e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530216"
---
# <a name="user-pox"></a>User （POX）

**User**元素提供用户特定的信息。 
  
[自动发现（POX）](autodiscover-pox.md)
  
[响应（POX）](response-pox.md)
  
[User （POX）](user-pox.md)
  
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
|[LegacyDN （POX）](legacydn-pox.md) <br/> |通过旧版可分辨名称标识用户的邮箱。  <br/> |
|[DeploymentId （POX）](deploymentid-pox.md) <br/> |唯一标识 Exchange 林。  <br/> |
|[AutoDiscoverSMTPAddress （POX）](autodiscoversmtpaddress-pox.md) <br/> |包含用于自动发现过程的用户的 SMTP 地址。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[响应（POX）](response-pox.md) <br/> |包含来自自动发现服务的响应。  <br/> |
   
## <a name="remarks"></a>备注

自动发现请求和响应必须是 UTF-8 编码的。
  
## <a name="see-also"></a>另请参阅



[Exchange 的 POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

