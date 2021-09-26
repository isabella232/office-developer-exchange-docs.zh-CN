---
title: CalendarPermissions
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CalendarPermissions
api_type:
- schema
ms.assetid: 9b659d83-45fb-42a2-b052-5bc4dbe3854d
description: CalendarPermissions 元素包含文件夹的日历权限数组。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: 2f7641cbd1193248424bfaae32cb34a765e1675c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59545564"
---
# <a name="calendarpermissions"></a>CalendarPermissions

**CalendarPermissions** 元素包含文件夹的日历权限数组。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。 
  
```xml
<CalendarPermissions>
   <PermissionSet/>
</CalendarPermissions>
```

 **ArrayOfCalendarPermissionsType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[CalendarPermission](calendarpermission.md) <br/> |定义委派用户对日历文件夹具有的访问权限。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[PermissionSet (CalendarPermissionSetType)](permissionset-calendarpermissionsettype.md) <br/> |包含日历文件夹的所有已配置的权限。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
   
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

