---
title: CalendarPermission
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarPermission
api_type:
- schema
ms.assetid: 3aafb221-a04b-41f6-804e-eda810f1ba28
description: CalendarPermission 元素定义日历文件夹的用户具有访问权限。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。
ms.openlocfilehash: 7f6ceb6895add3fdd82cdd595463b3a80db822e5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753417"
---
# <a name="calendarpermission"></a>CalendarPermission

**CalendarPermission**元素定义日历文件夹的用户具有访问权限。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。 
  
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

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[CalendarPermissionLevel](calendarpermissionlevel.md) <br/> |表示用户对日历文件夹的权限级别。 Exchange 2007 SP1 中引入了此元素。  <br/> |
|[CanCreateItems](cancreateitems.md) <br/> |指示用户是否有权文件夹中创建项目。 Exchange 2007 SP1 中引入了此元素。  <br/> |
|[CanCreateSubFolders](cancreatesubfolders.md) <br/> |指示用户是否有权在创建子文件夹。 Exchange 2007 SP1 中引入了此元素。  <br/> |
|[DeleteItems](deleteitems.md) <br/> |指示用户是否有权删除文件夹中的项目。 Exchange 2007 SP1 中引入了此元素。  <br/> |
|[EditItems](edititems.md) <br/> |指示用户是否有权编辑文件夹中的项目。 Exchange 2007 SP1 中引入了此元素。  <br/> |
|[IsFolderContact](isfoldercontact.md) <br/> |指示用户是否为文件夹的联系人。 Exchange 2007 SP1 中引入了此元素。  <br/> |
|[IsFolderOwner](isfolderowner.md) <br/> |指示用户是否为文件夹的所有者。 Exchange 2007 SP1 中引入了此元素。  <br/> |
|[IsFolderVisible](isfoldervisible.md) <br/> |指示用户是否可以查看文件夹。 Exchange 2007 SP1 中引入了此元素。  <br/> |
|[ReadItems (CalendarPermissionType)](readitems-calendarpermissiontype.md) <br/> |指示用户是否有权读取日历文件夹中的项目。 Exchange 2007 SP1 中引入了此元素。  <br/> |
|[用户 Id](userid.md) <br/> |标识委派用户或具有文件夹访问权限的用户。 Exchange 2007 SP1 中引入了此元素。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CalendarPermissions](calendarpermissions.md) <br/> |包含数组的日历文件夹的权限。 Exchange 2007 SP1 中引入了此元素。  <br/> |
   
## <a name="remarks"></a>备注

描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
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

