---
title: Create (FolderSync)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Create
api_type:
- schema
ms.assetid: 6b463d0a-70e9-40c5-ade4-c7d9a5f36bc1
description: Create 元素标识要在本地客户端存储创建的单个文件夹。
ms.openlocfilehash: 941fb580e3f10270cf213a7d9b78e4ef5b199d7c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59536546"
---
# <a name="create-foldersync"></a>Create (FolderSync)

**Create** 元素标识要在本地客户端存储创建的单个文件夹。 
  
[SyncFolderHierarchyResponse](syncfolderhierarchyresponse.md)
  
[ResponseMessages](responsemessages.md)
  
[SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md)
  
[Changes (Hierarchy)](changes-hierarchy.md)
  
[创建 (FolderSync)](create-foldersync.md)
  
```xml
<Create>
   <Folder/>
   <CalendarFolder/>
   <ContactsFolder/>
   <SearchFolder/>
   <TasksFolder/>
</Create>
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
|[TasksFolder](tasksfolder.md) <br/> |表示包含在邮箱中的任务文件夹。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Changes (Hierarchy)](changes-hierarchy.md) <br/> |包含一个变更类型的序列数组，这些更改类型表示客户端上的项目与客户端服务器上项目Exchange的类型。  <br/> |
   
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



[SyncFolderItems 操作](syncfolderitems-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

