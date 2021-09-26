---
title: TasksFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- TasksFolder
api_type:
- schema
ms.assetid: 5a9a4612-8064-4986-b467-c44f268c64df
description: TasksFolder元素表示包含在邮箱任务文件夹。
ms.openlocfilehash: 6c0225370dd4a4af700df9dd029c2e54154ad8e8
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543861"
---
# <a name="tasksfolder"></a>TasksFolder

本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **TasksFolder** 元素表示包含在邮箱任务文件夹。 
  
```xml
<TasksFolder>
   <FolderId/>
   <ParentFolderId/>
   <FolderClass/>
   <DisplayName/>
   <TotalCount/>
   <ChildFolderCount/>
   <ExtendedProperty/>
   <ManagedFolderInformation/>
   <UnreadCount/>
   <PermissionSet/>
      <EffectiveRights/>
</TasksFolder>
```

**TasksFolderType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |包含任务文件夹的标识符和更改键。  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |表示包含任务文件夹的父文件夹的标识符。  <br/> |
|[FolderClass](folderclass.md) <br/> |代表任务文件夹的文件夹类。  <br/> |
|[显示名称 (字符串)](displayname-string.md) <br/> |包含任务文件夹的显示名称。  <br/> |
|[TotalCount](totalcount.md) <br/> |代表任务文件夹中的项的总计数。  <br/> |
|[ChildFolderCount](childfoldercount.md) <br/> |代表任务文件夹中所包含的子文件夹数。此属性是只读的。  <br/> |
|[ExtendedProperty](extendedproperty.md) <br/> |标识任务文件夹的扩展的属性。  <br/> |
|[ManagedFolderInformation](managedfolderinformation.md) <br/> |包含有关托管文件夹的信息。  <br/> |
|[UnreadCount](unreadcount.md) <br/> |代表任务文件夹中未阅读项的计数。  <br/> |
|[PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) <br/> |包含文件夹的所有配置权限。Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |包含客户端的权利基础的项或文件夹的权限设置。此元素是只读的。在 Microsoft Exchange 2007 SP1 引入了此元素。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[AppendToFolderField](appendtofolderfield.md) <br/> |指定要在[UpdateFolder Operation](updatefolder-operation.md)期间追加到文件夹属性数据。  <br/> |
|[创建 (FolderSync)](create-foldersync.md) <br/> |标识要在本地客户端存储中创建一个文件夹。  <br/> |
|[SetFolderField](setfolderfield.md) <br/> |表示对[UpdateFolder Operation](updatefolder-operation.md)中的文件夹上的单个属性的更新。  <br/> |
|[更新 (FolderSync)](update-foldersync.md) <br/> |标识要在本地客户端存储中更新单个文件夹。  <br/> |
|[Folders](folders-ex15websvcsotherref.md) <br/> |包含一数组的文件夹操作中使用的文件夹。  <br/> |
   
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

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

