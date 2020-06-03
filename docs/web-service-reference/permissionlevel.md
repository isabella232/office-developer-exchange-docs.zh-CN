---
title: PermissionLevel
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PermissionLevel
api_type:
- schema
ms.assetid: 87978600-3523-451e-a725-ef092c543e2a
description: PermissionLevel 元素表示用户对文件夹拥有的权限级别。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: e1e441c53b5c40c16051eb852a6b35a8af7476e2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458038"
---
# <a name="permissionlevel"></a>PermissionLevel

**PermissionLevel**元素表示用户对文件夹拥有的权限级别。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。 
  
```xml
<PermissionLevel>None or Owner or PublishingEditor or Editor or PublishingAuthor or Author or NoneditingAuthor or Reviewer or Contributor or Custom</PermissionLevel>
```

 **PermissionLevelType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**描述**|
|:-----|:-----|
|[权限](permission.md) <br/> |到文件夹定义用户拥有的访问权限。在 Exchange 2007 SP1 引入了此元素。  <br/> |
   
## <a name="text-value"></a>文本值

下表列出了**PermissionLevel**元素的可能值。 
  
**PermissionLevel 元素文本值**

|**值**|**说明**|
|:-----|:-----|
|无  <br/> |指示用户对文件夹没有权限。  <br/> |
|所有者  <br/> |指示用户可以创建、读取、编辑和删除文件夹中的所有项目，并创建子文件夹。 用户是文件夹所有者和文件夹联系人。  <br/> |
|Publishingeditorcreateitems  <br/> |指示用户可以创建、读取、编辑和删除文件夹中的所有项目，并创建子文件夹。  <br/> |
|编辑器  <br/> |指示用户可以创建、读取、编辑和删除文件夹中的所有项目。  <br/> |
|Publishingauthorcreateitems  <br/> |指示用户可以创建和读取文件夹中的所有项目、仅编辑和删除用户创建的项目以及创建子文件夹。  <br/> |
|作者  <br/> |指示用户可以创建和读取文件夹中的所有项目，并只编辑和删除用户创建的项目。  <br/> |
|Noneditingauthorcreateitems  <br/> |指示用户可以创建和读取文件夹中的所有项目，并只删除用户创建的项目。  <br/> |
|Reviewer  <br/> |指示用户可以读取文件夹中的所有项目。  <br/> |
|参与者  <br/> |指示用户可以在文件夹中创建项目。 不显示文件夹的内容。  <br/> |
|自定义警报  <br/> |指示用户对该文件夹具有自定义访问权限。  <br/> |
   
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

