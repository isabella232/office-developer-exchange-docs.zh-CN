---
title: MailboxSearchScope
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: ef4a4203-61e5-46b8-9fa4-d1a10e785aa2
description: MailboxSearchScope 元素指定发现搜索的邮箱和搜索范围。
ms.openlocfilehash: 832992e4e1dcf96029be4228906b2762f11f3fbe
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544120"
---
# <a name="mailboxsearchscope"></a>MailboxSearchScope

**MailboxSearchScope** 元素指定发现搜索的邮箱和搜索范围。 
  
```XML
<MailboxSearchScope>
   <Mailbox/>
   <SearchScope/>
<MailboxSearchScope>
```

**MailboxSearchScopeType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

[邮箱 (字符串) ](mailbox-string.md)  | [SearchScope](searchscope.md)
  
### <a name="parent-elements"></a>父元素

[MailboxSearchScopes](mailboxsearchscopes.md)
  
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
   

