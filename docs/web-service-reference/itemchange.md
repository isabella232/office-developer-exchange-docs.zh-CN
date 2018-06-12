---
title: ItemChange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ItemChange
api_type:
- schema
ms.assetid: 5cb43b02-d444-4d9c-9075-cdc5a4427daf
description: ItemChange 元素包含项标识符和更新应用到的项。
ms.openlocfilehash: d10ce96cacb0be7411c4e8230ebc9b2803b7a5b1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826145"
---
# <a name="itemchange"></a>ItemChange

**ItemChange**元素包含项标识符和更新应用到的项。 
  
[UpdateItem](updateitem.md)
  
[ItemChanges](itemchanges.md)
  
[ItemChange](itemchange.md)
  
```xml
<ItemChange>
   <ItemId/>
   <Updates>...</Updates>
</ItemChange>
```

 **ItemChangeType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ItemId](itemid.md) <br/> |包含在 Exchange 存储中的项目的唯一标识符和更改的键。 如果未使用的[OccurrenceItemId](occurrenceitemid.md)或[RecurringMasterItemId](recurringmasteritemid.md)元素，此元素是必需的。  <br/> |
|[OccurrenceItemId](occurrenceitemid.md) <br/> |标识定期项目的一个匹配项。 如果使用此元素是必需的。 如果未使用的[RecurringMasterItemId](recurringmasteritemid.md)或[ItemId](itemid.md)元素，此元素是必需的。  <br/> |
|[RecurringMasterItemId](recurringmasteritemid.md) <br/> |标识通过其相关的匹配项的标识符之一确定定期主项目。 如果使用此元素是必需的。 如果未使用的[OccurrenceItemId](occurrenceitemid.md)或[ItemId](itemid.md)元素，此元素是必需的。  <br/> |
|[更新 （项）](updates-item.md) <br/> |包含定义的数组的 append、 设置和删除项目属性更改。 此元素是必需的。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ItemChanges](itemchanges.md) <br/> |包含确定项目和更新以应用于项目的[ItemChange](itemchange.md)元素的数组。  <br/> 以下是此元素的 XPath 表达式：  <br/>  `/UpdateItem/ItemChanges` <br/> |
   
## <a name="remarks"></a>备注

可在**ItemChange**元素只能包含单个[ItemId](itemid.md)、 [OccurrenceItemId](occurrenceitemid.md)或[RecurringMasterItemId](recurringmasteritemid.md)元素。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[UpdateItem 操作](updateitem-operation.md)

