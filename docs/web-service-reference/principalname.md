---
title: PrincipalName
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PrincipalName
api_type:
- schema
ms.assetid: 88c142d4-0bc7-43ea-a997-d7200664d900
description: PrincipalName 元素表示要用于 (帐户 (UPN) 用户主体Exchange名称。
ms.openlocfilehash: f3cc23b1cab69e166b59d7c358f663772e71ea09
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543014"
---
# <a name="principalname"></a>PrincipalName

**PrincipalName** 元素表示要用于 (模拟) 帐户的用户主体名称EXCHANGE UPN。 
  
```xml
<PrincipalName/>
```

 **PrincipalNameType**
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
   
## <a name="text-value"></a>文本值

文本值表示用户的 UPN。 此值存在于 Active Directory 目录服务中的用户对象上。 其中包含用户登录名和用于标识用户帐户所在的域的域名，格式如下：  `someone@example.com` 。
  
## <a name="remarks"></a>注解

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

