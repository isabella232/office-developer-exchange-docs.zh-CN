---
title: SyncState
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SyncState
api_type:
- schema
ms.assetid: e5ebaae3-0f07-481d-ac67-d9687a3c7ac3
description: SyncState 元素包含每次成功请求后更新的 base64 编码的同步数据形式。 这用于标识同步状态。
ms.openlocfilehash: 72a0e347b5732cbe397956f8cc50b3266fba9156
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543903"
---
# <a name="syncstate"></a>SyncState

**SyncState** 元素包含每次成功请求后更新的 base64 编码的同步数据形式。 这用于标识同步状态。 
  
```xml
<SyncState/>
```

 **String**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[SyncFolderHierarchy](syncfolderhierarchy.md) <br/> |定义在客户端上同步文件夹层次结构的请求。  <br/> |
|[SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md) <br/> |包含 SyncFolderHierarchy 请求的状态和结果。  <br/> |
|[SyncFolderItems](syncfolderitems.md) <br/> |定义同步邮件存储文件夹中Exchange的请求。  <br/> |
|[SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md) <br/> |包含 SyncFolderItems 请求的状态和结果。  <br/> |
   
## <a name="text-value"></a>文本值

当使用此元素时，需要文本值。
  
## <a name="remarks"></a>说明

描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[SyncFolderItems 操作](syncfolderitems-operation.md)
  
[SyncFolderHierarchy 操作](syncfolderhierarchy-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

