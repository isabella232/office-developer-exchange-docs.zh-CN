---
title: ExtractAllowed
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bc213f0e-a655-44e9-9ac9-bc1673bae1fe
description: ExtractAllowed 元素指定实体提取是否已启用。
ms.openlocfilehash: f9fcae72d6241e51f549fbf650f5b2aebe019e46
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461980"
---
# <a name="extractallowed"></a>ExtractAllowed

**ExtractAllowed**元素指定实体提取是否已启用。 
  
```XML
<ExtractAllowed>true | false</ExtractAllowed
```

 **Boolean**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[RightsManagementLicenseData](rightsmanagementlicensedata.md) <br/> |指定有关权限管理许可证的信息。  <br/> |
   
## <a name="text-value"></a>文本值

如果**ExtractAllowed**元素的文本值为**true** ，则表示实体提取已启用。 **如果值为 false** ，则表示未启用实体提取。 
  
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

