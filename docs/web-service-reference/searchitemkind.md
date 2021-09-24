---
title: SearchItemKind
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 89513c26-b751-4619-a300-0ed8f55b0102
description: SearchItemKind 元素指示为 FindMailboxStatisticsByKeyword 操作搜索的项目类型。
ms.openlocfilehash: 93803d181f32d88c30ab0fa9a72bb92f22907dde
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510853"
---
# <a name="searchitemkind"></a>SearchItemKind

**SearchItemKind** 元素指示为 **FindMailboxStatisticsByKeyword** 操作搜索的项目类型。 
  
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

**SearchItemKind** 元素的文本值是搜索关键字的项目类型。 以下列表包含可在 **SearchItemKind** 元素中使用的文本值。 
  
- **Email** - 指示电子邮件搜索关键字。 
    
- **会议** - 指示在会议中搜索关键字。 
    
- **Tasks** - 指示搜索任务中的关键字。 
    
- **备注** - 指示搜索关键字的注释。 
    
- **Docs** - 指示文档搜索关键字。 
    
- **月** 日 - 指示搜索关键字的日记。 
    
- **联系人** - 指示搜索联系人的关键字。 
    
- **Im** - 指示在即时消息中搜索关键字。 
    
- **语音邮件** - 指示语音邮件搜索关键字。 
    
- **Faxes** - 指示搜索传真的关键字。 
    
- **帖子** - 指示搜索文章的关键字。 
    
- **Rssfeeds** - 指示搜索 RSS 源的关键字。 
    
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> ||
   

