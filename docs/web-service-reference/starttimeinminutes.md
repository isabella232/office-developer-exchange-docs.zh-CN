---
title: StartTimeInMinutes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StartTimeInMinutes
api_type:
- schema
ms.assetid: 0fb60a78-6e79-4601-8e2f-5bd245c46d69
description: StartTimeInMinutes 元素表示邮箱用户的工作日的开始日期。
ms.openlocfilehash: b33cb12299a146b577dd17939a0585a15d50fb07
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458528"
---
# <a name="starttimeinminutes"></a>StartTimeInMinutes

**StartTimeInMinutes**元素表示邮箱用户的工作日的开始日期。 
  
- [GetUserAvailabilityResponse](getuseravailabilityresponse.md)
  
- [FreeBusyResponseArray](freebusyresponsearray.md)
  
- [FreeBusyResponse](freebusyresponse.md)
  
- [FreeBusyView](freebusyview.md)
  
- [WorkingHours](workinghours-ex15websvcsotherref.md)
  
- [WorkingPeriodArray](workingperiodarray.md)
  
- [WorkingPeriod](workingperiod.md)
  
- [StartTimeInMinutes](starttimeinminutes.md)
  
```xml
<StartTimeInMinutes>...</StartTimeInMinutes>
```

**int**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[WorkingPeriod](workingperiod.md) <br/> |包含邮箱用户的工作周天数和小时数。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/WorkingPeriodArray/WorkingPeriod` <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。 该文本值表示自一天开始起经过的分钟数的开始日期。 例如，开始时间为上午8点。 由480分钟表示。
  
此元素的可能值的范围是0到1440。
  
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

- [GetUserAvailability 操作](getuseravailability-operation.md)
- [GetUserAvailabilityResponse](getuseravailabilityresponse.md)
- [Getting User Availability](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

