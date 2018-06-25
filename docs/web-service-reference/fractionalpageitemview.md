---
title: FractionalPageItemView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FractionalPageItemView
api_type:
- schema
ms.assetid: 4111afec-35e7-4c6f-b291-9bbba603f633
description: FractionalPageItemView 元素介绍其中分页的视图启动和 FindItem 请求中返回的最大项目数。
ms.openlocfilehash: 38c35d2b68dabfca1a43ab034deaf72c47b0ea66
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754418"
---
# <a name="fractionalpageitemview"></a>FractionalPageItemView

**FractionalPageItemView**元素介绍其中分页的视图启动和[FindItem](finditem.md)请求中返回的最大项目数。 
  
[FindItem](finditem.md)
  
[FractionalPageItemView](fractionalpageitemview.md)
  
```xml
<FractionalPageItemView MaxEntriesReturned="" Numerator="" Denominator=""/>
```

 **FractionalPageViewType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|**MaxEntriesReturned** <br/> |标识要[FindItem](finditem.md)响应中返回结果的最大数量。 此属性是可选的。 如果未指定此属性，则呼叫将返回所有可用的项。  <br/> |
|**分子** <br/> |从结果集中的开始表示分数偏移量的分子。 此属性是必需的。 分子必须等于或小于分母。 此属性必须表示等于或大于零的整数值。  <br/> 有关详细信息，请参阅本主题后面的备注。  <br/> |
|**分母** <br/> |从结果集中的项目总数开始代表分数偏移量的分母，为。 此属性是必需的。 此属性必须表示大于 1 的整数值。  <br/> 有关详细信息，请参阅本主题后面的备注。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |定义查找邮箱中的项目的请求。  <br/> 以下是此元素的 XPath 表达式：  <br/>  `/FindItem` <br/> |
   
## <a name="remarks"></a>注解

通过一小部分介绍了从找到项集开始的分页的视图偏移量。 分数，由**分子**和**分母**属性定义，介绍的信息页的起始位置。 例如，如果**分子**等于四**分母**等于 5，返回的信息开始的项的页面位于五分之四中到结果集中的方式。 
  
如果 fraction 计算结果为零，用于指示结果集的开头。 如果 fraction 计算结果为一个，表明结果集的末尾。
  
> [!NOTE]
> 分数表示的页面的起始点，则将返回结果集内的结果不数量。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="example"></a>示例

下面的示例演示一个[FindItem](finditem.md)请求。 请求后启动第二个第三的所有项目在结果集中在搜索结果中返回的项目。 
  
```
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
          <t:FieldURI FieldURI="item:Subject"/>
        </t:AdditionalProperties>
      </ItemShape>
      <FractionalPageItemView MaxEntriesReturned="12" Numerator="2" Denominator="3"/>
      <GroupBy Order="Descending">
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

例如，如果在结果集中包含九个项目，分页的视图将返回达 12 个项，从开始到结果集中的方式中找到项三分之二。 在这种情况下，页上启动在第七个项目。 页将包含的第七个，第八个和第九个项目。 如果分子设置为零，将页面视图将在结果集中，只要数小于**MaxEntriesReturned**属性返回的所有项目。 
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[FindItem 操作](finditem-operation.md)


[查找项目](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

