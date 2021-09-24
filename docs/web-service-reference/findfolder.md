---
title: FindFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FindFolder
api_type:
- schema
ms.assetid: b8a59740-d978-454c-9629-a10792385ba0
description: FindFolder元素定义的请求，以便查找邮箱中的文件夹。
ms.openlocfilehash: 431efde28e417efec04f6fa1625a81b3766cb705
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518440"
---
# <a name="findfolder"></a>FindFolder

本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **FindFolder** 元素定义的请求，以便查找邮箱中的文件夹。 
  
```xml
<FindFolder Traversal="Shallow/Deep/SoftDeleted">
   <FolderShape/>
   <IndexedPageFolderView/>
   <Restriction/>
   <ParentFolderIds/>
</FindFolder>
```

```xml
<FindFolder Traversal="Shallow/Deep/SoftDeleted">
   <FolderShape/>
   <FractionalPageFolderView/>
   <Restriction/>
   <ParentFolderIds/>
</FindFolder>
```

**FindFolderType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|遍历  <br/> |定义如何执行搜索。此属性是必需的。  <br/> |
   
#### <a name="traversal-attribute-values"></a>遍历属性值

|**值**|**说明**|
|:-----|:-----|
|浅  <br/> |指示 FindFolder 操作来搜索仅标识的文件夹并返回只有文件夹 Id 尚未删除的项。这被称为浅层遍历。  <br/> |
|深  <br/> |指示 FindFolder 操作来标识的父文件夹的所有子文件夹中搜索并返回只有文件夹 Id 尚未删除的项。这被称为 deep 遍历。  <br/> |
|SoftDeleted  <br/> |指示要执行浅跨度搜索已删除的项的 FindFolder 操作。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[FolderShape](foldershape.md) <br/> |标识要在 FindFolder 响应中包含的文件夹属性。  <br/> |
|[IndexedPageFolderView](indexedpagefolderview.md) <br/> |描述如何分页的物料信息 FindFolder 响应中返回。此元素是可选的。  <br/> |
|[FractionalPageFolderView](fractionalpagefolderview.md) <br/> |介绍了分页的视图开始，并在 FindFolder 请求中返回的最大文件夹数。此元素是可选的。  <br/> |
|[限制](restriction.md) <br/> |定义用于筛选文件夹中的 FindFolder 操作的查询的限制。此元素是可选的。  <br/> |
|[ParentFolderIds](parentfolderids.md) <br/> |标识要搜索的 FindFolder 操作的文件夹。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>注解

描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="example"></a>示例

FindFolder 请求的下面的示例演示如何在窗体中查找位于收件箱中的所有文件夹的请求。
  
```xml
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

- [FindFolder Operation](findfolder-operation.md)

