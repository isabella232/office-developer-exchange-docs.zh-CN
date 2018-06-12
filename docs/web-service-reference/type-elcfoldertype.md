---
title: 类型 (ElcFolderType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6faad98f-1a92-4373-bde5-dd12af61765f
description: Type 元素指定文件夹中保留策略使用的类型。
ms.openlocfilehash: f679a9237a577d26d4b28e1b25f3e135f7193903
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838292"
---
# <a name="type-elcfoldertype"></a>类型 (ElcFolderType)

**Type**元素指定文件夹中保留策略使用的类型。 
  
```XML
<Type> Calendar | Contacts | DeletedItems | Drafts | Inbox | JunkEmail | Journal | Notes | Outbox | SentItems | Tasks | All | ManagedCustomFolder | RssSubscriptions | SyncIssues | ConversationHistory | Personal | RecoverableItems | NonIpmRoot <Type>
```

 **ElcFolderType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[RetentionPolicyTag](retentionpolicytag.md)
  
## <a name="text-value"></a>文本值

**Type**元素的文本值是保留策略中使用的文件夹类型。 文本值可以是下列值表示默认文件夹类型之一： 日历、 联系人、 DeletedItems、 草稿、 收件箱、 JunkEmail、 日志、 注释、 发件箱、 SentItems、 任务所有，ManagedCustomFolder RssSubscriptions、 SyncIssues，ConversationHistory、 个人、 RecoverableItems，或 NonIpmRoot 
  
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |false  <br/> |
   

