---
title: AppointmentState
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AppointmentState
api_type:
- schema
ms.assetid: ab3f5d04-ace1-4a15-9107-cefa6c41abc7
description: AppointmentState 元素指定约会的状态。
ms.openlocfilehash: 05e92a3fea10a84518b0680c425011a91bc43d93
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753248"
---
# <a name="appointmentstate"></a>AppointmentState

**AppointmentState**元素指定约会的状态。 
  
```XML
<AppointmentState/>
```

 **int**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[日历项目](calendaritem.md) <br/> |表示 Exchange 日历项。  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |表示 Exchange 存储中的会议。  <br/> |
   
## <a name="text-value"></a>文本值

此元素包含代表设置位的文本值。 这是整数窗体中。 此元素是只读的。 仅将在响应中返回它。
  
## <a name="remarks"></a>备注

返回的整数值表示的约会状态位掩码。 下表介绍了每一位。
  
|**名称**|**位**|**说明**|
|:-----|:-----|:-----|
|无  <br/> |0x0000  <br/> |已不设置任何标志。 不包括与会者的约会才使用此选项。  <br/> |
|会议  <br/> |0x0001  <br/> |该约会是会议。  <br/> |
|接收时间  <br/> |0x0002  <br/> |已收到此约会。  <br/> |
|已取消  <br/> |0x0004  <br/> |该约会已被取消。  <br/> |
   
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

