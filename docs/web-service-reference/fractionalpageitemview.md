---
title: FractionalPageItemView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FractionalPageItemView
api_type:
- schema
ms.assetid: 4111afec-35e7-4c6f-b291-9bbba603f633
description: FractionalPageItemView 元素描述分页视图的起始位置以及 FindItem 请求中返回的最大项目数。
ms.openlocfilehash: 0d948bad0ba24c4a105be32daa645d1864cb4f3b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59530244"
---
# <a name="fractionalpageitemview"></a>FractionalPageItemView

**FractionalPageItemView** 元素描述分页视图的起始位置以及 [FindItem](finditem.md)请求中返回的最大项目数。 
  
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
|**MaxEntriesReturned** <br/> |标识在 [FindItem](finditem.md) 响应中返回的最大结果数。 此特性是可选的。 如果未指定此属性，调用将返回所有可用项。  <br/> |
|**Numerator** <br/> |表示从起始位置开始的小数偏移的结果集。 此特性是必需的。 分子必须等于或小于分母。 此属性必须表示等于或大于零的整数值。  <br/> 有关详细信息，请参阅本主题稍后的"说明"。  <br/> |
|**Denominator** <br/> |表示从项目总数开始的小数偏移的分母结果集。 此特性是必需的。 此属性必须表示大于 1 的整数值。  <br/> 有关详细信息，请参阅本主题稍后的"说明"。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |定义查找邮箱中的项目的请求。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/FindItem` <br/> |
   
## <a name="remarks"></a>注解

从找到的项目集开始分页的视图偏移量由一个分数描述。 分数（由 **Numerator** 和 **Denominator** 属性定义）描述信息页的起始位置。 例如，如果 **Numerator** 等于 4 且 **Denominator** 等于 5，则返回信息的页面从位于进入该数字的 4/5 结果集。 
  
如果分数计算结果为零，则指示结果集的开始。 如果分数计算结果为 1，则表明结果结果集。
  
> [!NOTE]
> 分数表示页面的起始点，而不是返回结果集的结果数。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="example"></a>示例

下面的示例展示了 [FindItem](finditem.md) 请求。 该请求从搜索结果中返回项目，这些结果在项目的所有项目的第二个三结果集。 
  
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

例如，如果 结果集包含 9 个项目，则分页视图将返回最多 12 个项目，从找到的项的三分之二开始结果集。 在这种情况下，页面从第七个项目开始。 该页面将包含第七项、第八项和第九项。 如果分子设置为零，则页面视图将返回该数字结果集只要数字小于 **MaxEntriesReturned** 属性。 
  
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

