---
title: AddressEntity
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: ead22eab-f1e7-48b4-a165-db0e49fe86a8
description: AddressEntity 元素指定单个地址实体。
ms.openlocfilehash: 35fc5012e648494d2a1c0ddaf5a137164d33a842
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543749"
---
# <a name="addressentity"></a>AddressEntity

**AddressEntity** 元素指定单个地址实体。 
  
```XML
<AddressEntity>
    <Address></Address>
    <Position></Position>
</AddressEntity>
```

 **AddressEntityType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Address (string)](address-string.md) <br/> |指定地址。  <br/> |
|[Position](position.md) <br/> |指定电子邮件中的位置。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Addresses (ArrayOfAddressEntitiesType)](addresses-arrayofaddressentitiestype.md) <br/> |指定 **AddressEntity 元素的** 数组。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
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

