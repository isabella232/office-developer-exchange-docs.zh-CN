---
title: CreateFolderPath
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 282576cb-a921-49f7-8748-64158fd50c41
description: CreateFolderPath 元素用于创建文件夹路径，并包含父文件夹 Id 和相对文件夹路径。
ms.openlocfilehash: e6ce6c9b6e12a6a0fb6792b63368a79c87d06f07
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457534"
---
# <a name="createfolderpath"></a>CreateFolderPath

**CreateFolderPath**元素用于创建文件夹路径，并包含父文件夹 Id 和相对文件夹路径。 
  
```XML
<CreateFolderPath>
   <ParentFolderId/>
   <RelativeFolderPath/>
</CreateFolderPath>
```

 **CreateFolderPathType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

[ParentFolderId （TargetFolderIdType）](parentfolderid-targetfolderidtype.md)  | [RelativeFolderPath](relativefolderpath.md)
  
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>说明

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |消息 .xsd  <br/> |
|可以为空  <br/> |false  <br/> |
   

