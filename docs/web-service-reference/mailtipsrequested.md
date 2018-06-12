---
title: MailTipsRequested
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailTipsRequested
api_type:
- schema
ms.assetid: 8037bbe5-a37f-4f77-8209-27a94f9095ef
description: MailTipsRequested 元素包含的邮件提示从的服务请求的类型。
ms.openlocfilehash: fa2bef394ea8473aa65bdc2f1d39c0794186fdc6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826348"
---
# <a name="mailtipsrequested"></a>MailTipsRequested

**MailTipsRequested**元素包含的邮件提示从的服务请求的类型。 
  
```XML
<MailTipsRequested/>
```

 **MailTipTypes**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetMailTips](getmailtips.md) <br/> |包含要检索的收件人和类型的邮件提示。  <br/> |
   
## <a name="text-value"></a>文本值

下表列出了**MailTipsRequested**元素的可能值。 
  
|**值**|**说明**|
|:-----|:-----|
|所有  <br/> |代表所有可用的邮件提示。  <br/> |
|OutOfOfficeMessage  <br/> |代表外出 (OOF) 邮件。  <br/> |
|MailboxFullStatus  <br/> |表示邮箱已满的状态。  <br/> |
|CustomMailTip  <br/> |代表自定义邮件提示。  <br/> |
|ExternalMemberCount  <br/> |表示外部成员计数。  <br/> |
|TotalMemberCount  <br/> |表示所有成员的计数。  <br/> |
|MaxMessageSize  <br/> |表示收件人可以接受的最大邮件大小。  <br/> |
|DeliveryRestriction  <br/> |指示传递限制是否将到达收件人阻止发件人的邮件。  <br/> |
|ModerationStatus  <br/> |指示是否将由审阅者审查发件人的邮件。  <br/> |
|InvalidRecipient  <br/> |指示收件人无效。  <br/> |
   
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



- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

