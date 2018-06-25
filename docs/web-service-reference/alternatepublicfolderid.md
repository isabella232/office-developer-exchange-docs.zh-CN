---
title: AlternatePublicFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AlternatePublicFolderId
api_type:
- schema
ms.assetid: 0a4dc1cc-959e-4b93-aa3a-3020ca8b8a02
description: AlternatePublicFolderId 元素描述将转换为另一个标识符格式的公用文件夹标识符。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。
ms.openlocfilehash: 32e6e75eb381e479baf5fdb5ad0a40b32c1b02a9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753145"
---
# <a name="alternatepublicfolderid"></a>AlternatePublicFolderId

**AlternatePublicFolderId**元素描述将转换为另一个标识符格式的公用文件夹标识符。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。 
  
- [ConvertId](convertid.md)
  
- [SourceIds](sourceids.md)
  
- [AlternatePublicFolderId](alternatepublicfolderid.md)
  
```xml
<AlternatePublicFolderId FolderId="" Format="" />
```

 **AlternatePublicFolderIdType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|文件夹 Id  <br/> |包含要转换的公用文件夹标识符。 此属性是必需的。  <br/> |
|格式  <br/> |标识描述要转换的公用文件夹标识符的格式。 此属性是必需的。  <br/> |
   
#### <a name="format-attribute"></a>Format 属性

|**值**|**说明**|
|:-----|:-----|
|EwsLegacyId  <br/> |描述所产生的 Exchange Web 服务的初始发行版本的 Exchange 2007 中的标识符。  <br/> |
|EwsId  <br/> |描述所产生的开头 Exchange 2007 SP1 的 Exchange Web 服务的标识符。  <br/> |
|EntryId  <br/> |描述 MAPI 标识符，如 PR_ENTRYID 属性中所示。  <br/> |
|HexEntryId  <br/> |介绍 PR_ENTRYID 属性的十六进制编码表示形式。 这是可用性日历事件标识符的格式。  <br/> |
|StoreId  <br/> |描述 Exchange 存储区标识符。  <br/> |
|OwaId  <br/> |介绍 Outlook Web Access 标识符。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[SourceIds](sourceids.md) <br/> |包含要转换的源标识符。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。  <br/> |
   
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅

- [ConvertId 操作](convertid-operation.md)
- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)
- [转换标识符](http://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

