---
title: SearchScope
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4a53989e-eca6-45c4-afac-4d6ac19597d2
description: SearchScope 元素指定搜索的范围。
ms.openlocfilehash: df11c8db418ac90d1166030aeed3672c0b810052
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466862"
---
# <a name="searchscope"></a>SearchScope

**SearchScope**元素指定搜索的范围。 
  
```XML
<SearchScope> PrimaryOnly | ArchiveOnly | All </SearchScope>
```

 **MailboxSearchLocationType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[MailboxSearchScope](mailboxsearchscope.md)
  
## <a name="text-value"></a>文本值

**SearchScope**元素的文本值指示要搜索发现搜索的邮箱类型。 **PrimaryOnly**的文本值表示搜索主邮箱。 **ArchiveOnly**的文本值表示已搜索存档邮箱。 Text 值为**All**表示主邮箱和存档邮箱都将被搜索。 
  
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
   

