---
title: RecurringDateTransition
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RecurringDateTransition
api_type:
- schema
ms.assetid: 52fe1e05-3c50-40a1-8752-5c3c64c9f1ed
description: RecurringDateTransition 元素表示每年的特定日期发生的时区转换。
ms.openlocfilehash: 864f3f539c5440fbfc539ca6c2042b3d9edca267
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59529361"
---
# <a name="recurringdatetransition"></a>RecurringDateTransition

**RecurringDateTransition** 元素表示每年的特定日期发生的时区转换。 
  
```xml
<RecurringDateTransition>
   <To/>
   <TimeOffset/>
   <Month/>
   <Day/>
</RecurringDateTransition>
```

 **RecurringDateTransitionType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[To](to.md) <br/> |指定[作为时区](period.md)转换目标的 Period 或[TransitionsGroup。](transitionsgroup.md)  <br/> |
|[TimeOffset](timeoffset.md) <br/> |表示与时区转换的协调世界时 (UTC) 的持续时间偏移量。  <br/> |
|[Month (Time Zone Transition)](month-time-zone-transition.md) <br/> |表示时区转换发生的月份。  <br/> |
|[Day](day.md) <br/> |表示发生时区转换的月份中的哪一天。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Transitions](transitions.md) <br/> |表示时区转换的集合。  <br/> |
|[TransitionsGroup](transitionsgroup.md) <br/> |表示时区转换的集合。  <br/> |
   
## <a name="remarks"></a>注解

由 [RecurringDateTransition](recurringdatetransition.md) 元素表示的时区转换示例是每年 3 月 15 日发生的转换。 
  
描述此元素的架构位于运行已安装客户端访问服务器角色Microsoft Exchange Server的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

