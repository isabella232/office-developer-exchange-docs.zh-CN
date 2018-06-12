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
description: IndexedPageItemView 元素描述如何分页的对话或项目 FindItem 操作或 FindConversation 操作请求返回信息。
ms.openlocfilehash: f1743e22087158c1889977f03774fccbc5577390
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825919"
---
# <a name="indexedpageitemview"></a>IndexedPageItemView

**IndexedPageItemView**元素描述如何分页的对话或项目[FindItem 操作](finditem-operation.md)或[FindConversation 操作](findconversation-operation.md)请求返回信息。 
  
```XML
<IndexedPageViewItemView MaxEntriesReturned="" Offset="" BasePoint=""/>
```

 **IndexedPageViewType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|**MaxEntriesReturned** <br/> |最大个数的项目或在响应中返回的对话。 此属性是可选的。  <br/> |
|**Offset** <br/> |介绍从**基点**的偏移量。 如果**基点**等于开头，则偏移量为正数。 如果**基点**等于结束，则好像它是负数处理偏移量。 这标识哪一项或对话将第一个响应中传送。 此属性是必需的。  <br/> |
|**基点** <br/> |描述是否将从开头或结尾的一项或使用的搜索条件找到的对话的启动项或对话页。 始终从末尾查找往回搜索。 此属性是必需的。  <br/> |
   
#### <a name="basepoint-attribute"></a>基点属性

|**值**|**说明**|
|:-----|:-----|
|开始  <br/> |分页的视图从找到对话或项目集的开头。  <br/> |
|End  <br/> |找到对话或项目集末尾开始分页的视图。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |定义查找邮箱中的项目的请求。  <br/> 以下是此元素的 XPath 表达式：  <br/>  `/FindItem` <br/> |
|[FindConversation](findconversation.md) <br/> |定义查找邮箱中的对话的请求。  <br/> |
   
## <a name="remarks"></a>备注

从末尾查找涉及将移至原点标识的偏移量。 此外，将指针向后移动请求的记录数。 例如，如果有 100 条记录，偏移量为 25 从末尾，从 75 开始搜索。 如果返回了 10 条记录，10 个附加到 65 记录，并返回记录到 75 65 指针是向后移动。 下一个索引为 64。 从页面结尾的下一步偏移量为 100 减 64 其等于 36。 36 是从结束后，若要获取的已编制索引的下一页的下一步偏移量的值。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="example"></a>示例

下面的示例演示一个[FindItem 操作](finditem-operation.md)请求。 每个项目返回其 ID 和主题。 在响应中，指定**MaxEntriesReturned**属性返回的六个项目的最大值。 中按重要性分组的升序排列项目。 组中的项目进行聚合按主题。 
  
```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem Traversal="Shallow" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[FindItem 操作](finditem-operation.md)
  
[FindConversation Operation](findconversation-operation.md)


[查找项目](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

