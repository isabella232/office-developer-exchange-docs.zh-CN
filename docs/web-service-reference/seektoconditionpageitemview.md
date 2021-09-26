---
title: SeekToConditionPageItemView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: b3b86720-d086-47c3-94af-921fdd719edf
description: SeekToConditionPageItemView 元素标识用于标识搜索结束的条件、搜索的起始索引、要返回的最大条目以及 FindItem 或 FindConversation 搜索的搜索方向。
ms.openlocfilehash: 6f4797a6b90456a50922db1c829757711816273e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546103"
---
# <a name="seektoconditionpageitemview"></a>SeekToConditionPageItemView

**SeekToConditionPageItemView** 元素标识用于标识搜索结束的条件、搜索的起始索引、要返回的最大条目以及 **FindItem** 或 **FindConversation** 搜索的搜索方向。 
  
```XML
<SeekToConditionPageItemView BasePoint="" MaxEntriesReturned="">
   <Condition/>
</SeekToConditionPageItemView>
```

 **SeekToConditionPageViewType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|BasePoint  <br/> |**BasePoint** 属性的文本值是开始搜索的基点。 Beginning **的文本值指示** 搜索将在搜索的开头结果集。 End **的文本值指示** 搜索将在搜索结束时结果集。  <br/> |
|MaxEntriesReturned  <br/> |**MaxEntriesReturned** 属性的文本值是可返回的最大项目数结果集。  <br/> |
   
### <a name="child-elements"></a>子元素

[Condition (RestrictionType)](condition-restrictiontype.md)
  
### <a name="parent-elements"></a>父元素

[FindConversation](findconversation.md)  | [FindItem](finditem.md)
  
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |false  <br/> |
   

