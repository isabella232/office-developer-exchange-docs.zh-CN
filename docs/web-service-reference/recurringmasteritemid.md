---
title: RecurringMasterItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RecurringMasterItemId
api_type:
- schema
ms.assetid: 5800b58c-f3d7-4d8f-acc0-d13e02f4e258
description: RecurringMasterItemId 元素通过标识一个定期的主项目来标识该项目的相关发生项的标识符。
ms.openlocfilehash: 896a9ce95d619e7bb44c8158288bc4f62ce417d9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529880"
---
# <a name="recurringmasteritemid"></a>RecurringMasterItemId

**RecurringMasterItemId**元素通过标识一个定期的主项目来标识该项目的相关发生项的标识符。 
  
```XML
<RecurringMasterItemId OccurrenceId="" ChangeKey="" />
```

 **RecurringMasterItemIdType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**OccurrenceId** <br/> |标识定期主项目的单个事件。 此特性是必需的。  <br/> |
|**ChangeKey** <br/> |标识定期主项目的单个事件的特定版本。 此外，还会标识定期主项目，因为它和单个事件将包含相同的更改密钥。 此特性是可选的。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GlobalItemIds](globalitemids.md) <br/> |包含邮箱中所有会话项目的项标识符的集合。  <br/> |
|[ItemChange](itemchange.md) <br/> |包含项目标识符和要应用于项目的更新。 <br/> <br/> 下面是此元素的 XPath 表达式：  <br/> <br/>  `/UpdateItem/ItemChanges/ItemChange[i]` <br/> |
|[ItemIds](itemids.md) <br/> | 包含项目、具体值项目和定期主项目的唯一标识，这些标识用于删除、发送、获取、移动或复制 Exchange 存储中的项目。 <br/> <br/>  下面是此元素的 XPath 表达式：  <br/><br/>  `/DeleteItem/ItemIds` <br/>  `/SendItem/ItemIds` <br/>  `/GetItem/ItemIds` <br/>  `/MoveItem/ItemIds` <br/>  `/CopyItem//ItemIds` <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="example"></a>示例

下面的示例通过使用标识符56lkjh6 标识其匹配项之一来标识定期主项目。
  
```XML
<RecurringMasterItemId OccurrenceId="56lkjh6" />
```

## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [OccurrenceItemId](occurrenceitemid.md)
- [FindConversation 操作](findconversation-operation.md)

