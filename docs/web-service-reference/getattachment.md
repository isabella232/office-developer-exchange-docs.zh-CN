---
title: GetAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GetAttachment
api_type:
- schema
ms.assetid: 9443cf96-b451-4530-b868-490dff798673
description: GetAttachment 元素是请求从邮件存储获取附件的根Exchange元素。
ms.openlocfilehash: 057b42e78845f583cf1e52804e0108f335ef951c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546369"
---
# <a name="getattachment"></a>GetAttachment

**GetAttachment** 元素是请求从邮件存储获取附件的Exchange元素。 
  
```xml
<GetAttachment>
   <AttachmentShape/>
   <AttachmentIds/>
</GetAttachment>
```

 **GetAttachmentType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[AttachmentShape](attachmentshape.md) <br/> |标识在响应 [GetAttachment](getattachment.md) 请求时要返回的其他扩展项属性。 此元素为可选。  <br/> |
|[AttachmentIds](attachmentids.md) <br/> |包含附件标识符数组。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>注解

[AttachmentShape](attachmentshape.md)元素不需要标识响应中返回的属性。 [GetAttachment 操作](getattachment-operation.md)返回文件附件的 Name、ContentType、ContentId、ContentLocation 和 Content 属性。 对于项目附件，返回的属性为 Name、ContentType、ContentId、ContentLocation 以及所有附加项目的属性。 这等效于在 [GetItem](getitem.md) 请求中使用 AllProperties 基形状。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetAttachment 操作](getattachment-operation.md)
  
[GetAttachmentResponse](getattachmentresponse.md)

