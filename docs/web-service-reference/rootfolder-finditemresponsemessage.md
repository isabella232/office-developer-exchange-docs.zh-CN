---
title: RootFolder (FindItemResponseMessage)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RootFolder
api_type:
- schema
ms.assetid: 187e009f-efaa-42a8-8962-329a645213ab
description: RootFolder 元素包含 FindItem 操作过程中的单个根文件夹的搜索结果。
ms.openlocfilehash: ea17369ef4efc4112a738b430c8f0dbab3886341
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827254"
---
# <a name="rootfolder-finditemresponsemessage"></a>RootFolder (FindItemResponseMessage)

**RootFolder**元素包含[FindItem 操作](finditem-operation.md)期间的单个根文件夹的搜索结果。
  
```xml
<RootFolder IndexedPagingOffset="" NumeratorOffset="" AbsoluteDenominator="" IncludesLastItemInRange="" TotalItemsInView="">
   <Items/>
   <Groups/>
</RootFolder>
```

 **FindItemParentType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|**IndexedPagingOffset** <br/> |表示使用索引的分页视图时，则在下一个请求时应使用的下一个索引。  <br/> |
|**NumeratorOffset** <br/> |代表要用于下一个请求时使用分数页面视图的新分子值。  <br/> |
|**AbsoluteDenominator** <br/> |代表下一步分母执行分数分页时用于下一个请求。  <br/> |
|**IncludesLastItemInRange** <br/> |指示当前结果是否包含在查询中，最后一项，因此不需要进一步分页。  <br/> |
|**TotalItemsInView** <br/> |表示超出限制的项目总数。 在组合[FindItem 操作](finditem-operation.md)， **TotalItemsInView**属性返回的视图中的项目总数以及组的总数。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Items](items.md) <br/> |包含数组中找到的项目的已标识[FindItem 操作](finditem-operation.md)请求中的搜索条件。  <br/> |
|[组](groups.md) <br/> |包含一组具有[FindItem 操作](finditem-operation.md)请求中标识的搜索和聚合条件。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FindItemResponseMessage](finditemresponsemessage.md) <br/> |包含状态和[FindItem 操作](finditem-operation.md)请求的结果。  <br/> |
   
## <a name="remarks"></a>注解

描述此元素的架构位于安装了客户端访问服务器角色与运行 Exchange Server 的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
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


[查找项目](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

