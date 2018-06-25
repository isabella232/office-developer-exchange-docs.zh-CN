---
title: MovedEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MovedEvent
api_type:
- schema
ms.assetid: 572f8b40-dfa8-47bc-b0c1-e1a7138506fd
description: MovedEvent 元素表示在其中项目或文件夹从一个父文件夹移到另一个父文件夹的事件。
ms.openlocfilehash: a375f421ca9159103e47b515729316b21149c68a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826479"
---
# <a name="movedevent"></a>MovedEvent

**MovedEvent**元素表示在其中项目或文件夹从一个父文件夹移到另一个父文件夹的事件。 
  
```xml
<MovedEvent>
   <Watermark/>
   <TimeStamp/>
   <ItemId/>
   <ParentFolderId/>
   <OldItemId/>
   <OldParentFolderId/>
</MovedEvent>
```

 **MovedCopiedEventType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[水印](watermark.md) <br/> |代表邮箱事件表格中的事件书签。  <br/> |
|[时间戳](timestamp.md) <br/> |代表移动项目/文件夹邮箱事件的时间戳。  <br/> |
|[文件夹 Id](folderid.md) <br/> |代表移动文件夹的标识符。  <br/> |
|[ItemId](itemid.md) <br/> |代表移动项目的标识符。  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |表示包含移动的项目或文件夹的文件夹的标识符。  <br/> |
|[OldFolderId](oldfolderid.md) <br/> |它已移动或复制之前，请包含原始文件夹的文件夹标识符。  <br/> |
|[OldItemId](olditemid.md) <br/> |包含原始项目的唯一标识符，它移动之前。  <br/> |
|[OldParentFolderId](oldparentfolderid.md) <br/> |包含项或已移动的文件夹的原始父文件夹的标识符。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[通知](notification-ex15websvcsotherref.md) <br/> |包含有关订阅和自上次通知以来发生的事件的信息。  <br/> |
   
## <a name="remarks"></a>备注

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

