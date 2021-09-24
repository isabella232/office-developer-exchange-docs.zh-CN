---
title: ConversationNodes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 5c8a35b8-a940-4b3e-8768-9ba95766fd79
description: ConversationNodes 元素指定对话节点的集合。
ms.openlocfilehash: 8bacbc83676d9642ae8f842affbc11338cbdff0c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59536622"
---
# <a name="conversationnodes"></a>ConversationNodes

**ConversationNodes** 元素指定对话节点的集合。 
  
```XML
<ConversationNodes>
    <ConversationNode></ConversationNode>
</ConversationNodes>
```

 **ArrayOfConversationNodesType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ConversationNode](conversationnode.md) <br/> |指定对话中的节点。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Conversation (ConversationResponseType)](conversation-conversationresponsetype.md) <br/> |表示 **GetConversationItems 响应中返回的单个** 对话。  <br/> |
   
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |types.xsd  <br/> |
|可以为空  <br/> ||
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

