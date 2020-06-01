---
title: 设置（SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 43db26e1-f7be-49fd-b26b-fc1b10bd3458
description: Setting 元素表示要返回的配置设置。
ms.openlocfilehash: df3b55fe7ba2c5ae92f8c31ec0643dbe100fa072
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466743"
---
# <a name="setting-soap"></a>设置（SOAP）

**Setting**元素表示要返回的配置设置。 
  
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
|[RequestedSettings （SOAP）](requestedsettings-soap.md) <br/> |包含所请求的配置设置的名称。  <br/> |
   
## <a name="text-value"></a>文本值

此元素的文本值是配置设置。 下表列出了可能的配置设置。
  
|**配置设置**|**说明**|
|:-----|:-----|
|UserDisplayName  <br/> |用户的显示名称。  <br/> |
|UserDN  <br/> |用户的旧版可分辨名称。  <br/> |
|UserDeploymentId  <br/> |用户的部署标识符。  <br/> |
|InternalMailboxServer  <br/> |邮箱服务器的完全限定的域名（FQDN）。  <br/> |
|InternalRpcClientServer  <br/> |RPC 客户端服务器的完全限定域名。  <br/> |
|InternalMailboxServerDN  <br/> |邮箱服务器的旧版可分辨名称。  <br/> |
|InternalEcpUrl  <br/> |Exchange 控制面板的内部 URL。  <br/> |
|InternalEcpVoicemailUrl  <br/> |用于自定义语音邮件的 Exchange 控制面板的内部 URL。  <br/> |
|InternalEcpEmailSubscriptionsUrl  <br/> |用于电子邮件订阅的 Exchange 控制面板的内部 URL。  <br/> |
|InternalEcpTextMessagingUrl  <br/> |用于短信的 Exchange 控制面板的内部 URL。  <br/> |
|InternalEcpDeliveryReportUrl  <br/> |"送达报告" 的 Exchange 控制面板的内部 URL。  <br/> |
|InternalEcpRetentionPolicyTagsUrl  <br/> |Get-retentionpolicy 标记的 Exchange 控制面板的内部 URL。  <br/> |
|InternalEcpPublishingUrl  <br/> |用于发布的 Exchange 控制面板的内部 URL。  <br/> |
|InternalEwsUrl  <br/> |Exchange Web 服务的内部 URL。  <br/> |
|InternalOABUrl  <br/> |脱机通讯簿（OAB）的内部 URL。  <br/> |
|InternalUMUrl  <br/> |统一消息服务的内部 URL。  <br/> |
|InternalWebClientUrls  <br/> |Exchange Web 客户端的内部 Url。  <br/> |
|MailboxDN  <br/> |用户邮箱的邮箱数据库的可分辨名称。  <br/> |
|PublicFolderServer  <br/> |公用文件夹服务器的名称。  <br/> |
|ActiveDirectoryServer  <br/> |Active Directory 服务器的名称。  <br/> |
|ExternalMailboxServer  <br/> |RPC over HTTP 服务器的名称。  <br/> |
|ExternalMailboxServerRequiresSSL  <br/> |有关 RPC over HTTP 服务器是否需要 SSL 的指示器。  <br/> |
|ExternalMailboxServerAuthenticationMethods  <br/> |RPC over HTTP server 支持的身份验证方法。  <br/> |
|EcpVoicemailUrlFragment,  <br/> |用于自定义语音邮件的 Exchange 控制面板的 URL 片段。  <br/> |
|EcpEmailSubscriptionsUrlFragment  <br/> |用于电子邮件订阅的 Exchange 控制面板的 URL 片段。  <br/> |
|EcpTextMessagingUrlFragment  <br/> |用于短信的 Exchange 控制面板的 URL 片段。  <br/> |
|EcpDeliveryReportUrlFragment  <br/> |"传递报告" 的 Exchange 控制面板的 URL 片段。  <br/> |
|EcpRetentionPolicyTagsUrlFragment  <br/> |Get-retentionpolicy 标记的 Exchange 控制面板的 URL 片段。  <br/> |
|EcpPublishingUrlFragment  <br/> |用于发布的 Exchange 控制面板的 URL 片段。  <br/> |
|ExternalEcpUrl  <br/> |Exchange 控制面板的外部 URL。  <br/> |
|ExternalEcpVoicemailUrl  <br/> |用于自定义语音邮件的 Exchange 控制面板的外部 URL。  <br/> |
|ExternalEcpEmailSubscriptionsUrl  <br/> |用于电子邮件订阅的 Exchange 控制面板的外部 URL。  <br/> |
|ExternalEcpTextMessagingUrl  <br/> |用于短信的 Exchange 控制面板的外部 URL。  <br/> |
|ExternalEcpDeliveryReportUrl  <br/> |"传递报告" 的 Exchange 控制面板的外部 URL。  <br/> |
|ExternalEcpRetentionPolicyTagsUrl  <br/> |Get-retentionpolicy 标记的 Exchange 控制面板的外部 URL。  <br/> |
|ExternalEcpPublishingUrl  <br/> |用于发布的 Exchange 控制面板的外部 URL。  <br/> |
|ExternalEwsUrl  <br/> |Exchange Web 服务的外部 URL。  <br/> |
|ExternalOABUrl  <br/> |OAB 的外部 URL。  <br/> |
|ExternalUMUrl  <br/> |统一消息服务的外部 URL。  <br/> |
|ExternalWebClientUrls  <br/> |Exchange Web 客户端的外部 Url。  <br/> |
|CrossOrganizationSharingEnabled  <br/> |指示启用了跨组织共享。  <br/> |
|AlternateMailboxes  <br/> |备用邮箱的集合。  <br/> |
|CasVersion  <br/> |为请求提供服务的客户端访问服务器的版本（例如，14. XX。YYYY.ZZZ  <br/> |
|EwsSupportedSchemas  <br/> |Exchange Web 服务支持的架构版本的逗号分隔列表。 架构版本值将与**ExchangeServerVersion**枚举的值相同。  <br/> |
|InternalPop3Connections  <br/> |POP3 协议连接的内部连接设置列表。  <br/> |
|ExternalPop3Connections  <br/> |POP3 协议连接的外部连接设置列表。  <br/> |
|InternalImap4Connections  <br/> |IMAP4 协议连接的 "内部连接设置" 列表。  <br/> |
|ExternalImap4Connections  <br/> |IMAP4 协议连接的外部连接设置列表。  <br/> |
|InternalSmtpConnections  <br/> |SMTP 连接的 "内部连接设置" 列表。  <br/> |
|ExternalSmtpConnections  <br/> |SMTP 连接的 "外部连接设置" 列表。  <br/> |
|InternalServerExclusiveConnect  <br/> |内部服务器独占连接标志。 如果设置为 "关"，则客户端不应通过此协议进行连接。  <br/> |
|ExternalServerExclusiveConnect  <br/> |外部服务器独占连接标志。 如果设置为 "开启"，客户端应通过此协议进行连接。  <br/> |
|ExchangeRpcUrl  <br/> |用于远程过程调用的 URL。 此 URL 是服务器内部的，且不由客户端使用。  <br/> |
|ShowGalAsDefaultView  <br/> |指定一个布尔值，该值指示 GAL 是否应显示为通讯簿。 文本值为 "true" 表示默认情况下显示 GAL。 文本值为 "false" 表示显示联系人列表。  <br/> |
|AutoDiscoverSMTPAddress  <br/> |用户的自动发现主 SMTP 地址。 如果代理地址存在，则这是代理地址（替代用户的电子邮件地址）。  <br/> |
|InteropExternalEwsUrl  <br/> |服务器的 Web 服务终结点的外部 URL。 这是指向可为在不具有 Web 服务的服务器上托管的邮箱提供服务的服务器的 URL。  <br/> |
|ExternalEwsVersion  <br/> |正在传递指定请求的 Web 服务服务器的版本。  <br/> |
|InteropExternalEwsVersion  <br/> |服务器 InteropExternalEwsUrl 的版本指向。  <br/> |
|MobileMailboxPolicyInterop  <br/> |移动邮箱策略设置。  <br/> |
|GroupingInformation  <br/> |一个与 ExternalEwsUrl 设置结合使用的值，用于将多个邮箱组合在一起，以在订阅通知时[保持相关性](https://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx)。  <br/> |
|UserMSOnline  <br/> |一个布尔值，指示用户的邮箱是托管在 Exchange Online 中还是 Exchange Online 中作为 Office 365 的一部分承载。  <br/> |
|MapiHttpEnabled  <br/> |一个布尔值，指示是否可以通过 MAPI/HTTP 协议访问用户的邮箱。  <br/> |
   
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

