---
title: Attributions (ArrayOfPersonaAttributionsType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f61d843c-bca5-4c88-9667-fd03d2a963a1
description: Attributions 元素指定聚合到关联人员中的一个或多个联系人或 Active Directory 收件人的属性信息数组。
ms.openlocfilehash: 2c0ee8100398846be33827b5129557ca89789a17
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522025"
---
# <a name="attributions-arrayofpersonaattributionstype"></a>Attributions (ArrayOfPersonaAttributionsType)

**Attributions** 元素指定聚合到关联人员中的一个或多个联系人或 Active Directory 收件人的属性信息数组。 
  
```XML
<Attributions>
    <Attribution></Attribution>
</Attributions>
```

 **ArrayOfPersonaAttributionsType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Attribution (PersonaAttributionType)](attribution-personaattributiontype.md) <br/> |指定 **PersonaType** 元素的属性数组中的实例。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[角色](persona.md) <br/> |指定由 **GetPersona** 请求返回的一组人员数据。  <br/> |
   
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

