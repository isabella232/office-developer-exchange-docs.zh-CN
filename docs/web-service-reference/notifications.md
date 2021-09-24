---
title: 通知
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Notifications
api_type:
- schema
ms.assetid: 153cc420-d2fe-42f1-afb2-9a31ee09a750
description: Notifications 元素包含有关订阅和自上次通知以来已发生事件的信息数组。
ms.openlocfilehash: ab3c5bff205c450b71d772316b977040cded9ad5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59537523"
---
# <a name="notifications"></a>通知

**Notifications** 元素包含有关订阅和自上次通知以来已发生事件的信息数组。 
  
```xml
<Notifications>
   <Notification/>
</Notifications>
```

 **NonEmptyArrayOfNotificationsType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[通知](notification-ex15websvcsotherref.md) <br/> |包含有关订阅和自上次通知以来已发生事件的信息。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetStreamingEventsResponseMessage](getstreamingeventsresponsemessage.md) <br/> |包含单个 [GetStreamingEvents](getstreamingevents-operation.md) 操作请求的状态和结果。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>注解

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages 和 https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |邮件架构;类型架构  <br/> |
|验证文件  <br/> |Messages.xsd;Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetFolder 操作](getfolder-operation.md)
  
[DeleteFolder 操作](deletefolder-operation.md)
  
[MoveFolder 操作](movefolder-operation.md)
  
[CopyFolder 操作](copyfolder-operation.md)
  
[订阅操作](subscribe-operation.md)

