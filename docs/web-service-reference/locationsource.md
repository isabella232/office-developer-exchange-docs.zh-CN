---
title: LocationSource
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fc4d77d5-6200-4cf3-848a-1088fec0e0d6
description: LocationSource 元素指定关联的邮政地址，例如，联系人或电话簿原点有关的信息。
ms.openlocfilehash: 7f5cf5fcca0a72287593349fcf5090a74225d012
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826248"
---
# <a name="locationsource"></a>LocationSource

**LocationSource**元素指定关联的邮政地址，例如，联系人或电话簿原点有关的信息。 
  
```XML
<LocationSource> None | LocationServices | PhonebookServices | Device | Contact | Resource </LocationSource>
```

 **LocationSourceType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[值 (PersonaPostalAddressType)](value-personapostaladdresstype.md) | [PostalAddress (PersonaPostalAddressType)](postaladdress-personapostaladdresstype.md)
  
## <a name="text-value"></a>文本值

下表中列出的**LocationSource**元素的文本值： 
  
**LocationSource 元素的文本值**

|**值**|**说明**|
|:-----|:-----|
|无  <br/> |没有任何位置源。  <br/> |
|LocationServices  <br/> |从位置服务已获得的信息。  <br/> |
|PhonebookServices  <br/> |从通讯簿服务已获得的信息。  <br/> |
|设备  <br/> |从设备已获得的信息。  <br/> |
|联系人  <br/> |从联系人已获得的信息。  <br/> |
|资源  <br/> |从一个资源已获得的信息。  <br/> |
   
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  

