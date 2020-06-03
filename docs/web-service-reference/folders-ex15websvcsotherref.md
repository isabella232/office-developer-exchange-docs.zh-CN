---
title: 文件夹
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Folders
api_type:
- schema
ms.assetid: 8e71cb44-1df6-444a-add7-0c1363863f65
description: Folders 元素包含在文件夹操作中使用的一组文件夹。
ms.openlocfilehash: b087be0501f04390b80458458e7e7ccc24bf27bd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530977"
---
# <a name="folders"></a>Folders

**Folders**元素包含在文件夹操作中使用的一组文件夹。 
  
```xml
<Folders>
   <Folder/>
</Folders>
```

```xml
<Folders>
   <ContactsFolder/> 
</Folders>
```

```xml
<Folders>
   <TasksFolder/>
</Folders>
```

```xml
<Folders>
   <CalendarFolder/>
</Folders>
```

```xml
<Folders>
   <SearchFolder/> 
</Folders>
```

**ArrayOfFoldersType**或**NonEmptyArrayOfFoldersType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Folder](folder.md) <br/> |标识要创建、获取、查找、同步或更新的文件夹。  <br/> |
|[CalendarFolder](calendarfolder.md) <br/> |代表主要包含日历项目的文件夹。  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |表示邮箱中的 "联系人" 文件夹。  <br/> |
|[SearchFolder](searchfolder.md) <br/> |表示邮箱中包含的搜索文件夹。  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |表示邮箱中的任务文件夹。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CopyFolderResponseMessage](copyfolderresponsemessage.md) <br/> |包含单个[CopyFolder 操作](copyfolder-operation.md)请求的状态和结果。  <br/> |
|[CreateFolder](createfolder.md) <br/> |定义在 Exchange 存储区中创建文件夹的请求。  <br/> |
|[CreateFolderResponseMessage](createfolderresponsemessage.md) <br/> |包含单个[CreateFolder 操作](createfolder-operation.md)请求的状态和结果。  <br/> |
|[CreateManagedFolderResponseMessage](createmanagedfolderresponsemessage.md) <br/> |包含单个[CreateManagedFolder 操作](createmanagedfolder-operation.md)请求的状态和结果。  <br/> |
|[GetFolderResponseMessage](getfolderresponsemessage.md) <br/> |包含[GetFolder 操作](getfolder-operation.md)请求的状态和结果。  <br/> |
|[MoveFolderResponseMessage](movefolderresponsemessage.md) <br/> |包含[MoveFolder 操作](movefolder-operation.md)请求的状态和结果。  <br/> |
|[ParentFolderId （TargetFolderIdType）](parentfolderid-targetfolderidtype.md) <br/> |标识在其中创建新文件夹的文件夹。  <br/> |
|[RootFolder （FindFolderResponseMessage）](rootfolder-findfolderresponsemessage.md) <br/> |包含在[FindFolder 操作](findfolder-operation.md)过程中搜索单个根文件夹的结果。  <br/> |
|[UpdateFolderResponseMessage](updatefolderresponsemessage.md) <br/> |包含单个[UpdateFolder 操作](updatefolder-operation.md)请求的状态和结果。  <br/> |
   
## <a name="remarks"></a>备注

此元素是[ParentFolderId （TargetFolderIdType）](parentfolderid-targetfolderidtype.md)元素的必需子元素。 
  
描述此元素的架构位于运行 Microsoft Exchange Server 2010 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [ParentFolderId （TargetFolderIdType）](parentfolderid-targetfolderidtype.md)

