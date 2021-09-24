---
title: ConnectingSID
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ConnectingSID
api_type:
- schema
ms.assetid: 56d6aa52-8fa6-4773-9046-44a6f4f5d97c
description: ConnectingSID 元素表示在使用 ExchangeImpersonation SOAP 标头时要模拟的帐户。
ms.openlocfilehash: 21cfcfc3590ea5a8b8ca5b53dfdb403e108e37f7
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515969"
---
# <a name="connectingsid"></a>ConnectingSID

**ConnectingSID** 元素表示在使用 ExchangeImpersonation SOAP 标头时要模拟的帐户。 
  
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
|[PrincipalName](principalname.md) <br/> |表示要用于模拟 (UPN) 的用户主体名称。 这应该是存在用户帐户的域的 UPN。  <br/> |
|[SID](sid.md) <br/> |表示安全描述符定义语言 (SDDL) 安全标识符 (SID) 形式供帐户用于模拟。  <br/> |
|[PrimarySmtpAddress](primarysmtpaddress.md) <br/> |表示要用于 () 简单邮件传输协议或 SMTP Exchange地址。 如果提供了主 SMTP 地址，它将花费额外的 Active Directory 目录服务查找，以获取用户的 SID。 我们建议你使用 SID 或 UPN（如果它们可用）。  <br/> |
|[SmtpAddress](smtpaddress.md) <br/> |表示要用于 (模拟) 简单邮件传输协议 SMTP Exchange地址。 如果提供了 SMTP 地址，它将花费额外的 Active Directory 查找，以获取用户的 SID。 我们建议你使用 SID 或 UPN（如果它们可用）。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ExchangeImpersonation](exchangeimpersonation.md) <br/> |在请求的 SOAP 标头中使用。 存在此元素时，呼叫者将尝试模拟 **包含在 ExchangeImpersonation** 元素中的帐户。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/ExchangeImpersonation` <br/> |
   
## <a name="remarks"></a>注解

调用帐户必须在客户端访问服务器上具有 **ms-exch-impersonation** 权限，并且 **ms-exch-MayImpersonate** 权限位于包含要模拟的邮箱的邮箱数据库上，或者 Active Directory 用户或联系人对象上。 
  
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

