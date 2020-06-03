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
description: FindConversation 元素定义在邮箱中查找对话的请求。
ms.openlocfilehash: 98d692132ed9375d981c95d24600b0e2c4b1d8c1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462645"
---
# <a name="findconversation"></a>FindConversation

**FindConversation**元素定义在邮箱中查找对话的请求。 
  
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

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

****

|**属性**|**说明**|
|:-----|:-----|
|遍历  <br/> |标识子树遍历的类型。 此特性是可选的。  <br/> |
|ViewFilter  <br/> |标识类型视图筛选器。 此特性是可选的。  <br/> |
   
#### <a name="traversal-attribute-values"></a>遍历属性值

****

|**值**|**说明**|
|:-----|:-----|
|浅  <br/> |指示浅遍历。  <br/> |
|深  <br/> |指示深度遍历。  <br/> |
   
#### <a name="viewfilter-attribute-values"></a>ViewFilter 属性值

****

|**值**|**说明**|
|:-----|:-----|
|所有  <br/> |查找所有对话。  <br/> |
|带  <br/> |查找已标记的对话。  <br/> |
|HasAttachment  <br/> |查找有关附件的对话。  <br/> |
|ToOrCcMe  <br/> |查找解决或抄送给我的对话。  <br/> |
|未读  <br/> |查找未读对话。  <br/> |
|TaskActive  <br/> |查找活动任务。  <br/> |
|TaskOverdue  <br/> |查找过期的任务。  <br/> |
|TaskCompleted  <br/> |查找已完成的任务。  <br/> |
|NoClutter  <br/> |仅供内部使用。  <br/> |
|混乱邮件  <br/> |仅供内部使用。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**描述**|
|:-----|:-----|
|[IndexedPageItemView](indexedpageitemview.md) <br/> |介绍如何返回分页对话信息。  <br/> |
|[SeekToConditionPageItemView](seektoconditionpageitemview.md) <br/> |指定用于标识搜索的结束的条件、搜索的起始索引、要返回的最大项数以及**FindItem**或**FindConversation**搜索的搜索说明。  <br/> |
|[SortOrder](sortorder.md) <br/> |定义如何在[FindConversation 操作](findconversation-operation.md)请求中对项目进行排序。 **对话： LastDeliveryTime**属性是在使用**FindConversation**操作时，支持排序的唯一属性。  <br/> |
|[ParentFolderId （TargetFolderIdType）](parentfolderid-targetfolderidtype.md) <br/> |标识用于搜索对话的文件夹。  <br/> |
|[MailboxScope](mailboxscope.md) <br/> |指定对话的搜索或获取是否应跨越主邮箱、存档邮箱或同时位于主邮箱和存档邮箱中。  <br/> |
|[QueryString （QueryStringType）](querystring-querystringtype.md) <br/> |指定基于高级查询语法（AQS）的邮箱查询字符串。  <br/> |
|[ConversationShape](conversationshape.md) <br/> |标识设置为在[FindConversation 操作](findconversation-operation.md)响应中返回的属性。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[FindConversation 操作](findconversation-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)


[Conversations in EWS](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

