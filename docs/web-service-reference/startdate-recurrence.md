---
title: 起始日期（定期）
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
description: 起始日期元素表示定期任务或日历项目的开始日期。
ms.openlocfilehash: 4514f126b1de31c64a2650b9e7cb6b7412a726c7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457205"
---
# <a name="startdate-recurrence"></a>起始日期（定期）

**起始**日期元素表示定期任务或日历项目的开始日期。 
  
```xml
<StartDate/>
```

**Date**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[EndDateRecurrence](enddaterecurrence.md) <br/> |描述项目定期模式的开始日期和结束日期。  <br/> |
|[NoEndRecurrence](noendrecurrence.md) <br/> |描述不具有定义的结束日期的项目定期模式的开始日期。  <br/> |
|[NumberedRecurrence](numberedrecurrence.md) <br/> |描述定期项目的开始日期和发生次数。  <br/> |
   
## <a name="text-value"></a>文本值

如果使用此元素，则表示日期的文本值是必需的。 值不能小于 Apr、1、1601 00:00:00。
  
## <a name="remarks"></a>说明

描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

