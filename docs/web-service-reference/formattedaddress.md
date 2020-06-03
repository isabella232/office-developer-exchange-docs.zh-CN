---
title: FormattedAddress
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 643f8663-1fab-4625-a7e9-5724e352972b
description: FormattedAddress 元素指定关联的邮政地址的格式化显示值。
ms.openlocfilehash: 9150a3bb5bc81f7afecdafbf0cc33fafff597578
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461938"
---
# <a name="formattedaddress"></a>FormattedAddress

**FormattedAddress**元素指定关联的邮政地址的格式化显示值。 
  
```XML
<FormattedAddress></FormattedAddress>
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
|[Value （PersonaPostalAddressType）](value-personapostaladdresstype.md) <br/> |指定与邮政地址相关联的信息。  <br/> |
|[省略（PersonaPostalAddressType）](postaladdress-personapostaladdresstype.md) <br/> |指定位置的邮政地址。  <br/> |
   
## <a name="text-value"></a>文本值

**FormattedAddress**元素的文本值是一个 string 值，用于指定已设置格式的地址。 
  
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

