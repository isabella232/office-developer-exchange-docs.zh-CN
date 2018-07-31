---
title: FolderChange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderChange
api_type:
- schema
ms.assetid: 23279750-131b-4e1a-b7d1-be235c4e0891
description: FolderChange 元素表示要在单个文件夹执行的更改的集合。
ms.openlocfilehash: f25defa9974f7b5dd0c683c7657983741890d45d
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354328"
---
# <a name="folderchange"></a>FolderChange

**FolderChange**元素表示要在单个文件夹执行的更改的集合。 
  
- [UpdateFolder](updatefolder.md) 
- [FolderChanges](folderchanges.md) 
- [FolderChange](folderchange.md)
  
```xml
<FolderChange>
   <FolderId/>
   <Updates/>
</FolderChange>
```

```xml
<FolderChange>
   <DistinguishedFolderId/>
   <Updates/>
</FolderChange>
```

**FolderChangeType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |包含要更新的文件夹的标识符和更改密钥。  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |标识可以通过名称引用的 MicrosoftExchange Server 2007 文件夹。  <br/> |
|[Updates 文件夹](updates-folder.md) <br/> |定义文件夹，由[文件夹 Id](folderid.md)或[DistinguishedFolderId](distinguishedfolderid.md)元素执行更新的类型。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FolderChanges](folderchanges.md) <br/> |表示的文件夹的更改的集合。  <br/> 下面是此元素的 XPath 表达式:    <br/>  `/UpdateFolder/FolderChanges` <br/> |
   
## <a name="remarks"></a>说明

描述此元素的架构位于运行 Exchange Server 2007 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [UpdateFolder Operation](updatefolder-operation.md)

