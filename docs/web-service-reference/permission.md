---
title: Permission
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Permission
api_type:
- schema
ms.assetid: b8d0429a-0e58-4480-9847-4901970c7033
description: 权限元素到文件夹定义用户拥有的访问权限。
ms.openlocfilehash: 600d60f481c4f1d407c3a39ab65d6ddcf46d04e7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826735"
---
# <a name="permission"></a>权限

**权限**元素到文件夹定义用户拥有的访问权限。 
  
```XML
<Permission>
   <CanCreateItems/>
   <CanCreateSubfolders/>
   <IsFolderOwner/>
   <IsFolderVisible/>
   <IsFolderContact/>
   <EditItems/>
   <DeleteItems/>
   <PermissionLevel/>
   <ReadItems/>
   <UserId/>
</Permission>
```

 **PermissionType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[CanCreateItems](cancreateitems.md) <br/> |指示用户是否有权文件夹中创建项目。 Exchange 2007 SP1 中引入了此元素。  <br/> |
|[CanCreateSubFolders](cancreatesubfolders.md) <br/> |指示用户是否有权在创建子文件夹。 Exchange 2007 SP1 中引入了此元素。  <br/> |
|[DeleteItems](deleteitems.md) <br/> |指示用户是否有权删除文件夹中的项目。 Exchange 2007 SP1 中引入了此元素。  <br/> |
|[EditItems](edititems.md) <br/> |指示用户是否有权编辑文件夹中的项目。 Exchange 2007 SP1 中引入了此元素。  <br/> |
|[IsFolderContact](isfoldercontact.md) <br/> |指示用户是否为文件夹的联系人。 Exchange 2007 SP1 中引入了此元素。  <br/> |
|[IsFolderOwner](isfolderowner.md) <br/> |指示用户是否为文件夹的所有者。 Exchange 2007 SP1 中引入了此元素。  <br/> |
|[IsFolderVisible](isfoldervisible.md) <br/> |指示用户是否可以查看文件夹。 Exchange 2007 SP1 中引入了此元素。  <br/> |
|[PermissionLevel](permissionlevel.md) <br/> |表示用户对某个文件夹的权限的组合。 Exchange 2007 SP1 中引入了此元素。  <br/> |
|[ReadItems (PermissionType)](readitems-permissiontype.md) <br/> |指示用户是否有权读取文件夹中的项目。 Exchange 2007 SP1 中引入了此元素。  <br/> |
|[用户 Id](userid.md) <br/> |标识委派用户或具有文件夹访问权限的用户。 Exchange 2007 SP1 中引入了此元素。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[权限](permissions.md) <br/> |包含文件夹的所有已配置的权限。 Exchange 2007 SP1 中引入了此元素。  <br/> |
   
## <a name="remarks"></a>备注

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
此元素是在 Exchange Server 2007 Service Pack 1 (SP1) 中引入的。
  
### <a name="version-differences"></a>版本差异

应用程序面向 Exchange Online、 Exchange Online 作为 Office 365 的一部分或 Exchange 开头 Exchange 2013 的本地版本文件夹权限不返回时[BaseShape](baseshape.md)元素的值为**AllProperties**在[GetFolder](getfolder-operation.md)操作请求。 若要检索文件夹权限，请向**GetFolder**请求中[AdditionalProperties](additionalproperties.md) element 中添加[PermissionSet (PermissionSetType)](permissionset-permissionsettype.md)元素。 
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)


[Setting Folder-Level Permissions](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

