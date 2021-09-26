---
title: ContactsFolderPermissionLevel
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ContactsFolderPermissionLevel
api_type:
- schema
ms.assetid: 805f05e7-b320-436a-9965-ba1ee235ac41
description: ContactsFolderPermissionLevel 元素包含默认"联系人"文件夹的权限。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: 9b266efbd5817cd32bca415e2330b58586b38bd6
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544274"
---
# <a name="contactsfolderpermissionlevel"></a>ContactsFolderPermissionLevel

**ContactsFolderPermissionLevel** 元素包含默认"联系人"文件夹的权限。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。 
  
```xml
<ContactsFolderPermissionLevel>
   None or Editor or Reviewer or Author or Custom
</ContactsFolderPermissionLevel>
```

 **DelegateFolderPermissionLevelType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[DelegatePermissions](delegatepermissions.md) <br/> |包含用户的委派权限级别设置。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
   
## <a name="text-value"></a>文本值

下表列出了表示权限级别的文本值。
  
**权限级别文本值**

|**权限级别**|**说明**|
|:-----|:-----|
|无  <br/> |代理用户对"联系人"文件夹没有访问权限。  <br/> |
|Reviewer  <br/> |代理用户可以读取"联系人"文件夹中的项目。  <br/> |
|作者  <br/> |代理用户可以在"联系人"文件夹中读取和创建项目。  <br/> |
|编辑器  <br/> |代理用户可以读取、创建和修改"联系人"文件夹中的项目。  <br/> |
|自定义警报  <br/> |代理用户具有对"联系人"文件夹的自定义访问权限。  <br/> |
   
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



[AddDelegate 操作](adddelegate-operation.md)
  
[UpdateDelegate 操作](updatedelegate-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)


[添加代理人](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

