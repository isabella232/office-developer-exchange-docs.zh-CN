---
title: 文件夹
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Folders
api_type:
- schema
ms.assetid: 8e71cb44-1df6-444a-add7-0c1363863f65
description: Folders 元素包含用于文件夹操作的文件夹数组。
ms.openlocfilehash: 77442965c9d372a2895404cf1c919be38e98abb5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546432"
---
# <a name="folders"></a>Folders

**Folders** 元素包含用于文件夹操作的文件夹数组。 
  
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

**ArrayOfFoldersType** 或 **NonEmptyArrayOfFoldersType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Folder](folder.md) <br/> |标识要创建、获取、查找、同步或更新的文件夹。  <br/> |
|[CalendarFolder](calendarfolder.md) <br/> |表示一个主要包含日历项目的文件夹。  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |代表邮箱中的"联系人"文件夹。  <br/> |
|[SearchFolder](searchfolder.md) <br/> |表示邮箱中包含的搜索文件夹。  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |代表邮箱中的"任务"文件夹。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CopyFolderResponseMessage](copyfolderresponsemessage.md) <br/> |包含单个 [CopyFolder](copyfolder-operation.md) 操作请求的状态和结果。  <br/> |
|[CreateFolder](createfolder.md) <br/> |定义在邮件存储中创建文件夹Exchange请求。  <br/> |
|[CreateFolderResponseMessage](createfolderresponsemessage.md) <br/> |包含单个 [CreateFolder](createfolder-operation.md) 操作请求的状态和结果。  <br/> |
|[CreateManagedFolderResponseMessage](createmanagedfolderresponsemessage.md) <br/> |包含单个 [CreateManagedFolder 操作请求的状态和](createmanagedfolder-operation.md) 结果。  <br/> |
|[GetFolderResponseMessage](getfolderresponsemessage.md) <br/> |包含 [GetFolder](getfolder-operation.md) 操作请求的状态和结果。  <br/> |
|[MoveFolderResponseMessage](movefolderresponsemessage.md) <br/> |包含 [MoveFolder](movefolder-operation.md) 操作请求的状态和结果。  <br/> |
|[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) <br/> |标识新建文件夹的文件夹。  <br/> |
|[RootFolder (FindFolderResponseMessage)](rootfolder-findfolderresponsemessage.md) <br/> |包含 [FindFolder](findfolder-operation.md)操作期间搜索单个根文件夹的结果。  <br/> |
|[UpdateFolderResponseMessage](updatefolderresponsemessage.md) <br/> |包含单个 [UpdateFolder](updatefolder-operation.md) 操作请求的状态和结果。  <br/> |
   
## <a name="remarks"></a>注解

此元素是 [TargetFolderIdType 元素的 ParentFolderId (必需的) ](parentfolderid-targetfolderidtype.md) 元素。 
  
描述此元素的架构位于运行安装了客户端访问服务器角色的 Microsoft Exchange Server 2010 的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md)

