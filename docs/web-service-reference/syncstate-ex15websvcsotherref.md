---
title: SyncState
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncState
api_type:
- schema
ms.assetid: e5ebaae3-0f07-481d-ac67-d9687a3c7ac3
description: SyncState 元素包含 base64 编码的同步数据的每个请求成功后都会更新窗体。 这用于标识的同步状态。
ms.openlocfilehash: 3c600dde09fd813dcfb1f6e74671ebe9004701a1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838179"
---
# <a name="syncstate"></a>SyncState

**SyncState**元素包含 base64 编码的同步数据的每个请求成功后都会更新窗体。 这用于标识的同步状态。 
  
```xml
<SyncState/>
```

 **字符串**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[SyncFolderHierarchy](syncfolderhierarchy.md) <br/> |定义同步客户端上的文件夹层次结构的请求。  <br/> |
|[SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md) <br/> |包含状态和 SyncFolderHierarchy 请求的结果。  <br/> |
|[SyncFolderItems](syncfolderitems.md) <br/> |定义同步 Exchange 存储区文件夹中的项目的请求。  <br/> |
|[SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md) <br/> |包含状态和 SyncFolderItems 请求的结果。  <br/> |
   
## <a name="text-value"></a>文本值

使用此元素时所需的文本值。
  
## <a name="remarks"></a>备注

描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[SyncFolderItems 操作](syncfolderitems-operation.md)
  
[SyncFolderHierarchy 操作](syncfolderhierarchy-operation.md)


- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

