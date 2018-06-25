---
title: SeekToConditionPageItemView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b3b86720-d086-47c3-94af-921fdd719edf
description: SeekToConditionPageItemView 元素标识用于标识的末尾搜索、 搜索、 返回，最大条目和 FindItem 或 FindConversation 搜索的搜索方向的起始索引的条件。
ms.openlocfilehash: e95246079f8c6e7acffac1dabb278895265767d9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827328"
---
# <a name="seektoconditionpageitemview"></a>SeekToConditionPageItemView

**SeekToConditionPageItemView**元素标识用于**FindItem**或**FindConversation 标识的末尾搜索、 搜索和返回，最大条目的搜索方向的起始索引的条件**搜索。 
  
```XML
<SeekToConditionPageItemView BasePoint="" MaxEntriesReturned="">
   <Condition/>
</SeekToConditionPageItemView>
```

 **SeekToConditionPageViewType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|基点  <br/> |**基点**属性的文本值是从将在启动搜索基本点。 **开头**的文本值指示搜索将结果集的开头开始。 **结束**文本值指示搜索将结果集末尾开始。  <br/> |
|MaxEntriesReturned  <br/> |**MaxEntriesReturned**属性的文本值是可以在结果集中返回的项的最大数目。  <br/> |
   
### <a name="child-elements"></a>子元素

[条件 (RestrictionType)](condition-restrictiontype.md)
  
### <a name="parent-elements"></a>父元素

[FindConversation](findconversation.md) | [FindItem](finditem.md)
  
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |false  <br/> |
   

