---
title: ModifiedEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ModifiedEvent
api_type:
- schema
ms.assetid: ca1309f4-2df7-4289-811c-75c3db0e7072
description: ModifiedEvent 元素均表示修改项目或文件夹的事件。
ms.openlocfilehash: fb464fb0a270d8ca7d33d40e5425e260970b2f1e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826482"
---
# <a name="modifiedevent"></a>ModifiedEvent

**ModifiedEvent**元素均表示修改项目或文件夹的事件。 
  
```xml
<ModifiedEvent>
   <Watermark/>
   <TimeStamp/>
   <FolderId/>
   <ParentFolderId/>
   <UnreadCount/>
</ModifiedEvent>
```

 **ModifiedEventType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[水印](watermark.md) <br/> |代表邮箱事件表格中的事件书签。  <br/> |
|[时间戳](timestamp.md) <br/> |代表一个已修改的项或文件夹邮箱事件的时间戳。  <br/> |
|[文件夹 Id](folderid.md) <br/> |表示修改文件夹的标识符。  <br/> |
|[ItemId](itemid.md) <br/> |代表已修改的项目的标识符。  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |表示已修改的项或文件夹的父文件夹的标识符。  <br/> |
|[UnreadCount](unreadcount.md) <br/> |表示给定文件夹中未读项目的计数。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[通知](notification-ex15websvcsotherref.md) <br/> |包含有关订阅和自上次通知以来发生的事件的信息。  <br/> |
   
## <a name="remarks"></a>备注

为文件夹中的项目的每次修改生成两个已修改的事件。 一个事件是与更改的项相关的。 与项目的父文件夹相关其他事件。 这是针对创建订阅的同一个文件夹。 与文件夹关联的事件用于通信的潜在更改到的文件夹的[UnreadCount](unreadcount.md)属性。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[订阅操作](subscribe-operation.md)
  
[GetEvents 操作](getevents-operation.md)
  
[取消操作](unsubscribe-operation.md)

