---
title: 协议 (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: f77e4d66-6fdd-4999-9339-f7d7f9c86f44
description: 协议元素包含客户端连接到运行 Exchange Server 已安装了客户端访问服务器角色的计算机的规格。
ms.openlocfilehash: e58ae82ea5ec9d39db0f9219f6019df7da24a343
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826926"
---
# <a name="protocol-pox"></a>协议 (POX)

**协议**元素包含客户端连接到运行 Exchange Server 已安装了客户端访问服务器角色的计算机的规格。 
  
[自动发现 (POX)](autodiscover-pox.md)
  
[响应 (POX)](response-pox.md)
  
[帐户 (POX)](account-pox.md)
  
[协议 (POX)](protocol-pox.md)
  
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

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|类型  <br/> |指示此**协议**元素所述的协议类型。 唯一有效的值，此属性是"mapiHttp"。 此属性是仅存在如果自动发现请求的对应于此响应[包含 X MapiHttpCapability 标头](pox-autodiscover-request-for-exchange.md)。 此属性是适用于实现的 MAPI/HTTP 协议和目标 Exchange Online、 Exchange Online 作为 Office 365 的一部分的客户端或开头的 Exchange 内部部署版本生成 15.00.0847.032 (Exchange Server 2013 SP1)。  <br/> |
|版本  <br/> |指示此**协议**元素所述的协议的版本。 此属性仅有效值为"1"。 此属性才存在，则自动发现请求对应于此响应包含**X MapiHttpCapability**标头。 此属性是适用于实现的 MAPI/HTTP 协议和目标 Exchange Online、 Exchange Online 作为 Office 365 的一部分的客户端或开头的 Exchange 内部部署版本生成 15.00.0847.032 (Exchange Server 2013 SP1)。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[类型 (POX)](type-pox.md) <br/> |标识配置的邮件帐户的类型。  <br/> |
|[内部 (POX)](internal-pox.md) <br/> |包含客户端可以使用连接到从 Exchange 组织的网络内的 Url 的集合。  <br/> |
|[外部 (POX)](external-pox.md) <br/> |包含客户端可以使用连接到从 Exchange 组织的网络之外的 Url 的集合。  <br/> |
|[TTL (POX)](ttl-pox.md) <br/> |指定的时间生存，以小时，在此期间设置一直保持有效。  <br/> |
|[服务器 (POX)](server-pox.md) <br/> |指定的邮件服务器的名称。  <br/> |
|[ServerDN (POX)](serverdn-pox.md) <br/> |指定 Exchange 服务器可分辨的名称。  <br/> |
|[ServerVersion (POX)](serverversion-pox.md) <br/> |表示 Exchange Server 版本数。  <br/> |
|[MdbDN (POX)](mdbdn-pox.md) <br/> |表示的邮箱数据库的可分辨的名称。  <br/> |
|[PublicFolderServer (POX)](publicfolderserver-pox.md) <br/> |包含的完全限定域名 (FQDN) 的公用文件夹服务器的用户。  <br/> |
|[端口 (POX)](port-pox.md) <br/> |指定用于连接到存储的端口。  <br/> |
|[DirectoryPort (POX)](directoryport-pox.md) <br/> |指定用于连接到目录时使用的名称服务提供程序界面 (NSPI) 协议的端口。  <br/> |
|[ReferralPort (POX)](referralport-pox.md) <br/> |指定用于获取目录引用的端口。  <br/> |
|[ASUrl (POX)](asurl-pox.md) <br/> |指定已启用邮件的用户的 Exchange Web 服务的最佳实例的 URL。  <br/> |
|[EwsUrl (POX)](ewsurl-pox.md) <br/> |指定已启用邮件的用户的最佳的终结点实例的 URL 为 Exchange Web 服务 (EWS)。  <br/> |
|[EmwsUrl (POX)](emwsurl-pox.md) <br/> |指定已启用邮件的用户的最佳的终结点实例的 URL 为 Exchange Web 服务 (EWS)。  <br/> |
|[SharingUrl (POX)](sharingurl-pox.md) <br/> |包含用于跨组织共享日历和联系人信息的共享服务器的 URL。  <br/> |
|[EcpUrl (POX)](ecpurl-pox.md) <br/> |指定已启用邮件的用户的 Exchange 控制面板的 URL。  <br/> |
|[EcpUrl-um (POX)](ecpurl-um-pox.md) <br/> |指定可以结合使用[EcpUrl (POX)](ecpurl-pox.md)元素的值生成一个 URL，可用于访问已启用邮件的用户的语音邮件设置的部分 URL。  <br/> |
|[EcpUrl aggr (POX)](ecpurl-aggr-pox.md) <br/> |指定可以结合使用[EcpUrl (POX)](ecpurl-pox.md)元素的值生成一个 URL，可用于访问电子邮件的启用邮件的用户的聚合设置的部分 URL。  <br/> |
|[EcpUrl 黑 (POX)](ecpurl-mt-pox.md) <br/> |指定可以结合使用[EcpUrl (POX)](ecpurl-pox.md)元素的值生成一个 URL，可用于访问电子邮件跟踪已启用邮件的用户设置的部分 URL。  <br/> |
|[EcpUrl 寄信人 (POX)](ecpurl-ret-pox.md) <br/> |指定可以结合使用[EcpUrl (POX)](ecpurl-pox.md)元素的值生成一个 URL，可用于访问已启用邮件的用户的保留标记设置的部分 URL。  <br/> |
|[EcpUrl sms (POX)](ecpurl-sms-pox.md) <br/> |指定可以结合使用[EcpUrl (POX)](ecpurl-pox.md)元素的值生成一个 URL，可用于访问已启用邮件的用户的短信服务 (SMS) 设置的部分 URL。  <br/> |
|[EcpUrl 发布 (POX)](ecpurl-publish-pox.md) <br/> |指定可以结合使用[EcpUrl (POX)](ecpurl-pox.md)元素的值生成一个 URL，可用于访问日历发布已启用邮件的用户设置的部分 URL。  <br/> |
|[EcpUrl 照片 (POX)](ecpurl-photo-pox.md) <br/> |指定可以结合使用[EcpUrl (POX)](ecpurl-pox.md)元素的值生成一个 URL，可用于查看或更改已启用邮件的用户的当前照片的部分 URL。  <br/> |
|[EcpUrl tm (POX)](ecpurl-tm-pox.md) <br/> |指定可以结合使用[EcpUrl (POX)](ecpurl-pox.md)元素的值生成一个可用于访问其中的所有站点邮箱的已启用邮件的用户是当前成员的列表的 URL 的部分 URL。  <br/> |
|[EcpUrl tmCreating (POX)](ecpurl-tmcreating-pox.md) <br/> |指定可以结合使用[EcpUrl (POX)](ecpurl-pox.md)元素的值生成一个 URL，可用于创建新的站点邮箱的部分 URL。  <br/> |
|[EcpUrl tmHiding (POX)](ecpurl-tmhiding-pox.md) <br/> |指定可以结合使用[EcpUrl (POX)](ecpurl-pox.md)元素的值生成一个 URL，可用来取消订阅的站点邮箱用户的部分 URL。  <br/> |
|[EcpUrl tmEditing (POX)](ecpurl-tmediting-pox.md) <br/> |指定可以结合使用[EcpUrl (POX)](ecpurl-pox.md)元素的值生成一个 URL，可用于编辑现有的网站邮箱的部分 URL。  <br/> |
|[EcpUrl extinstall (POX)](ecpurl-extinstall-pox.md) <br/> |指定可以结合使用[EcpUrl (POX)](ecpurl-pox.md)元素的值生成一个可用于查看或更改当前用户的邮箱中安装邮件应用程序的 URL 的部分 URL。  <br/> |
|[OOFUrl (POX)](oofurl-pox.md) <br/> |指定已启用邮件的用户的可用性服务的最佳实例的 URL。  <br/> |
|[OABUrl (POX)](oaburl-pox.md) <br/> |指定 Exchange 拓扑的脱机通讯簿配置服务器 URL。  <br/> |
|[UMUrl (POX)](umurl-pox.md) <br/> |指定已启用邮件的用户的统一消息 Web 服务的最佳实例的 URL。  <br/> |
|[EwsPartnerUrl (POX)](ewspartnerurl-pox.md) <br/> |指定已启用邮件的用户的最佳的终结点实例的 URL 为 Exchange Web 服务 (EWS)。  <br/> |
|[使用 LoginName (POX)](loginname-pox.md) <br/> |指定用户的登录名。  <br/> |
|[DomainRequired (POX)](domainrequired-pox.md) <br/> |指示是否需要身份验证的域。  <br/> |
|[DomainName (POX)](domainname-pox.md) <br/> |指定用户的域。  <br/> |
|[SPA (POX)](spa-pox.md) <br/> |指示是否需要安全密码身份验证。  <br/> |
|[AuthPackage (POX)](authpackage-pox.md) <br/> |指定对已安装了邮箱服务器角色的 Exchange 2007 计算机时所使用的身份验证方案。  <br/> |
|[CertPrincipalName (POX)](certprincipalname-pox.md) <br/> |指定需要使用 SSL 连接到 Microsoft Exchange 组织的安全套接字层 (SSL) 证书主体名称。  <br/> |
|[SSL (POX)](ssl-pox.md) <br/> |指定是否需要安全登录。  <br/> |
|[AuthRequired (POX)](authrequired-pox.md) <br/> |指定是否需要身份验证。  <br/> |
|[UsePOPAuth (POX)](usepopauth-pox.md) <br/> |指示是否提供 POP3 类型的帐户的身份验证信息也使用的简单邮件传输协议 (SMTP)。  <br/> |
|[SMTPLast (POX)](smtplast-pox.md) <br/> |指定的 SMTP 服务器是否需要使用 SMTP 服务器发送电子邮件之前下载的电子邮件。  <br/> |
|[NetworkRequirements (POX)](networkrequirements-pox.md) <br/> |包含用于确定客户端计算机是否满足 Internet 服务提供商的要求，以连接到服务器的网络上的条件。  <br/> |
|[通讯簿 (POX)](addressbook-pox.md) <br/> |包含使用 MAPI/HTTP 协议客户端连接到通讯簿服务器的规范。 此元素是仅存在**协议**元素的**Type**属性是否存在并将设置为"mapiHttp"。 适用于实现的 MAPI/HTTP 协议和目标 Exchange Online 和 Exchange 开头 15.00.0847.032 版本的客户端的**通讯簿**元素。  <br/> |
|[MailStore (POX)](mailstore-pox.md) <br/> |包含使用 MAPI/HTTP 协议来连接到用户邮箱的客户端的规范。 此元素是仅存在**协议**元素的**Type**属性是否存在并将设置为"mapiHttp"。 适用于客户端实现的 MAPI/HTTP 协议和 Exchange Online 的目标和版本的 Exchange 开头 15.00.0847.032 **MailStore**元素。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[帐户 (POX)](account-pox.md) <br/> |指定用户帐户的设置。  <br/> |
   
## <a name="remarks"></a>备注

其[操作 (POX)](action-pox.md)值，它等于**设置**的响应中存在**协议**元素。
  
## <a name="see-also"></a>另请参阅



[Exchange POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

