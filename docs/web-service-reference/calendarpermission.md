---
title: CalendarPermission
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CalendarPermission
api_type:
- schema
ms.assetid: 3aafb221-a04b-41f6-804e-eda810f1ba28
description: CalendarPermission 元素定义用户对"日历"文件夹具有的访问权限。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: 7794cab261653f8cb6421d4e0633d496ba347a5f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514800"
---
# <a name="calendarpermission"></a>CalendarPermission

**CalendarPermission** 元素定义用户对"日历"文件夹具有的访问权限。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。 
  
```xml
<Permission>
   <CalendarPermissionLevel/>
   <CanCreateItems/>
   <CanCreateSubfolders/>
   <IsFolderOwner/>
   <IsFolderVisible/>
   <IsFolderContact/>
   <EditItems/>
   <DeleteItems/>
   <ReadItems/>
   <UserId/>
</Permission>
```

 **CalendarPermissionType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[CalendarPermissionLevel](calendarpermissionlevel.md) <br/> |表示用户对"日历"文件夹拥有的权限级别。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
|[CanCreateItems](cancreateitems.md) <br/> |指示用户是否有权在文件夹中创建项目。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
|[CanCreateSubFolders](cancreatesubfolders.md) <br/> |指示用户是否有权在文件夹中创建子文件夹。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
|[DeleteItems](deleteitems.md) <br/> |指示用户是否有权删除文件夹中的项目。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
|[EditItems](edititems.md) <br/> |指示用户是否有权编辑文件夹中的项目。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
|[IsFolderContact](isfoldercontact.md) <br/> |指示用户是否是文件夹的联系人。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
|[IsFolderOwner](isfolderowner.md) <br/> |指示用户是否是文件夹的所有者。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
|[IsFolderVisible](isfoldervisible.md) <br/> |指示用户是否可以查看文件夹。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
|[ReadItems (CalendarPermissionType)](readitems-calendarpermissiontype.md) <br/> |指示用户是否有权读取日历文件夹中的项目。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
|[UserId](userid.md) <br/> |标识委派用户或具有文件夹访问权限的用户。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CalendarPermissions](calendarpermissions.md) <br/> |包含文件夹的日历权限数组。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
   
## <a name="remarks"></a>说明

描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
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

