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
description: MimeContent 元素包含一个对象，表示 base64Binary 格式并支持 [RFC2045] 的 ASCII MIME 流。
ms.openlocfilehash: 60f2d42f09347611559137c494d93036f1192829
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826465"
---
# <a name="mimecontent"></a>MimeContent

**MimeContent**元素包含一个对象，表示 base64Binary 格式并支持[[RFC2045]](http://www.rfc-editor.org/rfc/rfc2045.txt)的 ASCII MIME 流。
  
```xml
<MimeContent CharacterSet="" />
```

 **MimeContentType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|**CharacterSet** <br/> |如果设置，此属性的值将被忽略该服务器。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[日历项目](calendaritem.md) | [联系人](contact.md) | [DistributionList](distributionlist.md) | [项](item.md) | [MeetingCancellation](meetingcancellation.md) | [MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md)  |  [MeetingResponse](meetingresponse.md) | [消息](message-ex15websvcsotherref.md) | [RemoveItem](removeitem.md) | [任务](task.md)
  
## <a name="text-value"></a>文本值

如果使用此元素，则需要一个表示 base64Binary MIME 流文本值。
  
## <a name="remarks"></a>备注

消息内容经历的编码然后将其存储在**MimeContent**值的以下三个级别： 
  
1. 消息正文 — 这是编码，如 iso-2022年-jp 日语字符的正文。
    
2. MIME 流 — 这是**MimeContent**元素中，消息文本的 ASCII 编码或[MimeContentUTF8](mimecontentutf8.md)元素的消息文本的 UTF8 编码。 
    
3. XML 文档 — 这始终是 base64 编码 ASCII 流 MIME 流，其中等字符\<，其中有意义为 XML，从 XML 分析程序已被隐藏。
    
每个级别都独立于它之前的级别。
  
**MimeContent**元素可能包含其他与项目返回的属性包含相同的数据。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

