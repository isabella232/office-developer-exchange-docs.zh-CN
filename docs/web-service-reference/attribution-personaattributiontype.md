---
title: Attribution (PersonaAttributionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: dc59e17e-baea-4617-8ca1-4382a89de0d7
description: Attribution 元素指定 PersonaType 元素的属性数组中的实例。
ms.openlocfilehash: eb2fe66042b6c7f52732be20195f0f4b94ab867c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524376"
---
# <a name="attribution-personaattributiontype"></a>Attribution (PersonaAttributionType)

**Attribution** 元素指定 **PersonaType** 元素的属性数组中的实例。 
  
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
|[ID (String)](id-string.md) <br/> |指定一个字符串，用于唯一标识应用或人物中的属性。  <br/> |
|[SourceId](sourceid.md) <br/> |指定联系人或 Active Directory 收件人的标识符。  <br/> |
|[显示名称 (字符串)](displayname-string.md) <br/> |定义显示名称、联系人、通讯组列表、代理用户或规则的名称。  <br/> |
|[IsWritable](iswritable.md) <br/> |指定是否可以将基础联系人或 Active Directory 收件人写入其中。  <br/> |
|[IsQuickContact](isquickcontact.md) <br/> |指定一个布尔值，该值指示基础联系人或 Active Directory 收件人是快速联系人。  <br/> |
|[IsHidden](ishidden.md) <br/> |包含一个布尔值，该值指示是隐藏基础联系人还是 Active Directory 收件人，或作为该人物的一部分显示。  <br/> |
|[FolderId](folderid.md) <br/> |包含一个文件夹的标识符和更改键。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Attributions (ArrayOfPersonaAttributionsType)](attributions-arrayofpersonaattributionstype.md) <br/> |指定聚合到关联人员中的一个或多个联系人或 active directory (AD) 属性信息数组。  <br/> |
   
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |types.xsd  <br/> |
|可以为空  <br/> ||
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

