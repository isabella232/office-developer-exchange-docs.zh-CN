---
title: Occurrence (Time Zone Transition)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Occurrence
api_type:
- schema
ms.assetid: 5c1142b1-c51f-42e1-bbb2-57e00cad0fdb
description: Occurrence 元素表示发生时区转换的一周中的一天。
ms.openlocfilehash: 9790b0e9541da0c22f2eac59850b8a361645c7b4
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59539274"
---
# <a name="occurrence-time-zone-transition"></a>Occurrence (Time Zone Transition)

**Occurrence** 元素表示发生时区转换的一周中的一天。 
  
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

|**元素**|**说明**|
|:-----|:-----|
|[RecurringDayTransition](recurringdaytransition.md) <br/> |表示时区转换发生在每年的同一天。  <br/> |
   
## <a name="text-value"></a>文本值

文本值是一个整数，表示发生时区转换的一周中的一天。 下表列出了可能的值。
  
|**值**|**说明**|
|:-----|:-----|
|1  <br/> |从该月开始一周中指定日期的第一次出现。  <br/> |
|2  <br/> |从该月开始一周中指定日期的第二次出现。  <br/> |
|3  <br/> |从该月开始一周中指定日期的第三次发生。  <br/> |
|4   <br/> |从该月开始一周中指定日期的第四次发生。  <br/> |
|-1  <br/> |从当月结束的一周中的指定日期的第一次出现。  <br/> |
|-2  <br/> |从当月结束起一周中指定日期的第二次出现。  <br/> |
|-3  <br/> |从当月结束的一周中的指定日期的第三次出现。  <br/> |
|-4  <br/> |从当月结束起一周中指定日期的第四次发生。  <br/> |
   
## <a name="remarks"></a>注解

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

