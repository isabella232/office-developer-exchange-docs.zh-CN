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
description: MailTipsRequested 元素包含从服务请求的邮件提示的类型。
ms.openlocfilehash: bcb2ebf15e628a04e8507f938d385cf113f2f2a3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465896"
---
# <a name="mailtipsrequested"></a>MailTipsRequested

**MailTipsRequested**元素包含从服务请求的邮件提示的类型。 
  
```XML
<MailTipsRequested/>
```

 **MailTipTypes**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**描述**|
|:-----|:-----|
|[GetMailTips](getmailtips.md) <br/> |包含要检索的邮件提示的收件人和类型。  <br/> |
   
## <a name="text-value"></a>文本值

下表列出了**MailTipsRequested**元素的可能值。 
  
|**值**|**说明**|
|:-----|:-----|
|所有  <br/> |表示所有可用的邮件提示。  <br/> |
|OutOfOfficeMessage  <br/> |代表 "外出" （OOF）邮件。  <br/> |
|MailboxFullStatus  <br/> |表示已满的邮箱的状态。  <br/> |
|CustomMailTip  <br/> |代表自定义邮件提示。  <br/> |
|ExternalMemberCount  <br/> |表示外部成员的计数。  <br/> |
|TotalMemberCount  <br/> |表示所有成员的计数。  <br/> |
|MaxMessageSize  <br/> |表示收件人可接受的最大邮件大小。  <br/> |
|DeliveryRestriction  <br/> |指示传递限制是否将阻止发件人的邮件到达收件人。  <br/> |
|ModerationStatus  <br/> |指示审阅者是否会检查发件人的邮件。  <br/> |
|InvalidRecipient  <br/> |指示收件人是否无效。  <br/> |
   
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

