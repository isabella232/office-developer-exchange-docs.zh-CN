---
title: AppointmentState
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- AppointmentState
api_type:
- schema
ms.assetid: ab3f5d04-ace1-4a15-9107-cefa6c41abc7
description: AppointmentState 元素指定约会的状态。
ms.openlocfilehash: f984bbd5a1319a6051a3394ed04d56deabbb2c5a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544280"
---
# <a name="appointmentstate"></a>AppointmentState

**AppointmentState** 元素指定约会的状态。 
  
```XML
<AppointmentState/>
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
|[CalendarItem](calendaritem.md) <br/> |表示 Exchange 日历项。  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |表示 Exchange 存储中的会议。  <br/> |
   
## <a name="text-value"></a>文本值

此元素包含表示设置位的文本值。 这是整数形式。 此元素是只读的。 它只会在响应中返回。
  
## <a name="remarks"></a>注解

返回的整数值表示约会状态位掩码。 下表介绍了每一位。
  
|**名称**|**Bit**|**说明**|
|:-----|:-----|:-----|
|无  <br/> |0x0000  <br/> |尚未设置任何标志。 这仅用于不包括与会者的约会。  <br/> |
|会议  <br/> |0x0001  <br/> |此约会是会议。  <br/> |
|接收时间  <br/> |0x0002  <br/> |已接收此约会。  <br/> |
|已取消  <br/> |0x0004  <br/> |此约会已取消。  <br/> |
   
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

