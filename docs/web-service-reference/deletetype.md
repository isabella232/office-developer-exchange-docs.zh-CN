---
title: DeleteType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteType
api_type:
- schema
ms.assetid: 6e3136cd-9cb4-493a-aa85-9678f719002d
description: DeleteType 元素指示如何删除会话中的项目。
ms.openlocfilehash: abaa0c3d8b7001b2f42a38d1c82475edba32d2c5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753814"
---
# <a name="deletetype"></a>DeleteType

**DeleteType**元素指示如何删除会话中的项目。 
  
- [ApplyConversationAction](applyconversationaction.md)  
- [ConversationActions](conversationactions.md)  
- [ConversationAction](conversationaction.md)  
- [DeleteType](deletetype.md)
  
```XML
<DeleteType> HardDelete | MoveToDeletedItems | SoftDelete </DeleteType>
```

 **DisposalType**
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

**DeleteType**元素的文本值指示如何删除会话中的项目。 以下是可能的文本值： 
  
- HardDelete-指示邮箱数据库从对话中的项目被永久删除。
    
- MoveToDeleteItems-指示对话中的项目已移动到已删除邮件文件夹。
    
- SoftDelete-指示对话中的项目是否已移动到转储程序如果转储程序已启用。
    
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

