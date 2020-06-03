---
title: 组
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Groups
api_type:
- schema
ms.assetid: 6b6b2d67-219d-4dfb-a4ed-d627b1cfb33f
description: Groups 元素包含使用在 FindItem 操作请求中标识的搜索和聚合条件找到的组的集合。
ms.openlocfilehash: 915d9dffd6d8cec1def6634e6b70642d563b5242
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530787"
---
# <a name="groups"></a>组

**Groups**元素包含使用在[FindItem 操作](finditem-operation.md)请求中标识的搜索和聚合条件找到的组的集合。 
  
```xml
<Groups>
   <GroupedItems/>
</Groups>
```

 **ArrayOfGroupedItemsType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[GroupedItems](groupeditems.md) <br/> |表示作为分组[FindItem 操作](finditem-operation.md)调用的结果的项的集合。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[RootFolder （FindItemResponseMessage）](rootfolder-finditemresponsemessage.md) <br/> |包含在[FindItem 操作](finditem-operation.md)操作过程中搜索单个根文件夹的结果。  <br/> |
   
## <a name="remarks"></a>备注

将为结果中的每个不同的组执行一个[GroupedItems](groupeditems.md)实例。 
  
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

