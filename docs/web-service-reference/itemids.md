---
title: ItemIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ItemIds
api_type:
- schema
ms.assetid: 6b82122b-5544-4adf-91b7-ef2db7d5046f
description: ItemIds 元素包含项目、发生项和用于删除、发送、获取、移动或复制项目（用于删除、发送、获取、移动或复制项目）Exchange标识。
ms.openlocfilehash: 7341b8214b4d61564bd87707a9d8c76fbca07628
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522885"
---
# <a name="itemids"></a>ItemIds
  
**ItemIds** 元素包含项目、发生项和用于删除、发送、获取、移动或复制项目（用于删除、发送、获取、移动或复制项目）Exchange标识。
  
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
|[ItemId](itemid.md) <br/> |包含项目存储中项的唯一标识符Exchange项。  <br/> |
|[OccurrenceItemId](occurrenceitemid.md) <br/> |标识定期项目的单个匹配项。  <br/> |
|[RecurringMasterItemId](recurringmasteritemid.md) <br/> |通过标识其相关事件项的标识符之一来标识定期主项。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[对话 (ConversationType)](conversation-conversationtype.md) <br/> |表示单个对话。  <br/> |
|[DeleteItem](deleteitem.md) <br/> |定义一个删除邮件存储中Exchange的请求。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/DeleteItem` <br/> |
|[SendItem](senditem.md) <br/> |定义发送项目请求的根元素Exchange存储区。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/SendItem` <br/> |
|[GetItem](getitem.md) <br/> |定义从应用商店获取Exchange请求。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/GetItem` <br/> |
|[MoveItem](moveitem.md) <br/> |定义一个请求，以移动项目Exchange存储区。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/MoveItem` <br/> |
|[CopyItem](copyitem.md) <br/> |定义一个请求，以复制Exchange项。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/CopyItem` <br/> |
   
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

