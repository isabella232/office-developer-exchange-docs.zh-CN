---
title: SearchItemKind
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 89513c26-b751-4619-a300-0ed8f55b0102
description: SearchItemKind 元素指示 FindMailboxStatisticsByKeyword 操作搜索的项目的类型。
ms.openlocfilehash: 1c099fc49ec882c1672b265ff0e3aa2c71c5f95b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827298"
---
# <a name="searchitemkind"></a>SearchItemKind

**SearchItemKind**元素指示**FindMailboxStatisticsByKeyword**操作搜索的项目的类型。 
  
```XML
<SearchItemKind>Email | Meetings | Tasks | Notes | Docs | Journals | Contacts | Im | Voicemail | Faxes | Posts | Rssfeeds</SearchItemKind>
```

 **SearchItemKindType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[MessageTypes](messagetypes.md)
  
## <a name="text-value"></a>文本值

**SearchItemKind**元素的文本值是项目的关键字搜索的类型。 以下列表包含可在**SearchItemKind**元素中的文本值。 
  
- **电子邮件**-指示要搜索的关键字的电子邮件。 
    
- **会议**-指示要搜索的关键字的会议。 
    
- **任务**-指示要搜索的关键字的任务。 
    
- **Notes** -指示说明要搜索的关键字。 
    
- **文档**-指示要搜索的关键字的文档。 
    
- **日志**-指示要搜索的关键字的日志。 
    
- **联系人**-指示要搜索的关键字的联系人。 
    
- **Im** -指示要搜索的关键字的即时消息。 
    
- **语音邮件**-指示要搜索的关键字的语音邮件。 
    
- **传真**-指示要搜索的关键字的传真。 
    
- **文章**-指示要搜索的关键字的文章。 
    
- **Rssfeeds** -指示要搜索的关键字的 RSS 源。 
    
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> ||
   

