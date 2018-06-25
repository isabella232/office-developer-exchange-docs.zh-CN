---
title: AttachmentId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AttachmentId
api_type:
- schema
ms.assetid: 55a5fd77-60d1-40fa-8144-770600cedc6a
description: AttachmentId 元素标识项目或文件附件。 在 CreateAttachment 响应中使用此元素。
ms.openlocfilehash: 2910503d1661ca3aaeeb4e319deb39f6b57c5c0a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753277"
---
# <a name="attachmentid"></a>AttachmentId

**AttachmentId**元素标识项目或文件附件。 在 CreateAttachment 响应中使用此元素。 
  
```xml
<AttachmentId Id="" RootItemId="" RootItemChangeKey="" />
```

 **AttachmentIdType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|
  **Id** <br/> |标识附件的唯一标识符。  <br/> |
|**RootItemId** <br/> |标识附件附加到根存储项的唯一标识符。  <br/> |
|**RootItemChangeKey** <br/> |标识附件附加到根存储项的更改键。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ItemAttachment](itemattachment.md) <br/> |代表附加到另一个 Exchange 项目的 Exchange 项目。  <br/> |
|[FileAttachment](fileattachment.md) <br/> |代表附加到 Exchange 存储中的项的文件。  <br/> |
   
## <a name="remarks"></a>注解

请务必注意创建附件时，已更改的根项目的更改键。
  
DeleteAttachment 和 GetAttachment 请求中使用[AttachmentId （GetAttachment 和 DeleteAttachment）](attachmentid-getattachment-and-deleteattachment.md)元素。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

