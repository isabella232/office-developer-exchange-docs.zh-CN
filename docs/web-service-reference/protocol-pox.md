---
title: 协议（POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: f77e4d66-6fdd-4999-9339-f7d7f9c86f44
description: Protocol 元素包含将客户端连接到运行 Exchange Server 且安装了客户端访问服务器角色的计算机的规范。
ms.openlocfilehash: 6fca347f49e27958ecb16cce345387b6a2146979
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/01/2020
ms.locfileid: "44467758"
---
# <a name="protocol-pox"></a>协议（POX）

**Protocol**元素包含将客户端连接到运行 Exchange server 且安装了客户端访问服务器角色的计算机的规范。 
  
[自动发现（POX）](autodiscover-pox.md)
  
[响应（POX）](response-pox.md)
  
[帐户（POX）](account-pox.md)
  
[协议（POX）](protocol-pox.md)
  
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
|类型  <br/> |指示此**协议**元素描述的协议的类型。 此属性唯一的有效值是 "Mapi"。 仅当与此响应对应的自动发现请求[包含 MapiHttpCapability 标头](pox-autodiscover-request-for-exchange.md)时，才会出现此属性。 此属性适用于实现 MAPI/HTTP 协议和目标 Exchange Online 的客户端、Exchange Online （作为 Office 365 的一部分）或 Exchange Online 版本（从 build 15.00.0847.032 （Exchange Server 2013 SP1）开始。  <br/> |
|版本  <br/> |指示此**协议**元素描述的协议的版本。 此属性唯一的有效值为 "1"。 仅当与此响应对应的自动发现请求包含**MapiHttpCapability**标头时，才会出现此属性。 此属性适用于实现 MAPI/HTTP 协议和目标 Exchange Online 的客户端、Exchange Online （作为 Office 365 的一部分）或 Exchange Online 版本（从 build 15.00.0847.032 （Exchange Server 2013 SP1）开始。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[类型（POX）](type-pox.md) <br/> |标识配置的邮件帐户的类型。  <br/> |
|[Internal （POX）](internal-pox.md) <br/> |包含客户端可用于从组织的网络内部连接到 Exchange 的 Url 的集合。  <br/> |
|[外部（POX）](external-pox.md) <br/> |包含一个 Url 集合，客户端可以使用这些 Url 从组织的网络外部连接到 Exchange。  <br/> |
|[TTL （POX）](ttl-pox.md) <br/> |指定设置保持有效的生存时间（以小时为单位）。  <br/> |
|[服务器（POX）](server-pox.md) <br/> |指定邮件服务器的名称。  <br/> |
|[ServerDN （POX）](serverdn-pox.md) <br/> |指定 Exchange 服务器可分辨名称。  <br/> |
|[ServerVersion （POX）](serverversion-pox.md) <br/> |表示 Exchange Server 版本号。  <br/> |
|[MdbDN （POX）](mdbdn-pox.md) <br/> |表示邮箱数据库的可分辨名称。  <br/> |
|[PublicFolderServer （POX）](publicfolderserver-pox.md) <br/> |包含用户的公用文件夹服务器的完全限定的域名（FQDN）。  <br/> |
|[端口（POX）](port-pox.md) <br/> |指定用于连接到存储区的端口。  <br/> |
|[DirectoryPort （POX）](directoryport-pox.md) <br/> |指定在使用名称服务提供程序接口（NSPI）协议时用于连接到目录的端口。  <br/> |
|[ReferralPort （POX）](referralport-pox.md) <br/> |指定用于获取目录检索的端口。  <br/> |
|[ASUrl （POX）](asurl-pox.md) <br/> |指定已启用邮件的用户的 Exchange Web 服务最佳实例的 URL。  <br/> |
|[Mailbox.ewsurl （POX）](ewsurl-pox.md) <br/> |指定已启用邮件的用户的 Exchange Web 服务（EWS）的最佳终结点实例的 URL。  <br/> |
|[EmwsUrl （POX）](emwsurl-pox.md) <br/> |指定已启用邮件的用户的 Exchange Web 服务（EWS）的最佳终结点实例的 URL。  <br/> |
|[SharingUrl （POX）](sharingurl-pox.md) <br/> |包含用于跨组织共享日历和联系人的共享服务器的 URL。  <br/> |
|[EcpUrl （POX）](ecpurl-pox.md) <br/> |指定已启用邮件的用户的 Exchange 控制面板的 URL。  <br/> |
|[EcpUrl-um （POX）](ecpurl-um-pox.md) <br/> |指定可与[EcpUrl （POX）](ecpurl-pox.md)元素的值组合在一起的部分 url，以生成可用于访问启用邮件的用户的语音邮件设置的 URL。  <br/> |
|[EcpUrl-aggr （POX）](ecpurl-aggr-pox.md) <br/> |指定可与[EcpUrl （POX）](ecpurl-pox.md)元素的值组合在一起的部分 url，以生成可用于访问启用邮件的用户的电子邮件聚合设置的 URL。  <br/> |
|[EcpUrl-mt （POX）](ecpurl-mt-pox.md) <br/> |指定可与[EcpUrl （POX）](ecpurl-pox.md)元素的值结合使用的部分 url，以生成可用于访问启用邮件的用户的电子邮件跟踪设置的 URL。  <br/> |
|[EcpUrl-ret （POX）](ecpurl-ret-pox.md) <br/> |指定可与[EcpUrl （POX）](ecpurl-pox.md)元素的值组合在一起的部分 url，以生成可用于访问启用邮件的用户的保留标记设置的 URL。  <br/> |
|[EcpUrl-sms （POX）](ecpurl-sms-pox.md) <br/> |指定可与[EcpUrl （POX）](ecpurl-pox.md)元素的值组合在一起的部分 url，以生成可用于为启用邮件的用户访问短信服务（SMS）设置的 URL。  <br/> |
|[EcpUrl-发布（POX）](ecpurl-publish-pox.md) <br/> |指定可与[EcpUrl （POX）](ecpurl-pox.md)元素的值组合在一起的部分 url，以生成可用于访问启用邮件的用户的日历发布设置的 URL。  <br/> |
|[EcpUrl-photo （POX）](ecpurl-photo-pox.md) <br/> |指定可与[EcpUrl （POX）](ecpurl-pox.md)元素的值结合使用的部分 url，以生成可用于查看或更改已启用邮件的用户的当前照片的 URL。  <br/> |
|[EcpUrl-tm （POX）](ecpurl-tm-pox.md) <br/> |指定可与[EcpUrl （POX）](ecpurl-pox.md)元素的值结合使用的部分 url，以生成一个 url，该 url 可用于访问已启用邮件的用户当前为其成员的所有站点邮箱的列表。  <br/> |
|[EcpUrl-tmCreating （POX）](ecpurl-tmcreating-pox.md) <br/> |指定可与[EcpUrl （POX）](ecpurl-pox.md)元素的值组合在一起以生成可用于创建新网站邮箱的 url 的部分 URL。  <br/> |
|[EcpUrl-tmHiding （POX）](ecpurl-tmhiding-pox.md) <br/> |指定可与[EcpUrl （POX）](ecpurl-pox.md)元素的值组合在一起的部分 url，以生成可用于从网站邮箱取消订阅用户的 URL。  <br/> |
|[EcpUrl-tmEditing （POX）](ecpurl-tmediting-pox.md) <br/> |指定可与[EcpUrl （POX）](ecpurl-pox.md)元素的值组合在一起以生成可用于编辑现有网站邮箱的 url 的部分 url。  <br/> |
|[EcpUrl-extinstall （POX）](ecpurl-extinstall-pox.md) <br/> |指定可与[EcpUrl （POX）](ecpurl-pox.md)元素的值组合在一起的部分 url，以生成可用于查看或更改当前安装在用户邮箱中的邮件应用程序的 url。  <br/> |
|[OOFUrl （POX）](oofurl-pox.md) <br/> |指定已启用邮件的用户的可用性服务的最佳实例的 URL。  <br/> |
|[OABUrl （POX）](oaburl-pox.md) <br/> |指定 Exchange 拓扑的脱机通讯簿配置服务器 URL。  <br/> |
|[UMUrl （POX）](umurl-pox.md) <br/> |指定已启用邮件的用户的统一消息 Web 服务的最佳实例的 URL。  <br/> |
|[EwsPartnerUrl （POX）](ewspartnerurl-pox.md) <br/> |指定已启用邮件的用户的 Exchange Web 服务（EWS）的最佳终结点实例的 URL。  <br/> |
|[Person.loginname （POX）](loginname-pox.md) <br/> |指定用户的登录名。  <br/> |
|[DomainRequired （POX）](domainrequired-pox.md) <br/> |指示是否需要域进行身份验证。  <br/> |
|[DomainName （POX）](domainname-pox.md) <br/> |指定用户的域。  <br/> |
|[SPA （POX）](spa-pox.md) <br/> |指示是否需要安全密码身份验证。  <br/> |
|[AuthPackage （POX）](authpackage-pox.md) <br/> |指定在对安装了邮箱服务器角色的 Exchange 2007 计算机进行身份验证时使用的身份验证方案。  <br/> |
|[CertPrincipalName （POX）](certprincipalname-pox.md) <br/> |指定使用 SSL 连接到 Microsoft Exchange 组织所需的安全套接字层（SSL）证书主体名称。  <br/> |
|[SSL （POX）](ssl-pox.md) <br/> |指定是否需要安全登录。  <br/> |
|[Resolver.rst.authrequired （POX）](authrequired-pox.md) <br/> |指定是否需要身份验证。  <br/> |
|[UsePOPAuth （POX）](usepopauth-pox.md) <br/> |指示是否还将为 POP3 帐户类型提供的身份验证信息用于简单邮件传输协议（SMTP）。  <br/> |
|[SMTPLast （POX）](smtplast-pox.md) <br/> |指定 SMTP 服务器是否要求先下载电子邮件，然后再使用 SMTP 服务器发送电子邮件。  <br/> |
|[NetworkRequirements （POX）](networkrequirements-pox.md) <br/> |包含用于确定客户端计算机是否位于满足 Internet 服务提供商要求以连接到服务器的网络上的条件。  <br/> |
|[AddressBook （POX）](addressbook-pox.md) <br/> |包含使用 MAPI/HTTP 协议将客户端连接到通讯簿服务器的规范。 仅当**Protocol**元素的**Type**属性存在并将其设置为 "mapi" 时，才会出现此元素。 **AddressBook**元素适用于实现 MAPI/HTTP 协议和目标 exchange Online 的客户端，以及从15.00.0847.032 开始的 exchange 版本。  <br/> |
|[MailStore （POX）](mailstore-pox.md) <br/> |包含使用 MAPI/HTTP 协议将客户端连接到用户邮箱的规范。 仅当**Protocol**元素的**Type**属性存在并将其设置为 "mapi" 时，才会出现此元素。 **MailStore**元素适用于实现 MAPI/HTTP 协议和目标 exchange Online 的客户端，以及从15.00.0847.032 开始的 exchange 版本。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[帐户（POX）](account-pox.md) <br/> |指定用户的帐户设置。  <br/> |
   
## <a name="remarks"></a>备注

**Protocol**元素存在于响应中，该响应具有与**设置**相等的[操作（POX）](action-pox.md)值。
  
## <a name="see-also"></a>另请参阅



[Exchange 的 POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

