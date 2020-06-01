---
title: 标准
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Standard
api_type:
- schema
ms.assetid: d598f0a6-e296-423f-8ce5-3da57cfd8189
description: Standard 元素表示时间从夏时制更改为标准时间的日期和时间。
ms.openlocfilehash: 1214a1debb53c9a31ca7c92a0c9e5c0722960d75
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467562"
---
# <a name="standard"></a>标准

**Standard**元素表示时间从夏时制更改为标准时间的日期和时间。 
  
```xml
<Standard TimeZoneName="">
   <Offset/>
   <RelativeYearlyRecurrence/>
   <Time/>
</Standard>
```

```xml
<Standard TimeZoneName="">
   <Offset/>
   <AbsoluteDate/>
   <Time/>
</Standard>
```

**TimeChangeType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**TimeZoneName** <br/> |描述时区的名称。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Offset](offset.md) <br/> |描述[BaseOffset](baseoffset.md)中的偏移量。 **Offset**元素与**BaseOffset**元素一起标识时间是标准时间还是夏时制。  <br/> |
|[RelativeYearlyRecurrence](relativeyearlyrecurrence.md) <br/> |描述时区转换日期的相对年定期模式。  <br/> |
|[AbsoluteDate](absolutedate.md) <br/> |表示从标准时间或夏时制的时间更改的日期。  <br/> |
|[Time （TimeChangeType）](time-timechangetype.md) <br/> |描述在标准时间和夏时制时间之间的时间更改时间。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[MeetingTimeZone](meetingtimezone.md) <br/> |表示时区的会议所在的位置。  <br/> |
   
## <a name="remarks"></a>说明

描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

