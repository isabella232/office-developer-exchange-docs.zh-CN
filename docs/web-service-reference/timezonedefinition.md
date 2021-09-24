---
title: TimeZoneDefinition
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- TimeZoneDefinition
api_type:
- schema
ms.assetid: b005a80c-addb-4409-beff-e5162076752c
description: TimeZoneDefinition 元素指定定义时区的时间段和转换。
ms.openlocfilehash: 6f2b580d2c3e31826ca74034cfda938cff71ee53
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59538812"
---
# <a name="timezonedefinition"></a>TimeZoneDefinition

**TimeZoneDefinition** 元素指定用于定义时区的时间段和转换。 
  
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
|[Periods](periods.md) <br/> |表示 Period [元素的](period.md) 数组，这些元素定义时区的不同阶段的时间偏移。  <br/> |
|[TransitionsGroups](transitionsgroups.md) <br/> |表示指定时区转换 [的 TransitionsGroup](transitionsgroup.md) 元素的数组。  <br/> |
|[Transitions](transitions.md) <br/> |表示时区转换的数组。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[TimeZoneDefinitions](timezonedefinitions.md) <br/> |表示时区定义的数组。  <br/> |
|[TimeZoneContext](timezonecontext.md) <br/> |表示默认时区定义，该定义用于对使用 Exchange Web Services (EWS) 创建、更新和检索的对象的 DateTime 属性进行范围) 。  <br/> |
   
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

