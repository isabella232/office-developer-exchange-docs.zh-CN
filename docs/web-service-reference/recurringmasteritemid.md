---
title: RecurringMasterItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RecurringMasterItemId
api_type:
- schema
ms.assetid: 5800b58c-f3d7-4d8f-acc0-d13e02f4e258
description: RecurringMasterItemId 元素通过标识其相关项之一的标识符来标识定期主项目。
ms.openlocfilehash: d00794f2b5b1893e1829a3f09df9f3e88266964d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523627"
---
# <a name="recurringmasteritemid"></a>RecurringMasterItemId

**RecurringMasterItemId** 元素通过标识其相关项之一的标识符来标识定期主项目。 
  
```XML
<RecurringMasterItemId OccurrenceId="" ChangeKey="" />
```

 **RecurringMasterItemIdType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**OccurrenceId** <br/> |标识定期主项目的单个匹配项。 此特性是必需的。  <br/> |
|**ChangeKey** <br/> |标识定期主项目的单个匹配项的特定版本。 此外，还标识了定期主项目，因为它和单个项目将包含相同的更改键。 此特性是可选的。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GlobalItemIds](globalitemids.md) <br/> |包含邮箱中所有会话项目的项目标识符集合。  <br/> |
|[ItemChange](itemchange.md) <br/> |包含项目标识符和要应用于项目的更新。 <br/> <br/> 下面是此元素的 XPath 表达式：  <br/> <br/>  `/UpdateItem/ItemChanges/ItemChange[i]` <br/> |
|[ItemIds](itemids.md) <br/> | 包含项目、发生项和用于删除、发送、获取、移动或复制项目（用于删除、发送、获取、移动或复制项目）Exchange标识。 <br/> <br/>  下面是此元素的 XPath 表达式：  <br/><br/>  `/DeleteItem/ItemIds` <br/>  `/SendItem/ItemIds` <br/>  `/GetItem/ItemIds` <br/>  `/MoveItem/ItemIds` <br/>  `/CopyItem//ItemIds` <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>注解

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="example"></a>示例

以下示例通过标识其标识符为 56lkjh6 的事件之一来标识定期主项目。
  
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

