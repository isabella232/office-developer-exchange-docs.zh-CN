---
title: RecurringMasterItemIdRanges
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 5c9c89b5-4ce8-437b-a332-fa7ed35c8388
description: RecurringMasterItemIdRanges 元素指定事件范围的数组。
ms.openlocfilehash: 582cbe27d468c1ff7ec22f03ba9f6976d244e234
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59529368"
---
# <a name="recurringmasteritemidranges"></a>RecurringMasterItemIdRanges

**RecurringMasterItemIdRanges** 元素指定事件范围的数组。 
  
```XML
<RecurringMasterItemIdRanges Id="" ChangeKey="">
   <Ranges/>
</RecurringMasterItemIdRanges>
```

 **RecurringMasterItemIdRangesType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**Id** <br/> |**Id** 属性的文本值是定期主项目的唯一标识符。 这是一 **个字符串** 值。  <br/> |
|**ChangeKey** <br/> |**ChangeKey** 属性的文本值是定期主项目的更改键。 这是一 **个字符串** 值。  <br/> |
   
### <a name="child-elements"></a>子元素

[Ranges](ranges.md)
  
### <a name="parent-elements"></a>父元素

[ItemIds](itemids.md)  | [GlobalItemIds](globalitemids.md)  | [DraftItemIds](draftitemids.md)  | [ContactIds](contactids.md)  | [GroupIds](groupids.md)
  
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> ||
   

