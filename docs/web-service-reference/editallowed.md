---
title: EditAllowed
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: e63c4f7e-77c0-4826-b4e2-43b795d03914
description: EditAllowed 元素指定是否可以编辑信息权限管理。
ms.openlocfilehash: 2bd88dd47eb3f1964eae678412a6748ee8d28ec8
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540116"
---
# <a name="editallowed"></a>EditAllowed

**EditAllowed** 元素指定是否可以编辑信息权限管理。 
  
```XML
<EditAllowed> true | false </EditAllowed>
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

**EditAllowed** 元素的文本值 **true** 指示可以编辑信息权限 (IRM) 信息权限管理。 false **值表示** 无法编辑 IRM。 
  
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

