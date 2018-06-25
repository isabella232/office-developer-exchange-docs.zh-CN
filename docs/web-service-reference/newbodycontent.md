---
title: NewBodyContent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- NewBodyContent
api_type:
- schema
ms.assetid: 0303600d-16d8-4685-88f2-980c5ca7e9a6
description: NewBodyContent 元素均表示一条消息的新正文内容。
ms.openlocfilehash: b87393e460b1eee1c13efebf38e898d17915bd71
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826516"
---
# <a name="newbodycontent"></a>NewBodyContent

**NewBodyContent**元素均表示一条消息的新正文内容。 
  
```xml
<NewBodyContent BodyType=""/>
```

 **BodyType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|**BodyType** <br/> |表示一条消息的实际正文内容。  <br/> |
   
#### <a name="bodytype-attribute"></a>BodyType 属性

|**值**|**说明**|
|:-----|:-----|
|**HTML** <br/> |将所有正文都转换为 HTML。  <br/> |
|**Text** <br/> |将所有正文都转换为纯文本。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ReplyToItem](replytoitem.md) <br/> |包含对 Exchange 存储中的项目的发件人的回复。  <br/> |
|[ReplyAllToItem](replyalltoitem.md) <br/> |包含对发件人和所有找出的 Exchange 存储中的项目的收件人的答复。  <br/> |
|[ForwardItem](forwarditem.md) <br/> |包含要转发给收件人的 Exchange 存储区项。  <br/> |
|[CancelCalendarItem](cancelcalendaritem.md) <br/> |表示用于取消会议的响应对象。  <br/> |
|[PostReplyItem](postreplyitem.md) <br/> |包含一个公告项目答复。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。  <br/> |
   
## <a name="text-value"></a>文本值

文本值表示一条消息的新正文内容。
  
## <a name="remarks"></a>注解

描述此元素的架构位于 Exchange 服务器已安装了客户端访问服务器角色的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

