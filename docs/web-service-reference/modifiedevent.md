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
description: ModifiedEvent 元素表示在其中修改项或文件夹的事件。
ms.openlocfilehash: 1a798773601a0857b9064c7fa6a532a7a36517ab
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468549"
---
# <a name="modifiedevent"></a>ModifiedEvent

**ModifiedEvent**元素表示在其中修改项或文件夹的事件。 
  
```xml
<ModifiedEvent>
   <Watermark/>
   <TimeStamp/>
   <FolderId/>
   <ParentFolderId/>
   <UnreadCount/>
</ModifiedEvent>
```

```xml
<ModifiedEvent>
   <Watermark/>
   <TimeStamp/>
   <ItemId/> 
   <ParentFolderId/>
   <UnreadCount/>
</ModifiedEvent>
```

**ModifiedEventType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Watermark](watermark.md) <br/> |表示邮箱事件表中的事件书签。  <br/> |
|[TimeStamp](timestamp.md) <br/> |表示已修改的项目或文件夹邮箱事件的时间戳。  <br/> |
|[FolderId](folderid.md) <br/> |表示已修改文件夹的标识符。  <br/> |
|[ItemId](itemid.md) <br/> |表示已修改的项的标识符。  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |表示已修改的项或文件夹的父文件夹的标识符。  <br/> |
|[UnreadCount](unreadcount.md) <br/> |表示给定文件夹中未读项目的计数。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[通知](notification-ex15websvcsotherref.md) <br/> |包含有关订阅以及上次通知之后发生的事件的信息。  <br/> |
   
## <a name="remarks"></a>备注

为文件夹中的项目的每个修改生成两个修改的事件。 一个事件与已更改的项目相关。 另一个事件与项目的父文件夹相关。 此文件夹与创建订阅所用的文件夹相同。 与该文件夹相关联的事件用于将潜在更改传递给文件夹的[UnreadCount](unreadcount.md)属性。 
  
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

