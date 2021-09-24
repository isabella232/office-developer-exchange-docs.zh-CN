---
title: RootFolder (FindItemResponseMessage)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RootFolder
api_type:
- schema
ms.assetid: 187e009f-efaa-42a8-8962-329a645213ab
description: RootFolder 元素包含在 FindItem 操作期间对单个根文件夹进行搜索的结果。
ms.openlocfilehash: 96fa9e162dde34394e7c34543dd25a6f018ae7de
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59527535"
---
# <a name="rootfolder-finditemresponsemessage"></a>RootFolder (FindItemResponseMessage)

**RootFolder** 元素包含在 FindItem 操作期间对单个根文件夹 [进行搜索的结果](finditem-operation.md)。
  
```xml
<RootFolder IndexedPagingOffset="" NumeratorOffset="" AbsoluteDenominator="" IncludesLastItemInRange="" TotalItemsInView="">
   <Items/>
   <Groups/>
</RootFolder>
```

 **FindItemParentType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**IndexedPagingOffset** <br/> |表示在使用索引分页视图时，下一个请求应该使用的下一个索引。  <br/> |
|**NumeratorOffset** <br/> |表示使用分数页面视图时用于下一个请求的新分子值。  <br/> |
|**AbsoluteDenominator** <br/> |表示执行小数分页时要用于下一个请求的下一个分母。  <br/> |
|**IncludesLastItemInRange** <br/> |指示当前结果是否包含查询中的最后一项，因此不需要进一步分页。  <br/> |
|**TotalItemsInView** <br/> |表示通过限制的项目总数。 在分组的 [FindItem](finditem-operation.md)操作中 **，TotalItemsInView** 属性返回视图中的项目总数以及组总数。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Items](items.md) <br/> |包含找到的搜索条件在 [FindItem](finditem-operation.md) 操作请求中标识的项目数组。  <br/> |
|[组](groups.md) <br/> |包含找到的组的集合，这些组在 [FindItem](finditem-operation.md) 操作请求中标识了搜索和聚合条件。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FindItemResponseMessage](finditemresponsemessage.md) <br/> |包含 [FindItem](finditem-operation.md) 操作请求的状态和结果。  <br/> |
   
## <a name="remarks"></a>注解

描述此元素的架构位于在安装了客户端访问服务器角色Exchange Server运行的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[FindItem 操作](finditem-operation.md)
  
[IndexedPagingOffset](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.IndexedPagingOffset.aspx)
  
[NumeratorOffset](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.NumeratorOffset.aspx)
  
[AbsoluteDenominator](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.AbsoluteDenominator.aspx)
  
[IncludesLastItemInRange](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.IncludesLastItemInRange.aspx)
  
[TotalItemsInView](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.TotalItemsInView.aspx)


[查找项目](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

