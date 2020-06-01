---
title: RecurringDateTransition
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RecurringDateTransition
api_type:
- schema
ms.assetid: 52fe1e05-3c50-40a1-8752-5c3c64c9f1ed
description: RecurringDateTransition 元素表示每年的特定日期发生的时区转换。
ms.openlocfilehash: 2acbd3afb50a92d4e4f3d7b552eecb36fe59be8b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461574"
---
# <a name="recurringdatetransition"></a>RecurringDateTransition

**RecurringDateTransition**元素表示每年的特定日期发生的时区转换。 
  
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
|[To](to.md) <br/> |指定作为时区转换目标的[时间段](period.md)或[TransitionsGroup](transitionsgroup.md) 。  <br/> |
|[TimeOffset](timeoffset.md) <br/> |表示时区转换与协调世界时（UTC）之间的持续时间偏移量。  <br/> |
|[Month （时区转换）](month-time-zone-transition.md) <br/> |表示发生时区转换的月份。  <br/> |
|[Day](day.md) <br/> |表示在每月的哪一天发生时区转换。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[移交](transitions.md) <br/> |表示时区转换的集合。  <br/> |
|[TransitionsGroup](transitionsgroup.md) <br/> |表示时区转换的集合。  <br/> |
   
## <a name="remarks"></a>备注

[RecurringDateTransition](recurringdatetransition.md)元素可以表示的时区转换的一个示例是每年3月15日发生的转换。 
  
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

