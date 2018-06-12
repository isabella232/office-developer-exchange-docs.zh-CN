---
title: RootFolder (FindFolderResponseMessage)
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
ms.assetid: 5089c815-663f-46be-bc59-aed9ee20f94a
description: RootFolder 元素包含 FindFolder 操作过程中的单个根文件夹的搜索结果。
ms.openlocfilehash: 1cd79d5fa34318e7fe29606df84cbf0ef0520b93
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827253"
---
# <a name="rootfolder-findfolderresponsemessage"></a>RootFolder (FindFolderResponseMessage)

**RootFolder**元素包含[FindFolder 操作](findfolder-operation.md)期间的单个根文件夹的搜索结果。
  
```xml
<RootFolder IndexedPagingOffset="" NumeratorOffset="" AbsoluteDenominator="" IncludesLastItemInRange="" TotalItemsInView="">
   <Folders/>
</RootFolder>
```

 **FindFolderParentType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|IndexedPagingOffset  <br/> |表示使用索引的分页视图时，则在下一个请求时应使用的下一个索引。  <br/> |
|NumeratorOffset  <br/> |代表要用于下一个请求时使用分数页面视图的新分子值。  <br/> |
|AbsoluteDenominator  <br/> |代表下一步分母执行分数分页时用于下一个请求。  <br/> |
|IncludesLastItemInRange  <br/> |指示当前结果是否包含在查询中的最后一个文件夹，因此不需要进一步分页。  <br/> |
|TotalItemsInView  <br/> |代表文件夹超出限制的总数。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Folders](folders-ex15websvcsotherref.md) <br/> |包含使用[FindFolder 操作](findfolder-operation.md)找到的文件夹的数组。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FindFolderResponseMessage](findfolderresponsemessage.md) <br/> |包含状态和[FindFolder 操作](findfolder-operation.md)请求的结果。  <br/> |
   
## <a name="remarks"></a>备注

描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[FindFolder Operation](findfolder-operation.md)


[Finding Folders](http://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

