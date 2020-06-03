---
title: GroupedItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GroupedItems
api_type:
- schema
ms.assetid: 53170df4-4272-4b37-b23f-cd8e2d4a7396
description: GroupedItems 元素表示作为分组 FindItem 操作调用的结果的项的集合。
ms.openlocfilehash: 0ee1ca3c6d0cf98e2daefa60a1cb1fd096cda478
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530809"
---
# <a name="groupeditems"></a>GroupedItems

**GroupedItems**元素表示作为分组[FindItem 操作](finditem-operation.md)调用的结果的项的集合。 
  
[FindItemResponse](finditemresponse.md)
  
[ResponseMessages](responsemessages.md)
  
[FindItemResponseMessage](finditemresponsemessage.md)
  
[RootFolder （FindItemResponseMessage）](rootfolder-finditemresponsemessage.md)
  
[组](groups.md)
  
[GroupedItems](groupeditems.md)
  
```xml
<GroupedItems>
   <GroupIndex/>
   <Items/>
</GroupedItems>
```

 **GroupedItemsType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[GroupIndex](groupindex.md) <br/> |表示用于对分组的[FindItem 操作](finditem-operation.md)调用中的项进行分组的属性值。  <br/> |
|[Items](items.md) <br/> |包含分组项的数组。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[组](groups.md) <br/> |包含使用[FindItem 操作](finditem-operation.md)请求中标识的搜索和聚合条件找到的组的集合。  <br/> |
   
## <a name="remarks"></a>备注

描述此元素的架构位于运行 Microsoft Exchange Server 2010 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[FindItem 操作](finditem-operation.md)


[查找项目](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

