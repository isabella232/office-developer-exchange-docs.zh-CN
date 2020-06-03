---
title: SeekToConditionPageItemView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b3b86720-d086-47c3-94af-921fdd719edf
description: SeekToConditionPageItemView 元素标识用于标识搜索的结束的条件、搜索的起始索引、要返回的最大项数以及 FindItem 或 FindConversation 搜索的搜索说明。
ms.openlocfilehash: dbb073263740ccdf75367f85f672b7d5ec78f7a0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466834"
---
# <a name="seektoconditionpageitemview"></a>SeekToConditionPageItemView

**SeekToConditionPageItemView**元素标识用于标识搜索的结束的条件、搜索的起始索引、要返回的最大项数以及**FindItem**或**FindConversation**搜索的搜索说明。 
  
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
|BasePoint  <br/> |**BasePoint**属性的文本值是搜索将从该处开始的基点。 文本值为 "**开始**" 指示搜索将从结果集的开头开始。 文本值为**end**表示搜索将从结果集的末尾开始。  <br/> |
|MaxEntriesReturned  <br/> |**MaxEntriesReturned**属性的文本值是在结果集中可返回的最大项目数。  <br/> |
   
### <a name="child-elements"></a>子元素

[条件（RestrictionType）](condition-restrictiontype.md)
  
### <a name="parent-elements"></a>父元素

[FindConversation](findconversation.md)  | [FindItem](finditem.md)
  
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |false  <br/> |
   

