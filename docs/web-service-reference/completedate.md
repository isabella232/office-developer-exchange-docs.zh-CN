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
description: CompleteDate 元素表示项目完成的日期。
ms.openlocfilehash: fff3d5d3105bf63c9cdd34cbcf828d57ca287b86
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461420"
---
# <a name="completedate"></a>CompleteDate

**CompleteDate**元素表示项目完成的日期。 
  
```xml
<CompleteDate/>
```

 **DateTime**
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
|[Flag](flag.md) <br/> |指定邮箱项目的标志。  <br/> |
   
## <a name="text-value"></a>文本值

如果使用此元素，则表示日期和时间的文本值是必需的。
  
## <a name="remarks"></a>备注

设置**CompleteDate**与将[百分比](percentcomplete.md)设置为100或将[状态](status.md)设置为 "已**完成**" 具有相同的效果。 在设置至少两个属性中的一个请求中，最后处理的属性将确定为这些元素设置的值。 例如，如果[百分比](percentcomplete.md)为100，则**CompleteDate**为 2007 1 月1日，且[状态](status.md)为**NotStarted**，并且按该顺序对属性进行了流式处理，则效果是将任务的[状态](status.md)设置为**NotStarted**，将[CompleteDate](completedate.md)设置为 null，[并将](percentcomplete.md)**值**为0。 
  
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


[创建任务](https://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[删除任务](https://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

