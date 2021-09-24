---
title: OccurrenceItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- OccurrenceItemId
api_type:
- schema
ms.assetid: 4a15bbc3-5b93-4193-b9ec-da32f0a9a552
description: OccurrenceItemId 元素标识定期项目的单个匹配项。
ms.openlocfilehash: ac6fc081e67f3897880ad30fcc1b62fe2e844459
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515416"
---
# <a name="occurrenceitemid"></a>OccurrenceItemId

**OccurrenceItemId** 元素标识定期项目的单个匹配项。 
  
```XML
<OccurrenceItemId RecurringMasterId="" ChangeKey="" InstanceIndex=""/>
```

**OccurrenceItemIdType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**RecurringMasterId** <br/> |标识定期项目的定期主控项。 此特性是必需的。  <br/> |
|**ChangeKey** <br/> |标识定期主控项或项目事件的特定版本。 如果定期主控服务器或它的任一匹配项发生更改 **，ChangeKey 将** 发生更改。 **ChangeKey** 对于定期主控服务器和所有事件都相同。  <br/> |
|**InstanceIndex** <br/> |标识项目出现的索引。 此特性是必需的。 此值表示一个整数。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GlobalItemIds](globalitemids.md) <br/> |包含邮箱中所有会话项目的项目标识符集合。  <br/> |
|[ItemIds](itemids.md) <br/> | 包含项目、发生项和用于删除、发送、获取、移动或复制项目（用于删除、发送、获取、移动或复制项目）Exchange标识。 <br/><br/>下面是此元素的 XPath 表达式： <br/><br/>  `/DeleteItem/ItemIds` <br/>  `/SendItem/ItemIds` <br/>  `/GetItem/ItemIds` <br/><br/>**注意**[：MoveItem 操作](moveitem-operation.md)和 [CopyItem 操作](copyitem-operation.md)仅适用于单个日历项目和定期主项目。 这些操作中的项目出现次数无效。           |
|[ItemChange](itemchange.md) <br/> |包含项目标识符和要应用于项目的更新。<br/><br/> 下面是此元素的 XPath 表达式：   <br/>  `/UpdateItem/ItemChanges/ItemChange[i]` <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>注解

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="example"></a>示例

以下示例标识标识为 34vswe4 的定期项目的第四次出现。
  
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

