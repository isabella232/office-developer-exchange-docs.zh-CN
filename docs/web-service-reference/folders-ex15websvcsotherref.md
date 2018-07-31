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
description: 文件夹元素包含在文件夹操作中使用的文件夹的数组。
ms.openlocfilehash: 34372f2480825c7a9977eeae8e730c201307f36b
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353586"
---
# <a name="folders"></a>文件夹

**文件夹**元素包含在文件夹操作中使用的文件夹的数组。 
  
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
|[Folder](folder.md) <br/> |标识要创建、 获取、 查找、 同步，或更新的文件夹。  <br/> |
|[CalendarFolder](calendarfolder.md) <br/> |表示主要包含日历项目的文件夹。  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |表示邮箱中的联系人文件夹。  <br/> |
|[SearchFolder](searchfolder.md) <br/> |表示邮箱中所包含的搜索文件夹。  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |表示邮箱中的任务文件夹。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CopyFolderResponseMessage](copyfolderresponsemessage.md) <br/> |包含状态和的单个结果[CopyFolder 操作](copyfolder-operation.md)请求。  <br/> |
|[CreateFolder](createfolder.md) <br/> |定义一个请求在 Exchange 存储中创建一个文件夹。  <br/> |
|[CreateFolderResponseMessage](createfolderresponsemessage.md) <br/> |包含状态和的单个结果[CreateFolder 操作](createfolder-operation.md)请求。  <br/> |
|[CreateManagedFolderResponseMessage](createmanagedfolderresponsemessage.md) <br/> |包含状态和的单个结果[CreateManagedFolder 操作](createmanagedfolder-operation.md)请求。  <br/> |
|[GetFolderResponseMessage](getfolderresponsemessage.md) <br/> |包含状态和[GetFolder 操作](getfolder-operation.md)请求的结果。  <br/> |
|[MoveFolderResponseMessage](movefolderresponsemessage.md) <br/> |包含状态和[MoveFolder 操作](movefolder-operation.md)请求的结果。  <br/> |
|[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) <br/> |标识在其中创建新文件夹的文件夹。  <br/> |
|[RootFolder (FindFolderResponseMessage)](rootfolder-findfolderresponsemessage.md) <br/> |包含搜索[FindFolder 操作](findfolder-operation.md)过程中的单个根文件夹的结果。  <br/> |
|[UpdateFolderResponseMessage](updatefolderresponsemessage.md) <br/> |包含状态和的单个结果[UpdateFolder 操作](updatefolder-operation.md)请求。  <br/> |
   
## <a name="remarks"></a>说明

此元素是[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md)元素的必需的子元素。 
  
描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md)

