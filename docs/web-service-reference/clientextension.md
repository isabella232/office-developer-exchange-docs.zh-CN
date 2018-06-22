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
ms.openlocfilehash: 5051248a2c8e664d82666bd7b42ee3c3046f43fe
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753452"
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

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|IsAvailable  <br/> |指定应用程序是否可用。 文本值为**true**的**IsAvailable**属性指示应用程序可用。 如果值为**false**指示应用程序不可用。 此属性是可选的。  <br/> |
|IsMandatory  <br/> |指定是否强制应用程序。 文本值为**true**的**IsMandatory**属性指示应用程序是必需的邮箱。 如果值为**false**指示应用程序不是强制性。 此属性是可选的。  <br/> |
|IsEnabledByDefault  <br/> |指定默认情况下是否启用应用程序。 文本值为**true**的**IsEnabledByDefault**属性指示，默认启用应用程序。 如果值为**false**指示，默认情况下不启用应用程序。 此属性是可选的。  <br/> |
|ProvidedTo  <br/> |指定向其提供应用程序。 此属性是可选的。  <br/> |
|类型  <br/> |指定应用程序的类型。  <br/> |
|范围  <br/> |指定应用程序的范围。  <br/> |
|MarketplaceAssetId  <br/> |指定应用程序的市场资产标识符。  <br/> |
|MarketplaceContentMarket  <br/> |指定的商城内容的用户看到的详细信息，并回顾有关应用程序。  <br/> |
|AppStatus  <br/> |在意外状态指定邮件应用程序的状态代码。  <br/> |
|Etoken  <br/> |指定付费或试用邮件应用程序许可证令牌。  <br/> |
   
#### <a name="type"></a>类型

|**值**|**说明**|
|:-----|:-----|
|默认  <br/> |指示应用程序是默认情况下可用。  <br/> |
|私有  <br/> |指示专用应用程序。  <br/> |
|市场  <br/> |指示应用程序的市场应用程序。  <br/> |
   
#### <a name="scope"></a>范围

|**值**|**说明**|
|:-----|:-----|
|无  <br/> |指示应用程序有无作用域。  <br/> |
|用户  <br/> |指示应用程序是每个用户。  <br/> |
|组织  <br/> |指示应用程序的组织。  <br/> |
|默认  <br/> |指示应用程序的默认应用程序。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[SpecificUsers](specificusers.md) <br/> |指定可以访问应用程序的电子邮件帐户。  <br/> |
|[Manifest](manifest.md) <br/> |包含 base64 编码的应用程序清单文件。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ClientExtensions](clientextensions.md) <br/> |指定**ClientExtension**元素的数组。  <br/> |
   
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

