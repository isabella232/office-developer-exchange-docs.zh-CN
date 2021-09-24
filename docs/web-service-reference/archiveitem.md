---
title: ArchiveItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: c2172e61-876a-4f76-bc9c-263c8be11429
description: ArchiveItem 元素包含源文件夹 ID 和关联的存档项目的项目 ID 数组。
ms.openlocfilehash: 876c86321c688e20fc3b5539c542bc46e67ba343
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59525293"
---
# <a name="archiveitem"></a>ArchiveItem

**ArchiveItem** 元素包含源文件夹 ID 和关联的存档项目的项目 ID 数组。 
  
```XML
<ArchiveItem>
   <ArchiveSourceFolderId/>
   <ItemIds/>
</ArchiveItem>
```

 **ArchiveItemType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

[ArchiveSourceFolderId](archivesourcefolderid.md)  | [ItemIds](itemids.md)
  
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |messages.xsd  <br/> |
|可以为空  <br/> |false  <br/> |
   

