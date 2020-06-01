---
title: ItemIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ItemIds
api_type:
- schema
ms.assetid: 6b82122b-5544-4adf-91b7-ef2db7d5046f
description: ItemIds 元素包含项目、具体值项目和定期主项目的唯一标识，这些标识用于删除、发送、获取、移动或复制 Exchange 存储中的项目。
ms.openlocfilehash: bbd594ce2610bd625b0e16a0383fda552ee9eb19
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460601"
---
# <a name="itemids"></a>ItemIds
  
**ItemIds**元素包含项目、具体值项目和定期主项目的唯一标识，这些标识用于删除、发送、获取、移动或复制 Exchange 存储中的项目。
  
```xml
<ItemIds>
   <ItemId/>
   <OccurrenceItemId/>
   <RecurringMasterItemId/>
</ItemIds>
```

**NonEmptyArrayOfBaseItemIdsType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。 
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ItemId](itemid.md) <br/> |包含 Exchange 存储中某项的唯一标识符和更改键。  <br/> |
|[OccurrenceItemId](occurrenceitemid.md) <br/> |标识定期项目的单个事件。  <br/> |
|[RecurringMasterItemId](recurringmasteritemid.md) <br/> |通过标识一个 "定期" 主项目的 "标识符" 标识该项目。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[对话 (ConversationType)](conversation-conversationtype.md) <br/> |表示单个对话。  <br/> |
|[DeleteItem](deleteitem.md) <br/> |定义在 Exchange 存储中删除项目的请求。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/DeleteItem` <br/> |
|[SendItem](senditem.md) <br/> |定义在 Exchange 存储中发送邮件的请求的根元素。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/SendItem` <br/> |
|[GetItem](getitem.md) <br/> |定义从 Exchange 存储中获取项目的请求。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/GetItem` <br/> |
|[MoveItem](moveitem.md) <br/> |定义在 Exchange 存储中移动项目的请求。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/MoveItem` <br/> |
|[CopyItem](copyitem.md) <br/> |定义在 Exchange 存储中复制项目的请求。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/CopyItem` <br/> |
   
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [DeleteItem 操作](deleteitem-operation.md)
- [SendItem 操作](senditem-operation.md) 
- [GetItem 操作](getitem-operation.md)
- [MoveItem 操作](moveitem-operation.md)
- [CopyItem 操作](copyitem-operation.md)
- [FindConversation 操作](findconversation-operation.md)

