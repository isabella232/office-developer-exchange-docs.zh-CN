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
description: ParentFolderIds 元素标识 FindItem 和 FindFolder 操作搜索的文件夹。
ms.openlocfilehash: 7c4dcc98d1cabc8e97f2846880c73111dd307dfb
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354167"
---
# <a name="parentfolderids"></a>ParentFolderIds

**ParentFolderIds**元素标识 FindItem 和 FindFolder 操作搜索的文件夹。 
  
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
|[FolderId](folderid.md) <br/> |包含一个文件夹的标识符和更改键。 此元素或[DistinguishedFolderId](distinguishedfolderid.md)元素，则必须使用**ParentFolderIds**元素。  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |标识可以通过名称引用的 Microsoft Exchange Server 2007 文件夹。 此元素或[文件夹 Id](folderid.md)元素，则必须使用**ParentFolderIds**元素。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FindFolder](findfolder.md) <br/> |定义一个请求，以确定邮箱中的文件夹。  <br/> |
|[FindItem](finditem.md) <br/> |定义查找邮箱中的项目的请求。  <br/> |
|[ResolveNames](resolvenames.md) <br/> |定义请求解析模糊名称。  <br/> |
   
## <a name="remarks"></a>说明

[文件夹 Id](folderid.md)或[DistinguishedFolderId](distinguishedfolderid.md)元素，则必须使用**ParentFolderIds**元素。 搜索可以定义任意的数量的文件夹。 
  
## <a name="example"></a>示例

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindFolder Traversal="Shallow" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [FindFolder 操作](findfolder-operation.md)  
- [FindItem 操作](finditem-operation.md) 
- [ResolveNames 操作](resolvenames-operation.md)

