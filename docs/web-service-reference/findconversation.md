---
title: FindConversation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindConversation
api_type:
- schema
ms.assetid: 94b7083c-60cf-478b-a9af-a88f7acb30fb
description: FindConversation 元素定义查找邮箱中的对话的请求。
ms.openlocfilehash: 990e15f468f836d51977329c524acb439014da95
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754323"
---
# <a name="findconversation"></a>FindConversation

**FindConversation**元素定义查找邮箱中的对话的请求。 
  
[FindConversation](findconversation.md)
  
```XML
<FindConversation Traversal="" ViewFilter="">
   <IndexedPageItemView/>
   <SeekToConditionPageItemView/>
   <SortOrder/>
   <ParentFolderId/>
   <MailboxScope/>
   <QueryString/>
   <ConversationShape/>
</FindConversation>
```

 **FindConversationType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

****

|**属性**|**说明**|
|:-----|:-----|
|遍历  <br/> |标识子树遍历的类型。 此属性是可选的。  <br/> |
|过滤  <br/> |标识类型视图筛选器。 此属性是可选的。  <br/> |
   
#### <a name="traversal-attribute-values"></a>遍历属性值

****

|**值**|**说明**|
|:-----|:-----|
|浅  <br/> |指示浅遍历。  <br/> |
|深  <br/> |指示遍历。  <br/> |
   
#### <a name="viewfilter-attribute-values"></a>过滤属性值

****

|**值**|**说明**|
|:-----|:-----|
|所有  <br/> |查找所有对话。  <br/> |
|标记  <br/> |查找已标记的对话。  <br/> |
|HasAttachment  <br/> |查找与附件的对话。  <br/> |
|ToOrCcMe  <br/> |发送的对话或抄送将我的查找。  <br/> |
|Unread  <br/> |查找未读的对话。  <br/> |
|TaskActive  <br/> |了解活动的任务。  <br/> |
|TaskOverdue  <br/> |查找过期任务。  <br/> |
|TaskCompleted  <br/> |查找已完成的任务。  <br/> |
|NoClutter  <br/> |仅供内部使用。  <br/> |
|混乱  <br/> |仅供内部使用。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[IndexedPageItemView](indexedpageitemview.md) <br/> |介绍如何分页的对话将返回的信息。  <br/> |
|[SeekToConditionPageItemView](seektoconditionpageitemview.md) <br/> |指定用于标识的末尾搜索、 搜索、 返回，最大条目和**FindItem**或**FindConversation**搜索的搜索方向的起始索引的条件。  <br/> |
|[SortOrder](sortorder.md) <br/> |定义项[FindConversation 操作](findconversation-operation.md)请求中的排序方式。 **对话： LastDeliveryTime**属性是排序使用**FindConversation**操作时支持的唯一属性。  <br/> |
|[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) <br/> |标识要搜索的对话的文件夹。  <br/> |
|[MailboxScope](mailboxscope.md) <br/> |指定搜索或进行对话的提取是否应跨越主邮箱、 存档邮箱或两个主要和存档邮箱。  <br/> |
|[查询字符串 (QueryStringType)](querystring-querystringtype.md) <br/> |指定基于上高级查询语法 (AQS) 的邮箱查询字符串。  <br/> |
|[ConversationShape](conversationshape.md) <br/> |标识设置[FindConversation 操作](findconversation-operation.md)响应中返回的属性。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>备注

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[FindConversation Operation](findconversation-operation.md)


- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)


[Conversations in EWS](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

