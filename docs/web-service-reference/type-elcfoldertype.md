---
title: Type (ElcFolderType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 6faad98f-1a92-4373-bde5-dd12af61765f
description: Type 元素指定保留策略中使用的文件夹类型。
ms.openlocfilehash: 09e958d56a97b5a169832fe8842276ba0b122243
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517516"
---
# <a name="type-elcfoldertype"></a>Type (ElcFolderType)

**Type** 元素指定保留策略中使用的文件夹类型。 
  
```XML
<Type> Calendar | Contacts | DeletedItems | Drafts | Inbox | JunkEmail | Journal | Notes | Outbox | SentItems | Tasks | All | ManagedCustomFolder | RssSubscriptions | SyncIssues | ConversationHistory | Personal | RecoverableItems | NonIpmRoot <Type>
```

 **ElcFolderType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[RetentionPolicyTag](retentionpolicytag.md)
  
## <a name="text-value"></a>文本值

**Type** 元素的文本值是保留策略中使用的文件夹类型。 文本值可以是表示默认文件夹类型的以下值之一：Calendar、Contacts、DeletedItems、Drafts、Inbox、JunkEmail、Journal、Notes、Outbox、SentItems、Tasks、All、ManagedCustomFolder、RssSubscriptions、SyncIssues、ConversationHistory、Personal、RecoverableItems 或 NonIpmRoot 
  
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |false  <br/> |
   

