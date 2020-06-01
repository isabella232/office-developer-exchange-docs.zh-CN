---
title: SyncFolderHierarchy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncFolderHierarchy
api_type:
- schema
ms.assetid: 55df4d01-e48e-4263-a851-78a66ad1093a
description: SyncFolderHierarchy 元素定义一个请求，以在客户端上同步文件夹层次结构。
ms.openlocfilehash: 68b607dbf603e955f74dfaccadd3ce6c4c9fb6ab
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466645"
---
# <a name="syncfolderhierarchy"></a>SyncFolderHierarchy

**SyncFolderHierarchy**元素定义一个请求，以在客户端上同步文件夹层次结构。 
  
```xml
<SyncFolderHierarchy>
   <FolderShape/>   <SyncFolderId/>
   <SyncState/>
</SyncFolderHierarchy>
```

 **SyncFolderHierarchyType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[FolderShape](foldershape.md) <br/> |标识要包含在[SyncFolderHierarchy](syncfolderhierarchy.md)响应中的文件夹属性。  <br/> |
|[SyncFolderId](syncfolderid.md) <br/> |表示包含要同步的项目的文件夹。 此元素为可选。  <br/> |
|[SyncState](syncstate-ex15websvcsotherref.md) <br/> |包含在每次成功请求后更新的、base64 编码的格式的同步数据。 这用于标识同步状态。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
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



[SyncFolderHierarchy 操作](syncfolderhierarchy-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

