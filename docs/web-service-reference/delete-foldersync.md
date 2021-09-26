---
title: Delete (FolderSync)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Delete
api_type:
- schema
ms.assetid: c4397d91-43ef-40a9-a80e-d31501a33caa
description: Delete 元素标识要在本地客户端存储中删除的单个文件夹。
ms.openlocfilehash: bd57c2f093fceda9948d8289fbd55b527bcf10cc
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542496"
---
# <a name="delete-foldersync"></a>Delete (FolderSync)

Delete 元素标识要在本地客户端存储中删除的单个文件夹。 
  
- [SyncFolderHierarchyResponse](syncfolderhierarchyresponse.md)  
- [ResponseMessages](responsemessages.md)  
- [SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md)  
- [Changes (Hierarchy)](changes-hierarchy.md)  
- [Delete (FolderSync)](delete-foldersync.md)
  
```xml
<Delete>
   <FolderId/>
</Delete>
```

**SyncFolderHierarchyDeleteType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |包含一个文件夹的标识符和更改键。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Changes (Hierarchy)](changes-hierarchy.md) <br/> |包含更改类型的排序数组，这些更改类型表示客户端上的文件夹与运行 Microsoft Exchange Server 2007 的计算机上的文件夹之间的差异的类型。  <br/> |
   
## <a name="remarks"></a>注解

描述此元素的架构位于安装了客户端访问服务器角色的 Exchange 2007 计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [SyncFolderHierarchy 操作](syncfolderhierarchy-operation.md)
- [Exchange 的 EWS 引用](ews-reference-for-exchange.md)
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

