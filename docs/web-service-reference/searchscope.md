---
title: SearchScope
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 4a53989e-eca6-45c4-afac-4d6ac19597d2
description: SearchScope 元素指定搜索的范围。
ms.openlocfilehash: d4caa87cd552a633812b99d7e97f2419b156fb78
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523396"
---
# <a name="searchscope"></a>SearchScope

**SearchScope** 元素指定搜索的范围。 
  
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

**SearchScope** 元素的文本值指示搜索发现搜索的邮箱类型。 **PrimaryOnly** 的文本值指示已搜索主邮箱。 **ArchiveOnly 的文本** 值指示已搜索存档邮箱。 文本值 **All** 指示同时搜索主邮箱和存档邮箱。 
  
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
   

