---
title: IndexedPageItemView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IndexedPageItemView
api_type:
- schema
ms.assetid: 6d1b0b04-cc35-4a57-bd7a-824136d14fda
description: IndexedPageItemView 元素描述如何返回 FindItem 操作或 FindConversation 操作请求的分页对话或项目信息。
ms.openlocfilehash: bf46bdbd457c4f4fa47e6b575d3b797b74f58995
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541124"
---
# <a name="indexedpageitemview"></a>IndexedPageItemView

**IndexedPageItemView** 元素描述如何返回 [FindItem](finditem-operation.md)操作或 [FindConversation](findconversation-operation.md)操作请求的分页对话或项目信息。 
  
```XML
<IndexedPageViewItemView MaxEntriesReturned="" Offset="" BasePoint=""/>
```

 **IndexedPageViewType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**MaxEntriesReturned** <br/> |描述在响应中返回的最大项目数或对话数。 此特性是可选的。  <br/> |
|**Offset** <br/> |描述与 **BasePoint 的偏移** 量。 如果 **BasePoint** 等于 Beginning，则偏移量为正。 如果 **BasePoint** 等于 End，则处理偏移量就像负值一样。 这将标识哪个项目或对话将在响应中第一个传递。 此特性是必需的。  <br/> |
|**BasePoint** <br/> |描述项目或对话页面是否从通过使用搜索条件找到的项目或对话集的开头或结尾开始。 从末尾查找始终向后搜索。 此特性是必需的。  <br/> |
   
#### <a name="basepoint-attribute"></a>BasePoint 属性

|**值**|**说明**|
|:-----|:-----|
|开始  <br/> |分页视图从找到的对话或项目集的开头开始。  <br/> |
|End  <br/> |分页视图从找到的对话或项目集的末尾开始。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |定义查找邮箱中的项目的请求。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/FindItem` <br/> |
|[FindConversation](findconversation.md) <br/> |定义在邮箱中查找对话的请求。  <br/> |
   
## <a name="remarks"></a>注解

从末尾进行寻找涉及移动到由偏移标识的原点。 此外，指针将移回所请求的记录数。 例如，如果有 100 条记录，并且从结尾偏移 25，则搜索从 75 开始。 如果返回 10 条记录，则指针向后移动 10 条记录到 65，并返回记录 65 到 75。 下一个索引为 64。 页面末尾的下一个偏移量是 100 减 64，等于 36。 36 是距离末尾的下一偏移量的值，用于获取下一个索引页。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="example"></a>示例

下面的示例展示了 [FindItem 操作](finditem-operation.md) 请求。 返回每个项目及其 ID 和主题。 响应中最多返回 6 个项目，如 **MaxEntriesReturned 属性** 指定。 这些项目按重要性的升序分组列出。 组中项目按主题聚合。 
  
```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem Traversal="Shallow" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject"/>
        </t:AdditionalProperties>
      </ItemShape>
      <IndexedPageItemView MaxEntriesReturned="6" BasePoint="Beginning" Offset="0" />
      <GroupBy Order="Ascending">
        <t:FieldURI FieldURI="item:Importance"/>
        <t:AggregateOn Aggregate="Maximum">
          <t:FieldURI FieldURI="item:Subject"/>
        </t:AggregateOn>
      </GroupBy>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox"/>
      </ParentFolderIds>
    </FindItem>
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



[FindItem 操作](finditem-operation.md)
  
[FindConversation 操作](findconversation-operation.md)


[查找项目](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

