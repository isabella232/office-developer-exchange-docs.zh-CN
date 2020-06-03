---
title: DisplayNameLastFirst
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d392e138-a514-4bce-81b1-1f484e353d1c
description: DisplayNameLastFirst 元素以格式、姓氏、名字指定关联角色的显示名称。
ms.openlocfilehash: d569a87ce77a4f1840ed4f865e671399726ede78
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463158"
---
# <a name="displaynamelastfirst"></a>DisplayNameLastFirst

**DisplayNameLastFirst**元素指定格式为 "Last name"，"First name" 的关联角色的显示名称。 
  
```XML
<DisplayNameLastFirst></DisplayNameLastFirst>
```

 **string**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[角色](persona.md) <br/> |指定由**GetPersona**请求返回的一组角色数据。  <br/> |
   
## <a name="text-value"></a>文本值

**DisplayNameLastFirst**元素的文本值是一个 string 值，它指定显示名称，姓先是。 
  
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

