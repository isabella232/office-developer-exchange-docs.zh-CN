---
title: 状态
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Status
api_type:
- schema
ms.assetid: 80121e41-291b-4fc0-a55e-6f677d4b5fb5
description: Status 元素表示任务项的状态。
ms.openlocfilehash: 5ec50e3f0c06ad3ec8301ddbe8e7bd249b1e8fe9
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59525538"
---
# <a name="status"></a>状态

**Status** 元素表示任务项的状态。 
  
```xml
<Status/>
```

 **TaskStatusType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[任务](task.md) <br/> |表示 Exchange 存储中的任务。  <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。 以下是此元素的可能文本值：
  
- NotStarted
    
- InProgress
    
- 已完成
    
- WaitingOnOthers
    
- 延迟
    
## <a name="remarks"></a>注解

设置 [CompleteDate](completedate.md) 与将 [PercentComplete](percentcomplete.md) 设置为 100 或 **将 Status** 设置为 **Completed 的效果相同**。 在至少设置其中两个属性的请求中，最后处理的属性将确定为这些元素设置的值。 例如，如果 **PercentComplete** 为 100，CompleteDate 为 1/1/2007，Status 为 NotStarted，并且按此顺序流式处理属性，则效果将为将任务的 **Status** 设置为 NotStarted，**将 CompleteDate** 设置为 **null，** 将 **PercentComplete** 设置为 0。   
  
描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)


[创建任务](https://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[删除任务](https://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

