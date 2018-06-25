---
title: ContactsFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContactsFolder
api_type:
- schema
ms.assetid: 6c299de8-2087-4aeb-8e66-2bc7586509a6
description: ContactsFolder元素表示的邮箱中包含联系人文件夹。
ms.openlocfilehash: 01302f00d84cfff9713e3b188b7799c537fc0629
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753507"
---
# <a name="contactsfolder"></a>ContactsFolder

本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **ContactsFolder**元素表示的邮箱中包含联系人文件夹。 
  
```xml
<ContactsFolder>
   <FolderId/>
   <ParentFolderId/>
   <FolderClass/>
   <DisplayName/>
   <TotalCount/>
   <ChildFolderCount/>
   <ExtendedProperty/>
   <ManagedFolderInformation/>
   <EffectiveRights/>
   <SharingEffectiveRights/>
   <PermissionSet/>
</ContactsFolder>
```

 **ContactsFolderType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[文件夹 Id](folderid.md) <br/> |包含联系人文件夹的标识符和更改键。  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |表示包含联系人文件夹的父文件夹的标识符。  <br/> |
|[FolderClass](folderclass.md) <br/> |表示联系人文件夹的文件夹类。  <br/> |
|[显示名称 (字符串)](displayname-string.md) <br/> |包含联系人文件夹的显示名称。  <br/> |
|[TotalCount](totalcount.md) <br/> |表示联系人文件夹中的项的总计数。  <br/> |
|[ChildFolderCount](childfoldercount.md) <br/> |代表联系人文件夹中包含的子文件夹数。此属性是只读的。  <br/> |
|[ExtendedProperty](extendedproperty.md) <br/> |标识联系人文件夹的扩展的属性。  <br/> |
|[ManagedFolderInformation](managedfolderinformation.md) <br/> |包含有关托管文件夹的信息。  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |包含客户端的权利基础的项或文件夹的权限设置。  <br/> |
|[SharingEffectiveRights (PermissionReadAccessType)](sharingeffectiverights-permissionreadaccesstype.md) <br/> |指示用户必须为要共享的联系人数据的权限。  <br/> |
|[PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) <br/> |包含文件夹的所有已配置的权限。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[AppendToFolderField](appendtofolderfield.md) <br/> |指定要在[UpdateFolder Operation](updatefolder-operation.md)期间追加到文件夹属性数据。  <br/> |
|[创建 (FolderSync)](create-foldersync.md) <br/> |标识要在本地客户端存储中创建一个文件夹。  <br/> |
|[SetFolderField](setfolderfield.md) <br/> |表示对[UpdateFolder Operation](updatefolder-operation.md)中的文件夹上的单个属性的更新。  <br/> |
|[更新 (FolderSync)](update-foldersync.md) <br/> |标识要在本地客户端存储中更新单个文件夹。  <br/> |
|[Folders](folders-ex15websvcsotherref.md) <br/> |包含一数组的文件夹操作中使用的文件夹。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>备注

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

