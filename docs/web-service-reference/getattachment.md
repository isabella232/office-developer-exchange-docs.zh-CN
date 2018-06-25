---
title: GetAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetAttachment
api_type:
- schema
ms.assetid: 9443cf96-b451-4530-b868-490dff798673
description: GetAttachment 元素是从 Exchange 存储中获取附件的请求中的根元素。
ms.openlocfilehash: fb639c86a0654e8f9e9601310f7c2f5b0fc7d729
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754466"
---
# <a name="getattachment"></a>GetAttachment

**GetAttachment**元素是从 Exchange 存储中获取附件的请求中的根元素。 
  
```xml
<GetAttachment>
   <AttachmentShape/>
   <AttachmentIds/>
</GetAttachment>
```

 **GetAttachmentType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[AttachmentShape](attachmentshape.md) <br/> |标识要[GetAttachment](getattachment.md)请求的响应中返回的其他扩展的项属性。 此元素是可选的。  <br/> |
|[AttachmentIds](attachmentids.md) <br/> |包含附件标识符的数组。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>注解

[AttachmentShape](attachmentshape.md)元素不需要确定在响应中返回的属性。 [GetAttachment 操作](getattachment-operation.md)返回的名称、 ContentType、 ContentId、 ContentLocation 和附件的文件的内容属性。 对于项目的附件，返回的属性的名称、 ContentType、 ContentId、 ContentLocation 和附加的项的所有属性。 这是等价于[GetItem](getitem.md)请求中使用 AllProperties 基本形状。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetAttachment 操作](getattachment-operation.md)
  
[GetAttachmentResponse](getattachmentresponse.md)

