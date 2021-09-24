---
title: Action (ConversationActionTypeType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Action
api_type:
- schema
ms.assetid: 8bbc12f2-76c5-4fda-828f-56b2086a0454
description: Action 元素包含对 ConversationId 元素指定的对话执行的操作。
ms.openlocfilehash: e75d9d5df75894d1de9831b0022269e7ace4fa63
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514891"
---
# <a name="action-conversationactiontypetype"></a>Action (ConversationActionTypeType)

**Action** 元素包含对 [ConversationId](conversationid.md)元素指定的对话执行的操作。 
  
- [ApplyConversationAction](applyconversationaction.md)
  
- [ConversationActions](conversationactions.md)
  
- [ConversationAction](conversationaction.md)
  
- [Action (ConversationActionTypeType)](action-conversationactiontypetype.md)
  
```XML
<Action> AlwaysCategorize | AlwaysDelete | AlwaysMove | Delete | Move | Copy | SetReadState </Action>
```

 **ConversationActionTypeType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ConversationAction](conversationaction.md) <br/> |包含要应用于单个对话的单个操作。  <br/> |
   
## <a name="text-value"></a>文本值

**Action** 元素的文本值指示将在对话中执行的操作。 以下是可能的文本值和相应的操作： 
  
- **AlwaysCategorize** - 对话中的当前项目和新项将自动使用 Categories 元素中标识的 [类别进行](categories-ex15websvcsotherref.md) 设置。 
    
- **AlwaysDelete** - 对话中的当前项目和新项将自动删除。 删除模式由 [DeleteType 元素](deletetype.md) 设置。 
    
- **AlwaysMove** - 对话中的当前项目和新项将自动移动到 [DestinationFolderId](destinationfolderid.md) 元素标识的文件夹。 
    
- **Delete** - 将删除对话中的当前项目。 不会删除对话中的后续项目。 删除模式由 [DeleteType 元素](deletetype.md) 设置。 
    
- **Move** - 对话中的当前项目将移动到 [DestinationFolderId](destinationfolderid.md) 元素标识的文件夹。 不会移动对话中的后续项目。 
    
- **Copy** - 对话中的当前项目将复制到 [DestinationFolderId](destinationfolderid.md) 元素标识的文件夹。 不会复制对话中的后续项目。 
    
- **SetReadState** - 对话中的当前项目将设置其读取状态。 读取状态由 [IsRead 元素](isread.md) 设置。 
    
- **Flag** - 对话中的当前项目将具有由 Flag 元素定义的 [标记](flag.md) 。 
    
## <a name="remarks"></a>注解

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [ApplyConversationAction 操作](applyconversationaction-operation.md)
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

