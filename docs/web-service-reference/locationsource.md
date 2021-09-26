---
title: LocationSource
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: fc4d77d5-6200-4cf3-848a-1088fec0e0d6
description: LocationSource 元素指定有关关联邮政地址的来源的信息，例如联系人或电话簿。
ms.openlocfilehash: f3569494d3e662fbc46060944c8bd399b62d656b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543259"
---
# <a name="locationsource"></a>LocationSource

**LocationSource** 元素指定有关关联邮政地址的来源的信息，例如联系人或电话簿。 
  
```XML
<LocationSource> None | LocationServices | PhonebookServices | Device | Contact | Resource </LocationSource>
```

 **LocationSourceType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[Value (PersonaPostalAddressType) ](value-personapostaladdresstype.md)  | [PostalAddress (PersonaPostalAddressType) ](postaladdress-personapostaladdresstype.md)
  
## <a name="text-value"></a>文本值

下表列出了 **LocationSource** 元素的文本值： 
  
**LocationSource 元素文本值**

|**值**|**说明**|
|:-----|:-----|
|无  <br/> |没有位置源。  <br/> |
|LocationServices  <br/> |该信息从定位服务获取。  <br/> |
|PhonebookServices  <br/> |该信息从电话簿服务获取。  <br/> |
|设备  <br/> |该信息从设备获取。  <br/> |
|联系人  <br/> |该信息是从联系人获取的。  <br/> |
|资源  <br/> |该信息从资源获取。  <br/> |
   
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  

