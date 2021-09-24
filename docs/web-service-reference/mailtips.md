---
title: MailTips
manager: sethgros
ms.date: 09/17/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MailTips
api_type:
- schema
ms.assetid: c1cba493-bccc-4b8e-be8e-bfa8a8b10882
description: MailTips 元素表示各种类型的邮件提示的值。
ms.openlocfilehash: bf7ed542d51f2a8cb3172275be12cb72104bc5b2
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59511136"
---
# <a name="mailtips"></a>MailTips

**MailTips** 元素表示各种类型的邮件提示的值。 
  
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
|[PendingMailTips](pendingmailtips.md) <br/> |指示在服务器的处理超时到期之前，无法评估此元素中的邮件提示。  <br/> |
|[OutOfOffice](outofoffice.md) <br/> |表示响应消息和发送响应邮件的持续时间。  <br/> |
|[MailboxFull](mailboxfull.md) <br/> |指示收件人的邮箱是否已满。  <br/> |
|[CustomMailTip](custommailtip.md) <br/> |表示自定义的邮件提示邮件。  <br/> |
|[TotalMemberCount](totalmembercount.md) <br/> |表示组中所有成员的计数。  <br/> |
|[ExternalMemberCount](externalmembercount.md) <br/> |表示组中外部成员的计数。  <br/> |
|[MaxMessageSize](maxmessagesize.md) <br/> |表示收件人可以接受的最大邮件大小。  <br/> |
|[DeliveryRestricted](deliveryrestricted.md) <br/> |指示传递限制是否阻止发件人的邮件到达收件人。  <br/> |
|[IsModerated](ismoderated.md) <br/> |指示收件人的邮箱是否正在被主持。  <br/> |
|[InvalidRecipient (MailTips)](invalidrecipient-mailtips.md) <br/> |指示收件人是否无效。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[MailTipsResponseMessageType](mailtipsresponsemessagetype.md) <br/> |代表邮件提示设置。  <br/> |
   
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



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

