---
title: 对话 (ConversationType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Conversation
api_type:
- schema
ms.assetid: 59d014cd-5886-49ea-8d36-ba5de7e675de
description: 对话元素均表示一个对话。
ms.openlocfilehash: e1ae055d6a77fc5a9b483341830b978e0c1a5b5a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753580"
---
# <a name="conversation-conversationtype"></a>对话 (ConversationType)

**对话**元素均表示一个对话。 
  
[FindConversationResponse](findconversationresponse.md)
  
[Conversations](conversations-ex15websvcsotherref.md)
  
[对话 (ConversationType)](conversation-conversationtype.md)
  
```XML
<Conversation>
   <ConversationId/>
   <ConversationTopic/>
   <UniqueRecipients/>
   <GlobalUniqueRecipients/>
   <UniqueUnreadSenders/>
   <GlobalUniqueUnreadSenders/>
   <UniqueSenders/>
   <GlobalUniqueSenders/>
   <LastDeliveryTime/>
   <GlobalLastDeliveryTime/>
   <Categories/>
   <GlobalCategories/>
   <FlagStatus/>
   <GlobalFlagStatus/>
   <HasAttachments/>
   <GlobalHasAttachments/>
   <MessageCount/>
   <GlobalMessageCount/>
   <UnreadCount/>
   <GlobalUnreadCount/>
   <Size/>   <GlobalSize/>
   <ItemClasses/>
   <GlobalItemClasses/>
   <Importance/>
   <GlobalImportance/>
   <ItemIds/>
   <GlobalItemIds/>
</Conversation>
```

 **ConversationType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ConversationId](conversationid.md) <br/> |表示对话的标识符。  <br/> |
|[ConversationTopic](conversationtopic.md) <br/> |代表对话主题。 此元素是只读的。  <br/> |
|[UniqueRecipients](uniquerecipients.md) <br/> |包含特定文件夹从聚合对话的收件人列表。 此元素是只读的。  <br/> |
|[GlobalUniqueRecipients](globaluniquerecipients.md) <br/> |包含跨邮箱聚合对话的收件人列表。 此元素是只读的。  <br/> |
|[UniqueUnreadSenders](uniqueunreadsenders.md) <br/> |包含所有已发送邮件的当前文件夹中的此对话中当前未读的人员列表。 此元素是只读的。  <br/> |
|[GlobalUniqueUnreadSenders](globaluniqueunreadsenders.md) <br/> |包含所有已发送邮件的邮箱中的所有文件夹中的当前未读此对话中的人员列表。  <br/> |
|[UniqueSenders](uniquesenders.md) <br/> |包含当前文件夹中的会话项目的所有发件人的列表。 此元素是只读的。  <br/> |
|[GlobalUniqueSenders](globaluniquesenders.md) <br/> |包含所有发件人的邮箱中的会话项目的列表。  <br/> |
|[LastDeliveryTime](lastdeliverytime.md) <br/> |包含上次当前文件夹中的此对话中收到的邮件的传递时间。  <br/> |
|[GlobalLastDeliveryTime](globallastdeliverytime.md) <br/> |包含在邮箱中的所有文件夹上次此对话中收到的邮件的传递时间。  <br/> |
|[类别](categories-ex15websvcsotherref.md) <br/> |包含字符串标识应用于当前文件夹中的所有对话项目的类别的集合。  <br/> |
|[GlobalCategories](globalcategories.md) <br/> |包含在邮箱中的所有对话项目类别列表。  <br/> |
|[FlagStatus](flagstatus.md) <br/> |包含当前文件夹中的会话项目的聚合的标志状态。  <br/> |
|[GlobalFlagStatus](globalflagstatus.md) <br/> |包含聚合的标志状态的邮箱中的所有对话项。  <br/> |
|[HasAttachments](hasattachments.md) <br/> |包含一个值，指示当前文件夹中的至少一个对话项目是否包含附件。  <br/> |
|[GlobalHasAttachments](globalhasattachments.md) <br/> |包含一个值，指示是否为邮箱中的至少一个对话项目包含附件。  <br/> |
|[MessageCount](messagecount.md) <br/> |包含当前文件夹中的会话项目的总数。  <br/> |
|[GlobalMessageCount](globalmessagecount.md) <br/> |包含邮箱中的对话项目的总数。  <br/> |
|[UnreadCount](unreadcount.md) <br/> |包含文件夹中的未读的对话项目的计数。  <br/> |
|[GlobalUnreadCount](globalunreadcount.md) <br/> |包含邮箱中的所有未读的对话项目的计数。  <br/> |
|[Size](size.md) <br/> |包含来自当前文件夹中的所有对话项目的大小计算出的对话大小。  <br/> |
|[GlobalSize](globalsize.md) <br/> |包含计算从邮箱中的所有对话项目的大小的对话的大小。  <br/> |
|[ItemClasses (ArrayOfItemClassType)](itemclasses-arrayofitemclasstype.md) <br/> |包含列表项类的值，该值代表当前文件夹中的会话项目的所有项类。  <br/> |
|[GlobalItemClasses](globalitemclasses.md) <br/> |包含列表项类的值，该值代表的邮箱中的会话项目的所有项类。  <br/> |
|[Importance](importance.md) <br/> |包含当前文件夹中的所有对话项目的聚合的重要性。  <br/> |
|[GlobalImportance](globalimportance.md) <br/> |包含聚合的邮箱中的所有对话项目的重要性。  <br/> |
|[ItemIds](itemids.md) <br/> |包含当前文件夹中的所有对话项目的项标识符的集合。  <br/> |
|[GlobalItemIds](globalitemids.md) <br/> |包含的项标识符的邮箱中的所有对话项的集合。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Conversations](conversations-ex15websvcsotherref.md) <br/> |包含数组**FindConversation**响应中返回的对话。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
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



[FindConversation Operation](findconversation-operation.md)
  
[ApplyConversationAction 操作](applyconversationaction-operation.md)


[Conversations in EWS](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

