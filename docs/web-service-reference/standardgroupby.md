---
title: StandardGroupBy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StandardGroupBy
api_type:
- schema
ms.assetid: 04a84f71-b7eb-44dc-ac2c-ed504b52c463
description: StandardGroupBy 元素表示分组 FindItem 操作的标准分组和聚合机制。
ms.openlocfilehash: 3e135feba322979de3d66d5a45d423654ccc9100
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467555"
---
# <a name="standardgroupby"></a>StandardGroupBy

**StandardGroupBy**元素表示分组 FindItem 操作的标准分组和聚合机制。 
  
[FindItem](finditem.md)
  
[DistinguishedGroupBy](distinguishedgroupby.md)
  
[StandardGroupBy](standardgroupby.md)
  
```xml
<StandardGroupBy/>
```

 **StandardGroupByType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[DistinguishedGroupBy](distinguishedgroupby.md) <br/> |提供 FindItem 查询的标准分组。  <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。 可用于此元素的唯一值是**ConversationTopic**。 **ConversationTopic**按邮件分组： ConversationTopic 和项目合计： DateTimeReceived （最大值）。 有关聚合的详细信息，请参阅[AggregateOn](aggregateon.md)。
  
## <a name="remarks"></a>说明

描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[FindItem 操作](finditem-operation.md)
  
[FindItem](finditem.md)


[查找项目](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

