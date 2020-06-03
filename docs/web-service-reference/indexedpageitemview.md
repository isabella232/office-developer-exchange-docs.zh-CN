---
title: IndexedPageItemView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IndexedPageItemView
api_type:
- schema
ms.assetid: 6d1b0b04-cc35-4a57-bd7a-824136d14fda
description: IndexedPageItemView 元素介绍如何为 FindItem 操作或 FindConversation 操作请求返回分页对话或项目信息。
ms.openlocfilehash: 0a66f17855fd425082e3651886d3eeec4f217ac4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456911"
---
# <a name="indexedpageitemview"></a>IndexedPageItemView

**IndexedPageItemView**元素介绍如何为[FindItem 操作](finditem-operation.md)或[FindConversation 操作](findconversation-operation.md)请求返回分页对话或项目信息。 
  
```XML
<IndexedPageViewItemView MaxEntriesReturned="" Offset="" BasePoint=""/>
```

 **IndexedPageViewType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**MaxEntriesReturned** <br/> |描述要在响应中返回的项目或对话的最大数量。 此特性是可选的。  <br/> |
|**Offset** <br/> |描述**BasePoint**中的偏移量。 如果**BasePoint**等于开头，则偏移量为正值。 如果**BasePoint**等于 End，则处理的是负的偏移量。 这标识在响应中将首先传递哪个项目或对话。 此特性是必需的。  <br/> |
|**BasePoint** <br/> |描述项目或对话的页面是从使用搜索条件找到的项目或对话集的开头还是结尾开始。 从末尾进行的查找始终向后搜索。 此特性是必需的。  <br/> |
   
#### <a name="basepoint-attribute"></a>BasePoint 属性

|**值**|**说明**|
|:-----|:-----|
|始  <br/> |分页视图从找到的对话或项目集的开头开始。  <br/> |
|End  <br/> |分页视图从找到的对话或项目集的末尾开始。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**描述**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |定义在邮箱中查找项目的请求。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/FindItem` <br/> |
|[FindConversation](findconversation.md) <br/> |定义在邮箱中查找对话的请求。  <br/> |
   
## <a name="remarks"></a>备注

从末尾进行查找包括移到由偏移量标识的源。 此外，还会按请求的记录数向后移动指针。 例如，如果有100条记录，偏移量是从末尾到25，则搜索从75开始。 如果返回10个记录，指针将向后移动10条记录到65，并返回记录65至75。 下一个索引为64。 距页面末尾的下一个偏移量是100减去64，等于36。 36是来自 end 的下一个偏移量的值，以获取下一个索引页。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="example"></a>示例

下面的示例展示了一个[FindItem 操作](finditem-operation.md)请求。 每个项目都返回其 ID 和主题。 响应中最多可返回6个项目，如**MaxEntriesReturned**属性指定。 项目按重要性分组按升序排列。 组中的项目按主题进行聚合。 
  
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

