---
title: UserSid
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UserSid
api_type:
- schema
ms.assetid: f8a0dcd9-8564-4e35-b307-c5d2761b48d8
description: UserSid 元素表示序列化安全上下文 SOAP 标头中的用户安全标识符的安全描述符定义语言（SDDL）形式。 不支持令牌序列化。
ms.openlocfilehash: b8ee51b1998546fc4ab14bd3666192ae63c8dba8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462015"
---
# <a name="usersid"></a>UserSid

**UserSid**元素表示序列化安全上下文 SOAP 标头中的用户安全标识符的安全描述符定义语言（SDDL）形式。 不支持令牌序列化。 
  
```xml
<UserSid/>
```

 **String**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[SerializedSecurityContext](serializedsecuritycontext.md) <br/> |在服务器到服务器身份验证中用于令牌序列化的 SOAP 标头中使用。  <br/> |
   
## <a name="text-value"></a>文本值

该文本值代表用户的安全标识符。
  
## <a name="remarks"></a>说明

描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

