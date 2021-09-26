---
title: SearchFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SearchFolder
api_type:
- schema
ms.assetid: 1a7d408b-2e98-4391-8834-085ed6d5757c
description: SearchFolder元素表示包含在一个邮箱中的搜索文件夹。
ms.openlocfilehash: 44f19dad83e8cd18045901bc7e3e48e31508b3db
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544001"
---
# <a name="searchfolder"></a>SearchFolder

本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **SearchFolder** 元素表示包含在一个邮箱中的搜索文件夹。 
  
```xml
<SearchFolder>
   <FolderId/>
   <ParentFolderId/>
   <FolderClass/>
   <DisplayName/>
   <TotalCount/>
   <ChildFolderCount/>
   <ExtendedProperty/>
   <ManagedFolderInformation/>
   <UnreadCount/>
   <SearchParameters/>
   <PermissionSet/>
      <EffectiveRights/>
</SearchFolder>
```

 **SearchFolderType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |包含一个文件夹的标识符和更改键。  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |表示包含该文件夹的父文件夹的标识符。  <br/> |
|[FolderClass](folderclass.md) <br/> |表示给定文件夹的文件夹类。  <br/> |
|[显示名称 (字符串)](displayname-string.md) <br/> |包含文件夹的显示名称。  <br/> |
|[TotalCount](totalcount.md) <br/> |表示给定文件夹中的项目总数。  <br/> |
|[ChildFolderCount](childfoldercount.md) <br/> |表示文件夹中包含的子文件夹数。此属性是只读的。  <br/> |
|[ExtendedProperty](extendedproperty.md) <br/> |标识文件夹的扩展的属性。  <br/> |
|[ManagedFolderInformation](managedfolderinformation.md) <br/> |包含有关托管文件夹的信息。  <br/> |
|[UnreadCount](unreadcount.md) <br/> |表示给定文件夹中未阅读项的计数。  <br/> |
|[SearchParameters](searchparameters.md) <br/> |包含用于定义搜索文件夹的参数。  <br/> |
|[PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) <br/> |包含文件夹的所有配置权限。Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |包含基于项目或文件夹的权限设置的客户端权限。此元素为只读。Exchange 2007 SP1 中引入了此元素。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[AppendToFolderField](appendtofolderfield.md) <br/> |指定要在[UpdateFolder Operation](updatefolder-operation.md)期间追加到文件夹属性数据。  <br/> |
|[创建 (FolderSync)](create-foldersync.md) <br/> |标识要在本地客户端存储中创建一个文件夹。  <br/> |
|[SetFolderField](setfolderfield.md) <br/> |表示对[UpdateFolder Operation](updatefolder-operation.md)中的文件夹上的单个属性的更新。  <br/> |
|[更新 (FolderSync)](update-foldersync.md) <br/> |标识要在本地客户端存储中更新单个文件夹。  <br/> |
|[Folders](folders-ex15websvcsotherref.md) <br/> |包含文件夹在文件夹操作中使用的数组。  <br/> |
   
## <a name="remarks"></a>注解

 **SearchFolder** 用于常规搜索文件夹和MicrosoftOfficeOutlook和Outlook Web Access的可见的文件夹中搜索。要对Outlook和Outlook Web Access是可见的搜索文件夹，必须在 SearchFolders 可分辨文件夹下创建文件夹。 
  
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

