---
title: Addresses (ArrayOfAddressesType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 711acc90-8e5b-4658-92d2-16cd441db56e
description: Addresses 元素指定 Address 元素的数组。
ms.openlocfilehash: a82c2df7bccf3b039f673ab8dc0716358fbd3de7
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546780"
---
# <a name="addresses-arrayofaddressestype"></a>Addresses (ArrayOfAddressesType)

**Addresses** 元素指定 Address 元素 **的** 数组。 
  
```XML
<Addresses>
    <Address></Address>
</Addresses>
```

 **ArrayOfAddressesType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Address (ContactType)](address-contacttype.md) <br/> |指定联系人的地址。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Contact (ContactType)](contact-contacttype.md) <br/> |指定统一联系人存储中的联系人。  <br/> |
   
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

