---
title: 事件（时区转换）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Occurrence
api_type:
- schema
ms.assetid: 5c1142b1-c51f-42e1-bbb2-57e00cad0fdb
description: 具体值元素表示发生时区转换的月份中的一周中的某一天的匹配项。
ms.openlocfilehash: 846f6b22f43bcda07b9408d768d0845a5acfe668
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467975"
---
# <a name="occurrence-time-zone-transition"></a>事件（时区转换）

**具体**值元素表示发生时区转换的月份中的一周中的某一天的匹配项。 
  
```xml
<Occurrence/>
```

**int**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**描述**|
|:-----|:-----|
|[RecurringDayTransition](recurringdaytransition.md) <br/> |表示时区转换发生在每年的同一天。  <br/> |
   
## <a name="text-value"></a>文本值

Text 值是一个整数，表示发生时区转换的月份中的某一天的匹配项。 下表列出了可能的值。
  
|**值**|**说明**|
|:-----|:-----|
|1  <br/> |指定的一周中第一天的第一次发生，从月初算起。  <br/> |
|双面  <br/> |第二次在一周中的某一天中指定的一天。  <br/> |
|第三章  <br/> |一周中指定日期的第三个匹配项。  <br/> |
|4   <br/> |从一月开始算起的指定星期几的第四个事件。  <br/> |
|-1  <br/> |一周中指定的一天的第一个匹配项，从月初结束。  <br/> |
|-2  <br/> |第二次出现在一周中的某一天，从月末结束。  <br/> |
|-3  <br/> |一周中指定的某一天的第三个事件（月份结束）。  <br/> |
|-4  <br/> |一周中指定日期的第四个事件（月份结束）。  <br/> |
   
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

