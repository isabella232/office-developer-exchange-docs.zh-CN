---
title: TransitionsGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TransitionsGroup
api_type:
- schema
ms.assetid: 19d56080-546a-4d53-929e-363d56186759
description: TransitionsGroup 元素均表示一个数组所在的时区转换。
ms.openlocfilehash: e5991ad7f73a1694e0d4abadd8d252acc04970e5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838286"
---
# <a name="transitionsgroup"></a>TransitionsGroup

**TransitionsGroup**元素均表示一个数组所在的时区转换。 
  
```xml
<TransitionsGroup Id="">
   <AbsoluteDateTransition/>
   <RecurringDayTransition/>
   <RecurringDateTransition/>
</TransitionsGroup>
```

 **ArrayOfTransitionsType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|Id  <br/> |一个字符串值，表示转换组的唯一标识符。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[AbsoluteDateTransition](absolutedatetransition.md) <br/> |代表在特定日期和在特定时间发生的时区转换。  <br/> |
|[RecurringDayTransition](recurringdaytransition.md) <br/> |表示时区转换发生在每年的同一天。  <br/> |
|[RecurringDateTransition](recurringdatetransition.md) <br/> |表示在一年中的指定日期发生所在的时区转换。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[TransitionsGroups](transitionsgroups.md) <br/> |代表所在的时区转换组的数组。  <br/> |
   
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

