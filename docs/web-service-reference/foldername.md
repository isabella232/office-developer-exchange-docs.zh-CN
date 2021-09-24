---
title: FolderName
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FolderName
api_type:
- schema
ms.assetid: c5a2cd55-ac47-43bf-94b5-3ab3a4c28a62
description: FolderName 元素标识要添加到邮箱的单个托管自定义文件夹。
ms.openlocfilehash: 76263d56c423411a58ea45d691ce93e2b3202571
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59511563"
---
# <a name="foldername"></a>FolderName

**FolderName** 元素标识要添加到邮箱的单个托管自定义文件夹。 
  
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
|[FolderNames](foldernames.md) <br/> |包含要添加到邮箱的命名托管自定义文件夹的数组。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/CreateManagedFolder/FolderNames` <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。 文本值表示文件夹名称。
  
## <a name="remarks"></a>注解

尽管您可以使用 Exchange Web 服务将托管自定义文件夹添加到邮箱，但您不能使用相同的技术访问可用托管自定义文件夹的列表。 通过使用命令行管理程序命令或与 Active Directory 目录服务交互的 API，Exchange托管自定义文件夹的列表。 文件夹名称是对应的 Active Directory 对象的名称。
  
可以使用 [FindFolder 操作查找](findfolder-operation.md) 托管自定义文件夹。 使用 [DeleteFolder 操作](deletefolder-operation.md) 可删除托管自定义文件夹。 
  
需要注意的是 **，FolderName** 是组织中现有托管自定义文件夹的名称。 尝试添加不在组织的文件夹将导致错误响应。 
  
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

