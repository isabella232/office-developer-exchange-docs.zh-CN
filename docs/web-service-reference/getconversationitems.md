---
title: GetConversationItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 4f7bcd0f-140c-4cbc-a5ed-daeffded1df1
description: GetConversationItems 元素定义一个请求，以通过在同一对话中获取一组相关项目。
ms.openlocfilehash: 0bd792553cbab0c03a6c2cd5bfdbc18dfeba4273
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59538115"
---
# <a name="getconversationitems"></a>GetConversationItems

**GetConversationItems** 元素定义一个请求，以通过在同一对话中获取一组相关项目。 
  
```XML
<GetConversationItems>
   <ItemShape/>
   <FoldersToIgnore/>
   <MaxItemsToReturn/>
   <SortOrder/>
   <MailboxScope/>
   <Conversations/>
</GetConversationItems>
```

 **GetConversationItemsType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

[ItemShape](itemshape.md)  | [FoldersToIgnore](folderstoignore.md)  | [MaxItemsToReturn](maxitemstoreturn.md)  | [SortOrder (ConversationNodeSortOrder) ](sortorder-conversationnodesortorder.md)  | [MailboxScope](mailboxscope.md)  | [对话](conversations-ex15websvcsotherref.md)
  
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |messages.xsd  <br/> |
|可以为空  <br/> |false  <br/> |
   

