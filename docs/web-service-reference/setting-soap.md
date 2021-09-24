---
title: Setting (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 43db26e1-f7be-49fd-b26b-fc1b10bd3458
description: Setting 元素表示要返回的配置设置。
ms.openlocfilehash: 2e03bfacaf36676ee4687c148f3b08732a9f17b1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59539141"
---
# <a name="setting-soap"></a>Setting (SOAP)

**Setting** 元素表示要返回的配置设置。 
  
```XML
<Setting/>
```

 **string**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[RequestedSettings (SOAP)](requestedsettings-soap.md) <br/> |包含请求的配置设置的名称。  <br/> |
   
## <a name="text-value"></a>文本值

此元素的文本值是配置设置。 下表列出了可能的配置设置。
  
|**配置设置**|**说明**|
|:-----|:-----|
|UserDisplayName  <br/> |用户的显示名称。  <br/> |
|UserDN  <br/> |用户的旧版可分辨名称。  <br/> |
|UserDeploymentId  <br/> |用户的部署标识符。  <br/> |
|InternalMailboxServer  <br/> |邮箱服务器的完全限定 (FQDN) FQDN。  <br/> |
|InternalRpcClientServer  <br/> |RPC 客户端服务器的完全限定域名。  <br/> |
|InternalMailboxServerDN  <br/> |邮箱服务器的旧版可分辨名称。  <br/> |
|InternalEcpUrl  <br/> |控制面板Exchange URL。  <br/> |
|InternalEcpVoicemailUrl  <br/> |VoiceMail 自定义Exchange控制面板的内部 URL。  <br/> |
|InternalEcpEmailSubscriptionsUrl  <br/> |电子邮件订阅Exchange控制面板的内部 URL。  <br/> |
|InternalEcpTextMessagingUrl  <br/> |文本消息Exchange控制面板的内部 URL。  <br/> |
|InternalEcpDeliveryReportUrl  <br/> |送达报告Exchange控制面板的内部 URL。  <br/> |
|InternalEcpRetentionPolicyTagsUrl  <br/> |RetentionPolicy 标记Exchange控制面板的内部 URL。  <br/> |
|InternalEcpPublishingUrl  <br/> |用于发布Exchange控制面板的内部 URL。  <br/> |
|InternalEwsUrl  <br/> |Web 服务Exchange URL。  <br/> |
|InternalOABUrl  <br/> |脱机通讯簿的内部 URL (OAB) 。  <br/> |
|InternalUMUrl  <br/> |统一消息服务的内部 URL。  <br/> |
|InternalWebClientUrls  <br/> |Web 客户端Exchange URL。  <br/> |
|MailboxDN  <br/> |用户邮箱的邮箱数据库的可分辨名称。  <br/> |
|PublicFolderServer  <br/> |公用文件夹服务器的名称。  <br/> |
|ActiveDirectoryServer  <br/> |Active Directory 服务器的名称。  <br/> |
|ExternalMailboxServer  <br/> |RPC over HTTP 服务器的名称。  <br/> |
|ExternalMailboxServerRequiresSSL  <br/> |用于指示 RPC over HTTP 服务器是否需要 SSL 的指示器。  <br/> |
|ExternalMailboxServerAuthenticationMethods  <br/> |RPC over HTTP 服务器支持的身份验证方法。  <br/> |
|EcpVoicemailUrlFragment，  <br/> |VoiceMail 自定义Exchange控制面板的 URL 片段。  <br/> |
|EcpEmailSubscriptionsUrlFragment  <br/> |电子邮件订阅Exchange控制面板的 URL 片段。  <br/> |
|EcpTextMessagingUrlFragment  <br/> |文本消息Exchange控制面板的 URL 片段。  <br/> |
|EcpDeliveryReportUrlFragment  <br/> |送达报告Exchange控制面板的 URL 片段。  <br/> |
|EcpRetentionPolicyTagsUrlFragment  <br/> |RetentionPolicy 标记Exchange控制面板的 URL 片段。  <br/> |
|EcpPublishingUrlFragment  <br/> |用于发布Exchange控制面板的 URL 片段。  <br/> |
|ExternalEcpUrl  <br/> |控制面板Exchange URL。  <br/> |
|ExternalEcpVoicemailUrl  <br/> |VoiceMail 自定义Exchange控制面板的外部 URL。  <br/> |
|ExternalEcpEmailSubscriptionsUrl  <br/> |电子邮件订阅Exchange控制面板的外部 URL。  <br/> |
|ExternalEcpTextMessagingUrl  <br/> |文本消息Exchange控制面板的外部 URL。  <br/> |
|ExternalEcpDeliveryReportUrl  <br/> |送达报告Exchange控制面板的外部 URL。  <br/> |
|ExternalEcpRetentionPolicyTagsUrl  <br/> |RetentionPolicy 标记Exchange控制面板的外部 URL。  <br/> |
|ExternalEcpPublishingUrl  <br/> |用于发布Exchange控制面板的外部 URL。  <br/> |
|ExternalEwsUrl  <br/> |Web 服务Exchange URL。  <br/> |
|ExternalOABUrl  <br/> |OAB 的外部 URL。  <br/> |
|ExternalUMUrl  <br/> |统一消息服务的外部 URL。  <br/> |
|ExternalWebClientUrls  <br/> |Web 客户端Exchange URL。  <br/> |
|CrossOrganizationSharingEnabled  <br/> |指示已启用跨组织共享。  <br/> |
|AlternateMailboxes  <br/> |备用邮箱的集合。  <br/> |
|CasVersion  <br/> |为请求提供服务的客户端访问服务器的版本 (例如，14.XX.YYYYY。ZZZ)   <br/> |
|EwsSupportedSchemas  <br/> |Web 服务支持的架构版本的逗号Exchange列表。 架构版本值与 **ExchangeServerVersion** 枚举的值相同。  <br/> |
|InternalPop3Connections  <br/> |POP3 协议连接的内部连接设置列表。  <br/> |
|ExternalPop3Connections  <br/> |POP3 协议连接的外部连接设置列表。  <br/> |
|InternalImap4Connections  <br/> |IMAP4 协议连接的内部连接设置列表。  <br/> |
|ExternalImap4Connections  <br/> |IMAP4 协议连接的外部连接设置列表。  <br/> |
|InternalSmtpConnections  <br/> |SMTP 连接的内部连接设置列表。  <br/> |
|ExternalSmtpConnections  <br/> |SMTP 连接的外部连接设置列表。  <br/> |
|InternalServerExclusiveConnect  <br/> |内部服务器独占连接标志。 如果设置为"关闭"，则客户端不应通过此协议进行连接。  <br/> |
|ExternalServerExclusiveConnect  <br/> |外部服务器独占连接标志。 如果设置为"打开"，则客户端应该通过此协议进行连接。  <br/> |
|ExchangeRpcUrl  <br/> |用于远程过程调用的 URL。 此 URL 位于服务器内部，不由客户端使用。  <br/> |
|ShowGalAsDefaultView  <br/> |指定一个布尔值，该值指示 GAL 是否应该显示为通讯簿。 文本值"true"指示 GAL 默认显示。 文本值"false"指示要显示联系人列表。  <br/> |
|AutoDiscoverSMTPAddress  <br/> |用户的自动发现主 SMTP 地址。 如果存在代理地址，则这是替代用户电子邮件地址的代理地址。  <br/> |
|InteropExternalEwsUrl  <br/> |服务器的 Web 服务终结点的外部 URL。 这是可服务于托管在不包含 Web 服务的服务器的邮箱的服务器的 URL。  <br/> |
|ExternalEwsVersion  <br/> |传递指定请求的 Web 服务服务器的版本。  <br/> |
|InteropExternalEwsVersion  <br/> |服务器 InteropExternalEwsUrl 指向的版本。  <br/> |
|MobileMailboxPolicyInterop  <br/> |移动邮箱策略设置。  <br/> |
|GroupingInformation  <br/> |与 ExternalEwsUrl 设置结合使用以将多个邮箱分组在一起以在[](https://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx)订阅通知时保持相关性的值。  <br/> |
|UserMSOnline  <br/> |一个布尔值，指示用户的邮箱托管在 Exchange Online 中Exchange Online还是作为 Office 365 的一Office 365。  <br/> |
|MapiHttpEnabled  <br/> |一个布尔值，指示用户邮箱是否可通过 MAPI/HTTP 协议访问。  <br/> |
   
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|架构名称  <br/> |自动发现架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetUserSettings 操作 (SOAP)](getusersettings-operation-soap.md)
  
[GetDomainSettings 操作 (SOAP)](getdomainsettings-operation-soap.md)

