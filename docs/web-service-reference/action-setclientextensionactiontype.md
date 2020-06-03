---
title: Action （SetClientExtensionActionType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c5624a87-3436-40ce-8d6b-cc01eecab64d
description: Action 元素包含 Exchange server 应对应用程序执行的操作。
ms.openlocfilehash: 29579e26377edacb5fb0bb8406144eeb116b8d15
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529684"
---
# <a name="action-setclientextensionactiontype"></a>Action （SetClientExtensionActionType）

**Action**元素包含 Exchange server 应对应用程序执行的操作。 
  
```XML
<Action ActionId="" ExtensionId="">
   <ClientExtension/>
</Action>
```

 **SetClientExtensionActionType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|ActionId  <br/> |指定操作的标识符。 此特性是必需的。  <br/> |
|ExtensionId  <br/> |指定扩展的标识符。 此特性是可选的。  <br/> |
   
#### <a name="actionid"></a>ActionId

|**值**|**说明**|
|:-----|:-----|
|配置  <br/> |指示配置操作。  <br/> |
|安装  <br/> |指示安装操作。  <br/> |
|Uninstall  <br/> |指示卸载操作。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**描述**|
|:-----|:-----|
|[ClientExtension](clientextension.md) <br/> |包含有关应用程序的用户和配置信息。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**描述**|
|:-----|:-----|
|[操作（ArrayOfSetClientExtensionActionsType）](actions-arrayofsetclientextensionactionstype.md) <br/> |指定**Action**元素的数组。  <br/> |
   
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

