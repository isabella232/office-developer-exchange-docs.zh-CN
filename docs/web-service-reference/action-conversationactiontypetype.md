---
title: 操作 (ConversationActionTypeType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Action
api_type:
- schema
ms.assetid: 8bbc12f2-76c5-4fda-828f-56b2086a0454
description: Action 元素包含要执行对话 ConversationId 元素所指定的操作。
ms.openlocfilehash: b468eeaf0c2509bfa53cbd83f497f0bae20a7f68
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753091"
---
# <a name="action-conversationactiontypetype"></a>操作 (ConversationActionTypeType)

**Action**元素包含要执行对话[ConversationId](conversationid.md)元素所指定的操作。 
  
- [ApplyConversationAction](applyconversationaction.md)
  
- [ConversationActions](conversationactions.md)
  
- [ConversationAction](conversationaction.md)
  
- [操作 (ConversationActionTypeType)](action-conversationactiontypetype.md)
  
```XML
<Action> AlwaysCategorize | AlwaysDelete | AlwaysMove | Delete | Move | Copy | SetReadState </Action>
```

 **ConversationActionTypeType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ConversationAction](conversationaction.md) <br/> |包含要应用于单个会话的单个操作。  <br/> |
   
## <a name="text-value"></a>文本值

**Action**元素的文本值指示将会话上执行哪些操作。 以下是可能的文本值和相应的操作： 
  
- [Categories](categories-ex15websvcsotherref.md)元素中标识的类别与将自动设置**AlwaysCategorize** -的当前项和会话中的新项目。 
    
- 将自动删除**AlwaysDelete** -的当前项和会话中的新项目。 删除模式设置[DeleteType](deletetype.md)元素。 
    
- **AlwaysMove** -的当前项和会话中的新项目将自动移动到[DestinationFolderId](destinationfolderid.md)元素标识的文件夹。 
    
- **删除**-对话中的当前项将被删除。 对话中的后续项目将不会被删除。 删除模式设置[DeleteType](deletetype.md)元素。 
    
- **移动**-对话中的当前项目将移动到[DestinationFolderId](destinationfolderid.md)元素标识的文件夹中。 对话中的后续项目将不移动。 
    
- **复制**-对话中的当前项将复制到由[DestinationFolderId](destinationfolderid.md)元素标识的文件夹。 对话中的后续项目不会复制。 
    
- **SetReadState** -对话中的当前项将有设置其只读的状态。 由[IsRead](isread.md)元素设置的只读的状态。 
    
- **标志**的对话中的当前项会设置由[标志](flag.md)元素定义的标志。 
    
## <a name="remarks"></a>备注

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [ApplyConversationAction 操作](applyconversationaction-operation.md)
- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

