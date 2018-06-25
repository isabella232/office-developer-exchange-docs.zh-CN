---
title: ContactsView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContactsView
api_type:
- schema
ms.assetid: 8534f44b-a5af-4a9f-9621-23a3eff5f9d8
description: ContactsView 元素定义基于按字母顺序排列的显示名称的联系人项搜索。
ms.openlocfilehash: e578eb4dd0042b8c478e883c7fa54d7f2e984229
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753520"
---
# <a name="contactsview"></a>ContactsView

**ContactsView**元素定义基于按字母顺序排列的显示名称的联系人项搜索。 
  
[FindItem](finditem.md)
  
[ContactsView](contactsview.md)
  
```xml
<ContactsView MaxEntriesReturned="" InitialName="" FinalName="" />
```

**ContactsViewType**

## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|**MaxEntriesReturned** <br/> |最大个数要[FindItem](finditem.md)响应中返回的结果。  <br/> |
|**InitialName** <br/> |在联系人列表中要返回的响应中定义第一个名称。 如果指定的初始名称定义的文化上下文不在联系人列表中，按字母顺序排列的下一个名称将返回，除**FinalName**如果出现的下一个名称。 如果省略**InitialName**属性，则响应将包含联系人列表中的第一个名称开头的联系人的列表。 此属性是可选的。  <br/> |
|**FinalName** <br/> |在联系人列表中要返回的响应中定义的最后一个名称。 如果省略**FinalName**属性，则响应中将包含指定的排序顺序中的所有后续联系人。 如果指定的最终名称不在联系人列表中，按字母顺序排列的下一个名称由文化上下文定义将排除。  <br/><br/>例如，如果 FinalName ="Name"，但名称不在联系人列表、 具有的联系人显示 Name1 的名称或名称将不包括在内。  <br/><br/>此属性是可选的。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |定义查找邮箱中的项目的请求。<br/><br/> 以下是此元素的 XPath 表达式：  <br/>  `/FindItem` <br/> |
   
## <a name="remarks"></a>备注

描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="example"></a>示例

请求的下面的示例演示如何查找与前三个联系人启动与联系人已凯利的显示名称。
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem Traversal="Shallow" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="contacts:DisplayName"/>
        </t:AdditionalProperties>
      </ItemShape>
      <ContactsView MaxEntriesReturned="3" InitialName="Kelly Rollin" />
      <SortOrder>
        <t:FieldOrder Order="Descending">
          <t:FieldURI FieldURI="contacts:DisplayName"/>
        </t:FieldOrder>
        </SortOrder>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="contacts"/>
      </ParentFolderIds>
    </FindItem>
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

- [FindItem 操作](finditem-operation.md)
- [查找项目](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

