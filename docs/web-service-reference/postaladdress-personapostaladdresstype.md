---
title: 省略（PersonaPostalAddressType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 075f7d65-9d05-47cb-af26-0dd6d5593439
description: 省略元素指定角色的邮政地址。
ms.openlocfilehash: 9e316e5e0135c2d18fab4067241988c65eceec66
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465385"
---
# <a name="postaladdress-personapostaladdresstype"></a>省略（PersonaPostalAddressType）

**省略**元素指定角色的邮政地址。 
  
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

[街道](street.md)  | [城市](city.md)  | [状态](state-ex15websvcsotherref.md)  | [国家/地区](country.md)  | [邮政编码](postalcode.md)  | [PostOfficeBox](postofficebox.md)  | [类型（字符串）](type-string.md)  | [纬度](latitude.md)  | [经度](longitude.md)  | [准确性](accuracy.md)  | [海拔](altitude.md)  | [AltitudeAccuracy](altitudeaccuracy.md)  | [FormattedAddress](formattedaddress.md)  | [LocationUri](locationuri.md)  | [LocationSource](locationsource.md)
  
### <a name="parent-elements"></a>父元素

[EnhancedLocation](enhancedlocation.md)
  
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> ||
   

