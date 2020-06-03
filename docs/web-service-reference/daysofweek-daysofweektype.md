---
title: DaysOfWeek （DaysOfWeekType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DaysOfWeek
api_type:
- schema
ms.assetid: c56f997d-28f3-4590-97b0-cb71f016dbe4
description: DaysOfWeek 元素描述在项目定期模式中使用的一周中的日期。
ms.openlocfilehash: 3036cbe3f93ff87b9a4d5dc7bf164e3e952b06fd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463718"
---
# <a name="daysofweek-daysofweektype"></a>DaysOfWeek （DaysOfWeekType）

**DaysOfWeek**元素描述在项目定期模式中使用的一周中的日期。 
  
```XML
<DaysOfWeek/>
```

**DaysOfWeekType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[WeeklyRecurrence](weeklyrecurrence.md) <br/> |介绍每周定期模式。  <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。 以下是可能的值：
  
- 星期日    
- 星期一    
- 星期二    
- 星期三    
- 星期四    
- 星期五    
- 星期六    
- Day （此值对于每周定期模式无效）    
- 工作日（此值对于每周定期模式无效）    
- WeekendDay （此值对于每周定期模式无效）
    
每周定期模式可包含多个值。 值之间用空格字符分隔。 例如，对于星期二和星期四的每周重复，文本值将为 "星期二星期四"。
  
## <a name="remarks"></a>备注

描述此元素的架构位于运行 Microsoft Exchange Server 2010 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

