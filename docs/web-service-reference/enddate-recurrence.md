---
title: EndDate (Recurrence)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- EndDate
api_type:
- schema
ms.assetid: 16026595-26f8-4770-8a6d-0d3e4157effd
description: EndDate 元素表示定期任务的结束日期或具有 EndDateRecurrence 模式类型的日历项目。
ms.openlocfilehash: c53d83a3fb2f3a6a841d7e16c94d20dd3c7a92a4
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540089"
---
# <a name="enddate-recurrence"></a>EndDate (Recurrence)

**EndDate** 元素表示定期任务的结束日期或具有 EndDateRecurrence 模式类型的日历项目。 
  
```xml
<EndDate/>
```

 **date**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[EndDateRecurrence](enddaterecurrence.md) <br/> |描述项目的开始日期和结束日期定期模式。  <br/> |
   
## <a name="text-value"></a>文本值

如果使用此元素，则代表日期的文本值是必需的。 该值不能大于 4500 年 9 月 1 日 00：00：00。
  
## <a name="remarks"></a>说明

描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

