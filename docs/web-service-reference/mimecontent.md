---
title: MimeContent
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MimeContent
api_type:
- schema
ms.assetid: 4f472a08-5653-4c54-ba65-831dfe32f20f
description: MimeContent 元素包含以 base64Binary 格式表示并支持 [RFC2045] 的对象的 ASCII MIME 流。
ms.openlocfilehash: 039ef1245d48e4cf13141970921dd210f4bd7d06
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530434"
---
# <a name="mimecontent"></a>MimeContent

**MimeContent**元素包含以 base64Binary 格式表示并支持[[RFC2045]](http://www.rfc-editor.org/rfc/rfc2045.txt)的对象的 ASCII MIME 流。
  
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

[CalendarItem](calendaritem.md)  | [联系人](contact.md)  | [DistributionList](distributionlist.md)  | [项](item.md)  | [MeetingCancellation](meetingcancellation.md)  | [MeetingMessage](meetingmessage.md)  | [MeetingRequest](meetingrequest.md)  | [MeetingResponse](meetingresponse.md)  | [邮件](message-ex15websvcsotherref.md)  | [RemoveItem](removeitem.md)  | [任务](task.md)
  
## <a name="text-value"></a>文本值

如果使用此元素，则表示 base64Binary MIME 流的文本值是必需的。
  
## <a name="remarks"></a>备注

邮件内容在存储在**MimeContent**值之前，会经历以下三种编码级别： 
  
1. 邮件文本—这是正文编码，例如，日语字符的 iso-2022-jp。
    
2. MIME 流—这是**MimeContent**元素的邮件文本的 ASCII 编码，或[MimeContentUTF8](mimecontentutf8.md)元素的邮件文本的 UTF8 编码。 
    
3. XML 文档—这始终是 MIME 流的 base64 编码的 ASCII 流，其中的字符（如 ""）在 XML 分析程序中是隐藏的，这些字符（如 ' \< '）对 xml 是有意义的。
    
每个级别都独立于它之前的级别。
  
**MimeContent**元素可能包含与项目一起返回的其他属性所包含的数据。 
  
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

