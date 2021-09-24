---
title: MailboxStat
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 5f24dc30-3ac2-4c82-9dfc-be9dbdb585be
description: MailboxStat 元素指定由发现搜索搜索的邮箱的统计信息。
ms.openlocfilehash: d48f033df4cfec47313ce690acd19d916b963c00
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522808"
---
# <a name="mailboxstat"></a>MailboxStat

**MailboxStat** 元素指定由发现搜索搜索的邮箱的统计信息。 
  
```XML
<MailboxStat>
   <MailboxId/>
   <DisplayName/>
   <ItemCount/>
   <Size/>
</MailboxStat>
```

**MailboxStatisticsItemType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

[MailboxId](mailboxid.md)  | [DisplayName (字符串) ](displayname-string.md)  | [ItemCount](itemcount.md)  | [大小 (长) ](size-long.md)
  
### <a name="parent-elements"></a>父元素

[MailboxStats](mailboxstats.md)
  
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
   

