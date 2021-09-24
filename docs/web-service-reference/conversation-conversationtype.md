---
title: Conversation (ConversationType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Conversation
api_type:
- schema
ms.assetid: 59d014cd-5886-49ea-8d36-ba5de7e675de
description: Conversation 元素表示单个对话。
ms.openlocfilehash: 7ce75fad17589f4d9a3ca52bcb2041eb1d1f4d2e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515955"
---
# <a name="conversation-conversationtype"></a>Conversation (ConversationType)

**Conversation** 元素表示单个对话。 
  
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

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ConversationId](conversationid.md) <br/> |表示对话的标识符。  <br/> |
|[ConversationTopic](conversationtopic.md) <br/> |表示对话主题。 此元素是只读的。  <br/> |
|[UniqueRecipients](uniquerecipients.md) <br/> |包含从特定文件夹聚合的对话的收件人列表。 此元素是只读的。  <br/> |
|[GlobalUniqueRecipients](globaluniquerecipients.md) <br/> |包含跨邮箱聚合的对话的收件人列表。 此元素是只读的。  <br/> |
|[UniqueUnreadSenders](uniqueunreadsenders.md) <br/> |包含当前文件夹中的此对话中当前未读邮件的所有发送者的列表。 此元素是只读的。  <br/> |
|[GlobalUniqueUnreadSenders](globaluniqueunreadsenders.md) <br/> |包含邮箱中所有文件夹之间发送了当前在此对话中未读的邮件的所有人员的列表。  <br/> |
|[UniqueSenders](uniquesenders.md) <br/> |包含当前文件夹中对话项目的所有发件人的列表。 此元素是只读的。  <br/> |
|[GlobalUniqueSenders](globaluniquesenders.md) <br/> |包含邮箱中会话项目的所有发件人的列表。  <br/> |
|[LastDeliveryTime](lastdeliverytime.md) <br/> |包含当前文件夹中此对话中最后一次接收的邮件的传递时间。  <br/> |
|[GlobalLastDeliveryTime](globallastdeliverytime.md) <br/> |包含邮箱中所有文件夹上一次在此对话中收到的邮件的传递时间。  <br/> |
|[Categories](categories-ex15websvcsotherref.md) <br/> |包含一个字符串集合，这些字符串标识应用于当前文件夹中所有会话项目的类别。  <br/> |
|[GlobalCategories](globalcategories.md) <br/> |包含邮箱中所有会话项目的类别列表。  <br/> |
|[FlagStatus](flagstatus.md) <br/> |包含当前文件夹中会话项目的聚合标志状态。  <br/> |
|[GlobalFlagStatus](globalflagstatus.md) <br/> |包含邮箱中所有会话项目的聚合标志状态。  <br/> |
|[HasAttachments](hasattachments.md) <br/> |包含一个值，该值指示当前文件夹中是否至少有一个对话项目具有附件。  <br/> |
|[GlobalHasAttachments](globalhasattachments.md) <br/> |包含一个值，该值指示邮箱中是否至少有一个对话项目具有附件。  <br/> |
|[MessageCount](messagecount.md) <br/> |包含当前文件夹中的对话项目总数。  <br/> |
|[GlobalMessageCount](globalmessagecount.md) <br/> |包含邮箱中的会话项目总数。  <br/> |
|[UnreadCount](unreadcount.md) <br/> |包含文件夹中未读对话项的计数。  <br/> |
|[GlobalUnreadCount](globalunreadcount.md) <br/> |包含邮箱中所有未读对话项目的计数。  <br/> |
|[尺寸](size.md) <br/> |包含根据当前文件夹中所有对话项目的大小计算的对话大小。  <br/> |
|[GlobalSize](globalsize.md) <br/> |包含根据邮箱中所有会话项目的大小计算的对话大小。  <br/> |
|[ItemClasses (ArrayOfItemClassType)](itemclasses-arrayofitemclasstype.md) <br/> |包含表示当前文件夹中的对话项目的所有项目类的项目类的列表。  <br/> |
|[GlobalItemClasses](globalitemclasses.md) <br/> |包含表示邮箱中会话项目的所有项目类的项目类列表。  <br/> |
|[Importance](importance.md) <br/> |包含当前文件夹中所有对话项目的聚合重要性。  <br/> |
|[GlobalImportance](globalimportance.md) <br/> |包含邮箱中所有会话项目的聚合重要性。  <br/> |
|[ItemIds](itemids.md) <br/> |包含当前文件夹中所有会话项目的项目标识符集合。  <br/> |
|[GlobalItemIds](globalitemids.md) <br/> |包含邮箱中所有会话项目的项目标识符集合。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[对话](conversations-ex15websvcsotherref.md) <br/> |包含 **FindConversation** 响应中返回的对话数组。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
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



[FindConversation Operation](findconversation-operation.md)
  
[ApplyConversationAction 操作](applyconversationaction-operation.md)


[Conversations in EWS](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

