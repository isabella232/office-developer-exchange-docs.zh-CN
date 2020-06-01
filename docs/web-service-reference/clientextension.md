---
title: ClientExtension
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3445ef2b-1bb1-43ea-bc93-85c72401e5b6
description: ClientExtension 元素包含有关应用程序的用户和配置信息。
ms.openlocfilehash: d3d9ce1d242a63f28da3464f0faff86abde502c9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460195"
---
# <a name="clientextension"></a>ClientExtension

**ClientExtension**元素包含有关应用程序的用户和配置信息。 
  
```XML
<ClientExtension IsAvailable=" true | false " IsMandatory=" true | false " IsEnabledByDefault=" true | false " Type="" Scope="" MarketplaceAssetId="" MarketplaceContentMarket="" AppStatus="" Etoken="">
    <SpecificUsers></SpecificUsers>
    <Manifest></Manifest>
</ClientExtension>
```

 **ClientExtensionType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|IsAvailable  <br/> |指定应用程序是否可用。 **IsAvailable**属性的文本值为**true**表示应用程序可用。 **如果值为 false** ，则表示应用程序不可用。 此特性是可选的。  <br/> |
|IsMandatory  <br/> |指定应用程序是否是必需的。 **IsMandatory**属性的文本值为**true**表示该应用程序对邮箱是必需的。 **如果值为 false** ，则表示应用程序不是强制性的。 此特性是可选的。  <br/> |
|IsEnabledByDefault  <br/> |指定是否在默认情况下启用应用程序。 **IsEnabledByDefault**属性的文本值为**true**表示应用程序在默认情况下处于启用状态。 **如果值为 false** ，则表示应用程序默认情况下不启用。 此特性是可选的。  <br/> |
|ProvidedTo  <br/> |指定向其提供应用程序的人员。 此特性是可选的。  <br/> |
|类型  <br/> |指定应用程序的类型。  <br/> |
|范围  <br/> |指定应用程序的范围。  <br/> |
|MarketplaceAssetId  <br/> |指定应用程序的市场资产标识符。  <br/> |
|MarketplaceContentMarket  <br/> |指定用户查看的有关应用程序的详细信息和评论的市场内容。  <br/> |
|AppStatus  <br/> |指定邮件应用程序处于意外状态时的状态代码。  <br/> |
|Etoken  <br/> |指定付费或试用邮件应用程序的许可证令牌。  <br/> |
   
#### <a name="type"></a>类型

|**值**|**说明**|
|:-----|:-----|
|默认  <br/> |指示应用程序在默认情况下可用。  <br/> |
|Private  <br/> |指示应用程序是私有的。  <br/> |
|市场  <br/> |指示应用程序是市场应用程序。  <br/> |
   
#### <a name="scope"></a>范围

|**值**|**说明**|
|:-----|:-----|
|无  <br/> |指示应用程序没有作用域。  <br/> |
|User  <br/> |指示应用程序是每个用户。  <br/> |
|组织  <br/> |指示应用程序适用于组织。  <br/> |
|默认  <br/> |指示应用程序是默认应用程序。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**描述**|
|:-----|:-----|
|[SpecificUsers](specificusers.md) <br/> |指定可访问应用程序的电子邮件帐户。  <br/> |
|[清单](manifest.md) <br/> |包含 base-64 编码的应用程序清单文件。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**描述**|
|:-----|:-----|
|[ClientExtensions](clientextensions.md) <br/> |指定**ClientExtension**元素的数组。  <br/> |
   
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

