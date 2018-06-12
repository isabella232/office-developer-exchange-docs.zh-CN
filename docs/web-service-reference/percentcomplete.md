---
title: PercentComplete
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PercentComplete
api_type:
- schema
ms.assetid: 58a67f8a-c4dc-42dc-97ae-a9e5cc672d2d
description: PercentComplete 元素描述任务的完成的状态。
ms.openlocfilehash: 18e53221ecdf60df195445ed7692c03795bdcc1e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826717"
---
# <a name="percentcomplete"></a>PercentComplete

**PercentComplete**元素描述任务的完成的状态。 
  
```xml
<PercentComplete/>
```

 **双**
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
   
## <a name="text-value"></a>文本值

所需的文本值，该值代表介于 0 和 100 之间的整数。
  
## <a name="remarks"></a>备注

将**PercentComplete**设置为 100 具有相同的效果设置[CompleteDate](completedate.md)元素或设置为**已完成**的[Status](status.md)元素。 在请求中，这些属性的设置至少两个，最后一个处理的属性将确定设置这些元素的值。 例如，如果**PercentComplete**为 100， [CompleteDate](completedate.md)是 2007 年 1 月 1 日和[状态](status.md)为 NotStarted，并且按此顺序流式传输属性，效果将为任务的[状态](status.md)设置为 NotStarted， [CompleteDate](completedate.md)为**null**，并且为 0 的**完成百分比**。 
  
描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
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

