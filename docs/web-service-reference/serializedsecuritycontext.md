---
title: SerializedSecurityContext
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SerializedSecurityContext
api_type:
- schema
ms.assetid: a02c4fc1-ed1a-40d9-a18e-6cfdae21a690
description: 在服务器到服务器身份验证中，在令牌序列化的简单对象访问协议（SOAP）头中使用 SerializedSecurityContext 元素。 不支持令牌序列化。
ms.openlocfilehash: 58fea1c7f613315d59e81935561f92f318afc769
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462050"
---
# <a name="serializedsecuritycontext"></a>SerializedSecurityContext

在服务器到服务器身份验证中，在令牌序列化的简单对象访问协议（SOAP）头中使用**SerializedSecurityContext**元素。 不支持令牌序列化。 
  
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
|[UserSid](usersid.md) <br/> |表示在序列化安全上下文 SOAP 标头中的用户安全标识符的安全描述符定义语言（SDDL）形式。  <br/> |
|[GroupSids](groupsids.md) <br/> |表示 Active Directory 目录服务组对象安全标识符的集合。  <br/> |
|[RestrictedGroupSids](restrictedgroupsids.md) <br/> |表示受限制的组的组安全标识符和属性。  <br/> |
|[PrimarySmtpAddress](primarysmtpaddress.md) <br/> |表示要用于服务器到服务器身份验证的帐户的主要简单邮件传输协议（SMTP）地址。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>说明

描述此元素的架构位于运行 Microsoft Exchange Server 2007 且安装了客户端访问服务器（CAS）角色的计算机的 EWS 虚拟目录中。
  
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

