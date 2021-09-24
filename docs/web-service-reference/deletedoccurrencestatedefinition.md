---
title: DeletedOccurrenceStateDefinition
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: a9c01c64-e76c-4adc-8b04-88af97bd0cc8
description: DeletedOccurrenceStateDefinition 指定日历项目的已删除事件的状态。
ms.openlocfilehash: 296eb1c99d5cc32cf8d1711bdb605ae10230ab34
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510279"
---
# <a name="deletedoccurrencestatedefinition"></a>DeletedOccurrenceStateDefinition

**DeletedOccurrenceStateDefinition** 指定日历项目的已删除事件的状态。 
  
```XML
<DeletedOccurrenceStateDefinition>
    <OccurrenceDate></OccurrenceDate>
    <IsOccurrencePresent></IsOccurrencePresent>
</DeletedOccurrenceStateDefinition>
```

 **DeletedOccurrenceStateDefinitionType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Occurrence (Time Zone Transition)](occurrence-time-zone-transition.md) <br/> |指定日历项目的发生日期。  <br/> |
|[IsOccurrencePresent](isoccurrencepresent.md) <br/> |指定一个布尔值，该值指示是否出现日历项目。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[StateDefinition](statedefinition.md) <br/> |指定状态定义。  <br/> |
   
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |types.xsd  <br/> |
|可以为空  <br/> ||
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

