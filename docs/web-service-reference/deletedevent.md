---
title: DeletedEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeletedEvent
api_type:
- schema
ms.assetid: c4565eb4-b537-466c-b1ff-11602533812b
description: DeletedEvent 元素表示在其中删除项目或文件夹的事件。
ms.openlocfilehash: 5eb0c947aacc592f81c595da2cc00bf4874f300b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526940"
---
# <a name="deletedevent"></a>DeletedEvent

**DeletedEvent**元素表示在其中删除项目或文件夹的事件。 
  
```xml
<DeletedEvent>
   <Watermark/>
   <TimeStamp/>
   <ItemId/>
   <ParentFolderId/>
</DeletedEvent>
```

```xml
<DeletedEvent>
   <Watermark/>
   <TimeStamp/>
   <FolderId/>
   <ParentFolderId/>
</DeletedEvent>
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
|[TimeStamp](timestamp.md) <br/> |表示已删除项目或文件夹邮箱事件的时间戳。  <br/> |
|[FolderId](folderid.md) <br/> |表示已删除文件夹的标识符。  <br/> |
|[ItemId](itemid.md) <br/> |表示已删除项的标识符。  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |表示删除项目或文件夹在删除之前的父文件夹的标识符。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[通知](notification-ex15websvcsotherref.md) <br/> |包含有关订阅以及上次通知之后发生的事件的信息。  <br/> |
   
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

- [订阅操作](subscribe-operation.md)  
- [GetEvents 操作](getevents-operation.md)  
- [取消订阅操作](unsubscribe-operation.md)

