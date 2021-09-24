---
title: 到
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- To
api_type:
- schema
ms.assetid: d14e46da-14bd-4a33-a78e-8ee314d9c1d8
description: To 元素指定时区转换的目标。 目标是时区时段或一组时区转换。
ms.openlocfilehash: 64f3f3258fd7c2bad051eabb1b33617bb056ab39
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522549"
---
# <a name="to"></a>到

To 元素指定时区转换的目标。 目标是时区时段或一组时区转换。 
  
```xml
<To Kind=""/>
```

 **TransitionTargetType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|Kind  <br/> |指示时区转换目标是时区时段还是一组时区转换。  <br/> |
   
#### <a name="kind-attribute-values"></a>类型属性值

|**值**|**说明**|
|:-----|:-----|
|Period  <br/> |指定时区转换目标为时区时间段。  <br/> |
|Group  <br/> |指定时区转换目标为一组时区转换。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[AbsoluteDateTransition](absolutedatetransition.md) <br/> |表示特定日期和特定时间发生的时区转换。  <br/> |
|[RecurringDayTransition](recurringdaytransition.md) <br/> |表示时区转换发生在每年的同一天。  <br/> |
|[RecurringDateTransition](recurringdatetransition.md) <br/> |表示在一年中的指定日期发生的时区转换。  <br/> |
|[Transition](transition.md) <br/> |表示时区转换。  <br/> |
   
## <a name="text-value"></a>文本值

文本值是一个字符串，用于指定作为时区转换目标的 [Period](period.md) 或 [TransitionsGroup](transitionsgroup.md) 的唯一标识符。 
  
## <a name="remarks"></a>注解

描述此元素的架构位于运行安装了客户端访问服务器角色Microsoft Exchange Server的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

