---
title: DayOfWeekIndex
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DayOfWeekIndex
api_type:
- schema
ms.assetid: 82420338-a1f7-4887-b338-b2d93b2c2bf1
description: DayOfWeekIndex 元素描述相对定期模式中使用某个月中的哪一周。
ms.openlocfilehash: c9235d83a944f9c8883439dd2adf190b88977f16
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529208"
---
# <a name="dayofweekindex"></a>DayOfWeekIndex

**DayOfWeekIndex**元素描述相对定期模式中使用某个月中的哪一周。 
  
```xml
<DayOfWeekIndex/>
```

**DayOfWeekIndexType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[RelativeYearlyRecurrence](relativeyearlyrecurrence.md) <br/> |介绍相对年定期模式。  <br/> |
|[RelativeMonthlyRecurrence](relativemonthlyrecurrence.md) <br/> |介绍相对月定期模式。  <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。 以下是可能的值：
  
- First    
- 秒    
- 第三节    
- 四分之一    
- 最后一个
    
## <a name="remarks"></a>备注

例如，一个月的第二个星期一可能发生在该月的第三个星期。 如果一个月从星期五开始，则该月的第一周仅包含几天，并且不包含星期一。 因此，第一个星期一必须在第二周发生。
  
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

