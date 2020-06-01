---
title: 更新（项目）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Updates
api_type:
- schema
ms.assetid: 5c1a855e-390d-4713-9d10-6e86ca392814
description: Updates 元素包含一组元素，这些元素定义追加、设置和删除对项目属性所做的更改。
ms.openlocfilehash: 6902ea4d3d3d9adc074745d5642cdfa6d91a9163
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456351"
---
# <a name="updates-item"></a>更新（项目）

**Updates**元素包含一组元素，这些元素定义追加、设置和删除对项目属性所做的更改。 
  
- [UpdateItem](updateitem.md)
  
- [ItemChanges](itemchanges.md)
  
- [ItemChange](itemchange.md)
  
- [更新（项目）](updates-item.md)
  
```xml
<Updates>
   <AppendToItemField/>
   <SetItemField/>
   <DeleteItemField/>
</Updates>
```

**NonEmptyArrayOfItemChangeDescriptionsType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[AppendToItemField](appendtoitemfield.md) <br/> |表示在[UpdateItem 操作](updateitem-operation.md)过程中追加到项的单个属性的数据。  <br/> |
|[SetItemField](setitemfield.md) <br/> |表示对[UpdateItem 操作](updateitem-operation.md)中项的单个属性的更新。  <br/> |
|[DeleteItemField](deleteitemfield.md) <br/> |表示在[UpdateItem 操作](updateitem-operation.md)过程中从项中删除给定属性的操作。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ItemChange](itemchange.md) <br/> |包含项目标识符和要应用于项目的更新。  <br/> 下面是此元素的 XPath 表达式:  `/UpdateItem/ItemChanges/ItemChange[i]` <br/> |
   
## <a name="remarks"></a>备注

此元素定义的更新将对由[ItemId](itemid.md)、 [OccurrenceItemId](occurrenceitemid.md)或[RecurringMasterItemId](recurringmasteritemid.md)元素标识的项目执行。 
  
描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [UpdateItem 操作](updateitem-operation.md)
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

