---
title: Mailbox (Availability)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Mailbox
api_type:
- schema
ms.assetid: affd192e-8914-473f-9098-d9bdf898de2c
description: Mailbox 元素表示 SetUserOofSettings 或 GetUserOofSettings 请求的邮箱用户。
ms.openlocfilehash: 5e32c4be807dae92b27df7012caa8eb1b295b26c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522920"
---
# <a name="mailbox-availability"></a>Mailbox (Availability)

Mailbox 元素表示 SetUserOofSettings 或 GetUserOofSettings 请求的邮箱用户。 
  
```xml
<Mailbox>
   <Name>...</Name>
   <Address>...</Address>
   <RoutingType>...</RoutingType>
</Mailbox>
```

**EmailAddressType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Name (EmailAddress)](name-emailaddress.md) <br/> |表示显示名称的用户的邮箱。 此元素在 SetUserOofSettingsRequest 中是可选的。 GetUserOofSettingsRequest 将返回此元素。  <br/> |
|[Address (string)](address-string.md) <br/> |表示邮箱用户的电子邮件地址。 此元素是必需的。  <br/> |
|[RoutingType (EmailAddress)](routingtype-emailaddress.md) <br/> |表示邮件的路由协议。 此元素在 SetUserOofSettingsRequest 中是可选的。 GetUserOofSettingsRequest 将返回此元素。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetUserOofSettingsRequest](getuseroofsettingsrequest.md) <br/> |用于获取邮箱用户的外出 OOF Office (设置) 邮件。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/GetUserOofSettingsRequest` <br/> |
|[SetUserOofSettingsRequest](setuseroofsettingsrequest.md) <br/> |用于设置邮箱用户的 OOF 设置和邮件。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/SetUserOofSettingsRequest` <br/> |
   
## <a name="remarks"></a>注解

电子邮件地址用于标识包含 OOF 设置的日历文件夹。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [GetUserOofSettings 操作](getuseroofsettings-operation.md)
- [SetUserOofSettings 操作](setuseroofsettings-operation.md)

