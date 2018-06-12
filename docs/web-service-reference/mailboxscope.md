---
title: MailboxScope
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c9778823-f290-4827-ba19-5f391ed4f877
description: MailboxScope 元素标识是否搜索或进行对话的提取应跨越主邮箱、 存档邮箱或两个主要并存档邮箱。
ms.openlocfilehash: 89c9776079d686b114d6b744150f1c6df3711eab
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826293"
---
# <a name="mailboxscope"></a>MailboxScope

**MailboxScope**元素标识是否搜索或进行对话的提取应跨越主邮箱、 存档邮箱或两个主要并存档邮箱。 
  
```XML
<MailboxScope> PrimaryOnly | ArchiveOnly | All </MailboxScope>
```

**MailboxSearchLocationType**

## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[FindConversation](findconversation.md) | [GetConversationItems](getconversationitems.md) | [对话 (ConversationType)](conversation-conversationtype.md)
  
## <a name="text-value"></a>文本值

**MailboxScope**元素的文本值是用于查找的作用域或获取项目在任一主邮箱跨对话中，存档邮箱或两个主和存档邮箱。 **PrimaryOnly**文本值表示目标用户的主邮箱的范围。 **ArchiveOnly**文本值表示目标用户的存档邮箱的范围。 文本值的**所有**表示目标的主邮箱和存档邮箱的范围。 
  
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |false  <br/> |
   

