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
description: To 元素指定的时区转换的目标。 目标是所在的时区句点或一组所在的时区转换。
ms.openlocfilehash: dc7df8ed3ddd6a9b4222ffab4c2b47b00ee4ba0c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838242"
---
# <a name="to"></a>To

**To**元素指定的时区转换的目标。 目标是所在的时区句点或一组所在的时区转换。 
  
```xml
<To Kind=""/>
```

 **TransitionTargetType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|类型  <br/> |指示所在的时区转换目标是否所在的时区期间或一组所在的时区转换。  <br/> |
   
#### <a name="kind-attribute-values"></a>Kind 属性值

|**值**|**说明**|
|:-----|:-----|
|句点  <br/> |指定时区转换目标时区句号。  <br/> |
|组  <br/> |指定时区转换目标是一组所在的时区转换。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[AbsoluteDateTransition](absolutedatetransition.md) <br/> |代表在特定日期和在特定时间发生的时区转换。  <br/> |
|[RecurringDayTransition](recurringdaytransition.md) <br/> |表示时区转换发生在每年的同一天。  <br/> |
|[RecurringDateTransition](recurringdatetransition.md) <br/> |表示在一年中的指定日期发生所在的时区转换。  <br/> |
|[转换](transition.md) <br/> |代表所在的时区转换。  <br/> |
   
## <a name="text-value"></a>文本值

文本值是一个字符串，指定的[时间段](period.md)或[TransitionsGroup](transitionsgroup.md)所在的时区转换的目标的唯一标识符。 
  
## <a name="remarks"></a>备注

描述此元素的架构位于运行 Microsoft Exchange Server 已安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

