---
title: SearchItemKind
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 89513c26-b751-4619-a300-0ed8f55b0102
description: SearchItemKind 元素指示要在其中搜索 FindMailboxStatisticsByKeyword 操作的项目的类型。
ms.openlocfilehash: e0625ac169c3083702494c094da15d38d220fe67
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463998"
---
# <a name="searchitemkind"></a>SearchItemKind

**SearchItemKind**元素指示要在其中搜索**FindMailboxStatisticsByKeyword**操作的项目的类型。 
  
```XML
<SearchItemKind>Email | Meetings | Tasks | Notes | Docs | Journals | Contacts | Im | Voicemail | Faxes | Posts | Rssfeeds</SearchItemKind>
```

 **SearchItemKindType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[MessageTypes](messagetypes.md)
  
## <a name="text-value"></a>文本值

**SearchItemKind**元素的文本值是要搜索关键字的项的类型。 以下列表包含可在**SearchItemKind**元素中使用的文本值。 
  
- **电子**邮件-指示将搜索电子邮件中的关键字。 
    
- **会议**-指示搜索会议的关键字。 
    
- **任务**-指示搜索任务的关键字。 
    
- **备注**-指示搜索笔记中的关键字。 
    
- **文档**-指示搜索文档中的关键字。 
    
- "**日记**"-指示搜索日记以查找关键字。 
    
- **联系人**-表示搜索联系人的关键字。 
    
- **Im** -指示搜索即时消息中的关键字。 
    
- **语音邮件**-指示搜索语音邮件中的关键字。 
    
- "**传真**"-指示搜索传真以查找关键字。 
    
- **帖子**-表示搜索帖子中的关键字。 
    
- **Rssfeeds** -指示将搜索 RSS 源以查找关键字。 
    
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> ||
   

