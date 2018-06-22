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
description: BaseShape 元素标识项目或文件夹响应中返回的属性的集。
ms.openlocfilehash: 69b27d23fd75d4c1a274f31dfa419b759dbb2bbe
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753323"
---
# <a name="baseshape"></a>BaseShape

**BaseShape**元素标识项目或文件夹响应中返回的属性的集。 
  
```xml
<BaseShape>IdOnly or Default or AllProperties</BaseShape>
```

 **DefaultShapeNamesType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FolderShape](foldershape.md) <br/> | 标识要在 GetFolder、 FindFolder 或 SyncFolderHierarchy 响应中包含的文件夹属性。<br/><br/>下面是此元素的 XPath 表达式：<br/><br/>`/GetFolder/FolderShape` <br/>  `/FindFolder/FolderShape` <br/>  `/SyncFolderHierarchy/FolderShape` <br/> |
|[ItemShape](itemshape.md) <br/> | 标识项目属性和 GetItem、 FindItem 或 SyncFolderItems 响应中包括的内容。<br/><br/>下面是此元素的 XPath 表达式：<br/><br/>`/GetItem/ItemShape` <br/>  `/FindItem/ItemShape` <br/>  `/SyncFolderItems/ItemShape` <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。 下表列出了可能的文本值。
  
**BaseShape 元素的文本值**

|**值**|**说明**|
|:-----|:-----|
|IdOnly  <br/> |返回仅项目或文件夹的 id。  <br/> |
|默认  <br/> |返回一组定义为项目或文件夹的默认属性。  <br/> |
|AllProperties  <br/> |返回所有 Exchange 业务逻辑层用于构造文件夹的属性。  <br/> |
   
下表列出了 FindFolder 请求返回的默认属性。 按名称顺序返回给定文件夹的所有子文件夹。
  
**默认属性**

|**Folder**|**默认属性**|
|:-----|:-----|
|Inbox  <br/> |文件夹 Id，显示名称、 未读的计数、 总计、 子文件夹数  <br/> |
|联系人  <br/> |文件夹 Id，显示名称、 总计、 子文件夹计数  <br/> |
|日历  <br/> |文件夹 Id，显示名称子文件夹数  <br/> |
|草稿  <br/> |文件夹 Id，显示名称、 未读的计数、 总计、 子文件夹数  <br/> |
|已删除的项目  <br/> |文件夹 Id，显示名称、 未读的计数、 总计、 子文件夹数  <br/> |
|其他文件夹  <br/> |文件夹 Id，显示名称、 未读的计数、 总计、 子文件夹数  <br/> |
|发件箱  <br/> |文件夹 Id，显示名称、 未读的计数、 总计、 子文件夹数  <br/> |
|任务  <br/> |文件夹 Id，显示名称过去截止计数、 总计、 子文件夹计数  <br/> |
|笔记  <br/> |文件夹 Id，显示名称、 总计、 子文件夹计数  <br/> |
   
## <a name="remarks"></a>备注

若要返回除外标识[BaseShape](baseshape.md)元素的属性，请使用[AdditionalProperties](additionalproperties.md)元素。 
  
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
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [FolderShape](foldershape.md)
- [ItemShape](itemshape.md)

