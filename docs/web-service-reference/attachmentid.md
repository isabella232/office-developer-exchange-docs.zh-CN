---
title: AttachmentId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- AttachmentId
api_type:
- schema
ms.assetid: 55a5fd77-60d1-40fa-8144-770600cedc6a
description: AttachmentId 元素标识项目或文件附件。 此元素在 CreateAttachment 响应中使用。
ms.openlocfilehash: a6363fad4e7ef9f0c21377f2c1ea8c19c494cdef
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522017"
---
# <a name="attachmentid"></a>AttachmentId

**AttachmentId** 元素标识项目或文件附件。 此元素在 CreateAttachment 响应中使用。 
  
```xml
<AttachmentId Id="" RootItemId="" RootItemChangeKey="" />
```

 **AttachmentIdType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**Id** <br/> |标识附件的唯一标识符。  <br/> |
|**RootItemId** <br/> |标识附件附加到的根存储项的唯一标识符。  <br/> |
|**RootItemChangeKey** <br/> |标识附件附加到的根存储项更改密钥。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ItemAttachment](itemattachment.md) <br/> |代表Exchange附加到其他项目的项目Exchange项。  <br/> |
|[FileAttachment](fileattachment.md) <br/> |表示附加到项目存储中的Exchange文件。  <br/> |
   
## <a name="remarks"></a>注解

请注意，创建附件时，将更改根项目的更改键。
  
AttachmentId [ (GetAttachment 和 DeleteAttachment) ](attachmentid-getattachment-and-deleteattachment.md) 元素用于 DeleteAttachment 和 GetAttachment 请求中。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

