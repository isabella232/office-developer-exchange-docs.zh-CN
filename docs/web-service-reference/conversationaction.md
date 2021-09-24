---
title: ConversationAction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ConversationAction
api_type:
- schema
ms.assetid: 9ecea41a-3860-4569-8e9b-284b451fc4e0
description: ConversationAction 元素包含要应用于单个对话的单个操作。
ms.openlocfilehash: 04af68b4ad8442160792fd3aa9f3259058a0f3a4
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59531104"
---
# <a name="conversationaction"></a>ConversationAction

**ConversationAction** 元素包含要应用于单个对话的单个操作。 
  
[ApplyConversationAction](applyconversationaction.md)
  
[ConversationActions](conversationactions.md)
  
[ConversationAction](conversationaction.md)
  
```XML
<ConversationAction>
   <Action/>
   <ConversationId/>
   <ContextFolderId/>
   <ConversationLastSyncTime/>
   <ProcessRightAway/>
   <DestinationFolderId/>
   <Categories/>
   <EnableAlwaysDelete/>
   <IsRead/>
   <DeleteType/>
</ConversationAction>
```

 **ConversationActionType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Action (ConversationActionTypeType)](action-conversationactiontypetype.md) <br/> |包含对 [ConversationId](conversationid.md) 元素指定的对话执行的操作。 此元素必须存在。  <br/> |
|[ConversationId](conversationid.md) <br/> |包含将具有 Action 指定的操作的对话的标识符 ([ConversationActionTypeType ](action-conversationactiontypetype.md)) 应用于对话中的项目。 此元素必须存在。  <br/> |
|[ContextFolderId](contextfolderid.md) <br/> |指示针对使用文件夹的操作的文件夹。 在复制、删除、移动和设置目标文件夹中的对话项的读取状态时，此元素必须存在。  <br/> |
|[ConversationLastSyncTime](conversationlastsynctime.md) <br/> |包含对话上次同步的日期和时间。 尝试删除对话中截至指定时间接收的所有项目时，必须存在此元素。  <br/> |
|[ProcessRightAway](processrightaway.md) <br/> |指示操作开始在服务器上进行处理后是否立即发送响应，或者是否在操作完成后发送响应。 此元素必须存在，响应以异步方式发送到请求的操作。  <br/> |
|[DestinationFolderId](destinationfolderid.md) <br/> |指示复制和移动操作的目标文件夹。  <br/> |
|[Categories](categories-ex15websvcsotherref.md) <br/> |包含字符串的集合，这些字符串标识对话中的项目所属的类别。  <br/> |
|[EnableAlwaysDelete](enablealwaysdelete.md) <br/> |指定一个标志，该标志允许删除对话中所有新项。  <br/> |
|[IsRead](isread.md) <br/> |指示是否已阅读邮件。  <br/> |
|[DeleteType](deletetype.md) <br/> |指示如何删除对话中的项目。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ConversationActions](conversationactions.md) <br/> |包含对话集合以及要应用于对话的操作。  <br/> |
   
## <a name="text-value"></a>文本值

**ConversationAction 元素文本值**

|**值**|**说明**|
|:-----|:-----|
|AlwaysCategorize  <br/> |始终对会话进行分类。  <br/> |
|AlwaysDelete  <br/> |始终删除对话。  <br/> |
|AlwaysMove  <br/> |始终移动对话。  <br/> |
|删除  <br/> |删除对话。  <br/> |
|移动  <br/> |移动对话。  <br/> |
|复制  <br/> |复制对话。  <br/> |
|SetReadState  <br/> |设置对话的读取状态。  <br/> |
|SetRetentionPolicy  <br/> |设置对话的保留策略。  <br/> |
   
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



[ApplyConversationAction 操作](applyconversationaction-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

