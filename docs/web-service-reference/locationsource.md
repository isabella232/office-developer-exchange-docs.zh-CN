---
title: LocationSource
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fc4d77d5-6200-4cf3-848a-1088fec0e0d6
description: LocationSource 元素指定有关关联邮政地址的来源的信息，例如，联系人或电话簿。
ms.openlocfilehash: ceba52c43d1c798bb8f5492b779c7c45d7d00b0b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467100"
---
# <a name="locationsource"></a>LocationSource

**LocationSource**元素指定有关关联邮政地址的来源的信息，例如，联系人或电话簿。 
  
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

[Value （PersonaPostalAddressType）](value-personapostaladdresstype.md)  | [省略（PersonaPostalAddressType）](postaladdress-personapostaladdresstype.md)
  
## <a name="text-value"></a>文本值

下表列出了**LocationSource**元素的文本值： 
  
**LocationSource 元素文本值**

|**值**|**说明**|
|:-----|:-----|
|无  <br/> |没有位置源。  <br/> |
|LocationServices  <br/> |信息是从位置服务获取的。  <br/> |
|PhonebookServices  <br/> |此信息是通过电话簿服务获取的。  <br/> |
|设备  <br/> |信息是从设备获取的。  <br/> |
|Contact  <br/> |信息是从联系人获取的。  <br/> |
|Resource  <br/> |信息是从资源获取的。  <br/> |
   
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  

