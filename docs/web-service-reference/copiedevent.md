---
title: CopiedEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CopiedEvent
api_type:
- schema
ms.assetid: 82f2fcac-deaa-4ff8-801f-4fe28d8a19f5
description: CopiedEvent 元素表示其中复制项目或文件夹的事件。
ms.openlocfilehash: bc4902eb1e62344a7d5980ec573ac13b1bb084ee
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59536591"
---
# <a name="copiedevent"></a>CopiedEvent

**CopiedEvent** 元素表示其中复制项目或文件夹的事件。 
  
```xml
<CopiedEvent>
   <Watermark/>
   <TimeStamp/>
   <FolderId/>
   <ParentFolderId/>
   <OldFolderId/>
   <OldParentFolderId/>
</CopiedEvent>
```

```xml
<CopiedEvent>
   <Watermark/>
   <TimeStamp/>
   <ItemId/>
   <ParentFolderId/>
   <OldItemId/>
   <OldParentFolderId/>
</CopiedEvent>
```

**MovedCopiedEventType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Watermark](watermark.md) <br/> |表示邮箱事件表中的事件书签。  <br/> |
|[TimeStamp](timestamp.md) <br/> |表示复制项目/文件夹邮箱事件的时间戳。  <br/> |
|[FolderId](folderid.md) <br/> |表示文件夹的标识符。  <br/> |
|[ItemId](itemid.md) <br/> |表示项的标识符。  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |表示包含副本的文件夹的标识符。  <br/> |
|[OldFolderId](oldfolderid.md) <br/> |表示原始文件夹在复制之前的文件夹标识符。  <br/> |
|[OldItemId](olditemid.md) <br/> |包含原始项在复制之前的唯一标识符。  <br/> |
|[OldParentFolderId](oldparentfolderid.md) <br/> |包含复制的项目或文件夹的原始父文件夹的标识符。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[通知](notification-ex15websvcsotherref.md) <br/> |包含有关订阅和自上次通知以来已发生事件的信息。  <br/> |
   
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
- [Unsubscribe 操作](unsubscribe-operation.md)
- [使用拉取订阅](https://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx) 
- [推送通知示例应用程序](https://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx)

