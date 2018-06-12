---
title: 出现 （所在的时区转换）
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
description: 出现元素均表示所在的时区转换发生当月星期几的匹配项。
ms.openlocfilehash: bc5160480cc6881bb9d724aa61323f5717d1f2fa
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826636"
---
# <a name="occurrence-time-zone-transition"></a>出现 （所在的时区转换）

**出现**元素均表示所在的时区转换发生当月星期几的匹配项。 
  
```xml
<Occurrence/>
```

**int**

## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[RecurringDayTransition](recurringdaytransition.md) <br/> |表示时区转换发生在每年的同一天。  <br/> |
   
## <a name="text-value"></a>文本值

文本值是一个整数，表示发生所在的时区切换当月星期几的匹配项。 下表列出了可能的值。
  
|**值**|**说明**|
|:-----|:-----|
|1  <br/> |指定的日期相应月份的从头一周的第一个匹配项。  <br/> |
|2  <br/> |指定星期几从头相应月份的第二个匹配项。  <br/> |
|3  <br/> |第三个月的开始从一周中的指定日期发生。  <br/> |
|4  <br/> |指定的日期相应月份的从头一周的第四个匹配项。  <br/> |
|-1  <br/> |指定一天从相应月份的末尾一周中的第一个匹配项。  <br/> |
|-2  <br/> |指定一天从相应月份的末尾一周中的第二个匹配项。  <br/> |
|-3  <br/> |指定一天从相应月份的末尾一周中的第三个匹配项。  <br/> |
|-4  <br/> |指定一天从相应月份的末尾一周中的第四个匹配项。  <br/> |
   
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

