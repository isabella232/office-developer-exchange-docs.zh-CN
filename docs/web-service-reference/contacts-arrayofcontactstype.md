---
title: 联系人（ArrayOfContactsType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a2c1e833-5f8c-438d-bad7-bb5dcc29ca9e
description: "\"联系人\" 元素指定联系人数组。"
ms.openlocfilehash: eeb202f41fcf5ec7aad12a8a2b8e6dd539b3dba4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529439"
---
# <a name="contacts-arrayofcontactstype"></a>联系人（ArrayOfContactsType）

"**联系人**" 元素指定联系人数组。 
  
```XML
<Contacts>
    <Contact></Contact>
</Contacts>
```

 **ArrayOfContactsType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Contact （ContactType）](contact-contacttype.md) <br/> |指定统一联系人存储库中的联系人。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[EntityExtractionResult](entityextractionresult.md) <br/> |指定项的**EntityExtractionResult**属性。  <br/> |
   
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

