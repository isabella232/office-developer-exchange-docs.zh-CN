---
title: OccurrenceItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OccurrenceItemId
api_type:
- schema
ms.assetid: 4a15bbc3-5b93-4193-b9ec-da32f0a9a552
description: OccurrenceItemId 元素标识定期项目的单个事件。
ms.openlocfilehash: 37c3a2442afb3302bca88ef0301e98013ff0319b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468374"
---
# <a name="occurrenceitemid"></a>OccurrenceItemId

**OccurrenceItemId**元素标识定期项目的单个事件。 
  
```XML
<OccurrenceItemId RecurringMasterId="" ChangeKey="" InstanceIndex=""/>
```

**OccurrenceItemIdType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**RecurringMasterId** <br/> |标识定期项目的定期母版。 此特性是必需的。  <br/> |
|**ChangeKey** <br/> |标识定期母版或项目发生的特定版本。 如果定期主数据或其任何发生发生更改，则**ChangeKey**会发生更改。 对于定期母版和所有事件， **ChangeKey**是相同的。  <br/> |
|**InstanceIndex** <br/> |标识项目发生的索引。 此特性是必需的。 此值表示一个整数。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GlobalItemIds](globalitemids.md) <br/> |包含邮箱中所有会话项目的项标识符的集合。  <br/> |
|[ItemIds](itemids.md) <br/> | 包含项目、具体值项目和定期主项目的唯一标识，这些标识用于删除、发送、获取、移动或复制 Exchange 存储中的项目。 <br/><br/>下面是此元素的 XPath 表达式： <br/><br/>  `/DeleteItem/ItemIds` <br/>  `/SendItem/ItemIds` <br/>  `/GetItem/ItemIds` <br/><br/>**注意**： [MoveItem 操作](moveitem-operation.md)和[CopyItem 操作](copyitem-operation.md)仅适用于单个日历项目和定期的主项目。 通过这些操作，项目发生次数无效。           |
|[ItemChange](itemchange.md) <br/> |包含项目标识符和要应用于项目的更新。<br/><br/> 下面是此元素的 XPath 表达式：   <br/>  `/UpdateItem/ItemChanges/ItemChange[i]` <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="example"></a>示例

下面的示例确定具有标识34vswe4 的定期项的第四次发生。
  
```XML
<OccurrenceItemId RecurringMasterId="34vswe4" InstanceIndex="4" />
```

## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [RecurringMasterItemId](recurringmasteritemid.md)
- [FindConversation 操作](findconversation-operation.md)
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

