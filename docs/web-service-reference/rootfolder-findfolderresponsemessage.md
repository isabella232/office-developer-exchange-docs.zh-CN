---
title: RootFolder （FindFolderResponseMessage）
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
description: RootFolder 元素包含在 FindFolder 操作过程中搜索单个根文件夹的结果。
ms.openlocfilehash: b5601d6abec67196c9991908e272a2122a201d69
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457135"
---
# <a name="rootfolder-findfolderresponsemessage"></a>RootFolder （FindFolderResponseMessage）

**RootFolder**元素包含在[FindFolder 操作](findfolder-operation.md)过程中搜索单个根文件夹的结果。
  
```xml
<RootFolder IndexedPagingOffset="" NumeratorOffset="" AbsoluteDenominator="" IncludesLastItemInRange="" TotalItemsInView="">
   <Folders/>
</RootFolder>
```

 **FindFolderParentType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|IndexedPagingOffset  <br/> |表示在使用索引分页视图时应用于下一个请求的下一个索引。  <br/> |
|NumeratorOffset  <br/> |表示在使用分数页面视图时用于下一个请求的新的分子值。  <br/> |
|AbsoluteDenominator  <br/> |表示执行分数分页时用于下一个请求的下一个分母。  <br/> |
|IncludesLastItemInRange  <br/> |指示当前结果是否包含查询中的最后一个文件夹，以便不需要进一步分页。  <br/> |
|TotalItemsInView  <br/> |表示传递限制的文件夹总数。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Folders](folders-ex15websvcsotherref.md) <br/> |包含通过使用[FindFolder 操作](findfolder-operation.md)找到的文件夹数组。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FindFolderResponseMessage](findfolderresponsemessage.md) <br/> |包含[FindFolder 操作](findfolder-operation.md)请求的状态和结果。  <br/> |
   
## <a name="remarks"></a>备注

描述此元素的架构位于运行 Microsoft Exchange Server 2010 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[FindFolder 操作](findfolder-operation.md)


[Finding Folders](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

