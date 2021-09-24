---
title: MimeContentUTF8
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 31544c95-5231-4b57-958c-2a689464d29b
description: MimeContentUTF8 元素包含以 base64Binary 格式表示的对象的 UTF-8 MIME 流，并支持电子邮件地址国际化和 [RFC6530]。
ms.openlocfilehash: f0ab38368d3a18be38f63c86183a238e2fd0a474
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540753"
---
# <a name="mimecontentutf8"></a>MimeContentUTF8

**MimeContentUTF8** 元素包含以 base64Binary 格式表示的对象的 UTF-8 MIME 流，并支持电子邮件地址国际化 [和 [RFC6530]](http://www.rfc-editor.org/rfc/rfc6530.txt)。
  
```XML
<MimeContentUTF8 CharacterSet="" />
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

如果此元素已使用，则代表 base64binary MIME 流的文本值是必需的。
  
## <a name="remarks"></a>注解

邮件内容先经过以下三个级别的编码，然后再存储在 **MimeContentUTF8** 值中： 
  
1. 消息文本 — 这是正文编码，例如 iso-2022-jp 表示日语字符。
    
2. MIME 流 — 这是 **MimeContentUTF8** 元素的邮件文本的 UTF8 编码，或 [MimeContent](mimecontent.md) 元素的邮件文本的 ASCII 编码。 
    
3. XML 文档 — 这始终是 MIME 流的 base64 编码的 ASCII 流，其中对 XML 有意义的字符（例如''）在 XML 分析器中 \< 隐藏。
    
每个级别都独立于它之前的水平。
  
**MimeContentUTF8** 元素可能包含与项目所返回的其他属性相同的数据。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
### <a name="version-differences"></a>版本差异

此元素在版本 15.00.0986.00 Exchange版本提供。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

