---
title: Update (FolderSync)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Update
api_type:
- schema
ms.assetid: 47ed8edb-2a94-471b-b965-93f91456252e
description: Update 元素标识要在本地客户端存储中更新的单个文件夹。
ms.openlocfilehash: 460d1d9efb3f5dde34bfbb85c332ed150fe4d17a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517488"
---
# <a name="update-foldersync"></a>Update (FolderSync)

**Update** 元素标识要在本地客户端存储中更新的单个文件夹。 
  
- [SyncFolderHierarchyResponse](syncfolderhierarchyresponse.md) 
- [ResponseMessages](responsemessages.md) 
- [SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md)  
- [Changes (Hierarchy)](changes-hierarchy.md) 
- [更新 (FolderSync)](update-foldersync.md)
  
```xml
<Update>
   <Folder/>
</Update>
```

```xml
<Update>
   <CalendarFolder/>
</Update>
```

```xml
<Update>
   <ContactsFolder/>
</Update>
```

```xml
<Update>
   <TasksFolder/>
</Update>
```

```xml
<Update>
   <SearchFolder/>
</Update>
```

**SyncFolderHierarchyCreateOrUpdateType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Folder](folder.md) <br/> |定义要创建、获取、查找、同步或更新的文件夹。  <br/> |
|[CalendarFolder](calendarfolder.md) <br/> |表示一个主要包含日历项目的文件夹。  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |表示邮箱中的联系人文件夹。  <br/> |
|[SearchFolder](searchfolder.md) <br/> |表示包含在邮箱中的搜索文件夹。  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |表示邮箱中包含的任务文件夹 t。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Changes (Hierarchy)](changes-hierarchy.md) <br/> |包含一个更改类型的排序数组，这些更改类型表示客户端上的文件夹和服务器上文件夹Exchange的类型。  <br/> |
   
## <a name="remarks"></a>说明

描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [SyncFolderItems 操作](syncfolderitems-operation.md)
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

