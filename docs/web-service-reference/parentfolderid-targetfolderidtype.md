---
title: ParentFolderId (TargetFolderIdType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ParentFolderId
api_type:
- schema
ms.assetid: 0e3e6e5f-06d0-499b-8ca4-d36036521658
description: ParentFolderId 元素标识的文件夹中创建一个新的文件夹或搜索 FindConversation 操作的文件夹。
ms.openlocfilehash: 8e80b9b342274a8b2004838ebd16f8425a2d3fa3
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353824"
---
# <a name="parentfolderid-targetfolderidtype"></a>ParentFolderId (TargetFolderIdType)

**ParentFolderId**元素标识的文件夹中创建一个新的文件夹或搜索[FindConversation 操作](findconversation-operation.md)的文件夹。
  
```xml
<ParentFolderId>
   <DistinguishedFolderId/>
</ParentFolderId>
```

```xml
<ParentFolderId>
   <FolderId/> 
</ParentFolderId>
```

**TargetFolderIdType**

## <a name="attributes-and-elements"></a>属性和元素

**ParentFolderId**元素包含两个子元素。 子元素的架构中相互排斥。 
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |包含所需的标识符和文件夹中的可选更改密钥其创建一个新文件夹或[FindConversation 操作](findconversation-operation.md)搜索文件夹。 使用此元素不包括[DistinguishedFolderId](distinguishedfolderid.md)元素的使用。  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |标识默认的 Microsoft Exchange Server 2007 文件夹。 使用此元素不包括[文件夹 Id](folderid.md)元素的使用。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CreateFolder](createfolder.md) <br/> |定义一个请求 Exchange 数据库中创建文件夹。  <br/> 下面是此元素的 XPath 表达式:  `/CreateFolder` <br/> |
|[FindConversation](findconversation.md) <br/> |定义查找邮箱中的对话的请求。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>说明

两个子元素用于定义将包含新文件夹的文件夹。 您必须选择[文件夹 Id](folderid.md)或[DistinguishedFolderId](distinguishedfolderid.md)元素来标识新的文件夹的父文件夹。 不能同时使用这两个元素。 此元素需要创建文件夹。 
  
[ParentFolderId](parentfolderid.md)元素描述现有项目和文件夹的位置。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [CreateFolder 操作](createfolder-operation.md)
- [FindConversation 操作](findconversation-operation.md)
- [Creating Folders (Exchange Web Services)](http://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

