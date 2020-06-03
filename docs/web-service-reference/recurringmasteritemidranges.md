---
title: RecurringMasterItemIdRanges
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5c9c89b5-4ce8-437b-a332-fa7ed35c8388
description: RecurringMasterItemIdRanges 元素指定发生的范围的数组。
ms.openlocfilehash: 784676844c5c58c65b8cc6177843bf26d351b7d9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528753"
---
# <a name="recurringmasteritemidranges"></a>RecurringMasterItemIdRanges

**RecurringMasterItemIdRanges**元素指定发生的范围的数组。 
  
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
|**Id** <br/> |**Id**属性的文本值是定期主项目的唯一标识符。 这是一个**字符串**值。  <br/> |
|**ChangeKey** <br/> |**ChangeKey**属性的文本值是定期主项目的更改密钥。 这是一个**字符串**值。  <br/> |
   
### <a name="child-elements"></a>子元素

[Ranges](ranges.md)
  
### <a name="parent-elements"></a>父元素

[ItemIds](itemids.md)  | [GlobalItemIds](globalitemids.md)  | [DraftItemIds](draftitemids.md)  | [ContactIds](contactids.md)  | [Groupid](groupids.md)
  
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> ||
   

