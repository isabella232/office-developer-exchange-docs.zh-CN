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
description: FolderChange 元素表示要对单个文件夹执行的更改的集合。
ms.openlocfilehash: e4a025bef100fdd478be545b6448b15886e47c60
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530237"
---
# <a name="folderchange"></a>FolderChange

**FolderChange**元素表示要对单个文件夹执行的更改的集合。 
  
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
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |标识可通过名称引用的 MicrosoftExchange Server 2007 文件夹。  <br/> |
|[Updates 文件夹](updates-folder.md) <br/> |定义在由[FolderId](folderid.md)或[DistinguishedFolderId](distinguishedfolderid.md)元素标识的文件夹上执行的更新类型。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FolderChanges](folderchanges.md) <br/> |表示文件夹的更改集合。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/UpdateFolder/FolderChanges` <br/> |
   
## <a name="remarks"></a>备注

描述此元素的架构位于运行 Exchange Server 2007 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [UpdateFolder Operation](updatefolder-operation.md)

