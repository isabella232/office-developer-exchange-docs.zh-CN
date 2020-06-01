---
title: MailTipsConfiguration (MailTipsServiceConfiguration)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailTipsConfiguration
api_type:
- schema
ms.assetid: 9a34515e-815b-4c61-b118-d5f66b80238f
description: MailTipsConfiguration 元素包含邮件提示服务的服务配置信息。
ms.openlocfilehash: 9128ee99545066899c3b27b624f10a9f1bd36c9d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467786"
---
# <a name="mailtipsconfiguration-mailtipsserviceconfiguration"></a>MailTipsConfiguration (MailTipsServiceConfiguration)

**MailTipsConfiguration**元素包含邮件提示服务的服务配置信息。 
  
```XML
<MailTipsConfiguration>
   <MailTipsEnabled/>
   <MaxRecipientsPerGetMailTipsRequest/>
   <MaxMessageSize/>
   <LargeAudienceThreshold/>
   <ShowExternalRecipientCount/>
   <InternalDomains/>
</MailTipsConfiguration>
```

 **MailTipsServiceConfiguration**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[MailTipsEnabled](mailtipsenabled.md) <br/> |指示是否可以使用邮件提示服务。 此元素是必需的。  <br/> |
|[MaxRecipientsPerGetMailTipsRequest](maxrecipientspergetmailtipsrequest.md) <br/> |指示可传递给[GetMailTips 操作](getmailtips-operation.md)的最大收件人数。 此元素是必需的。  <br/> |
|[MaxMessageSize](maxmessagesize.md) <br/> |表示收件人可接受的最大邮件大小。 此元素是必需的。  <br/> |
|[LargeAudienceThreshold](largeaudiencethreshold.md) <br/> |表示客户端的大型访问群体阈值。 此元素是必需的。  <br/> |
|[ShowExternalRecipientCount](showexternalrecipientcount.md) <br/> |指示[GetMailTips 操作](getmailtips-operation.md)的使用者是否必须显示指示向其发送邮件的外部收件人数的邮件提示。 此元素是必需的。  <br/> |
|[InternalDomains （SmtpDomainList）](internaldomains-smtpdomainlist.md) <br/> |标识组织的内部 SMTP 域的列表。 此元素是必需的。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ServiceConfigurationResponseMessageType](serviceconfigurationresponsemessagetype.md) <br/> |包含服务配置设置。  <br/> |
   
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

