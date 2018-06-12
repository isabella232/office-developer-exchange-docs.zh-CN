---
title: 设置 (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 43db26e1-f7be-49fd-b26b-fc1b10bd3458
description: Setting 元素表示要返回的配置设置。
ms.openlocfilehash: cb5b1d6ab2109b48810b96221b76c6b8fc9803ac
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827472"
---
# <a name="setting-soap"></a>设置 (SOAP)

**Setting**元素表示要返回的配置设置。 
  
```XML
<Setting/>
```

 **string**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

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
|UserDN  <br/> |用户的旧的可分辨的名称。  <br/> |
|UserDeploymentId  <br/> |用户的部署标识符。  <br/> |
|InternalMailboxServer  <br/> |完全限定的域名 (FQDN) 的邮箱服务器。  <br/> |
|InternalRpcClientServer  <br/> |RPC 客户端服务器的完全限定的域名。  <br/> |
|InternalMailboxServerDN  <br/> |邮箱服务器的旧的可分辨的名称。  <br/> |
|InternalEcpUrl  <br/> |Exchange 控制面板该内部 URL。  <br/> |
|InternalEcpVoicemailUrl  <br/> |Exchange 控制面板的语音邮件的自定义该内部 URL。  <br/> |
|InternalEcpEmailSubscriptionsUrl  <br/> |Exchange 控制面板的电子邮件订阅该内部 URL。  <br/> |
|InternalEcpTextMessagingUrl  <br/> |Exchange 控制面板的短信服务的内部 URL。  <br/> |
|InternalEcpDeliveryReportUrl  <br/> |Exchange 控制面板送达报告的内部 URL。  <br/> |
|InternalEcpRetentionPolicyTagsUrl  <br/> |Exchange 控制面板 RetentionPolicy 标记该内部 URL。  <br/> |
|InternalEcpPublishingUrl  <br/> |Exchange 控制面板发布该内部 URL。  <br/> |
|InternalEwsUrl  <br/> |内部 URL 的 Exchange Web 服务。  <br/> |
|InternalOABUrl  <br/> |脱机通讯簿 (OAB) 的内部 URL。  <br/> |
|InternalUMUrl  <br/> |统一消息服务的内部 URL。  <br/> |
|InternalWebClientUrls  <br/> |Exchange Web 客户端的内部 Url。  <br/> |
|MailboxDN  <br/> |用户的邮箱的邮箱数据库的可分辨的名称。  <br/> |
|PublicFolderServer  <br/> |公用文件夹服务器的名称。  <br/> |
|ActiveDirectoryServer  <br/> |Active Directory 服务器的名称。  <br/> |
|ExternalMailboxServer  <br/> |RPC over HTTP 服务器的名称。  <br/> |
|ExternalMailboxServerRequiresSSL  <br/> |有关 RPC over HTTP 服务器是否需要 SSL 指示器。  <br/> |
|ExternalMailboxServerAuthenticationMethods  <br/> |RPC over HTTP 服务器支持的身份验证方法。  <br/> |
|EcpVoicemailUrlFragment，  <br/> |Exchange 控制面板的语音邮件的自定义 URL 片段。  <br/> |
|EcpEmailSubscriptionsUrlFragment  <br/> |Exchange 控制面板的电子邮件订阅 URL 片段。  <br/> |
|EcpTextMessagingUrlFragment  <br/> |Exchange 控制面板的短信服务 URL 片段。  <br/> |
|EcpDeliveryReportUrlFragment  <br/> |Exchange 控制面板的送达报告 URL 片段。  <br/> |
|EcpRetentionPolicyTagsUrlFragment  <br/> |Exchange 控制面板 RetentionPolicy 标记 URL 片段。  <br/> |
|EcpPublishingUrlFragment  <br/> |Exchange 控制面板发布 URL 片段。  <br/> |
|ExternalEcpUrl  <br/> |Exchange 控制面板外部 URL。  <br/> |
|ExternalEcpVoicemailUrl  <br/> |Exchange 控制面板的语音邮件的自定义外部 URL。  <br/> |
|ExternalEcpEmailSubscriptionsUrl  <br/> |为电子邮件订阅 Exchange 控制面板外部 URL。  <br/> |
|ExternalEcpTextMessagingUrl  <br/> |Exchange 控制面板的短信服务的外部 URL。  <br/> |
|ExternalEcpDeliveryReportUrl  <br/> |Exchange 控制面板送达报告的外部 URL。  <br/> |
|ExternalEcpRetentionPolicyTagsUrl  <br/> |Exchange 控制面板 RetentionPolicy 标记外部 URL。  <br/> |
|ExternalEcpPublishingUrl  <br/> |Exchange 控制面板发布外部 URL。  <br/> |
|ExternalEwsUrl  <br/> |Exchange Web 服务的外部 URL。  <br/> |
|ExternalOABUrl  <br/> |OAB 的外部 URL。  <br/> |
|ExternalUMUrl  <br/> |统一消息服务的外部 URL。  <br/> |
|ExternalWebClientUrls  <br/> |Exchange Web 客户端的外部 Url。  <br/> |
|CrossOrganizationSharingEnabled  <br/> |指示启用跨组织共享。  <br/> |
|AlternateMailboxes  <br/> |备用邮箱的集合。  <br/> |
|CasVersion  <br/> |承担请求 (例如，14.XX 客户端访问服务器版本。YYYY。ZZZ)  <br/> |
|EwsSupportedSchemas  <br/> |架构版本支持的 Exchange Web 服务的以逗号分隔列表。 架构版本值将为**ExchangeServerVersion**枚举的值相同。  <br/> |
|InternalPop3Connections  <br/> |POP3 协议连接内部连接设置列表。  <br/> |
|ExternalPop3Connections  <br/> |POP3 协议连接外部连接设置列表。  <br/> |
|InternalImap4Connections  <br/> |IMAP4 协议连接内部连接设置列表。  <br/> |
|ExternalImap4Connections  <br/> |IMAP4 协议连接外部连接设置列表。  <br/> |
|InternalSmtpConnections  <br/> |SMTP 连接的内部连接设置列表。  <br/> |
|ExternalSmtpConnections  <br/> |SMTP 连接外部连接设置列表。  <br/> |
|InternalServerExclusiveConnect  <br/> |内部服务器独占连接标志。 如果设置为"Off"然后客户端不应该连接通过此协议。  <br/> |
|ExternalServerExclusiveConnect  <br/> |外部服务器独占连接标志。 如果设置为"开"然后客户端应通过此协议连接。  <br/> |
|ExchangeRpcUrl  <br/> |用于远程过程调用的 URL。 此 URL 是内部服务器，并且无法由客户端使用。  <br/> |
|ShowGalAsDefaultView  <br/> |指定布尔值，该值指示是否应为通讯簿显示 GAL。 文本值"true"表示 GAL 是默认显示。 为"false"的文本值指示显示联系人列表。  <br/> |
|AutoDiscoverSMTPAddress  <br/> |自动发现主 SMTP 地址的用户。 如果代理地址存在，这是而不是用户的电子邮件地址的代理地址。  <br/> |
|InteropExternalEwsUrl  <br/> |外部服务器的 Web 服务终结点的 URL。 这是可用于在没有 Web 服务的服务器上托管的邮箱服务器的 URL。  <br/> |
|ExternalEwsVersion  <br/> |提供了指定的请求的 Web services 服务器版本。  <br/> |
|InteropExternalEwsVersion  <br/> |指向服务器 InteropExternalEwsUrl 的版本。  <br/> |
|MobileMailboxPolicyInterop  <br/> |移动邮箱策略设置。  <br/> |
|GroupingInformation  <br/> |用与 ExternalEwsUrl 设置结合使用时订阅通知分组在一起以[维护关联](http://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx)的多个邮箱的值。  <br/> |
|UserMSOnline  <br/> |一个布尔值，指示是否在用户邮箱位于 Exchange Online 或 Exchange Online 作为 Office 365 的一部分。  <br/> |
|MapiHttpEnabled  <br/> |一个布尔值，该值指示是否可通过 MAPI/HTTP 协议访问用户的邮箱。  <br/> |
   
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|架构名称  <br/> |自动发现架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetUserSettings 操作 (SOAP)](getusersettings-operation-soap.md)
  
[GetDomainSettings 操作 (SOAP)](getdomainsettings-operation-soap.md)

