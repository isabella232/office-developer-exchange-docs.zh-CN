---
title: ClientExtension
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 3445ef2b-1bb1-43ea-bc93-85c72401e5b6
description: ClientExtension 元素包含有关应用的用户和配置信息。
ms.openlocfilehash: fa02ad0f5f4312fefecee32d2ed24f0bb0585365
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519959"
---
# <a name="clientextension"></a>ClientExtension

**ClientExtension** 元素包含有关应用的用户和配置信息。 
  
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
|IsAvailable  <br/> |指定应用是否可用。 **IsAvailable** 属性的文本值 **true** 指示应用可用。 false **值表示** 应用不可用。 此特性是可选的。  <br/> |
|IsMandatory  <br/> |指定应用是否是必需的。 **IsMandatory** 属性的文本值 **true** 指示应用对于邮箱是必需的。 false **值表示** 应用不是必需的。 此特性是可选的。  <br/> |
|IsEnabledByDefault  <br/> |指定默认情况下是否启用应用。 **IsEnabledByDefault** 属性的文本值 **true** 指示应用默认启用。 false **值表示** 默认情况下未启用应用。 此特性是可选的。  <br/> |
|ProvidedTo  <br/> |指定向谁提供应用。 此特性是可选的。  <br/> |
|类型  <br/> |指定应用的类型。  <br/> |
|范围  <br/> |指定应用程序的范围。  <br/> |
|MarketplaceAssetId  <br/> |指定应用程序的市场资产标识符。  <br/> |
|MarketplaceContentMarket  <br/> |指定用户看到的市场内容，以了解有关应用的详细信息和评论。  <br/> |
|AppStatus  <br/> |指定邮件应用程序在意外状态的状态代码。  <br/> |
|Etoken  <br/> |指定付费或试用邮件应用程序的许可证令牌。  <br/> |
   
#### <a name="type"></a>类型

|**值**|**说明**|
|:-----|:-----|
|默认值  <br/> |指示应用默认可用。  <br/> |
|Private  <br/> |指示应用是私有的。  <br/> |
|MarketPlace  <br/> |指示应用是市场应用。  <br/> |
   
#### <a name="scope"></a>范围

|**值**|**说明**|
|:-----|:-----|
|无  <br/> |指示应用没有范围。  <br/> |
|用户  <br/> |指示应用是按用户应用。  <br/> |
|组织  <br/> |指示应用适用于组织。  <br/> |
|默认值  <br/> |指示应用是默认应用。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[SpecificUsers](specificusers.md) <br/> |指定可以访问该应用的电子邮件帐户。  <br/> |
|[清单](manifest.md) <br/> |包含 Base64 编码的应用清单文件。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ClientExtensions](clientextensions.md) <br/> |指定 **ClientExtension 元素的** 数组。  <br/> |
   
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

