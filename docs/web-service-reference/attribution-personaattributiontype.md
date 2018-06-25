---
title: 归属 (PersonaAttributionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dc59e17e-baea-4617-8ca1-4382a89de0d7
description: 属性元素指定实例 PersonaType 元素的属性数组中。
ms.openlocfilehash: 0e800c92c75bf0c475d4bffd33d6ab49f9ad9a9a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753291"
---
# <a name="attribution-personaattributiontype"></a>归属 (PersonaAttributionType)

**属性**元素指定实例**PersonaType**元素的属性数组中。 
  
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

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ID （字符串）](id-string.md) <br/> |指定一个唯一标识应用程序或在角色归属的字符串。  <br/> |
|[SourceId](sourceid.md) <br/> |指定的联系人或 Active Directory 收件人的标识符。  <br/> |
|[显示名称 (字符串)](displayname-string.md) <br/> |定义文件夹、 联系人、 通讯组列表、 代理用户或规则的显示名称。  <br/> |
|[IsWritable](iswritable.md) <br/> |指定是否可以向写入基础联系人或 Active Directory 收件人。  <br/> |
|[IsQuickContact](isquickcontact.md) <br/> |指定一个布尔值，指示快速联系人基础联系人或 Active Directory 收件人。  <br/> |
|[IsHidden](ishidden.md) <br/> |包含一个布尔值，该值指示是否应隐藏或显示该角色的一部分的基础联系人或 Active Directory 收件人。  <br/> |
|[文件夹 Id](folderid.md) <br/> |包含一个文件夹的标识符和更改键。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[归属 (ArrayOfPersonaAttributionsType)](attributions-arrayofpersonaattributionstype.md) <br/> |指定一个或多个联系人或聚合到相关联的角色的 active directory (AD) 收件人的归属信息的数组。  <br/> |
   
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |types.xsd  <br/> |
|可以为空  <br/> ||
   
## <a name="see-also"></a>另请参阅

- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

