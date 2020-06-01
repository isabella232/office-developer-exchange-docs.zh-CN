---
title: AlternatePublicFolderItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AlternatePublicFolderItemId
api_type:
- schema
ms.assetid: a67df9b9-8fdb-42de-b9c5-8377b71fa3d9
description: AlternatePublicFolderItemId 元素描述要转换为另一种标识符格式的公用文件夹项目标识符。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: 11a9fafec78a9bd14e4d98982fd38954d45e4d1a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464768"
---
# <a name="alternatepublicfolderitemid"></a>AlternatePublicFolderItemId

**AlternatePublicFolderItemId**元素描述要转换为另一种标识符格式的公用文件夹项目标识符。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。 
  
- [ConvertId](convertid.md)
  
- [SourceIds](sourceids.md)
  
- [AlternatePublicFolderItemId](alternatepublicfolderitemid.md)
  
```xml
<AlternatePublicFolderItemId FolderId="" Format="" ItemId=""/>
```

 **AlternatePublicFolderItemIdType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|FolderId  <br/> |标识包含公用文件夹项目的公用文件夹。 此特性是必需的。  <br/> |
|Format  <br/> |标识描述要转换的公用文件夹项目标识符的格式。 此特性是必需的。  <br/> |
|ItemId  <br/> |标识符要转换的公用文件夹项目。 此特性是必需的。  <br/> |
   
#### <a name="format-attribute-values"></a>格式属性值

|**值**|**说明**|
|:-----|:-----|
|EwsLegacyId  <br/> |介绍 exchange 2007 的初始发布版本中的 Exchange Web 服务生成的标识符。  <br/> |
|EwsId  <br/> |介绍了 Exchange Web 服务从 Exchange 2007 SP1 开始生成的标识符。  <br/> |
|EntryId  <br/> |描述 MAPI 标识符，如 PR_ENTRYID 属性中所示。  <br/> |
|HexEntryId  <br/> |描述了 PR_ENTRYID 属性的十六进制编码表示形式。 这是可用性日历事件标识符的格式。  <br/> |
|StoreId  <br/> |描述 Exchange 存储标识符。  <br/> |
|OwaId  <br/> |介绍 Outlook Web Access 标识符。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**描述**|
|:-----|:-----|
|[SourceIds](sourceids.md) <br/> |包含要转换的源标识符。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
   
## <a name="remarks"></a>说明

描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅

- [ConvertId 操作](convertid-operation.md)
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)
- [转换标识符](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

