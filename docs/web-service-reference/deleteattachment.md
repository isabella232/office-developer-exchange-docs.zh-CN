---
title: DeleteAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DeleteAttachment
api_type:
- schema
ms.assetid: 43d0c1cb-92ca-4399-9b3a-acb2b5c22624
description: DeleteAttachment 元素是请求从邮件存储中删除附件的根Exchange元素。
ms.openlocfilehash: 803bd748020dd459e7629825fb572d990adadf71
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59545459"
---
# <a name="deleteattachment"></a>DeleteAttachment

**DeleteAttachment** 元素是请求从邮件存储中删除附件的根Exchange元素。 
  
```xml
<DeleteAttachment>
   <AttachmentIds/>
</DeleteAttachment>
```

**DeleteAttachmentType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[AttachmentIds](attachmentids.md) <br/> |包含用于删除附件的附件标识符数组。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>注解

描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [DeleteAttachment 操作](deleteattachment-operation.md)

