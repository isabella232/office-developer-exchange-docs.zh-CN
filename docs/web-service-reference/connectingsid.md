---
title: ConnectingSID
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConnectingSID
api_type:
- schema
ms.assetid: 56d6aa52-8fa6-4773-9046-44a6f4f5d97c
description: ConnectingSID 元素表示在使用 ExchangeImpersonation SOAP 标头时要模拟的帐户。
ms.openlocfilehash: f4edf63f129fc769f4a2d710a505b40da4057fab
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459277"
---
# <a name="connectingsid"></a>ConnectingSID

**ConnectingSID**元素表示在使用 ExchangeImpersonation SOAP 标头时要模拟的帐户。 
  
- [ExchangeImpersonation](exchangeimpersonation.md) 
- [ConnectingSID](connectingsid.md)
  
```xml
<ConnectingSID>
   <PrincipalName/>
</ConnectingSID>
```

```xml
<ConnectingSID>
   <SmtpAddress/>
</ConnectingSID>
```

```xml
<ConnectingSID>
    <SID/> 
</ConnectingSID>
```

```xml
<ConnectingSID>
   <PrimarySmtpAddress/>
</ConnectingSID>
```

**ConnectingSIDType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[PrincipalName](principalname.md) <br/> |表示要用于模拟的帐户的用户主体名称（UPN）。 这应该是用户帐户所在域的 UPN。  <br/> |
|[SID](sid.md) <br/> |表示用于模拟的帐户的安全标识符（SID）的安全描述符定义语言（SDDL）形式。  <br/> |
|[PrimarySmtpAddress](primarysmtpaddress.md) <br/> |表示要用于 Exchange 模拟的帐户的主要简单邮件传输协议（SMTP）地址。 如果提供了主 SMTP 地址，则将花费额外的 Active Directory 目录服务查找，以便获取用户的 SID。 我们建议使用 SID 或 UPN （如果有）。  <br/> |
|[SmtpAddress](smtpaddress.md) <br/> |表示要用于 Exchange 模拟的帐户的简单邮件传输协议（SMTP）地址。 如果提供了 SMTP 地址，则将花费额外的 Active Directory 查找以获取用户的 SID。 我们建议使用 SID 或 UPN （如果有）。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ExchangeImpersonation](exchangeimpersonation.md) <br/> |在请求的 SOAP 标头中使用。 存在此元素时，调用方将尝试模拟**ExchangeImpersonation**元素中包含的帐户。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/ExchangeImpersonation` <br/> |
   
## <a name="remarks"></a>备注

如果邮箱数据库包含要模拟的邮箱或 Active Directory 用户或 contact 对象，则呼叫帐户必须在客户端访问服务器上和**ms-exch-MayImpersonate**权限中直接拥有**exch-模拟**权限。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [EWS 中的服务器到服务器授权](https://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)

