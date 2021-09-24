---
title: FoldersToIgnore
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: b5d18516-a617-4daf-8baf-c7ce29c76f6b
description: FoldersToIgnore 元素标识在获取对话中的项目时忽略的文件夹列表。 GetConversationItems 响应中不会返回忽略的文件夹中所有对话项目。
ms.openlocfilehash: c0102d12b24df2cadd5e307e80c5acda9a3c0589
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59528657"
---
# <a name="folderstoignore"></a>FoldersToIgnore

**FoldersToIgnore** 元素标识在获取对话中的项目时忽略的文件夹列表。 GetConversationItems 响应中不会返回忽略 **的文件夹中所有对话** 项目。 
  
```XML
<FoldersToIgnore>
   <FolderId/>
   <DistinguishedFolderId/>
</FoldersToIgnore>
```

 **NonEmptyArrayOfBaseFolderIdsType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

[FolderId](folderid.md)  | [DistinguishedFolderId](distinguishedfolderid.md)
  
### <a name="parent-elements"></a>父元素

[GetConversationItems](getconversationitems.md)
  
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
   

