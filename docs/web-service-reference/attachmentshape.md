---
title: AttachmentShape
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AttachmentShape
api_type:
- schema
ms.assetid: 734914b5-3a16-4744-90a5-741fd30c4676
description: AttachmentShape 元素标识要 GetAttachment 请求的响应中返回的其他属性。
ms.openlocfilehash: dc6769faa5fd28ce31b796f86c507aec54abff7a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753281"
---
# <a name="attachmentshape"></a>AttachmentShape

**AttachmentShape**元素标识要[GetAttachment](getattachment.md)请求的响应中返回的其他属性。 
  
- [GetAttachment](getattachment.md)
  
- [AttachmentShape](attachmentshape.md)
  
```xml
<AttachmentShape>
   <IncludeMimeContent/>
   <BodyType/>
   <FilterHtmlContent/>
   <AdditionalProperties/>
</AttachmentShape>
```

 **AttachmentResponseShapeType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[IncludeMimeContent](includemimecontent.md) <br/> |指定是否在响应中返回的项目或附件多用途 Internet 邮件扩展 (MIME) 内容。 此元素是可选的。  <br/> |
|[BodyType](bodytype.md) <br/> |介绍如何在响应中设置的正文文本的格式。 此元素是可选的。  <br/> |
|[FilterHtmlContent](filterhtmlcontent.md) <br/> |指定是否从附件筛选存在安全隐患的 HTML 内容。 此元素是可选的。  <br/> |
|[AdditionalProperties](additionalproperties.md) <br/> |标识要返回的响应中的其他属性。 此元素是可选的。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetAttachment](getattachment.md) <br/> |定义一个请求以获取从 Exchange 存储中的邮箱的附件的元素。  <br/> 以下是此元素的 XPath 表达式：  <br/>  `/GetAttachment` <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>备注

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [GetAttachment 操作](getattachment-operation.md)
- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

