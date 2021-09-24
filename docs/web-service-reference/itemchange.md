---
title: ItemChange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ItemChange
api_type:
- schema
ms.assetid: 5cb43b02-d444-4d9c-9075-cdc5a4427daf
description: ItemChange 元素包含项目标识符以及要应用于项目的更新。
ms.openlocfilehash: 8ace3cf78eb902e48529a0534e39ce7d584bd164
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59537747"
---
# <a name="itemchange"></a>ItemChange

**ItemChange** 元素包含项目标识符以及要应用于项目的更新。 
  
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
|[ItemId](itemid.md) <br/> |包含项目在项目存储中的唯一标识符Exchange项。 如果未使用 [OccurrenceItemId](occurrenceitemid.md) 或 [RecurringMasterItemId](recurringmasteritemid.md) 元素，则此元素是必需的。  <br/> |
|[OccurrenceItemId](occurrenceitemid.md) <br/> |标识定期项目的单个匹配项。 如果使用，则此元素是必需的。 如果未使用 [RecurringMasterItemId](recurringmasteritemid.md) 或 [ItemId](itemid.md) 元素，则此元素是必需的。  <br/> |
|[RecurringMasterItemId](recurringmasteritemid.md) <br/> |通过标识其相关事件项的标识符之一来标识定期主项。 如果使用，则此元素是必需的。 如果未使用 [OccurrenceItemId](occurrenceitemid.md) 或 [ItemId](itemid.md) 元素，则此元素是必需的。  <br/> |
|[Updates (Item)](updates-item.md) <br/> |包含一个数组，该数组定义对项目属性的追加、设置和删除更改。 此元素是必需的。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ItemChanges](itemchanges.md) <br/> |包含一个 [ItemChange](itemchange.md) 元素数组，用于标识项目以及要应用于项目的更新。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/UpdateItem/ItemChanges` <br/> |
   
## <a name="remarks"></a>注解

**ItemChange** 元素中只能使用单个 [ItemId](itemid.md) [、OccurrenceItemId](occurrenceitemid.md)或 [RecurringMasterItemId](recurringmasteritemid.md)元素。 
  
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

