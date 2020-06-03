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
description: ConversationAction 元素包含要应用于单个对话的单个操作。
ms.openlocfilehash: cb7d874f787b105d5185749dfaf1e940d2411d89
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529250"
---
# <a name="conversationaction"></a>ConversationAction

**ConversationAction**元素包含要应用于单个对话的单个操作。 
  
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

|**元素**|**描述**|
|:-----|:-----|
|[Action （ConversationActionTypeType）](action-conversationactiontypetype.md) <br/> |包含要对[ConversationId](conversationid.md)元素指定的会话执行的操作。 此元素必须存在。  <br/> |
|[ConversationId](conversationid.md) <br/> |包含会话的标识符，该会话将具有应用于对话中项目的[操作（ConversationActionTypeType）](action-conversationactiontypetype.md)元素指定的操作。 此元素必须存在。  <br/> |
|[ContextFolderId](contextfolderid.md) <br/> |指示针对使用文件夹的操作的文件夹。 在复制、删除、移动和设置目标文件夹中会话项的读取状态时，必须存在此元素。  <br/> |
|[ConversationLastSyncTime](conversationlastsynctime.md) <br/> |包含上次同步会话的日期和时间。 在尝试删除会话中的所有已收到指定时间的项目时，必须存在此元素。  <br/> |
|[ProcessRightAway](processrightaway.md) <br/> |指示是否在操作在服务器上开始处理时立即发送响应，或者在操作完成后是否发送响应。 必须存在此元素，才能将异步向请求的操作发送异步响应。  <br/> |
|[DestinationFolderId](destinationfolderid.md) <br/> |指示复制和移动操作的目标文件夹。  <br/> |
|[类别](categories-ex15websvcsotherref.md) <br/> |包含一个字符串集合，这些字符串标识对话中的项目所属的类别。  <br/> |
|[EnableAlwaysDelete](enablealwaysdelete.md) <br/> |指定对对话中的所有新项目启用删除的标志。  <br/> |
|[IsRead](isread.md) <br/> |指示是否已阅读邮件。  <br/> |
|[DeleteType](deletetype.md) <br/> |指示如何删除对话中的项目。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**描述**|
|:-----|:-----|
|[ConversationActions](conversationactions.md) <br/> |包含对话的集合以及要应用于它们的操作。  <br/> |
   
## <a name="text-value"></a>文本值

**ConversationAction 元素文本值**

|**值**|**说明**|
|:-----|:-----|
|AlwaysCategorize  <br/> |始终对对话进行分类。  <br/> |
|AlwaysDelete  <br/> |始终删除对话。  <br/> |
|AlwaysMove  <br/> |始终移动对话。  <br/> |
|Delete  <br/> |删除对话。  <br/> |
|移动  <br/> |移动对话。  <br/> |
|复制  <br/> |复制对话。  <br/> |
|SetReadState  <br/> |设置对话的读取状态。  <br/> |
|SetRetentionPolicy  <br/> |设置会话的保留策略。  <br/> |
   
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

