---
title: ConversationLastSyncTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConversationLastSyncTime
api_type:
- schema
ms.assetid: 90f8f9e3-5fc6-4a6a-bdfb-fc91fa51f8a2
description: ConversationLastSyncTime 元素包含上次同步会话的日期和时间。 在尝试删除会话中的所有已收到指定时间的项目时，必须存在此元素。
ms.openlocfilehash: f7cc6e205ab9936685d7b8c1f34129b799a53021
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461427"
---
# <a name="conversationlastsynctime"></a>ConversationLastSyncTime

**ConversationLastSyncTime**元素包含上次同步会话的日期和时间。 在尝试删除会话中的所有已收到指定时间的项目时，必须存在此元素。 
  
[ApplyConversationAction](applyconversationaction.md)
  
[ConversationActions](conversationactions.md)
  
[ConversationAction](conversationaction.md)
  
[ConversationLastSyncTime](conversationlastsynctime.md)
  
```XML
<ConversationLastSyncTime/>
```

 **xs： dateTime**
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

**ConversationLastSyncTime**的文本值指示上次同步会话的时间。 
  
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



[ApplyConversationAction 操作](applyconversationaction-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

