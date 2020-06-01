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
description: ItemChange 元素包含项目标识符和要应用于项目的更新。
ms.openlocfilehash: 916ef1ba2c7a709ec1fd80ababd72999506773c4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459915"
---
# <a name="itemchange"></a>ItemChange

**ItemChange**元素包含项目标识符和要应用于项目的更新。 
  
- [UpdateItem](updateitem.md) 
- [ItemChanges](itemchanges.md)
- [ItemChange](itemchange.md)
  
```xml
<ItemChange>
   <ItemId/>
   <Updates>...</Updates>
</ItemChange>
```

```xml
<ItemChange>
   <OccurrenceItemId>...</OccurrenceItemId>
   <Updates>...</Updates>
</ItemChange>
```

```xml
<ItemChange>
   <RecurringMasterItemId>...</RecurringMasterItemId>
   <Updates>...</Updates>
</ItemChange>
```

**ItemChangeType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ItemId](itemid.md) <br/> |包含 Exchange 存储中某项的唯一标识符和更改键。 如果未使用[OccurrenceItemId](occurrenceitemid.md)或[RecurringMasterItemId](recurringmasteritemid.md)元素，则此元素是必需的。  <br/> |
|[OccurrenceItemId](occurrenceitemid.md) <br/> |标识定期项目的单个事件。 如果使用此元素，则此元素是必需的。 如果未使用[RecurringMasterItemId](recurringmasteritemid.md)或[ItemId](itemid.md)元素，则此元素是必需的。  <br/> |
|[RecurringMasterItemId](recurringmasteritemid.md) <br/> |通过标识一个 "定期" 主项目的 "标识符" 标识该项目。 如果使用此元素，则此元素是必需的。 如果未使用[OccurrenceItemId](occurrenceitemid.md)或[ItemId](itemid.md)元素，则此元素是必需的。  <br/> |
|[更新（项目）](updates-item.md) <br/> |包含定义追加、设置和删除对项属性所做的更改的数组。 此元素是必需的。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ItemChanges](itemchanges.md) <br/> |包含标识项目和要应用于项目的更新的[ItemChange](itemchange.md)元素的数组。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/UpdateItem/ItemChanges` <br/> |
   
## <a name="remarks"></a>备注

只有一个[ItemId](itemid.md)、 [OccurrenceItemId](occurrenceitemid.md)或[RecurringMasterItemId](recurringmasteritemid.md)元素可以在**ItemChange**元素中使用。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [UpdateItem 操作](updateitem-operation.md)

