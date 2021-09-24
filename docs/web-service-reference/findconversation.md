---
title: FindConversation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FindConversation
api_type:
- schema
ms.assetid: 94b7083c-60cf-478b-a9af-a88f7acb30fb
description: FindConversation 元素定义在邮箱中查找对话的请求。
ms.openlocfilehash: e48e0d9fd71dac12fe6848031b2c056ea9a913ce
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59535168"
---
# <a name="findconversation"></a>FindConversation

**FindConversation** 元素定义在邮箱中查找对话的请求。 
  
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
|浅  <br/> |指示浅表遍历。  <br/> |
|深  <br/> |指示深层遍历。  <br/> |
   
#### <a name="viewfilter-attribute-values"></a>ViewFilter 属性值

****

|**值**|**说明**|
|:-----|:-----|
|全部  <br/> |查找所有对话。  <br/> |
|已标记  <br/> |查找带标记的对话。  <br/> |
|HasAttachment  <br/> |查找带附件的对话。  <br/> |
|ToOrCcMe  <br/> |查找已解决或抄送我的对话。  <br/> |
|未读  <br/> |查找未读对话。  <br/> |
|TaskActive  <br/> |查找活动任务。  <br/> |
|TaskOverdue  <br/> |查找过期任务。  <br/> |
|TaskCompleted  <br/> |查找已完成的任务。  <br/> |
|NoClutter  <br/> |仅供内部使用。  <br/> |
|混乱邮件  <br/> |仅供内部使用。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[IndexedPageItemView](indexedpageitemview.md) <br/> |介绍如何返回分页对话信息。  <br/> |
|[SeekToConditionPageItemView](seektoconditionpageitemview.md) <br/> |指定用于标识搜索结束的条件、搜索的起始索引、要返回的最大条目以及 **FindItem** 或 **FindConversation** 搜索的搜索方向。  <br/> |
|[SortOrder](sortorder.md) <br/> |定义如何在 [FindConversation](findconversation-operation.md) 操作请求中对项目进行排序。 **conversation：LastDeliveryTime** 属性是使用 **FindConversation** 操作时唯一支持进行排序的属性。  <br/> |
|[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) <br/> |标识要搜索对话的文件夹。  <br/> |
|[MailboxScope](mailboxscope.md) <br/> |指定搜索或提取对话应跨越主邮箱、存档邮箱还是同时跨越主邮箱和存档邮箱。  <br/> |
|[QueryString (QueryStringType)](querystring-querystringtype.md) <br/> |指定基于高级查询语法的邮箱查询字符串 (AQS) 。  <br/> |
|[ConversationShape](conversationshape.md) <br/> |标识在 [FindConversation](findconversation-operation.md) 操作响应中要返回的属性集。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>注解

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

