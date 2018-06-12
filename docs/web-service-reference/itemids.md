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
description: ItemIds 元素包含唯一标识的项目和匹配项，用于删除、 发送、 获取、 移动或在 Exchange 存储中复制项的定期主项目。
ms.openlocfilehash: 1bd4d6f4593a7c3b418561269d8b29707cc6030c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826155"
---
# <a name="itemids"></a>ItemIds
  
**ItemIds**元素包含唯一标识的项目和匹配项，用于删除、 发送、 获取、 移动或在 Exchange 存储中复制项的定期主项目。
  
```xml
<ItemIds>
   <ItemId/>
   <OccurrenceItemId/>
   <RecurringMasterItemId/>
</ItemIds>
```

**NonEmptyArrayOfBaseItemIdsType**

## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。 
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ItemId](itemid.md) <br/> |包含在 Exchange 存储中的项目的唯一标识符和更改的键。  <br/> |
|[OccurrenceItemId](occurrenceitemid.md) <br/> |标识定期项目的一个匹配项。  <br/> |
|[RecurringMasterItemId](recurringmasteritemid.md) <br/> |标识通过其相关的匹配项的标识符之一确定定期主项目。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[对话 (ConversationType)](conversation-conversationtype.md) <br/> |表示单个对话。  <br/> |
|[删除项](deleteitem.md) <br/> |定义删除 Exchange 存储中的项目的请求。  <br/> 以下是此元素的 XPath 表达式：  <br/>  `/DeleteItem` <br/> |
|[SendItem](senditem.md) <br/> |定义发送 Exchange 存储中的项目的请求的根元素。  <br/> 以下是此元素的 XPath 表达式：  <br/>  `/SendItem` <br/> |
|[GetItem](getitem.md) <br/> |定义从 Exchange 存储中获取项的请求。  <br/> 以下是此元素的 XPath 表达式：  <br/>  `/GetItem` <br/> |
|[MoveItem](moveitem.md) <br/> |定义将项目移 Exchange 存储中的请求。  <br/> 以下是此元素的 XPath 表达式：  <br/>  `/MoveItem` <br/> |
|[CopyItem](copyitem.md) <br/> |定义在 Exchange 存储中复制项的请求。  <br/> 以下是此元素的 XPath 表达式：  <br/>  `/CopyItem` <br/> |
   
## <a name="remarks"></a>备注

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [删除项操作](deleteitem-operation.md)
- [SendItem 操作](senditem-operation.md) 
- [GetItem 操作](getitem-operation.md)
- [MoveItem 操作](moveitem-operation.md)
- [CopyItem 操作](copyitem-operation.md)
- [FindConversation Operation](findconversation-operation.md)

