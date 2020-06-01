---
title: Updates 文件夹
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Updates
api_type:
- schema
ms.assetid: b047e3a4-a5ab-4098-b7a0-273bc809e702
description: Updates元素中包含的一组定义的元素追加、 设置，以及删除对文件夹属性的更改。
ms.openlocfilehash: 3282171dfc188a9d4735a19a97e80fe0e2f79b89
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457177"
---
# <a name="updates-folder"></a>Updates 文件夹

本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **Updates**元素中包含的一组定义的元素追加、 设置，以及删除对文件夹属性的更改。 
  
- [UpdateFolder](updatefolder.md)
  
- [FolderChanges](folderchanges.md)
  
- [FolderChange](folderchange.md)
  
- [Updates 文件夹](updates-folder.md)
  
```xml
<Updates>
   <AppendToFolderField/>
   <SetFolderField/>
   <DeleteFolderField/>
</Updates>
```

**NonEmptyArrayOfFolderChangeDescriptionsType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[AppendToFolderField](appendtofolderfield.md) <br/> |表示要在[UpdateFolder Operation](updatefolder-operation.md)期间追加到文件夹属性数据。  <br/> |
|[SetFolderField](setfolderfield.md) <br/> |表示对[UpdateFolder Operation](updatefolder-operation.md)中的文件夹上的单个属性的更新。  <br/> |
|[DeleteFolderField](deletefolderfield.md) <br/> |表示要在[UpdateFolder Operation](updatefolder-operation.md)期间从文件夹中删除给定的属性的操作。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FolderChange](folderchange.md) <br/> |表示要在单个文件夹上进行的更改的集合。  <br/> 下面是此元素的 XPath 表达式:  `/UpdateFolder/FolderChanges/FolderChange[i]` <br/> |
   
## <a name="remarks"></a>说明

描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [UpdateFolder 操作](updatefolder-operation.md)
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

