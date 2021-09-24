---
title: Protocol (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: f77e4d66-6fdd-4999-9339-f7d7f9c86f44
description: Protocol 元素包含用于将客户端连接到运行Exchange Server安装了客户端访问服务器角色的计算机的规范。
ms.openlocfilehash: 4f308951c74612936755e6d4c16620e38277aecb
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516396"
---
# <a name="protocol-pox"></a>Protocol (POX)

**Protocol** 元素包含用于将客户端连接到正在运行客户端访问服务器角色Exchange Server的计算机的规范。 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
```xml
<Protocol>
   <Type/>
   <Internal/>
   <External/>
   <TTL/>
   <Server/>
   <ServerDN/>
   <ServerVersion/>
   <MdbDN/>
   <PublicFolderServer/>
   <Port/>
   <DirectoryPort/>
   <ReferralPort/>
   <ASUrl/>
   <EwsUrl/>
   <EmwsUrl/>
   <SharingUrl/>
   <EcpUrl/>
   <EcpUrl-um/>
   <EcpUrl-aggr/>
   <EcpUrl-mt/>
   <EcpUrl-ret/>
   <EcpUrl-sms/>
   <EcpUrl-publish/>
   <EcpUrl-photo/>
   <EcpUrl-tm/>
   <EcpUrl-tmCreating/>
   <EcpUrl-tmHiding/>
   <EcpUrl-tmEditing/>
   <EcpUrl-extinstall/>
   <OOFUrl/>
   <OABUrl/>
   <UMUrl/>
   <EwsPartnerUrl/>
   <LoginName/>
   <DomainRequired/>
   <DomainName/>
   <SPA/>
   <AuthPackage/>
   <CertPrincipalName/>
   <SSL/>
   <AuthRequired/>
   <UsePOPAuth/>
   <SMTPLast/>
   <NetworkRequirements/>
   <AddressBook/>
   <MailStore/>
</Protocol>
```

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|类型  <br/> |指示此 Protocol 元素描述 **的协议** 类型。 此属性的唯一有效值为"mapiHttp"。 此属性仅在此响应对应的自动发现请求包含 [X-MapiHttpCapability 标头时存在](pox-autodiscover-request-for-exchange.md)。 此属性适用于从内部版本 15.00.0847.032 (Exchange Server 2013 SP1) 起实现 MAPI/HTTP 协议和目标 Exchange Online、Exchange Online 作为 Office 365 一部分的 Exchange 或本地版本的客户端。  <br/> |
|版本  <br/> |指示此 **Protocol** 元素描述的协议的版本。 此属性的唯一有效值为"1"。 此属性仅在此响应对应的自动发现请求包含 **X-MapiHttpCapability** 标头时存在。 此属性适用于从内部版本 15.00.0847.032 (Exchange Server 2013 SP1) 起实现 MAPI/HTTP 协议和目标 Exchange Online、Exchange Online 作为 Office 365 一部分的 Exchange 或本地版本的客户端。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Type (POX)](type-pox.md) <br/> |标识已配置的邮件帐户的类型。  <br/> |
|[Internal (POX)](internal-pox.md) <br/> |包含一组 URL，客户端可以使用这些 URL Exchange组织网络内部的 URL。  <br/> |
|[External (POX)](external-pox.md) <br/> |包含客户端可用于从组织网络外部连接到Exchange的 URL 集合。  <br/> |
|[TTL (POX)](ttl-pox.md) <br/> |指定生存时间（以小时表示，在此期间设置仍然有效）。  <br/> |
|[Server (POX)](server-pox.md) <br/> |指定邮件服务器的名称。  <br/> |
|[ServerDN (POX)](serverdn-pox.md) <br/> |指定可Exchange Server名称。  <br/> |
|[ServerVersion (POX)](serverversion-pox.md) <br/> |表示Exchange Server版本号。  <br/> |
|[MdbDN (POX)](mdbdn-pox.md) <br/> |表示邮箱数据库的可分辨名称。  <br/> |
|[PublicFolderServer (POX)](publicfolderserver-pox.md) <br/> |包含用户的公用文件夹 (FQDN) 完全限定的域名。  <br/> |
|[Port (POX)](port-pox.md) <br/> |指定用于连接到存储的端口。  <br/> |
|[DirectoryPort (POX)](directoryport-pox.md) <br/> |指定在使用名称服务提供程序接口或 NSPI 协议时 (连接到) 端口。  <br/> |
|[ReferralPort (POX)](referralport-pox.md) <br/> |指定用于获取目录引用的端口。  <br/> |
|[ASUrl (POX)](asurl-pox.md) <br/> |指定启用邮件的用户Exchange Web 服务的最佳实例的 URL。  <br/> |
|[EwsUrl (POX)](ewsurl-pox.md) <br/> |指定启用邮件的用户Exchange EWS Exchange (EWS) 的最佳终结点实例的 URL。  <br/> |
|[EmwsUrl (POX)](emwsurl-pox.md) <br/> |指定启用邮件的用户Exchange EWS Exchange (EWS) 的最佳终结点实例的 URL。  <br/> |
|[SharingUrl (POX)](sharingurl-pox.md) <br/> |包含用于日历和联系人的跨组织共享的共享服务器的 URL。  <br/> |
|[EcpUrl (POX)](ecpurl-pox.md) <br/> |指定启用邮件Exchange控制面板的 URL。  <br/> |
|[EcpUrl-um (POX)](ecpurl-um-pox.md) <br/> |指定可以与 [EcpUrl (POX) ](ecpurl-pox.md) 元素的值组合的部分 URL，以生成可用于访问启用邮件的用户的语音邮件设置的 URL。  <br/> |
|[EcpUrl-aggr (POX)](ecpurl-aggr-pox.md) <br/> |指定可以与 [EcpUrl (POX) ](ecpurl-pox.md) 元素的值组合的部分 URL，以生成可用于访问已启用邮件的用户的电子邮件聚合设置的 URL。  <br/> |
|[EcpUrl-mt (POX)](ecpurl-mt-pox.md) <br/> |指定可以与 [EcpUrl (POX) ](ecpurl-pox.md) 元素的值组合的部分 URL，以生成可用于访问启用邮件的用户的电子邮件跟踪设置的 URL。  <br/> |
|[EcpUrl-ret (POX)](ecpurl-ret-pox.md) <br/> |指定可以与 [EcpUrl (POX) ](ecpurl-pox.md) 元素的值组合的部分 URL，以生成可用于访问启用邮件的用户的保留标记设置的 URL。  <br/> |
|[EcpUrl-sms (POX)](ecpurl-sms-pox.md) <br/> |指定可以与 [EcpUrl (POX) ](ecpurl-pox.md) 元素的值组合的部分 URL，以生成可用于访问启用邮件的用户的短信服务 (SMS) 设置的 URL。  <br/> |
|[EcpUrl-publish (POX)](ecpurl-publish-pox.md) <br/> |指定可以与 [EcpUrl (POX) ](ecpurl-pox.md) 元素的值组合的部分 URL，以生成可用于访问已启用邮件的用户的日历发布设置的 URL。  <br/> |
|[EcpUrl-photo (POX)](ecpurl-photo-pox.md) <br/> |指定可以与 [EcpUrl (POX) ](ecpurl-pox.md) 元素的值组合的部分 URL，以生成可用于查看或更改启用邮件的用户的当前照片的 URL。  <br/> |
|[EcpUrl-tm (POX)](ecpurl-tm-pox.md) <br/> |指定可以与 [EcpUrl (POX) ](ecpurl-pox.md) 元素的值组合的部分 URL，以生成可用于访问已启用邮件的用户当前是其中成员的所有网站邮箱列表的 URL。  <br/> |
|[EcpUrl-tmCreating (POX)](ecpurl-tmcreating-pox.md) <br/> |指定一个部分 URL，该 URL 可以与 [EcpUrl ](ecpurl-pox.md) (POX) 元素的值结合使用，以生成可用于创建新网站邮箱的 URL。  <br/> |
|[EcpUrl-tmHiding (POX)](ecpurl-tmhiding-pox.md) <br/> |指定可以与 [EcpUrl ](ecpurl-pox.md) (POX) 元素的值组合的部分 URL，以生成可用于从网站邮箱取消订阅用户的 URL。  <br/> |
|[EcpUrl-tmEditing (POX)](ecpurl-tmediting-pox.md) <br/> |指定一个部分 URL，该 URL 可以与 [EcpUrl ](ecpurl-pox.md) (POX) 元素的值结合使用，以生成可用于编辑现有网站邮箱的 URL。  <br/> |
|[EcpUrl-extinstall (POX)](ecpurl-extinstall-pox.md) <br/> |指定可以与 [EcpUrl (POX) ](ecpurl-pox.md) 元素的值组合的部分 URL，以生成可用于查看或更改当前安装在用户邮箱中的邮件应用程序的 URL。  <br/> |
|[OOFUrl (POX)](oofurl-pox.md) <br/> |为启用邮件的用户指定可用性服务的最佳实例的 URL。  <br/> |
|[OABUrl (POX)](oaburl-pox.md) <br/> |指定拓扑的脱机通讯簿配置Exchange URL。  <br/> |
|[UMUrl (POX)](umurl-pox.md) <br/> |指定启用邮件的用户的统一消息 Web 服务的最佳实例的 URL。  <br/> |
|[EwsPartnerUrl (POX)](ewspartnerurl-pox.md) <br/> |指定启用邮件的用户Exchange EWS Exchange (EWS) 的最佳终结点实例的 URL。  <br/> |
|[LoginName (POX)](loginname-pox.md) <br/> |指定用户的登录名。  <br/> |
|[DomainRequired (POX)](domainrequired-pox.md) <br/> |指示身份验证是否需要域。  <br/> |
|[DomainName (POX)](domainname-pox.md) <br/> |指定用户的域。  <br/> |
|[SPA (POX)](spa-pox.md) <br/> |指示是否需要安全密码身份验证。  <br/> |
|[AuthPackage (POX)](authpackage-pox.md) <br/> |指定对安装了邮箱服务器角色的 Exchange 2007 计算机进行身份验证时所使用的身份验证方案。  <br/> |
|[CertPrincipalName (POX)](certprincipalname-pox.md) <br/> |指定安全套接字层 (SSL) 使用 SSL 连接到 Microsoft Exchange 组织所需的证书主体名称。  <br/> |
|[SSL (POX)](ssl-pox.md) <br/> |指定是否需要安全登录。  <br/> |
|[AuthRequired (POX)](authrequired-pox.md) <br/> |指定是否需要身份验证。  <br/> |
|[UsePOPAuth (POX)](usepopauth-pox.md) <br/> |指示为 POP3 类型的帐户提供的身份验证信息是否也用于简单邮件传输协议 (SMTP) 。  <br/> |
|[SMTPLast (POX)](smtplast-pox.md) <br/> |指定 SMTP 服务器是否要求在使用 SMTP 服务器发送电子邮件之前先下载电子邮件。  <br/> |
|[NetworkRequirements (POX)](networkrequirements-pox.md) <br/> |包含用于确定客户端计算机是否位于满足 Internet 服务提供商连接到服务器的要求的网络上的条件。  <br/> |
|[AddressBook (POX)](addressbook-pox.md) <br/> |包含使用 MAPI/HTTP 协议将客户端连接到通讯簿服务器的规范。 此元素仅在 **Protocol** 元素上的 **Type** 属性存在并设置为"mapiHttp"时存在。 **AddressBook** 元素适用于从 15.00.0847.032 开始实现 MAPI/HTTP 协议和目标 Exchange Online 和 Exchange 版本的客户端。  <br/> |
|[MailStore (POX)](mailstore-pox.md) <br/> |包含使用 MAPI/HTTP 协议将客户端连接到用户邮箱的规范。 此元素仅在 **Protocol** 元素上的 **Type** 属性存在并设置为"mapiHttp"时存在。 **MailStore** 元素适用于从 15.00.0847.032 开始实现 MAPI/HTTP 协议并面向 Exchange Online 和 Exchange 版本的客户端。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Account (POX)](account-pox.md) <br/> |指定用户的帐户设置。  <br/> |
   
## <a name="remarks"></a>注解

**Protocol** 元素存在于一个响应中，该响应的 Action ([POX](action-pox.md)) 值等于 **设置**。
  
## <a name="see-also"></a>另请参阅



[用于存储的 POX 自动发现 XML Exchange](pox-autodiscover-xml-elements-for-exchange.md)

