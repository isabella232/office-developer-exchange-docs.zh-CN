---
title: ConversationNode
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: b7f7acd3-ed65-441e-9976-8b4ed5f12c0b
description: ConversationNode 元素指定对话中的节点。
ms.openlocfilehash: 2668d3cfaa8b43812a4a20ab8d92f419d636e368
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510356"
---
# <a name="conversationnode"></a>ConversationNode

**ConversationNode** 元素指定对话中的节点。 
  
```XML
<ConversationNode>
    <InternetMessageId></InternetMessageId>
    <ParentInternetMessageId></ParentInternetMessageId>
    <Items></Items>
</ConversationNode>
```

 **ConversationNodeType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[InternetMessageId](internetmessageid.md) <br/> |表示项目的 Internet 邮件标识符。  <br/> |
|[ParentInternetMessageId](parentinternetmessageid.md) <br/> |指定父 Internet 邮件的标识符。  <br/> |
|[ItemIds (NonEmptyArrayOfItemIdsType)](itemids-nonemptyarrayofitemidstype.md) <br/> |指定对话节点中所有的项目。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ConversationNodes](conversationnodes.md) <br/> |指定对话节点的集合。  <br/> |
   
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |types.xsd  <br/> |
|可以为空  <br/> ||
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

