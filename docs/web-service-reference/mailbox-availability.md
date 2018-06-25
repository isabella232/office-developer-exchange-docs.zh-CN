---
title: 邮箱 （可用性）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Mailbox
api_type:
- schema
ms.assetid: affd192e-8914-473f-9098-d9bdf898de2c
description: 邮箱元素表示 SetUserOofSettings 邮箱用户或 GetUserOofSettings 请求。
ms.openlocfilehash: 2e901ae0df56542f56f247184254294735018468
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826254"
---
# <a name="mailbox-availability"></a>邮箱 （可用性）

**邮箱**元素表示 SetUserOofSettings 邮箱用户或 GetUserOofSettings 请求。 
  
```xml
<Mailbox>
   <Name>...</Name>
   <Address>...</Address>
   <RoutingType>...</RoutingType>
</Mailbox>
```

**EmailAddressType**

## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[名称 （电子邮件地址）](name-emailaddress.md) <br/> |代表邮箱用户的显示名称。 此元素是在 SetUserOofSettingsRequest 可选的。 GetUserOofSettingsRequest 将返回此元素。  <br/> |
|[地址 （字符串）](address-string.md) <br/> |代表邮箱用户的电子邮件地址。 此元素是必需的。  <br/> |
|[RoutingType （电子邮件地址）](routingtype-emailaddress.md) <br/> |代表邮件路由的协议。 此元素是在 SetUserOofSettingsRequest 可选的。 GetUserOofSettingsRequest 将返回此元素。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetUserOofSettingsRequest](getuseroofsettingsrequest.md) <br/> |用于获取邮箱用户的外出 (OOF) 设置和消息。  <br/> 以下是此元素的 XPath 表达式：  <br/>  `/GetUserOofSettingsRequest` <br/> |
|[SetUserOofSettingsRequest](setuseroofsettingsrequest.md) <br/> |用于设置邮箱用户的 OOF 设置和消息。  <br/> 以下是此元素的 XPath 表达式：  <br/>  `/SetUserOofSettingsRequest` <br/> |
   
## <a name="remarks"></a>注解

电子邮件地址用于标识日历文件夹包含 OOF 设置。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [GetUserOofSettings 操作](getuseroofsettings-operation.md)
- [SetUserOofSettings 操作](setuseroofsettings-operation.md)

