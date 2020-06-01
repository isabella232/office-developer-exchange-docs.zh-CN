---
title: 创建 (FolderSync)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Create
api_type:
- schema
ms.assetid: 6b463d0a-70e9-40c5-ade4-c7d9a5f36bc1
description: Create 元素标识要在本地客户端存储中创建的单个文件夹。
ms.openlocfilehash: 43f6a6b3c084c8ecae767c512181bbdf50c7e786
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458374"
---
# <a name="create-foldersync"></a>创建 (FolderSync)

**Create**元素标识要在本地客户端存储中创建的单个文件夹。 
  
[SyncFolderHierarchyResponse](syncfolderhierarchyresponse.md)
  
[ResponseMessages](responsemessages.md)
  
[SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md)
  
[更改（层次结构）](changes-hierarchy.md)
  
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
|[CalendarFolder](calendarfolder.md) <br/> |代表主要包含日历项目的文件夹。  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |表示邮箱中的联系人文件夹。  <br/> |
|[SearchFolder](searchfolder.md) <br/> |表示邮箱中包含的搜索文件夹。  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |表示邮箱中包含的任务文件夹。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[更改（层次结构）](changes-hierarchy.md) <br/> |包含更改类型的序列数组，这些类型表示客户端上的项与 Exchange 服务器上的项之间的差异类型。  <br/> |
   
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

