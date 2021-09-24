---
title: RelativeFolderPath
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 54e3ba52-08a6-4d48-8a44-6fd5fdbffb25
description: RelativeFolderPath 元素包含一个文件夹数组，该数组指示要创建的文件夹路径的相对文件夹路径。
ms.openlocfilehash: f9a1f193678e9dbd7686376c630ab2fbd0eaf1bd
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513456"
---
# <a name="relativefolderpath"></a>RelativeFolderPath

**RelativeFolderPath** 元素包含一个文件夹数组，该数组指示要创建的文件夹路径的相对文件夹路径。 
  
```XML
<RelativeFolderPath>
   <Folder/>
   <CalendarFolder/>
   <ContactsFolder/>
   <SearchFolder/>
   <TasksFolder/>
</RelativeFolderPath>
```

 **NonEmptyArrayOfFoldersType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

[Folder](folder.md)  | [CalendarFolder](calendarfolder.md)  | [ContactsFolder](contactsfolder.md)  | [SearchFolder](searchfolder.md)  | [TasksFolder](tasksfolder.md)
  
### <a name="parent-elements"></a>父元素

[CreateFolderPath](createfolderpath.md)
  
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> ||
   

