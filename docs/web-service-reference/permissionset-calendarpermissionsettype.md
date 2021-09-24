---
title: PermissionSet (CalendarPermissionSetType)
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
ms.assetid: 75f20033-85eb-4627-b4f8-be85e4889e96
description: PermissionSet 元素包含为日历文件夹配置的所有权限。
ms.openlocfilehash: 26351be8fd9fbe56ea5abb2dd346cb9c9458c463
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59539149"
---
# <a name="permissionset-calendarpermissionsettype"></a>PermissionSet (CalendarPermissionSetType)

**PermissionSet** 元素包含为日历文件夹配置的所有权限。 
  
```XML
<PermissionSet>
   <CalendarPermissions/>
   <UnknownEntries/>
</PermissionSet>
```

 **CalendarPermi创建SetType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[CalendarPermissions](calendarpermissions.md) <br/> |包含文件夹的日历权限数组。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
|[UnknownEntries](unknownentries.md) <br/> |包含无法针对 Active Directory 目录服务解析的未知条目数组。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CalendarFolder](calendarfolder.md) <br/> |表示一个主要包含日历项目的文件夹。  <br/> |
   
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
此元素在 sp1 Exchange Server 2007 Service Pack 1 (中) 。
  
### <a name="version-differences"></a>版本差异

对于面向 Exchange Online、Exchange Online 作为 Office 365 一部分的应用程序或从 Exchange 2013 开始本地版本的 Exchange 的应用程序，当 [BaseShape](baseshape.md)元素在 [GetFolder](getfolder-operation.md)中具有 **AllProperties** 的值时，不会返回文件夹权限操作请求。 若要检索文件夹权限，将 PermissionSet ([PermissionSetType)](permissionset-permissionsettype.md)添加到 **GetFolder** 请求中的 [AdditionalProperties](additionalproperties.md)元素。 
  
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

