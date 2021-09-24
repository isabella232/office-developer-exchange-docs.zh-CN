---
title: PostalAddress (PersonaPostalAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 075f7d65-9d05-47cb-af26-0dd6d5593439
description: PostalAddress 元素指定某个人物的邮政地址。
ms.openlocfilehash: 4e95a94c5a7ce917a0a4b9abf7b7ef120301ae6c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523900"
---
# <a name="postaladdress-personapostaladdresstype"></a>PostalAddress (PersonaPostalAddressType)

**PostalAddress** 元素指定某个人物的邮政地址。 
  
```XML
<PostalAddress>
   <Street/>
   <City/>
   <State/>
   <Country/>
   <PostalCode/>
   <PostOfficeBox/>
   <Type/>
   <Latitude/>
   <Longitude/>
   <Accuracy/>
   <Altitude/>
   <AltitudeAccuracy/>
   <FormattedAddress/>
   <LocationUri/>
   <LocationSource/>
</PostalAddress>
```

 **PersonaPostalAddressType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

[Street](street.md)  | [城市](city.md)  | [State](state-ex15websvcsotherref.md)  | [国家/地区](country.md)  | [PostalCode](postalcode.md)  | [PostOfficeBox](postofficebox.md)  | [键入 (字符串) ](type-string.md)  | [Latitude](latitude.md)  | [经度](longitude.md)  | [准确性](accuracy.md)  | [Altitude](altitude.md)  | [AltitudeAccuracy](altitudeaccuracy.md)  | [FormattedAddress](formattedaddress.md)  | [LocationUri](locationuri.md)  | [LocationSource](locationsource.md)
  
### <a name="parent-elements"></a>父元素

[EnhancedLocation](enhancedlocation.md)
  
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> ||
   

