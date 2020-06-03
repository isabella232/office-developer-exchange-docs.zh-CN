---
title: ParentFolderId （TargetFolderIdType）
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
description: ParentFolderId 元素标识在其中创建新文件夹的文件夹或用于搜索 FindConversation 操作的文件夹。
ms.openlocfilehash: 36e63266d10603c4d453a37e2b0d22e02599e516
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467800"
---
# <a name="parentfolderid-targetfolderidtype"></a>ParentFolderId （TargetFolderIdType）

**ParentFolderId**元素标识在其中创建新文件夹的文件夹或用于搜索[FindConversation 操作](findconversation-operation.md)的文件夹。
  
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

## <a name="attributes-and-elements"></a>特性和元素

**ParentFolderId**元素包含两个子元素。 在架构中，子元素是相互排斥的。 
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |包含要在其中创建新文件夹的文件夹的必需标识符和可选更改键，或者是要为[FindConversation 操作](findconversation-operation.md)搜索的文件夹。 使用此元素将排除[DistinguishedFolderId](distinguishedfolderid.md)元素的使用。  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |标识默认的 Microsoft Exchange Server 2007 文件夹。 使用此元素将排除[FolderId](folderid.md)元素的使用。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CreateFolder](createfolder.md) <br/> |定义在 Exchange 数据库中创建文件夹的请求。  <br/> 下面是此元素的 XPath 表达式:  `/CreateFolder` <br/> |
|[FindConversation](findconversation.md) <br/> |定义在邮箱中查找对话的请求。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>说明

这两个子元素用于定义将包含新文件夹的文件夹。 您必须选择 " [FolderId](folderid.md) " 或 " [DistinguishedFolderId](distinguishedfolderid.md) " 元素以标识新文件夹的父文件夹。 您不能同时使用这两个元素。 此元素是创建文件夹所必需的。 
  
[ParentFolderId](parentfolderid.md)元素描述现有项目和文件夹的位置。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [CreateFolder 操作](createfolder-operation.md)
- [FindConversation 操作](findconversation-operation.md)
- [Creating Folders (Exchange Web Services)](https://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

