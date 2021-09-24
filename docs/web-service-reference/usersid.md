---
title: UserSid
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- UserSid
api_type:
- schema
ms.assetid: f8a0dcd9-8564-4e35-b307-c5d2761b48d8
description: UserSid 元素表示序列化 (SOAP 标头) 用户安全标识符形式的 SDDL 安全描述符定义语言。 不支持令牌序列化。
ms.openlocfilehash: b32c9fc8347fba07bff57b942adf6510d37ebf2f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517348"
---
# <a name="usersid"></a>UserSid

**UserSid** 元素表示安全描述符定义语言 (序列化) SOAP 标头中的用户安全标识符形式的 SDDL 定义语言。 不支持令牌序列化。 
  
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
|[SerializedSecurityContext](serializedsecuritycontext.md) <br/> |在 SOAP 标头中用于服务器到服务器身份验证中的令牌序列化。  <br/> |
   
## <a name="text-value"></a>文本值

文本值表示用户的安全标识符。
  
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

