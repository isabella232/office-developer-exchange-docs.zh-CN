---
title: CopiedEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CopiedEvent
api_type:
- schema
ms.assetid: 82f2fcac-deaa-4ff8-801f-4fe28d8a19f5
description: CopiedEvent 元素表示复制的项或文件夹的事件。
ms.openlocfilehash: 89ca9fb1fd2f4187efdec0e087d840bfee197a29
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753600"
---
# <a name="copiedevent"></a>CopiedEvent

**CopiedEvent**元素表示复制的项或文件夹的事件。 
  
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

 **MovedCopiedEventType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[水印](watermark.md) <br/> |代表邮箱事件表格中的事件书签。  <br/> |
|[时间戳](timestamp.md) <br/> |代表副本项/文件夹邮箱事件的时间戳。  <br/> |
|[文件夹 Id](folderid.md) <br/> |表示的文件夹的标识符。  <br/> |
|[ItemId](itemid.md) <br/> |表示项目的标识符。  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |表示包含复制的文件夹的标识符。  <br/> |
|[OldFolderId](oldfolderid.md) <br/> |它已复制之前，则表示原始文件夹的文件夹标识符。  <br/> |
|[OldItemId](olditemid.md) <br/> |它已复制之前，请包含原始项目的唯一标识符。  <br/> |
|[OldParentFolderId](oldparentfolderid.md) <br/> |包含项或已复制的文件夹的原始父文件夹的标识符。  <br/> |
   
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


[使用请求订阅](http://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx)
  
[推送通知示例应用程序](http://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx)

