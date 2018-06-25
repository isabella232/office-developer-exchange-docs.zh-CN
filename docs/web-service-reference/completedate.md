---
title: CompleteDate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CompleteDate
api_type:
- schema
ms.assetid: b2b53b87-6a0b-4a55-bcfc-3bf67d3c1700
description: CompleteDate 元素均表示已完成项目的日期。
ms.openlocfilehash: 00a1ec25be737ec0a5cc874063e1bce19a96cee0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753461"
---
# <a name="completedate"></a>CompleteDate

**CompleteDate**元素均表示已完成项目的日期。 
  
```xml
<CompleteDate/>
```

 **DateTime**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[任务](task.md) <br/> |表示 Exchange 存储中的任务。  <br/> |
|[Flag](flag.md) <br/> |邮箱项目上指定的标志。  <br/> |
   
## <a name="text-value"></a>文本值

如果使用此元素，则需要一个文本值，表示的日期和时间。
  
## <a name="remarks"></a>注解

设置**CompleteDate**与将[PercentComplete](percentcomplete.md)设置为 100 或**已完成**[状态](status.md)的效果相同。 在请求中，这些属性的设置至少两个，最后一个处理的属性将确定设置这些元素的值。 例如，如果[PercentComplete](percentcomplete.md)为 100， **CompleteDate**是 2007 年 1 月 1 日和[状态](status.md)为**NotStarted**，并且该顺序流式传输属性，将效果设置为 NotStarted**任务的[状态](status.md)**， [CompleteDate](completedate.md)为**null**，并且为 0 的[完成百分比](percentcomplete.md)。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)


[创建任务](http://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[删除任务](http://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

