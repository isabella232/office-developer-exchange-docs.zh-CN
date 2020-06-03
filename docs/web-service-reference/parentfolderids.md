---
title: ParentFolderIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ParentFolderIds
api_type:
- schema
ms.assetid: e7998023-e5e0-465c-91fa-2aa6d1559f64
description: ParentFolderIds 元素标识用于搜索的 FindItem 和 FindFolder 操作的文件夹。
ms.openlocfilehash: 6bc4b9cfe96c6c83cbeb623ec176e33177356bbc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465427"
---
# <a name="parentfolderids"></a>ParentFolderIds

**ParentFolderIds**元素标识用于搜索的 FindItem 和 FindFolder 操作的文件夹。 
  
```xml
<ParentFolderIds>
   <DistinguishedFolderId/>
<ParentFolderIds>
```

```xml
<ParentFolderIds>
   <FolderId/> 
<ParentFolderIds>
```

**NonEmptyArrayOfBaseFolderIdsType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |包含一个文件夹的标识符和更改键。 **ParentFolderIds**元素必须使用此元素或[DistinguishedFolderId](distinguishedfolderid.md)元素。  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |标识可通过名称引用的 Microsoft Exchange Server 2007 文件夹。 **ParentFolderIds**元素必须使用此元素或[FolderId](folderid.md)元素。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FindFolder](findfolder.md) <br/> |定义用于标识邮箱中的文件夹的请求。  <br/> |
|[FindItem](finditem.md) <br/> |定义在邮箱中查找项目的请求。  <br/> |
|[ResolveNames](resolvenames.md) <br/> |定义用于解析不明确名称的请求。  <br/> |
   
## <a name="remarks"></a>备注

**ParentFolderIds**元素必须使用[FolderId](folderid.md)或[DistinguishedFolderId](distinguishedfolderid.md)元素。 可以为搜索定义无限制数量的文件夹。 
  
## <a name="example"></a>示例

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindFolder Traversal="Shallow" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <FolderShape>
        <t:BaseShape>Default</t:BaseShape>
      </FolderShape>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox"/>
      </ParentFolderIds>
    </FindFolder>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [FindFolder 操作](findfolder-operation.md)  
- [FindItem 操作](finditem-operation.md) 
- [ResolveNames 操作](resolvenames-operation.md)

