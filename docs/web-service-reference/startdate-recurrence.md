---
title: StartDate （重复）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StartDate
api_type:
- schema
ms.assetid: bd65ac06-b3ac-4c9b-9568-3e4dc94378e7
description: StartDate 元素均表示一个周期性任务或日历项的开始日期。
ms.openlocfilehash: 6a38e63bbcf010ab6dca8f66440a2b0a559cf88d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827551"
---
# <a name="startdate-recurrence"></a>StartDate （重复）

**StartDate**元素均表示一个周期性任务或日历项的开始日期。 
  
```xml
<StartDate/>
```

**日期**

## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[EndDateRecurrence](enddaterecurrence.md) <br/> |介绍的开始日期和结束日期的项目定期模式。  <br/> |
|[NoEndRecurrence](noendrecurrence.md) <br/> |介绍没有定义的结束日期项目定期模式的开始日期。  <br/> |
|[NumberedRecurrence](numberedrecurrence.md) <br/> |介绍的开始日期和定期项目的次数。  <br/> |
   
## <a name="text-value"></a>文本值

如果使用此元素，则需要表示日期的文本值。 值不能小于 Apr，1，该值表示自 1601年 00:00:00。
  
## <a name="remarks"></a>备注

描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

