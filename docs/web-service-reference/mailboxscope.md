---
title: MailboxScope
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: c9778823-f290-4827-ba19-5f391ed4f877
description: MailboxScope 元素标识搜索或提取对话应跨越主邮箱、存档邮箱还是同时跨越主邮箱和存档邮箱。
ms.openlocfilehash: 705c72ae2aefbb16599f392eb712d080668490b0
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522878"
---
# <a name="mailboxscope"></a>MailboxScope

**MailboxScope** 元素标识搜索或提取对话应跨越主邮箱、存档邮箱还是同时跨越主邮箱和存档邮箱。 
  
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

[FindConversation](findconversation.md)  | [GetConversationItems](getconversationitems.md)  | [Conversation (ConversationType) ](conversation-conversationtype.md)
  
## <a name="text-value"></a>文本值

**MailboxScope** 元素的文本值是跨主邮箱、存档邮箱或主邮箱和存档邮箱查找或获取对话中的项目的范围。 **PrimaryOnly** 的文本值指示面向用户的主邮箱的范围。 **ArchiveOnly 的文本** 值指示面向用户的存档邮箱的范围。 文本值 **All** 指示同时面向主邮箱和存档邮箱的作用域。 
  
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |false  <br/> |
   

