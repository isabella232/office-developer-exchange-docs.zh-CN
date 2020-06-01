---
title: TimeZoneDefinition
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TimeZoneDefinition
api_type:
- schema
ms.assetid: b005a80c-addb-4409-beff-e5162076752c
description: TimeZoneDefinition 元素指定用于定义时区的周期和转换。
ms.openlocfilehash: 58d34556686bfc77244b5829798eada51a1df843
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466064"
---
# <a name="timezonedefinition"></a>TimeZoneDefinition

**TimeZoneDefinition**元素指定用于定义时区的周期和转换。 
  
```XML
<TimeZoneDefinition Id="" Name="">
   <Periods/>
   <TransitionsGroups/>
   <Transitions/>
</TimeZoneDefinition>

```

 **TimeZoneDefinitionType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|Id  <br/> |表示时区的唯一标识符。  <br/> |
|名称  <br/> |表示时区的描述性名称。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[课时](periods.md) <br/> |表示用于定义时区的不同阶段的时间偏移量的[Period](period.md)元素的数组。  <br/> |
|[TransitionsGroups](transitionsgroups.md) <br/> |表示[TransitionsGroup](transitionsgroup.md)元素的数组，这些元素指定时区转换。  <br/> |
|[移交](transitions.md) <br/> |表示时区转换的数组。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[TimeZoneDefinitions](timezonedefinitions.md) <br/> |表示时区定义的数组。  <br/> |
|[TimeZoneContext](timezonecontext.md) <br/> |表示用于限定使用 Exchange Web 服务（EWS）创建、更新和检索的对象的日期/时间属性的默认时区定义。  <br/> |
   
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

