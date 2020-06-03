---
title: UnknownEntries
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UnknownEntries
api_type:
- schema
ms.assetid: 107ec73e-083a-4956-9d37-33d4734cc157
description: UnknownEntries 元素包含无法针对 Active Directory 目录服务解析的未知权限条目数组。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: 68cb2518b895ca0a74e6b9ed649ee92b7502ab05
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459417"
---
# <a name="unknownentries"></a>UnknownEntries

**UnknownEntries**元素包含无法针对 Active directory 目录服务解析的未知权限条目数组。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。 
  
```xml
<UnknownEntries>
   <UnknownEntry/>
</UnknownEntries>
```

 **ArrayOfUnknownEntriesType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[UnknownEntry](unknownentry.md) <br/> |代表单个无法对 Active Directory 进行解析的未知权限条目。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) <br/> |包含为文件夹配置的所有权限。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
|[PermissionSet （CalendarPermissionSetType）](permissionset-calendarpermissionsettype.md) <br/> |包含为 "日历" 文件夹配置的所有权限。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
   
## <a name="remarks"></a>备注

您可以通过将 UpdateFolder 操作与[SetFolderField](setfolderfield.md)元素一起使用，从文件夹中删除未知条目。 使用 UpdateFolder 操作的 SetFolderField 选项重置 PermissionSet 时，将删除未知的条目。 Exchange Web 服务不支持删除单个条目。 
  
描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[UpdateFolder 操作](updatefolder-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)


[Setting Folder-Level Permissions](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

