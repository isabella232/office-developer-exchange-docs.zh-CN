---
title: SearchDumpster
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: ddb62dce-c87a-4714-8023-a6b697a29699
description: SearchDumpster 元素指定是否在垃圾站中Exchange搜索。
ms.openlocfilehash: 4d8f05393691e38e3a4154e955d03c8591064a1a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521688"
---
# <a name="searchdumpster"></a>SearchDumpster

**SearchDumpster** 元素指定是否在垃圾站中Exchange搜索。 
  
```XML
<SearchDumpster> true | false </SearchDumpster>
```

 ****
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[FindMailboxStatisticsByKeywords](findmailboxstatisticsbykeywords.md)
  
## <a name="text-value"></a>文本值

**SearchDumpster** 元素的文本值 **true** 指示邮箱统计信息搜索包括 Exchange Dumpster。 false **值表示** 不Exchange垃圾站。 
  
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
   

