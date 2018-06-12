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
description: FolderName 元素标识单个托管自定义文件夹添加到邮箱。
ms.openlocfilehash: 56a7a7d256624c5103c88a333222807519d21501
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754397"
---
# <a name="foldername"></a>FolderName

**FolderName**元素标识单个托管自定义文件夹添加到邮箱。 
  
[CreateManagedFolder](createmanagedfolder.md)
  
[FolderNames](foldernames.md)
  
[FolderName](foldername.md)
  
```xml
<FolderName>...</FolderName>
```

 **string**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FolderNames](foldernames.md) <br/> |包含命名托管的自定义文件夹添加到邮箱的数组。  <br/> 以下是此元素的 XPath 表达式：  <br/>  `/CreateManagedFolder/FolderNames` <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。 文本值表示的文件夹名称。
  
## <a name="remarks"></a>备注

尽管可以使用 Exchange Web 服务添加到邮箱的托管自定义文件夹，但不能使用相同的技术以访问可用托管自定义文件夹的列表。 通过使用 Exchange 命令行管理程序命令或通过使用 Active Directory 目录服务的 API 的接口，您可以获取托管自定义文件夹的列表。 文件夹名称为相应的 Active Directory 对象的名称。
  
您可以使用[FindFolder 操作](findfolder-operation.md)查找托管自定义文件夹。 使用[DeleteFolder 操作](deletefolder-operation.md)删除托管自定义文件夹。 
  
请务必注意**FolderName**是组织中现有托管自定义文件夹的名称。 尝试添加文件夹不在组织中将导致错误响应。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[FindFolder Operation](findfolder-operation.md)


[Finding Folders](http://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
  
[Adding Managed Folders](http://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

