---
title: FolderName
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderName
api_type:
- schema
ms.assetid: c5a2cd55-ac47-43bf-94b5-3ab3a4c28a62
description: 文件夹名元素标识要添加到邮箱中的单个托管自定义文件夹。
ms.openlocfilehash: 1bb63e50c06e81337d1142a6624213fb2db12457
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461350"
---
# <a name="foldername"></a>FolderName

**文件夹**名元素标识要添加到邮箱中的单个托管自定义文件夹。 
  
[CreateManagedFolder](createmanagedfolder.md)
  
[FolderNames](foldernames.md)
  
[FolderName](foldername.md)
  
```xml
<FolderName>...</FolderName>
```

 **string**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FolderNames](foldernames.md) <br/> |包含要添加到邮箱中的已命名托管自定义文件夹的数组。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/CreateManagedFolder/FolderNames` <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。 该文本值表示文件夹的名称。
  
## <a name="remarks"></a>备注

虽然您可以使用 Exchange Web 服务将托管自定义文件夹添加到邮箱中，但不能使用相同的技术来访问可用的托管自定义文件夹的列表。 您可以通过使用 Exchange 命令行管理程序命令或通过使用与 Active Directory 目录服务接口的 API，获取托管自定义文件夹的列表。 文件夹名称是对应的 Active Directory 对象的名称。
  
您可以使用[FindFolder 操作](findfolder-operation.md)查找托管自定义文件夹。 使用[DeleteFolder 操作](deletefolder-operation.md)可删除托管自定义文件夹。 
  
请务必注意，**文件夹**名称是组织中现有托管自定义文件夹的名称。 尝试添加不在组织中的文件夹将导致错误响应。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[FindFolder 操作](findfolder-operation.md)


[Finding Folders](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
  
[Adding Managed Folders](https://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

