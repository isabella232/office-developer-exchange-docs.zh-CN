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
description: UnknownEntries 元素包含一个数组无法解析针对 Active Directory 目录服务的未知的权限条目。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。
ms.openlocfilehash: 306e5f226a56694bb1ff32362f77e7dff80865ad
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838344"
---
# <a name="unknownentries"></a>UnknownEntries

**UnknownEntries**元素包含一个数组无法解析针对 Active Directory 目录服务的未知的权限条目。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。 
  
```xml
<UnknownEntries>
   <UnknownEntry/>
</UnknownEntries>
```

 **ArrayOfUnknownEntriesType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[UnknownEntry](unknownentry.md) <br/> |表示无法解析的 Active directory 的单个未知的权限条目。 Exchange 2007 SP1 中引入了此元素。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) <br/> |包含所有配置的文件夹的权限。 Exchange 2007 SP1 中引入了此元素。  <br/> |
|[PermissionSet (CalendarPermissionSetType)](permissionset-calendarpermissionsettype.md) <br/> |包含所有配置的日历文件夹的权限。 Exchange 2007 SP1 中引入了此元素。  <br/> |
   
## <a name="remarks"></a>备注

可以通过使用[SetFolderField](setfolderfield.md)元素 UpdateFolder 操作从文件夹中删除未知的条目。 通过使用 UpdateFolder 操作的 SetFolderField 选项重置 PermissionSet 时，将删除未知的条目。 Exchange Web 服务不支持各项的删除。 
  
描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[UpdateFolder Operation](updatefolder-operation.md)


- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)


[Setting Folder-Level Permissions](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

