---
title: ConversationAction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConversationAction
api_type:
- schema
ms.assetid: 9ecea41a-3860-4569-8e9b-284b451fc4e0
description: ConversationAction 元素包含要应用于单个会话的单个操作。
ms.openlocfilehash: 45cd6df3aba94062bd5aa0ddf9367e8cf118dc6b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753579"
---
# <a name="conversationaction"></a>ConversationAction

**ConversationAction**元素包含要应用于单个会话的单个操作。 
  
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

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[操作 (ConversationActionTypeType)](action-conversationactiontypetype.md) <br/> |包含要执行对话[ConversationId](conversationid.md)元素所指定的操作。 此元素必须存在。  <br/> |
|[ConversationId](conversationid.md) <br/> |包含将具有指定应用于对话中的项目的[操作 (ConversationActionTypeType)](action-conversationactiontypetype.md)元素的操作的会话的标识符。 此元素必须存在。  <br/> |
|[ContextFolderId](contextfolderid.md) <br/> |指示使用文件夹的操作的目标文件夹。 此元素必须存在时复制、 删除、 移动和目标文件夹中的对话项目上设置只读的状态。  <br/> |
|[ConversationLastSyncTime](conversationlastsynctime.md) <br/> |包含的日期和对话上次同步的时间。 此元素必须存在时尝试删除接收到指定的时间过去的对话中的所有项目。  <br/> |
|[ProcessRightAway](processrightaway.md) <br/> |指示是否将响应发送只要操作对服务器或是否将响应发送操作完成后启动处理。 此元素必须存在以响应发送异步到请求的操作。  <br/> |
|[DestinationFolderId](destinationfolderid.md) <br/> |指示副本的目标文件夹，并移动操作。  <br/> |
|[类别](categories-ex15websvcsotherref.md) <br/> |包含字符串标识会话中的项目所属的类别的集合。  <br/> |
|[EnableAlwaysDelete](enablealwaysdelete.md) <br/> |指定允许的所有新项目在对话中删除的标志。  <br/> |
|[IsRead](isread.md) <br/> |指示是否已读取一条消息。  <br/> |
|[DeleteType](deletetype.md) <br/> |指示如何删除会话中的项目。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ConversationActions](conversationactions.md) <br/> |包含对话和适用于它们的操作的集合。  <br/> |
   
## <a name="text-value"></a>文本值

**ConversationAction 元素的文本值**

|**值**|**说明**|
|:-----|:-----|
|AlwaysCategorize  <br/> |始终对对话进行分类。  <br/> |
|AlwaysDelete  <br/> |始终删除对话。  <br/> |
|AlwaysMove  <br/> |总是移动对话。  <br/> |
|Delete  <br/> |删除对话。  <br/> |
|移动  <br/> |移动对话。  <br/> |
|复制  <br/> |复制对话。  <br/> |
|SetReadState  <br/> |设置读的对话状态。  <br/> |
|SetRetentionPolicy  <br/> |设置对话的保留策略。  <br/> |
   
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



[ApplyConversationAction 操作](applyconversationaction-operation.md)


- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

