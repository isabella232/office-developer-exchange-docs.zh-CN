---
title: RootItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RootItemId
api_type:
- schema
ms.assetid: f613c705-17ce-48ce-aa64-4dc2cea25e31
description: RootItemId 元素标识已删除附件的根项目。
ms.openlocfilehash: eab3cc30c2e3f2b6cdc443ba8eb7ae4bfa38d257
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59509364"
---
# <a name="rootitemid"></a>RootItemId

**RootItemId** 元素标识已删除附件的根项目。 
  
[DeleteAttachmentResponse](deleteattachmentresponse.md)
  
[ResponseMessages](responsemessages.md)
  
[DeleteAttachmentResponseMessage](deleteattachmentresponsemessage.md)
  
[RootItemId](rootitemid.md)
  
```xml
<RootItemId RootItemId="" RootItemChangeKey="" />
```

 **RootItemIdType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**RootItemId** <br/> |标识已删除附件的根项目。  <br/> |
|**RootItemChangeKey** <br/> |标识已删除附件的根项目的新更改密钥。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[DeleteAttachmentResponseMessage](deleteattachmentresponsemessage.md) <br/> |包含 DeleteAttachment 请求的状态和结果。  <br/> |
   
## <a name="remarks"></a>注解

**RootItemId** 元素仅在 DeleteAttachment 响应中使用。 这将标识根项标识符，更重要的是，标识父项的新更改键。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[DeleteAttachment](deleteattachment.md)
  
[DeleteAttachment 操作](deleteattachment-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

