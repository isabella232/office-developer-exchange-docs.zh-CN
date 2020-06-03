---
title: StartDateTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StartDateTime
api_type:
- schema
ms.assetid: 6fd41b7b-6c83-43b6-8b16-0bdb3d173d73
description: StartDateTime 元素指定规则或搜索的开始日期和时间。
ms.openlocfilehash: 28b78fad87abb1148cfe49fee4f9bb98f822eae5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462841"
---
# <a name="startdatetime"></a>StartDateTime

**StartDateTime**元素指定规则或搜索的开始日期和时间。 
  
```XML
<StartDate/>
```

**dateTime**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FindMessageTrackingReport](findmessagetrackingreport.md) <br/> |指定要查找的邮件类型的条件。  <br/> |
|[WithinDateRange](withindaterange.md) <br/> |指定要在其中接收传入邮件的日期范围，以便条件或例外情况适用。  <br/> |
   
## <a name="text-value"></a>文本值

 如果使用此元素，则表示日期/时间的文本值是必需的。 
  
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

