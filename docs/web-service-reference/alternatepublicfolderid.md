---
title: AlternatePublicFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- AlternatePublicFolderId
api_type:
- schema
ms.assetid: 0a4dc1cc-959e-4b93-aa3a-3020ca8b8a02
description: AlternatePublicFolderId 元素描述要转换为其他标识符格式的公用文件夹标识符。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: 7c4471c0c1e3e1eee3b47eba42f924340891c777
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59525356"
---
# <a name="alternatepublicfolderid"></a>AlternatePublicFolderId

**AlternatePublicFolderId** 元素描述要转换为其他标识符格式的公用文件夹标识符。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。 
  
- [ConvertId](convertid.md)
  
- [SourceIds](sourceids.md)
  
- [AlternatePublicFolderId](alternatepublicfolderid.md)
  
```xml
<AlternatePublicFolderId FolderId="" Format="" />
```

 **AlternatePublicFolderIdType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|FolderId  <br/> |包含要转换的公用文件夹标识符。 此特性是必需的。  <br/> |
|格式  <br/> |标识描述要转换的公用文件夹标识符的格式。 此特性是必需的。  <br/> |
   
#### <a name="format-attribute"></a>Format 属性

|**值**|**说明**|
|:-----|:-----|
|EwsLegacyId  <br/> |介绍由 Exchange 2007 初始发行版中的 Web 服务Exchange标识符。  <br/> |
|EwsId  <br/> |介绍从 2007 SP1 Exchange Web 服务Exchange生成的标识符。  <br/> |
|EntryId  <br/> |描述 MAPI 标识符，如 PR_ENTRYID 属性。  <br/> |
|HexEntryId  <br/> |描述 PR_ENTRYID 属性的十六进制编码表示形式。 这是可用性日历事件标识符的格式。  <br/> |
|StoreId  <br/> |介绍Exchange标识符。  <br/> |
|OwaId  <br/> |描述一Outlook Web Access 标识符。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[SourceIds](sourceids.md) <br/> |包含要转换的源标识符。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。  <br/> |
   
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

