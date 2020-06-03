---
title: 权限
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
description: 权限元素定义用户对文件夹所拥有的访问权限。
ms.openlocfilehash: 0f7515dbb06f8423f8d4d95e1391496e8ac73653
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459256"
---
# <a name="permission"></a>权限

**权限**元素定义用户对文件夹所拥有的访问权限。 
  
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

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[CanCreateItems](cancreateitems.md) <br/> |指示用户是否有权在文件夹中创建项目。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
|[CanCreateSubFolders](cancreatesubfolders.md) <br/> |指示用户是否有权在文件夹中创建子文件夹。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
|[DeleteItems](deleteitems.md) <br/> |指示用户是否有权删除文件夹中的项目。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
|[EditItems](edititems.md) <br/> |指示用户是否有权编辑文件夹中的项目。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
|[IsFolderContact](isfoldercontact.md) <br/> |指示用户是否为文件夹的联系人。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
|[IsFolderOwner](isfolderowner.md) <br/> |指示用户是否为文件夹的所有者。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
|[IsFolderVisible](isfoldervisible.md) <br/> |指示用户是否可以查看文件夹。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
|[PermissionLevel](permissionlevel.md) <br/> |代表用户对文件夹所拥有的权限的组合。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
|[ReadItems （PermissionType）](readitems-permissiontype.md) <br/> |指示用户是否有权读取文件夹中的项目。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
|[UserId](userid.md) <br/> |标识代理用户或具有文件夹访问权限的用户。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[权限](permissions.md) <br/> |包含文件夹的所有已配置的权限。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
   
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
此元素是在 Exchange Server 2007 Service Pack 1 （SP1）中引入的。
  
### <a name="version-differences"></a>版本差异

对于面向 Exchange Online 的应用程序，Exchange Online 作为 Office 365 的一部分，或从 Exchange 2013 开始的 Exchange 内部部署版本，当[BaseShape](baseshape.md)元素的[GetFolder](getfolder-operation.md)操作请求中的值为**AllProperties**时，不会返回文件夹权限。 若要检索文件夹权限，请将[PermissionSet （PermissionSetType）](permissionset-permissionsettype.md)元素添加到**GetFolder**请求中的[AdditionalProperties](additionalproperties.md)元素。 
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)


[Setting Folder-Level Permissions](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

