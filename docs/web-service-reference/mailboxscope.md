---
title: MailboxScope
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c9778823-f290-4827-ba19-5f391ed4f877
description: MailboxScope 元素确定对话的搜索或获取是否应跨越主邮箱、存档邮箱或主邮箱和存档邮箱。
ms.openlocfilehash: 92823c06d4fe186917c3cfb532eda821bd6a95a7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455371"
---
# <a name="mailboxscope"></a>MailboxScope

**MailboxScope**元素确定对话的搜索或获取是否应跨越主邮箱、存档邮箱或主邮箱和存档邮箱。 
  
```XML
<MailboxScope> PrimaryOnly | ArchiveOnly | All </MailboxScope>
```

**MailboxSearchLocationType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[FindConversation](findconversation.md)  | [GetConversationItems](getconversationitems.md)  | [对话（ConversationType）](conversation-conversationtype.md)
  
## <a name="text-value"></a>文本值

**MailboxScope**元素的文本值是在整个主邮箱、存档邮箱或主邮箱和存档邮箱中查找或获取项目的作用域。 **PrimaryOnly**的文本值表示针对某个用户的主邮箱的作用域。 **ArchiveOnly**的文本值表示针对某个用户的存档邮箱的作用域。 "**全部**" 文本值表示一个作用域，该作用域面向主邮箱和存档邮箱。 
  
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |false  <br/> |
   

