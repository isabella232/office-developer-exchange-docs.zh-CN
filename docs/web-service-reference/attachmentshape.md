---
title: AttachmentShape
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- AttachmentShape
api_type:
- schema
ms.assetid: 734914b5-3a16-4744-90a5-741fd30c4676
description: AttachmentShape 元素标识响应 GetAttachment 请求时要返回的其他属性。
ms.openlocfilehash: 2c7ceb25f481ec07577117e46e26537e657e18c7
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520036"
---
# <a name="attachmentshape"></a>AttachmentShape

**AttachmentShape** 元素标识响应 [GetAttachment](getattachment.md)请求时要返回的其他属性。 
  
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

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[IncludeMimeContent](includemimecontent.md) <br/> |指定是否在响应中返回项目或 (MIME) 多用途 Internet 邮件扩展或 MIME 邮件扩展。 此元素为可选。  <br/> |
|[BodyType](bodytype.md) <br/> |标识如何在响应中设置正文文本的格式。 此元素为可选。  <br/> |
|[FilterHtmlContent](filterhtmlcontent.md) <br/> |指定是否从附件筛选可能不安全的 HTML 内容。 此元素为可选。  <br/> |
|[AdditionalProperties](additionalproperties.md) <br/> |标识响应中要返回的其他属性。 此元素为可选。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetAttachment](getattachment.md) <br/> |定义从邮箱存储中的邮箱获取附件Exchange元素。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/GetAttachment` <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>注解

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [GetAttachment 操作](getattachment-operation.md)
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

