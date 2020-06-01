---
title: ReturnQueueEvents
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReturnQueueEvents
api_type:
- schema
ms.assetid: 69d22417-320c-4c6f-9fb4-2020f2480bb2
description: ReturnQueueEvents 元素指示正在运行该任务的人员处于特权角色中。
ms.openlocfilehash: 9d07bc8c3d32f1cd532febaf4ae04e4a2d31d243
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466589"
---
# <a name="returnqueueevents"></a>ReturnQueueEvents

**ReturnQueueEvents**元素指示正在运行该任务的人员处于特权角色中。 
  
```XML
<ReturnQueueEvents>true | false</ReturnQueueEvents>
```

 **Boolean**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetMessageTrackingReport](getmessagetrackingreport.md) <br/> |包含[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)的请求，以检索指定 ID 的完整邮件跟踪报告。  <br/> |
   
## <a name="text-value"></a>文本值

表示一个布尔值的文本值是必需的。 **如果值为 true** ，则表示运行该任务的人员处于特权角色中;**如果值为 false** ，则表示运行该任务的人员不在特权角色中。 
  
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



[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

