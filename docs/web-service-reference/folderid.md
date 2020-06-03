---
title: FolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderId
api_type:
- schema
ms.assetid: 00d14e3e-4365-4f21-8f88-eaeea73b9bf7
description: FolderId 元素包含文件夹的标识符和更改键。
ms.openlocfilehash: 7aa5070fa7a2c51303c7159de04fe277f909a874
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461385"
---
# <a name="folderid"></a>FolderId

**FolderId**元素包含文件夹的标识符和更改键。 
  
```XML
<FolderId Id="" ChangeKey="" />
```

 **FolderIdType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|Id  <br/> |包含标识 Exchange 存储中的文件夹的字符串。 此特性是必需的。  <br/> |
|ChangeKey  <br/> |包含标识由 Id 属性标识的文件夹版本的字符串。 此特性是可选的。 使用此属性可确保使用的是正确的文件夹版本。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ContextFolderId](contextfolderid.md) <br/> |指示针对使用文件夹的操作的文件夹。  <br/> |
|[CopiedEvent](copiedevent.md) <br/> |表示在其中复制项目或文件夹的事件。  <br/> |
|[DestinationFolderId](destinationfolderid.md) <br/> |指示复制和移动操作的目标文件夹。  <br/> |
|[ParentFolderId （TargetFolderIdType）](parentfolderid-targetfolderidtype.md) <br/> | 标识在其中创建新文件夹或项目的文件夹。  <br/><br/>  下面是此元素的 XPath 表达式：<br/>  <br/> `/CreateItem/ParentFolderId` <br/><br/>  `/CreateFolder/ParentFolderId` <br/> |
|[BaseFolderIds](basefolderids.md) <br/> |表示将挖掘的文件夹集合，以确定搜索文件夹的内容。  <br/> |
|[Delete （FolderSync）](delete-foldersync.md) <br/> |标识要在本地客户端存储中删除的单个文件夹。  <br/> |
|[Folder](folder.md) <br/> |表示邮箱中的文件夹。  <br/> |
|[CalendarFolder](calendarfolder.md) <br/> |代表邮箱中的 "日历" 文件夹。  <br/> |
|[FolderChange](folderchange.md) <br/> |表示要在单个文件夹上进行的更改的集合。  <br/> 下面是此元素的 XPath 表达式:  `/UpdateFolder/FolderChanges/FolderChange` <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |表示邮箱中的联系人文件夹。  <br/> |
|[SearchFolder](searchfolder.md) <br/> |表示邮箱中的搜索文件夹。  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |表示邮箱中的任务文件夹。  <br/> |
|[ToFolderId](tofolderid.md) <br/> | 代表复制或移动的项或文件夹的目标文件夹。 <br/> <br/>  下面是此元素的 XPath 表达式： <br/> <br/>  `/MoveFolder/ToFolderId` <br/> <br/> `/CopyFolder/ToFolderId` <br/> <br/> `/MoveItem/ToFolderId`<br/> <br/>  `/CopyItem/ToFolderId` <br/> |
|[SavedItemFolderId](saveditemfolderid.md) <br/> | 标识在 Exchange 存储中更新、发送和创建项目的操作的目标文件夹。  <br/><br/>  下面是此元素的 XPath 表达式： <br/> <br/>  `/CreateItem/SavedItemFolderId` <br/><br/>  `/UpdateItem/SavedItemFolderId` <br/><br/>  `/SendItem/SavedItemFolderId` <br/> |
|[SyncFolderId](syncfolderid.md) <br/> |表示包含要同步的项目的文件夹。  <br/> |
|[UserConfigurationName](userconfigurationname.md) <br/> |表示用户配置对象的名称。 "用户配置" 对象名称是 "用户配置" 对象的标识符。  <br/> |
|[CopyToFolder](copytofolder.md) <br/> |标识电子邮件项目将复制到的文件夹的 ID。  <br/> |
|[MoveToFolder](movetofolder.md) <br/> |标识电子邮件项目将移动到的文件夹的 ID。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>说明

所有**FolderId**元素均属于**FolderIdType**类型。 除了其类型扩展了**BaseFolderType**的元素或**FolderId**元素是选项的一部分的元素中， **FolderId**元素都是必需的。 有关详细信息，请查看架构。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)
- [Creating Folders (Exchange Web Services)](https://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

