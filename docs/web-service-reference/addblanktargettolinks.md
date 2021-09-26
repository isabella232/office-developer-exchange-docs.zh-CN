---
title: AddBlankTargetToLinks
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 30180298-2501-4369-9b8f-2f7663f02336
description: AddBlankTargetToLinks 元素指定 HTML 链接中的目标属性设置为打开一个新窗口。
ms.openlocfilehash: c8d7a5973e60e43638472b0da29842ce1caacc98
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543826"
---
# <a name="addblanktargettolinks"></a>AddBlankTargetToLinks

**AddBlankTargetToLinks** 元素指定 HTML 链接中的目标属性设置为打开一个新窗口。 
  
```XML
<AddBlankTargetToLinks> true | false </AddBlankTargetToLinks>
```

**xs：Boolean**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ItemShape](itemshape.md) <br/> | 标识要包括在 **GetItem、FindItem、GetConversationItems** 或 **SyncFolderItems** 响应中的项目属性和内容。  <br/><br/>  下面是此元素的 XPath 表达式：<br/><br/>  `/GetItem/ItemShape` <br/>  `/FindItem/ItemShape` <br/>  `/SyncFolderItems/ItemShape` <br/>  `/GetConversationItems/ItemShape` <br/> |
   
## <a name="text-value"></a>文本值

**AddBlankTargetToLinks** 元素的文本值 **true** 指示所有 HTML 链接将设置为打开一个新窗口。 false **值表示** HTML 链接将在当前窗口中打开。 
  
## <a name="remarks"></a>说明

此元素为可选。
  
Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |types.xsd  <br/> |
|可以为空  <br/> ||
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

