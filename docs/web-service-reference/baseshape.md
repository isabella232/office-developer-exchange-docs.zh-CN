---
title: BaseShape
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- BaseShape
api_type:
- schema
ms.assetid: 42c04f3b-abaa-4197-a3d6-d21677ffb1c0
description: BaseShape 元素标识要在项目或文件夹响应中返回的属性集。
ms.openlocfilehash: 9b3f00ff94fbfe6ad6373b16ad95eb9136f81c64
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464488"
---
# <a name="baseshape"></a>BaseShape

**BaseShape**元素标识要在项目或文件夹响应中返回的属性集。 
  
```xml
<BaseShape>IdOnly or Default or AllProperties</BaseShape>
```

 **DefaultShapeNamesType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无
  
### <a name="parent-elements"></a>父元素

|**元素**|**描述**|
|:-----|:-----|
|[FolderShape](foldershape.md) <br/> | 标识要包括在 GetFolder、FindFolder 或 SyncFolderHierarchy 响应中的文件夹属性。<br/><br/>下面是此元素的 XPath 表达式：<br/><br/>`/GetFolder/FolderShape` <br/>  `/FindFolder/FolderShape` <br/>  `/SyncFolderHierarchy/FolderShape` <br/> |
|[ItemShape](itemshape.md) <br/> | 标识要包括在 GetItem、FindItem 或 SyncFolderItems 响应中的项目属性和内容。<br/><br/>下面是此元素的 XPath 表达式：<br/><br/>`/GetItem/ItemShape` <br/>  `/FindItem/ItemShape` <br/>  `/SyncFolderItems/ItemShape` <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。 下表列出了可能的文本值。
  
**BaseShape 元素的文本值**

|**值**|**说明**|
|:-----|:-----|
|IdOnly  <br/> |仅返回项或文件夹 ID。  <br/> |
|默认  <br/> |返回一组属性，这些属性定义为项或文件夹的默认值。  <br/> |
|AllProperties  <br/> |返回 Exchange 业务逻辑层用来构造文件夹的所有属性。  <br/> |
   
下表列出了为 FindFolder 请求返回的默认属性。 给定文件夹的所有子文件夹按名称的顺序返回。
  
**默认属性**

|**Folder**|**默认属性**|
|:-----|:-----|
|Inbox  <br/> |FolderId、显示名称、未读计数、总计计数、子文件夹计数  <br/> |
|联系人  <br/> |FolderId、显示名称、总计计数、子文件夹计数  <br/> |
|日历  <br/> |FolderId、显示名称、子文件夹计数  <br/> |
|草稿  <br/> |FolderId、显示名称、未读计数、总计计数、子文件夹计数  <br/> |
|已删除项目  <br/> |FolderId、显示名称、未读计数、总计计数、子文件夹计数  <br/> |
|其他文件夹  <br/> |FolderId、显示名称、未读计数、总计计数、子文件夹计数  <br/> |
|发件箱  <br/> |FolderId、显示名称、未读计数、总计计数、子文件夹计数  <br/> |
|任务  <br/> |FolderId、显示名称、过期计数、总计计数、子文件夹计数  <br/> |
|注释  <br/> |FolderId、显示名称、总计计数、子文件夹计数  <br/> |
   
## <a name="remarks"></a>备注

若要返回除[BaseShape](baseshape.md)元素标识的属性之外的属性，请使用[AdditionalProperties](additionalproperties.md)元素。 
  
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
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [FolderShape](foldershape.md)
- [ItemShape](itemshape.md)

