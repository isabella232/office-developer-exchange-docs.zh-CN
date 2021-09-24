---
title: MailTipsConfiguration (MailTipsServiceConfiguration)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MailTipsConfiguration
api_type:
- schema
ms.assetid: 9a34515e-815b-4c61-b118-d5f66b80238f
description: MailTipsConfiguration 元素包含邮件提示服务的服务配置信息。
ms.openlocfilehash: eb86291572f6854710d01badcee2db24406844c6
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524033"
---
# <a name="mailtipsconfiguration-mailtipsserviceconfiguration"></a>MailTipsConfiguration (MailTipsServiceConfiguration)

**MailTipsConfiguration** 元素包含邮件提示服务的服务配置信息。 
  
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
|[MailTipsEnabled](mailtipsenabled.md) <br/> |指示邮件提示服务是否可用。 此元素是必需的。  <br/> |
|[MaxRecipientsPerGetMailTipsRequest](maxrecipientspergetmailtipsrequest.md) <br/> |指示可以传递给 [GetMailTips](getmailtips-operation.md)操作的最大收件人数。 此元素是必需的。  <br/> |
|[MaxMessageSize](maxmessagesize.md) <br/> |表示收件人可以接受的最大邮件大小。 此元素是必需的。  <br/> |
|[LargeAudienceThreshold](largeaudiencethreshold.md) <br/> |表示客户端的大型受众阈值。 此元素是必需的。  <br/> |
|[ShowExternalRecipientCount](showexternalrecipientcount.md) <br/> |指示 [GetMailTips](getmailtips-operation.md) 操作使用者是否必须显示邮件提示，以指示邮件要发送到的外部收件人的数量。 此元素是必需的。  <br/> |
|[InternalDomains (SmtpDomainList)](internaldomains-smtpdomainlist.md) <br/> |标识组织的内部 SMTP 域的列表。 此元素是必需的。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ServiceConfigurationResponseMessageType](serviceconfigurationresponsemessagetype.md) <br/> |包含服务配置设置。  <br/> |
   
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

