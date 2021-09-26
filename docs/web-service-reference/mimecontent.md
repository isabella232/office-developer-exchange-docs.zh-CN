---
title: MimeContent
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MimeContent
api_type:
- schema
ms.assetid: 4f472a08-5653-4c54-ba65-831dfe32f20f
description: MimeContent 元素包含以 base64Binary 格式表示并支持 [RFC2045] 的对象的 ASCII MIME 流。
ms.openlocfilehash: 43040f241008010620ff4f1018cc5410a7a00e42
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542069"
---
# <a name="mimecontent"></a>MimeContent

**MimeContent** 元素包含以 base64Binary 格式表示并支持 [[RFC2045]](http://www.rfc-editor.org/rfc/rfc2045.txt)的对象的 ASCII MIME 流。
  
```xml
<MimeContent CharacterSet="" />
```

 **MimeContentType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**CharacterSet** <br/> |如果设置，则服务器将忽略此属性的值。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[CalendarItem](calendaritem.md)  | [联系人](contact.md)  | [DistributionList](distributionlist.md)  | [Item](item.md)  | [MeetingCancellation](meetingcancellation.md)  | [MeetingMessage](meetingmessage.md)  | [MeetingRequest](meetingrequest.md)  | [MeetingResponse](meetingresponse.md)  | [邮件](message-ex15websvcsotherref.md)  | [RemoveItem](removeitem.md)  | [任务](task.md)
  
## <a name="text-value"></a>文本值

如果使用此元素，则需要表示 base64Binary MIME 流的文本值。
  
## <a name="remarks"></a>注解

邮件内容先经过以下三个级别的编码，然后再存储在 **MimeContent** 值中： 
  
1. 消息文本 — 这是正文编码，例如 iso-2022-jp 表示日语字符。
    
2. MIME 流 — 这是 **MimeContent** 元素的邮件文本的 ASCII 编码，或 [MimeContentUTF8](mimecontentutf8.md) 元素的邮件文本的 UTF8 编码。 
    
3. XML 文档 — 这始终是 MIME 流的 base64 编码的 ASCII 流，其中对 XML 有意义的字符（例如''）在 XML 分析器中 \< 隐藏。
    
每个级别都独立于它之前的水平。
  
**MimeContent** 元素可能包含与项目所返回的其他属性相同的数据。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

