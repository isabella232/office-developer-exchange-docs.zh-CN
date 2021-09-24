---
title: Value (PersonaPostalAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: be838fc2-cfcb-4856-b095-a8e5366bb6c6
description: Value 元素指定与邮政地址关联的信息。
ms.openlocfilehash: 2f017cfc513b9c22d65f8437565646506f3be1ab
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517341"
---
# <a name="value-personapostaladdresstype"></a>Value (PersonaPostalAddressType)

**Value** 元素指定与邮政地址关联的信息。 
  
```XML
<Value>
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
</Value>
```

**PersonaPostalAddressType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

[Street](street.md)  | [城市](city.md)  | [State](state-ex15websvcsotherref.md)  | [国家/地区](country.md)  | [PostalCode](postalcode.md)  | [PostOfficeBox](postofficebox.md)  | [键入 (字符串) ](type-string.md)  | [Latitude](latitude.md)  | [经度](longitude.md)  | [准确性](accuracy.md)  | [Altitude](altitude.md)  | [AltitudeAccuracy](altitudeaccuracy.md)  | [FormattedAddress](formattedaddress.md)  | [LocationUri](locationuri.md)  | [LocationSource](locationsource.md)
  
### <a name="parent-elements"></a>父元素

[PostalAddressAttributedValue](postaladdressattributedvalue.md)
  
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
   

