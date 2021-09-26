---
title: FreeBusyChangedEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FreeBusyChangedEvent
api_type:
- schema
ms.assetid: 63abbfc5-c29f-4110-a922-6b1247187f28
description: FreeBusyChangedEvent 元素表示一个事件，其中项目的忙/闲时间已更改。
ms.openlocfilehash: 503f6f2e7c30e2103fda08b3a8011eb09eb78436
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59545025"
---
# <a name="freebusychangedevent"></a>FreeBusyChangedEvent

**FreeBusyChangedEvent** 元素表示一个事件，其中项目的忙/闲时间已更改。 
  
```xml
<CreatedEvent>
   <Watermark/>
   <TimeStamp/>
   <ItemId/>
   <ParentFolderId/>
</CreatedEvent>
```

 **BaseObjectChangedEventType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Watermark](watermark.md) <br/> |表示邮箱事件表中的事件书签。  <br/> |
|[TimeStamp](timestamp.md) <br/> |表示忙/闲项目邮箱事件的时间戳。  <br/> |
|[ItemId](itemid.md) <br/> |表示忙/闲项目的标识符。  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |表示忙/闲项目的父文件夹的标识符。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[通知](notification-ex15websvcsotherref.md) <br/> |包含有关订阅和自上次通知以来已发生事件的信息。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>注解

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[订阅操作](subscribe-operation.md)
  
[GetEvents 操作](getevents-operation.md)
  
[Unsubscribe 操作](unsubscribe-operation.md)


[使用拉取订阅](https://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx)
  
[EWS 中的事件通知](https://msdn.microsoft.com/library/4fd4b351-d35c-4ccc-9ed9-878932ab9d50%28Office.15%29.aspx)

