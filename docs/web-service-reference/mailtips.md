---
title: 邮件提示
manager: sethgros
ms.date: 09/17/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailTips
api_type:
- schema
ms.assetid: c1cba493-bccc-4b8e-be8e-bfa8a8b10882
description: 邮件提示元素表示各种邮件提示类型的值。
ms.openlocfilehash: 9bacdea7b4f3108f700ed102025445e01a73e69d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44447594"
---
# <a name="mailtips"></a>邮件提示

邮件**提示元素表示**各种邮件提示类型的值。 
  
```XML
<MailTips>
   <RecipientAddress/>
   <PendingMailTips/>
   <OutOfOffice/>
   <MailboxFull/>
   <CustomMailTip/>
   <TotalMemberCount/>
   <ExternalMemberCount/>
   <MaxMessageSize/>
   <DeliveryRestricted/>
   <IsModerated/>
   <InvalidRecipient/>
</MailTips>
```

 **邮件提示**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[RecipientAddress](recipientaddress.md) <br/> |表示收件人的邮箱。  <br/> |
|[PendingMailTips](pendingmailtips.md) <br/> |指示在服务器的处理超时过期之前无法评估此元素中的邮件提示。  <br/> |
|[外出](outofoffice.md) <br/> |表示响应消息和发送响应消息的持续时间。  <br/> |
|[MailboxFull](mailboxfull.md) <br/> |指示收件人的邮箱是否已满。  <br/> |
|[CustomMailTip](custommailtip.md) <br/> |代表自定义的邮件提示邮件。  <br/> |
|[TotalMemberCount](totalmembercount.md) <br/> |表示组中所有成员的计数。  <br/> |
|[ExternalMemberCount](externalmembercount.md) <br/> |表示组中的外部成员的计数。  <br/> |
|[MaxMessageSize](maxmessagesize.md) <br/> |表示收件人可接受的最大邮件大小。  <br/> |
|[DeliveryRestricted](deliveryrestricted.md) <br/> |指示传递限制是否将阻止发件人的邮件到达收件人。  <br/> |
|[IsModerated](ismoderated.md) <br/> |指示是否正在仲裁收件人的邮箱。  <br/> |
|[InvalidRecipient （邮件提示）](invalidrecipient-mailtips.md) <br/> |指示收件人是否无效。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[MailTipsResponseMessageType](mailtipsresponsemessagetype.md) <br/> |代表 "邮件提示设置"。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
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

