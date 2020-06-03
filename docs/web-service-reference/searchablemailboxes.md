---
title: SearchableMailboxes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eb0a7897-c642-4c93-a238-be03128af54e
description: SearchableMailboxes 元素包含从 GetSearchableMailboxes 请求返回的邮箱的数组。
ms.openlocfilehash: 5de15e1c2ae4a587052f836b189651450a1e7482
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467443"
---
# <a name="searchablemailboxes"></a>SearchableMailboxes

**SearchableMailboxes**元素包含从**GetSearchableMailboxes**请求返回的邮箱的数组。 
  
```XML
<SearchableMailboxes>
   <SearchableMailbox/>
</SearchableMailboxes>
```

 **ArrayOfSearchableMailboxesType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

[SearchableMailbox](searchablemailbox.md)
  
### <a name="parent-elements"></a>父元素

[GetSearchableMailboxesResponse](getsearchablemailboxesresponse.md)
  
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> ||
   

