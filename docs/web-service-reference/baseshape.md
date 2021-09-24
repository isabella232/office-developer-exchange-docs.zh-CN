---
title: BaseShape
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- BaseShape
api_type:
- schema
ms.assetid: 42c04f3b-abaa-4197-a3d6-d21677ffb1c0
description: BaseShape 元素标识项目或文件夹响应中要返回的属性集。
ms.openlocfilehash: b4e7f5c6d6520e7338f274b6275e371366b1bed5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514856"
---
# <a name="baseshape"></a>BaseShape

**BaseShape** 元素标识项目或文件夹响应中要返回的属性集。 
  
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

|**元素**|**说明**|
|:-----|:-----|
|[FolderShape](foldershape.md) <br/> | 标识要包括在 GetFolder、FindFolder 或 SyncFolderHierarchy 响应中的文件夹属性。<br/><br/>下面是此元素的 XPath 表达式：<br/><br/>`/GetFolder/FolderShape` <br/>  `/FindFolder/FolderShape` <br/>  `/SyncFolderHierarchy/FolderShape` <br/> |
|[ItemShape](itemshape.md) <br/> | 标识要包括在 GetItem、FindItem 或 SyncFolderItems 响应中的项目属性和内容。<br/><br/>下面是此元素的 XPath 表达式：<br/><br/>`/GetItem/ItemShape` <br/>  `/FindItem/ItemShape` <br/>  `/SyncFolderItems/ItemShape` <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。 下表列出了可能的文本值。
  
**BaseShape 元素的文本值**

|**值**|**说明**|
|:-----|:-----|
|IdOnly  <br/> |仅返回项目或文件夹 ID。  <br/> |
|默认值  <br/> |返回定义为项目或文件夹的默认值的属性集。  <br/> |
|AllProperties  <br/> |返回业务逻辑层Exchange构造文件夹的所有属性。  <br/> |
   
下表列出了为 FindFolder 请求返回的默认属性。 按名称顺序返回给定文件夹的所有子文件夹。
  
**默认属性**

|**Folder**|**默认属性**|
|:-----|:-----|
|Inbox  <br/> |FolderId、显示名称、未读计数、总计计数、子文件夹计数  <br/> |
|联系人  <br/> |FolderId、显示名称、总计、子文件夹计数  <br/> |
|日历  <br/> |FolderId、显示名称、子文件夹计数  <br/> |
|草稿  <br/> |FolderId、显示名称、未读计数、总计计数、子文件夹计数  <br/> |
|已删除项目  <br/> |FolderId、显示名称、未读计数、总计计数、子文件夹计数  <br/> |
|其他文件夹  <br/> |FolderId、显示名称、未读计数、总计计数、子文件夹计数  <br/> |
|发件箱  <br/> |FolderId、显示名称、未读计数、总计计数、子文件夹计数  <br/> |
|Tasks  <br/> |FolderId、显示名称、过去到期计数、总计数、子文件夹计数  <br/> |
|注意  <br/> |FolderId、显示名称、总计、子文件夹计数  <br/> |
   
## <a name="remarks"></a>注解

若要返回 [BaseShape](baseshape.md) 元素标识的属性之外的属性，请使用 [AdditionalProperties](additionalproperties.md) 元素。 
  
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

