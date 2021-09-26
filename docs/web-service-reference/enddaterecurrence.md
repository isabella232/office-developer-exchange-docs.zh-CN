---
title: EndDateRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- EndDateRecurrence
api_type:
- schema
ms.assetid: a5ee2504-db84-49ee-870c-cca9269f2e26
description: EndDateRecurrence 元素描述项目的开始日期和结束日期定期模式。
ms.openlocfilehash: 8052ad490d32073dc04c194b6d98e2a92ac3bea2
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541425"
---
# <a name="enddaterecurrence"></a>EndDateRecurrence

**EndDateRecurrence** 元素描述项目的开始日期和结束日期定期模式。 
  
```xml
<EndDateRecurrence>
   <StartDate/>
   <EndDate/>
</EndDateRecurrence>
```

 **EndDateRecurrenceRangeType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[StartDate (Recurrence)](startdate-recurrence.md) <br/> |表示定期任务或日历项目的开始日期。  <br/> |
|[EndDate (Recurrence)](enddate-recurrence.md) <br/> |表示定期任务或日历项目的结束日期。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Recurrence (RecurrenceType)](recurrence-recurrencetype.md) <br/> |包含定期模式项和会议请求的联系人。  <br/> |
|[Recurrence (TaskRecurrenceType)](recurrence-taskrecurrencetype.md) <br/> |包含定期模式任务的组。  <br/> |
   
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

