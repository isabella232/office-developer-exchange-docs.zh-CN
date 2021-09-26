---
title: SerializedSecurityContext
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SerializedSecurityContext
api_type:
- schema
ms.assetid: a02c4fc1-ed1a-40d9-a18e-6cfdae21a690
description: SerializedSecurityContext 元素在 Simple Object Access Protocol (SOAP) 标头中用于服务器到服务器身份验证中的令牌序列化。 不支持令牌序列化。
ms.openlocfilehash: 55fe752813fc2d7e3ed5416401ff46b5e00516e3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546040"
---
# <a name="serializedsecuritycontext"></a>SerializedSecurityContext

**SerializedSecurityContext** 元素在 Simple Object Access Protocol (SOAP) 标头中用于服务器到服务器身份验证中的令牌序列化。 不支持令牌序列化。 
  
```xml
<SerializedSecurityContext>
   <UserSid/>
   <GroupSids/>
   <RestrictedGroupSids/>
   <PrimarySmtpAddress/>
</SerializedSecurityContext>
```

 **SerializedSecurityContextType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[UserSid](usersid.md) <br/> |表示序列化安全上下文 SOAP 标头 (用户) 形式的 SDDL 安全描述符定义语言。  <br/> |
|[GroupSids](groupsids.md) <br/> |表示 Active Directory 目录服务组对象安全标识符的集合。  <br/> |
|[RestrictedGroupSids](restrictedgroupsids.md) <br/> |表示受限组的组安全标识符和属性。  <br/> |
|[PrimarySmtpAddress](primarysmtpaddress.md) <br/> |表示要用于服务器到 () 的帐户的主简单邮件传输协议或 SMTP 地址。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>注解

描述此元素的架构位于运行安装了客户端访问服务器 (CAS) 角色的 Microsoft Exchange Server 2007 的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)


[EWS 中的服务器到服务器授权](https://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)

