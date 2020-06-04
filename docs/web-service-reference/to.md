---
title: To
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- To
api_type:
- schema
ms.assetid: d14e46da-14bd-4a33-a78e-8ee314d9c1d8
description: To 元素指定时区转换的目标。 目标为时区时间段或时区转换组。
ms.openlocfilehash: 8cce700eedd64035f2e21be4db6b517f3f85d98d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468794"
---
# <a name="to"></a>To

**To**元素指定时区转换的目标。 目标为时区时间段或时区转换组。 
  
```xml
<To Kind=""/>
```

 **TransitionTargetType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|Kind  <br/> |指示时区转换目标是时区转换的时间段还是一组时区转换。  <br/> |
   
#### <a name="kind-attribute-values"></a>Kind 属性值

|**值**|**说明**|
|:-----|:-----|
|句点  <br/> |指定时区转换目标为时区时间段。  <br/> |
|Group  <br/> |指定时区转换目标是一组时区转换。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**描述**|
|:-----|:-----|
|[AbsoluteDateTransition](absolutedatetransition.md) <br/> |表示在特定日期和特定时间发生的时区转换。  <br/> |
|[RecurringDayTransition](recurringdaytransition.md) <br/> |表示时区转换发生在每年的同一天。  <br/> |
|[RecurringDateTransition](recurringdatetransition.md) <br/> |表示在指定的一年中的某一天发生的时区转换。  <br/> |
|[移交](transition.md) <br/> |表示时区转换。  <br/> |
   
## <a name="text-value"></a>文本值

Text 值是一个字符串，它指定作为时区转换目标的[句点](period.md)或[TransitionsGroup](transitionsgroup.md)的唯一标识符。 
  
## <a name="remarks"></a>备注

描述此元素的架构位于运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

