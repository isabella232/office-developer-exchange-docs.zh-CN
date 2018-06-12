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
description: SerializedSecurityContext 元素用于简单对象访问协议 (SOAP) 标头中令牌序列化的服务器到服务器身份验证。 不支持令牌序列化。
ms.openlocfilehash: c5590551dc0780d918b05902e4f48fb9d1390b59
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827363"
---
# <a name="serializedsecuritycontext"></a>SerializedSecurityContext

**SerializedSecurityContext**元素用于简单对象访问协议 (SOAP) 标头中令牌序列化的服务器到服务器身份验证。 不支持令牌序列化。 
  
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

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[UserSid](usersid.md) <br/> |代表安全描述符定义语言 (SDDL) 窗体的序列化的安全性上下文 SOAP 标头中的用户安全标识符。  <br/> |
|[GroupSids](groupsids.md) <br/> |代表 Active Directory 目录服务组对象安全标识符的集合。  <br/> |
|[RestrictedGroupSids](restrictedgroupsids.md) <br/> |表示组安全标识符和受限制的组的属性。  <br/> |
|[PrimarySmtpAddress](primarysmtpaddress.md) <br/> |代表要用于服务器到服务器授权的帐户的主要简单邮件传输协议 (SMTP) 地址。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>备注

描述此元素的架构位于运行 Microsoft Exchange Server 2007 的安装了客户端访问服务器 (CAS) 角色的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)


[EWS 中的服务器到服务器授权](http://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)

