---
title: SortOrder （ConversationNodeSortOrder）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f9c4295c-8089-4533-b92f-2051eae9afeb
description: SortOrder 元素指定用于 GetConversationItems 请求结果的排序顺序。
ms.openlocfilehash: 69d362b9f769749bcc9692825b64ff486e8b60a0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530963"
---
# <a name="sortorder-conversationnodesortorder"></a>SortOrder （ConversationNodeSortOrder）

**SortOrder**元素指定用于**GetConversationItems**请求结果的排序顺序。 
  
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

**SortOrder**元素的文本值是排列对话的顺序。 **TreeOrderAscending**的文本值表示按升序顺序对对话进行排序。 **TreeOrderDescending**的文本值表示按降序顺序对对话进行排序。 **DateOrderAscending**的文本值表示按照按升序排序的会话日期对对话进行排序。 **DateOrderDescending**的文本值表示根据会话日期的降序对对话进行排序。 
  
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> ||
   

