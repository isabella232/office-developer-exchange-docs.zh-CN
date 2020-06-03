---
title: GroupIdentifier
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GroupIdentifier
api_type:
- schema
ms.assetid: bdc6fc1e-4979-42da-a35b-e3017988c7d3
description: GroupIdentifier 元素代表帐户所属的 Active Directory 目录服务对象组的单个安全标识符和属性。
ms.openlocfilehash: 8b427b9228cc5e66f46f70389acf2fa4bcd283b3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530801"
---
# <a name="groupidentifier"></a>GroupIdentifier

**GroupIdentifier**元素代表帐户所属的 Active Directory 目录服务对象组的单个安全标识符和属性。 
  
```xml
<GroupIdentifier>
   <SecurityIdentifier/>
</GroupIdentifier>
```

 **SidAndAttributesType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|**Attributes** <br/> |包含组属性。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[SecurityIdentifier](securityidentifier.md) <br/> |表示表示组的安全标识符（[SID](sid.md)）的安全描述符定义语言（SDDL）形式。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GroupSids](groupsids.md) <br/> |表示用于组成令牌序列化帐户令牌的 Active Directory 组对象安全标识符的集合。 不支持令牌序列化。  <br/> |
   
## <a name="remarks"></a>说明

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

