---
title: 时区定义
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
description: 时区定义元素指定时间段和定义时区的切换。
ms.openlocfilehash: ffd5ed0c862af794e4aff2387f508849b1d5fd5d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838248"
---
# <a name="timezonedefinition"></a>时区定义

**时区定义**元素指定时间段和定义时区的切换。 
  
```XML
<TimeZoneDefinition Id="" Name="">
   <Periods/>
   <TransitionsGroups/>
   <Transitions/>
</TimeZoneDefinition>

```

 **TimeZoneDefinitionType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|Id  <br/> |代表时区的唯一标识符。  <br/> |
|名称  <br/> |代表时区的描述性名称。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[时间段](periods.md) <br/> |表示定义的时间偏移量的时区的不同阶段的[时间段](period.md)元素的数组。  <br/> |
|[TransitionsGroups](transitionsgroups.md) <br/> |代表指定时区转换的[TransitionsGroup](transitionsgroup.md)元素的数组。  <br/> |
|[切换](transitions.md) <br/> |代表所在的时区转换的数组。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[TimeZoneDefinitions](timezonedefinitions.md) <br/> |代表所在的时区定义的数组。  <br/> |
|[TimeZoneContext](timezonecontext.md) <br/> |表示用于范围对象的创建、 更新和使用 Exchange Web Services (EWS) 检索 DateTime 属性的默认时区定义。  <br/> |
   
## <a name="remarks"></a>备注

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

