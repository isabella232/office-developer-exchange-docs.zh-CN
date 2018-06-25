---
title: TrackingPropertyType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TrackingPropertyType
api_type:
- schema
ms.assetid: 1d0f219b-1063-4eaa-9d3b-da384a544f89
description: TrackingPropertyType 元素均表示字符串用于创建邮件跟踪报告的属性的名称 / 值的对。
ms.openlocfilehash: 762c7d364382c3087277651cc01329e3c85df4e4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838277"
---
# <a name="trackingpropertytype"></a>TrackingPropertyType

**TrackingPropertyType**元素均表示字符串用于创建邮件跟踪报告的属性的名称 / 值的对。 
  
[属性 (ArrayOfTrackingPropertiesType)](properties-arrayoftrackingpropertiestype.md)
  
[TrackingPropertyType](trackingpropertytype.md)
  
```xml
<TrackingPropertyType>
   <Name/>
   <Value/>
</TrackingPropertyType>
```

 **TrackingPropertyType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[名称 （邮件跟踪）](name-message-tracking.md) <br/> |定义邮件跟踪报告属性的名称。  <br/> |
|[值 （邮件跟踪）](value-message-tracking.md) <br/> |定义邮件跟踪报告属性的值。 此元素是可选的。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[属性 (ArrayOfTrackingPropertiesType)](properties-arrayoftrackingpropertiestype.md) <br/> |包含一个或多个跟踪属性的列表。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>备注

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

