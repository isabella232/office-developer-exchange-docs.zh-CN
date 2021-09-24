---
title: DeleteFromFolderStateDefinition
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 3aba59a0-f12a-48b5-842b-11cf4530dd51
description: DeleteFromFolderStateDefinition 元素指定从文件夹中删除项目时的状态。
ms.openlocfilehash: 270edfc0b7abd70b74ff8c8b4353140ec5fbe27b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510237"
---
# <a name="deletefromfolderstatedefinition"></a>DeleteFromFolderStateDefinition

**DeleteFromFolderStateDefinition** 元素指定从文件夹中删除项目时的状态。 
  
```XML
<DeleteFromFolderStateDefinition>
    <OccurrenceDate></OccurrenceDate>
    <IsOccurrencePresent></IsOccurrencePresent>
</DeleteFromFolderStateDefinition>
```

 **DeleteFromFolderStateDefinitionType**
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

