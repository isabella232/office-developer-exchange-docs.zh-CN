---
title: Action （ConversationActionTypeType）
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
description: Action 元素包含要对 ConversationId 元素指定的会话执行的操作。
ms.openlocfilehash: f97b04b98cdc29bee9aff5fa1fc6f37400b8314c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527542"
---
# <a name="action-conversationactiontypetype"></a>Action （ConversationActionTypeType）

**Action**元素包含要对[ConversationId](conversationid.md)元素指定的会话执行的操作。 
  
- [ApplyConversationAction](applyconversationaction.md)
  
- [ConversationActions](conversationactions.md)
  
- [ConversationAction](conversationaction.md)
  
- [Action （ConversationActionTypeType）](action-conversationactiontypetype.md)
  
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

**Action**元素的文本值指示将对对话执行的操作。 以下是可能的文本值和相应的操作： 
  
- **AlwaysCategorize** -将自动使用在 "[类别](categories-ex15websvcsotherref.md)" 元素中标识的类别设置对话中的当前项目和新项目。 
    
- **AlwaysDelete** -将自动删除对话中的当前项目和新项目。 删除模式由[DeleteType](deletetype.md)元素设置。 
    
- **AlwaysMove** -将自动将对话中的当前项目和新项目移至[DestinationFolderId](destinationfolderid.md)元素所标识的文件夹。 
    
- **删除**-对话中的当前项目将被删除。 会话中的后续项目不会被删除。 删除模式由[DeleteType](deletetype.md)元素设置。 
    
- **Move** -对话中的当前项目将被移动到由[DestinationFolderId](destinationfolderid.md)元素标识的文件夹。 会话中的后续项目将不会移动。 
    
- **复制**-将对话中的当前项目复制到由[DestinationFolderId](destinationfolderid.md)元素标识的文件夹。 会话中的后续项目不会被复制。 
    
- **SetReadState** -对话中的当前项目将设置为其读取状态。 读取状态由[IsRead](isread.md)元素设置。 
    
- **标记**-对话中的当前项目的[标志元素所](flag.md)定义的标志。 
    
## <a name="remarks"></a>备注

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

