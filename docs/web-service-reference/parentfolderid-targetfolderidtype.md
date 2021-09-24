---
title: ParentFolderId (TargetFolderIdType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ParentFolderId
api_type:
- schema
ms.assetid: 0e3e6e5f-06d0-499b-8ca4-d36036521658
description: ParentFolderId 元素标识新建文件夹的文件夹或要搜索 FindConversation 操作的文件夹。
ms.openlocfilehash: 53a5721b2c20c211a61b7e71b2e4f636700456b4
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524621"
---
# <a name="parentfolderid-targetfolderidtype"></a>ParentFolderId (TargetFolderIdType)

**ParentFolderId** 元素标识新建文件夹的文件夹或要搜索 [FindConversation](findconversation-operation.md)操作的文件夹。
  
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

**ParentFolderId** 元素包含两个子元素。 子元素在架构中相互排斥。 
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |包含新建文件夹的文件夹或搜索 [FindConversation](findconversation-operation.md)操作的文件夹的必需标识符和可选更改键。 使用此元素将不使用 [DistinguishedFolderId](distinguishedfolderid.md) 元素。  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |标识默认的 Microsoft Exchange Server 2007 文件夹。 使用此元素将排除 [FolderId 元素](folderid.md) 的使用。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CreateFolder](createfolder.md) <br/> |定义在数据库数据库内创建文件夹Exchange请求。  <br/> 下面是此元素的 XPath 表达式:  `/CreateFolder` <br/> |
|[FindConversation](findconversation.md) <br/> |定义在邮箱中查找对话的请求。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>注解

这两个子元素用于定义将包含新文件夹的文件夹。 必须选择 [FolderId](folderid.md) 或 [DistinguishedFolderId](distinguishedfolderid.md) 元素来标识新文件夹的父文件夹。 不能同时使用这两个元素。 创建文件夹需要此元素。 
  
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

