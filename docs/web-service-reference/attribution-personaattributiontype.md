---
title: 归属（PersonaAttributionType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dc59e17e-baea-4617-8ca1-4382a89de0d7
description: 归属元素指定 PersonaType 元素的属性数组中的一个实例。
ms.openlocfilehash: 05b0d41c116f2ed7b8dbb3ac44108bb879256b5c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464173"
---
# <a name="attribution-personaattributiontype"></a>归属（PersonaAttributionType）

**归属**元素指定**PersonaType**元素的属性数组中的一个实例。 
  
```XML
<Attribution>
    <Id></Id>
    <SourceId></SourceId>
    <DisplayName></DisplayName>
    <IsWritable></IsWritable>
    <IsQuickContact></IsQuickContact>
    <IsHidden></IsHidden>
    <FolderId></FolderId>
</Attribution>
```

 **PersonaAttributionType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ID （字符串）](id-string.md) <br/> |指定一个唯一标识某一角色中的应用程序或某个特性的字符串。  <br/> |
|[SourceId](sourceid.md) <br/> |指定联系人或 Active Directory 收件人的标识符。  <br/> |
|[显示名称 (字符串)](displayname-string.md) <br/> |定义文件夹、联系人、通讯组列表、代理用户或规则的显示名称。  <br/> |
|[IsWritable](iswritable.md) <br/> |指定基础联系人或 Active Directory 收件人是否可以写入。  <br/> |
|[IsQuickContact](isquickcontact.md) <br/> |指定一个布尔值，该值指示基础联系人或 Active Directory 收件人是否为快速联系人。  <br/> |
|[IsHidden](ishidden.md) <br/> |包含一个布尔值，该值指示是否应隐藏基础联系人或 Active Directory 收件人，或将其作为角色的一部分显示。  <br/> |
|[FolderId](folderid.md) <br/> |包含一个文件夹的标识符和更改键。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[归属（ArrayOfPersonaAttributionsType）](attributions-arrayofpersonaattributionstype.md) <br/> |为聚合到关联角色中的一个或多个联系人或 active directory （AD）收件人指定归属信息的数组。  <br/> |
   
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |类型 .xsd  <br/> |
|可以为空  <br/> ||
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

