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
description: OccurrenceItemId 元素标识定期项目的一个匹配项。
ms.openlocfilehash: 073639ecbca6ffda872e9253b7c7e44c3541f13b
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353460"
---
# <a name="occurrenceitemid"></a>OccurrenceItemId

**OccurrenceItemId**元素标识定期项目的一个匹配项。 
  
```XML
<OccurrenceItemId RecurringMasterId="" ChangeKey="" InstanceIndex=""/>
```

**OccurrenceItemIdType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**RecurringMasterId** <br/> |标识定期项目的定期母的版。 此属性是必需的。  <br/> |
|**更改密钥** <br/> |标识定期主控形状或项匹配项的特定版本。 如果定期主控形状或其出现的任何更改，**更改密钥**更改。 **更改密钥**是相同的定期主控形状和所有匹配项。  <br/> |
|**InstanceIndex** <br/> |标识项目匹配项的索引。 此属性是必需的。 此值表示的整数。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GlobalItemIds](globalitemids.md) <br/> |包含的项标识符的邮箱中的所有对话项的集合。  <br/> |
|[ItemIds](itemids.md) <br/> | 包含唯一标识的项目和匹配项，用于删除、 发送、 获取、 移动或在 Exchange 存储中复制项的定期主项目。 <br/><br/>下面是此元素的 XPath 表达式： <br/><br/>  `/DeleteItem/ItemIds` <br/>  `/SendItem/ItemIds` <br/>  `/GetItem/ItemIds` <br/><br/>**注意**： [MoveItem 操作](moveitem-operation.md)和[CopyItem 操作](copyitem-operation.md)仅使用单个日历项和定期主项目。 项目出现，则使用这些操作无效。           |
|[ItemChange](itemchange.md) <br/> |包含项标识符和更新应用到的项。<br/><br/> 下面是此元素的 XPath 表达式:    <br/>  `/UpdateItem/ItemChanges/ItemChange[i]` <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="example"></a>示例

以下示例标识具有标识 34vswe4 定期项目的第四个匹配项。
  
```XML
<OccurrenceItemId RecurringMasterId="34vswe4" InstanceIndex="4" />
```

## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [RecurringMasterItemId](recurringmasteritemid.md)
- [FindConversation 操作](findconversation-operation.md)
- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

