---
title: FileAsIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 71cae100-b68e-454b-b9b6-ddbcb4d78f3f
description: FileAsIds 元素指定 StringAttributedValue 元素的数组以及关联角色的源归属的标识符。
ms.openlocfilehash: ecdf30fac345834600439227709504b0d56b988b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461042"
---
# <a name="fileasids"></a>FileAsIds

**FileAsIds**元素指定**StringAttributedValue**元素的数组以及关联角色的源归属的标识符。 
  
```XML
<FileAsIds>
    <StringAttributedValue/>
<FileAsIds>
```

 **ArrayOfStringAttributedValuesType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[StringAttributedValue](stringattributedvalue.md) <br/> |指定与 persona 元素相关联的属性数组中的实例。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[角色](persona.md) <br/> |指定由**GetPersona**请求返回的一组角色数据。  <br/> |
   
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

