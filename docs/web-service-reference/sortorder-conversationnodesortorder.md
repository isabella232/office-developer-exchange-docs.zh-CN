---
title: SortOrder (ConversationNodeSortOrder)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f9c4295c-8089-4533-b92f-2051eae9afeb
description: SortOrder 元素指定用于 GetConversationItems 请求结果的排序顺序。
ms.openlocfilehash: 0091968f1359b0cf744525139b5c6a8cf1687d81
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544673"
---
# <a name="sortorder-conversationnodesortorder"></a>SortOrder (ConversationNodeSortOrder)

**SortOrder** 元素指定用于 **GetConversationItems** 请求结果的排序顺序。 
  
```XML
<SortOrder>TreeOrderAscending | TreeOrderDescending | DateOrderAscending | DateOrderDescending</SortOrder>
```

 **ConversationNodeSortOrder**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[GetConversationItems](getconversationitems.md)
  
## <a name="text-value"></a>文本值

**SortOrder** 元素的文本值是对话的排序顺序。 **TreeOrderAscending** 的文本值指示对话是按照对话树按升序排序的。 **TreeOrderDescending** 的文本值指示对话是按照对话树按降序排序的。 **DateOrderAscending** 的文本值指示对话按对话日期的升序排序。 **DateOrderDescending** 的文本值指示对话按对话日期按降序排序。 
  
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> ||
   

