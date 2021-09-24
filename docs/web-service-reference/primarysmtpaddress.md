---
title: PrimarySmtpAddress
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PrimarySmtpAddress
api_type:
- schema
ms.assetid: eee79904-9412-4e61-b9b8-aff0ce25fade
description: PrimarySmtpAddress 元素表示要用于服务器到服务器授权或委派访问的帐户的主简单邮件传输协议 (SMTP) 地址。
ms.openlocfilehash: 7963fbc92de88b38da93e577ebd2c39dbedac009
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523872"
---
# <a name="primarysmtpaddress"></a>PrimarySmtpAddress

**PrimarySmtpAddress** 元素表示用于服务器到服务器授权或委派访问的帐户的主简单邮件传输协议 (SMTP) 地址。 
  
```xml
<PrimarySmtpAddress/>
```

 **PrimarySmtpAddressType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ConnectingSID](connectingsid.md) <br/> |表示在使用 ExchangeImpersonation SOAP 标头时要模拟的帐户。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/ExchangeImpersonation/ConnectingSID` <br/> |
|[SerializedSecurityContext](serializedsecuritycontext.md) <br/> |在 SOAP 标头中用于服务器到服务器身份验证中的令牌序列化。  <br/> |
|[UserId](userid.md) <br/> |标识委派用户或具有文件夹访问权限的用户。  <br/> |
   
## <a name="text-value"></a>文本值

需要一个代表 SMTP 地址的文本值。
  
## <a name="remarks"></a>注解

ExchangeWeb 服务要求邮箱由邮箱的主 SMTP 地址标识。 不接受代理地址或备用地址。
  
描述此元素的架构位于运行安装了客户端访问服务器角色的 Microsoft Exchange Server 2010 的计算机的 EWS 虚拟目录中。
  
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
  
[使用委派访问](https://msdn.microsoft.com/library/dfd6b4a3-8fd3-47ba-83c0-52465cb5f3f3%28Office.15%29.aspx)

