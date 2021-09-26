---
title: PermissionSet (PermissionSetType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PermissionSet
api_type:
- schema
ms.assetid: 6ac1bd17-a089-46bb-b9e6-f5b1dfe1076d
description: PermissionSet 元素包含为文件夹配置的所有权限。
ms.openlocfilehash: b18fef33d3be6cb8c525f731a264860c3a83afdc
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543140"
---
# <a name="permissionset-permissionsettype"></a>PermissionSet (PermissionSetType)

**PermissionSet** 元素包含为文件夹配置的所有权限。 
  
```XML
<PermissionSet>
   <Permissions/>
   <UnknownEntries/>
</PermissionSet>
```

 **PermissionSetType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[权限](permissions.md) <br/> |包含文件夹的权限集合。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
|[UnknownEntries](unknownentries.md) <br/> |包含无法针对 Active Directory 目录服务解析的未知条目数组。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Folder](folder.md) <br/> |定义要创建、获取、查找、同步或更新的文件夹。  <br/> |
|[SearchFolder](searchfolder.md) <br/> |表示包含在邮箱中的搜索文件夹。  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |表示包含在邮箱中的联系人文件夹。  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |表示包含在邮箱中的任务文件夹。  <br/> |
   
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
此元素是在 sp1 Exchange Server 2007 Service Pack 1 (中引入) 。
  
### <a name="version-differences"></a>版本差异

对于面向 Exchange Online、Exchange Online 作为 Office 365 的一部分或自 Exchange 2013 起本地版本的 Exchange 的应用程序，当 [BaseShape](baseshape.md)元素在 [GetFolder](getfolder-operation.md)中具有 **AllProperties** 的值时，不会返回文件夹权限操作请求。 若要检索文件夹权限，可以将 PermissionSet ([PermissionSetType)](permissionset-permissionsettype.md)添加到 **GetFolder** 请求中的 [AdditionalProperties](additionalproperties.md)元素。 
  
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

