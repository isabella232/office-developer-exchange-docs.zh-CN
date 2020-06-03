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
description: FractionalPageItemView 元素说明分页视图的起始位置以及在 FindItem 请求中返回的最大项目数。
ms.openlocfilehash: cbf45838558873dc5846823c2d1b26cf2c8af514
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461308"
---
# <a name="fractionalpageitemview"></a>FractionalPageItemView

**FractionalPageItemView**元素说明分页视图的起始位置以及在[FindItem](finditem.md)请求中返回的最大项目数。 
  
[FindItem](finditem.md)
  
[FractionalPageItemView](fractionalpageitemview.md)
  
```xml
<FractionalPageItemView MaxEntriesReturned="" Numerator="" Denominator=""/>
```

 **FractionalPageViewType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**MaxEntriesReturned** <br/> |标识要在[FindItem](finditem.md)响应中返回的最大结果数。 此特性是可选的。 如果未指定此属性，则该调用将返回所有可用项目。  <br/> |
|**分子** <br/> |表示从结果集的开头的小数偏移量的分子。 此特性是必需的。 分子必须等于或小于分母。 此属性必须代表等于或大于零的整数值。  <br/> 有关详细信息，请参阅本主题后面的 "备注"。  <br/> |
|**母** <br/> |表示从结果集内的项目总数开始的小数偏移量的分母。 此特性是必需的。 此属性必须代表大于1的整数值。  <br/> 有关详细信息，请参阅本主题后面的 "备注"。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |定义在邮箱中查找项目的请求。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/FindItem` <br/> |
   
## <a name="remarks"></a>备注

从一组找到的项目开始的分页视图偏移量按分数进行描述。 由**分子**和**分母**属性定义的小数描述了信息页面的起始位置。 例如，如果**分子**等于四，**分母**等于5，则返回的信息的页面从 fifths 中的一个条目开始，该条目位于结果集内。 
  
如果分式的计算结果为零，则指示结果集的开头。 如果该分数的计算结果为1，则指示结果集的结尾。
  
> [!NOTE]
> 分数表示页面的起始点，而不是返回结果集中的结果数。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="example"></a>示例

下面的示例展示了一个[FindItem](finditem.md)请求。 请求返回搜索结果中的项目，这些项目在结果集内的所有项目的第二个第二个之后开始。 
  
```
<?xml version="1.0" encoding="utf-8"?>
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

例如，如果结果集包含九个项目，分页视图将返回最长12个项目，从项目中的第一到结果集中找到了三分之二。 在这种情况下，页面从第七个项目开始。 页面将包含第七个、第八个和第九个项目。 如果分子设置为零，则页面视图将返回结果集中的所有项，前提是该数字小于**MaxEntriesReturned**属性。 
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[FindItem 操作](finditem-operation.md)


[查找项目](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

