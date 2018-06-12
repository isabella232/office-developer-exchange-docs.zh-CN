---
title: 文件夹 Id
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
description: 文件夹 Id 元素包含标识符和更改密钥的文件夹。
ms.openlocfilehash: 5764a164d5af183b8f313955ace5274dc6023a6a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754393"
---
# <a name="folderid"></a>文件夹 Id

**文件夹 Id**元素包含标识符和更改密钥的文件夹。 
  
```XML
<FolderId Id="" ChangeKey="" />
```

 **FolderIdType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|Id  <br/> |包含一个字符串，标识 Exchange 存储中的文件夹。 此属性是必需的。  <br/> |
|更改密钥  <br/> |包含一个字符串，标识的文件夹的 Id 属性标识的版本。 此属性是可选的。 使用此属性以确保正确版本的文件夹使用。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ContextFolderId](contextfolderid.md) <br/> |指示使用文件夹的操作的目标文件夹。  <br/> |
|[CopiedEvent](copiedevent.md) <br/> |表示复制的项或文件夹的事件。  <br/> |
|[DestinationFolderId](destinationfolderid.md) <br/> |指示副本的目标文件夹，并移动操作。  <br/> |
|[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) <br/> | 标识在其中创建新的文件夹或项目的文件夹。  <br/><br/>  下面是此元素的 XPath 表达式：<br/>  <br/> `/CreateItem/ParentFolderId` <br/><br/>  `/CreateFolder/ParentFolderId` <br/> |
|[BaseFolderIds](basefolderids.md) <br/> |代表将用于确定搜索文件夹的内容的文件夹的集合。  <br/> |
|[删除 (FolderSync)](delete-foldersync.md) <br/> |标识为在本地客户端库删除单个文件夹。  <br/> |
|[Folder](folder.md) <br/> |表示邮箱中的文件夹。  <br/> |
|[CalendarFolder](calendarfolder.md) <br/> |表示邮箱中的日历文件夹。  <br/> |
|[FolderChange](folderchange.md) <br/> |表示要在单个文件夹上进行的更改的集合。  <br/> 下面是此元素的 XPath 表达式:  `/UpdateFolder/FolderChanges/FolderChange` <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |表示邮箱中的联系人文件夹。  <br/> |
|[SearchFolder](searchfolder.md) <br/> |表示邮箱中的搜索文件夹。  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |表示邮箱中的任务文件夹。  <br/> |
|[ToFolderId](tofolderid.md) <br/> | 表示复制或移动项目或文件夹的目标文件夹。 <br/> <br/>  下面是此元素的 XPath 表达式： <br/> <br/>  `/MoveFolder/ToFolderId` <br/> <br/> `/CopyFolder/ToFolderId` <br/> <br/> `/MoveItem/ToFolderId`<br/> <br/>  `/CopyItem/ToFolderId` <br/> |
|[SavedItemFolderId](saveditemfolderid.md) <br/> | 标识用于更新、 发送和在 Exchange 存储中创建项目的操作的目标文件夹。  <br/><br/>  下面是此元素的 XPath 表达式： <br/> <br/>  `/CreateItem/SavedItemFolderId` <br/><br/>  `/UpdateItem/SavedItemFolderId` <br/><br/>  `/SendItem/SavedItemFolderId` <br/> |
|[SyncFolderId](syncfolderid.md) <br/> |代表包含要同步的项的文件夹。  <br/> |
|[UserConfigurationName](userconfigurationname.md) <br/> |代表用户配置对象的名称。 用户配置对象名称为用户配置对象的标识符。  <br/> |
|[CopyToFolder](copytofolder.md) <br/> |标识的文件夹的电子邮件项目将被复制到的 ID。  <br/> |
|[MoveToFolder](movetofolder.md) <br/> |标识的文件夹的电子邮件项目将移动到的 ID。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>备注

所有**文件夹 Id**元素是**FolderIdType**类型。 **文件夹 Id**元素中除其类型扩展**BaseFolderType**元素中每种情况下都需要或其中的**文件夹 Id**元素是选择的一部分。 查看架构的详细信息。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)
- [Creating Folders (Exchange Web Services)](http://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

