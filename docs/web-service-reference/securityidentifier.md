---
title: SecurityIdentifier
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SecurityIdentifier
api_type:
- schema
ms.assetid: f7656729-f2c9-41cc-b1ec-60f480fc4dab
description: SecurityIdentifier 元素表示安全描述符定义语言 (SDDL) SID (形式) 。
ms.openlocfilehash: 803c8c0efae1ccd6356d9ce3b5aa85e1d86aa565
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521594"
---
# <a name="securityidentifier"></a>SecurityIdentifier

**SecurityIdentifier** 元素表示安全描述符定义语言 (SDDL) SID ([形式的 SDDL](sid.md)) 。
  
```xml
<SecurityIdentifier/>
```

 **string**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GroupIdentifier](groupidentifier.md) <br/> |表示帐户是其中一个成员的 Active Directory 对象组的单个安全标识符和属性。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/SerializedSecurityContext/GroupSids/GroupIdentifier[i]` <br/> |
|[RestrictedGroupIdentifier](restrictedgroupidentifier.md) <br/> |表示用户令牌中受限组的组安全标识符和属性。  <br/> |
   
## <a name="remarks"></a>注解

此元素用于 Simple Object Access Protocol (SOAP) 标头。
  
描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

