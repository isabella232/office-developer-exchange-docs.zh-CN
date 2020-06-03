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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467758"
---
# <a name="protocol-pox"></a><span data-ttu-id="567c4-103">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-103">Protocol (POX)</span></span>

<span data-ttu-id="567c4-104">**Protocol**元素包含将客户端连接到运行 Exchange server 且安装了客户端访问服务器角色的计算机的规范。</span><span class="sxs-lookup"><span data-stu-id="567c4-104">The **Protocol** element contains the specifications for connecting a client to the computer that is running Exchange Server that has the Client Access server role installed.</span></span> 
  
[<span data-ttu-id="567c4-105">自动发现（POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="567c4-106">响应（POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="567c4-107">帐户（POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="567c4-108">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-108">Protocol (POX)</span></span>](protocol-pox.md)
  
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

## <a name="attributes-and-elements"></a><span data-ttu-id="567c4-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="567c4-109">Attributes and elements</span></span>

<span data-ttu-id="567c4-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="567c4-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="567c4-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="567c4-111">Attributes</span></span>

|<span data-ttu-id="567c4-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="567c4-112">**Attribute**</span></span>|<span data-ttu-id="567c4-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="567c4-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="567c4-114">类型</span><span class="sxs-lookup"><span data-stu-id="567c4-114">Type</span></span>  <br/> |<span data-ttu-id="567c4-115">指示此**协议**元素描述的协议的类型。</span><span class="sxs-lookup"><span data-stu-id="567c4-115">Indicates the type of protocol described by this **Protocol** element.</span></span> <span data-ttu-id="567c4-116">此属性唯一的有效值是 "Mapi"。</span><span class="sxs-lookup"><span data-stu-id="567c4-116">The only valid value for this attribute is "mapiHttp".</span></span> <span data-ttu-id="567c4-117">仅当与此响应对应的自动发现请求[包含 MapiHttpCapability 标头](pox-autodiscover-request-for-exchange.md)时，才会出现此属性。</span><span class="sxs-lookup"><span data-stu-id="567c4-117">This attribute is only present if the Autodiscover request that corresponds to this response [included an X-MapiHttpCapability header](pox-autodiscover-request-for-exchange.md).</span></span> <span data-ttu-id="567c4-118">此属性适用于实现 MAPI/HTTP 协议和目标 Exchange Online 的客户端、Exchange Online （作为 Office 365 的一部分）或 Exchange Online 版本（从 build 15.00.0847.032 （Exchange Server 2013 SP1）开始。</span><span class="sxs-lookup"><span data-stu-id="567c4-118">This attribute is applicable to clients that implement the MAPI/HTTP protocol and target Exchange Online, Exchange Online as part of Office 365, or on-premises versions of Exchange starting with build 15.00.0847.032 (Exchange Server 2013 SP1).</span></span>  <br/> |
|<span data-ttu-id="567c4-119">版本</span><span class="sxs-lookup"><span data-stu-id="567c4-119">Version</span></span>  <br/> |<span data-ttu-id="567c4-120">指示此**协议**元素描述的协议的版本。</span><span class="sxs-lookup"><span data-stu-id="567c4-120">Indicates the version of the protocol described by this **Protocol** element.</span></span> <span data-ttu-id="567c4-121">此属性唯一的有效值为 "1"。</span><span class="sxs-lookup"><span data-stu-id="567c4-121">The only valid value for this attribute is "1".</span></span> <span data-ttu-id="567c4-122">仅当与此响应对应的自动发现请求包含**MapiHttpCapability**标头时，才会出现此属性。</span><span class="sxs-lookup"><span data-stu-id="567c4-122">This attribute is only present if the Autodiscover request that corresponds to this response included an **X-MapiHttpCapability** header.</span></span> <span data-ttu-id="567c4-123">此属性适用于实现 MAPI/HTTP 协议和目标 Exchange Online 的客户端、Exchange Online （作为 Office 365 的一部分）或 Exchange Online 版本（从 build 15.00.0847.032 （Exchange Server 2013 SP1）开始。</span><span class="sxs-lookup"><span data-stu-id="567c4-123">This attribute is applicable to clients that implement the MAPI/HTTP protocol and target Exchange Online, Exchange Online as part of Office 365, or on-premises versions of Exchange starting with build 15.00.0847.032 (Exchange Server 2013 SP1).</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="567c4-124">子元素</span><span class="sxs-lookup"><span data-stu-id="567c4-124">Child elements</span></span>

|<span data-ttu-id="567c4-125">**元素**</span><span class="sxs-lookup"><span data-stu-id="567c4-125">**Element**</span></span>|<span data-ttu-id="567c4-126">**说明**</span><span class="sxs-lookup"><span data-stu-id="567c4-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="567c4-127">类型（POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-127">Type (POX)</span></span>](type-pox.md) <br/> |<span data-ttu-id="567c4-128">标识配置的邮件帐户的类型。</span><span class="sxs-lookup"><span data-stu-id="567c4-128">Identifies the type of the configured mail account.</span></span>  <br/> |
|[<span data-ttu-id="567c4-129">Internal （POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-129">Internal (POX)</span></span>](internal-pox.md) <br/> |<span data-ttu-id="567c4-130">包含客户端可用于从组织的网络内部连接到 Exchange 的 Url 的集合。</span><span class="sxs-lookup"><span data-stu-id="567c4-130">Contains a collection of URLs that a client can use to connect to Exchange from inside the organization's network.</span></span>  <br/> |
|[<span data-ttu-id="567c4-131">外部（POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-131">External (POX)</span></span>](external-pox.md) <br/> |<span data-ttu-id="567c4-132">包含一个 Url 集合，客户端可以使用这些 Url 从组织的网络外部连接到 Exchange。</span><span class="sxs-lookup"><span data-stu-id="567c4-132">Contains a collection of URLs that a client can use to connect to Exchange from outside of the organization's network.</span></span>  <br/> |
|[<span data-ttu-id="567c4-133">TTL （POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-133">TTL (POX)</span></span>](ttl-pox.md) <br/> |<span data-ttu-id="567c4-134">指定设置保持有效的生存时间（以小时为单位）。</span><span class="sxs-lookup"><span data-stu-id="567c4-134">Specifies the Time to Live, in hours, during which the settings remain valid.</span></span>  <br/> |
|[<span data-ttu-id="567c4-135">服务器（POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-135">Server (POX)</span></span>](server-pox.md) <br/> |<span data-ttu-id="567c4-136">指定邮件服务器的名称。</span><span class="sxs-lookup"><span data-stu-id="567c4-136">Specifies the name of the mail server.</span></span>  <br/> |
|[<span data-ttu-id="567c4-137">ServerDN （POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-137">ServerDN (POX)</span></span>](serverdn-pox.md) <br/> |<span data-ttu-id="567c4-138">指定 Exchange 服务器可分辨名称。</span><span class="sxs-lookup"><span data-stu-id="567c4-138">Specifies the Exchange Server distinguished name.</span></span>  <br/> |
|[<span data-ttu-id="567c4-139">ServerVersion （POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-139">ServerVersion (POX)</span></span>](serverversion-pox.md) <br/> |<span data-ttu-id="567c4-140">表示 Exchange Server 版本号。</span><span class="sxs-lookup"><span data-stu-id="567c4-140">Represents the Exchange Server version number.</span></span>  <br/> |
|[<span data-ttu-id="567c4-141">MdbDN （POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-141">MdbDN (POX)</span></span>](mdbdn-pox.md) <br/> |<span data-ttu-id="567c4-142">表示邮箱数据库的可分辨名称。</span><span class="sxs-lookup"><span data-stu-id="567c4-142">Represents the distinguished name of the mailbox database.</span></span>  <br/> |
|[<span data-ttu-id="567c4-143">PublicFolderServer （POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-143">PublicFolderServer (POX)</span></span>](publicfolderserver-pox.md) <br/> |<span data-ttu-id="567c4-144">包含用户的公用文件夹服务器的完全限定的域名（FQDN）。</span><span class="sxs-lookup"><span data-stu-id="567c4-144">Contains the fully-qualified domain name (FQDN) of the public folder server for the user.</span></span>  <br/> |
|[<span data-ttu-id="567c4-145">端口（POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-145">Port (POX)</span></span>](port-pox.md) <br/> |<span data-ttu-id="567c4-146">指定用于连接到存储区的端口。</span><span class="sxs-lookup"><span data-stu-id="567c4-146">Specifies the port that is used to connect to the store.</span></span>  <br/> |
|[<span data-ttu-id="567c4-147">DirectoryPort （POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-147">DirectoryPort (POX)</span></span>](directoryport-pox.md) <br/> |<span data-ttu-id="567c4-148">指定在使用名称服务提供程序接口（NSPI）协议时用于连接到目录的端口。</span><span class="sxs-lookup"><span data-stu-id="567c4-148">Specifies the port that is used to connect to the directory when the Name Service Provider Interface (NSPI) protocol is used.</span></span>  <br/> |
|[<span data-ttu-id="567c4-149">ReferralPort （POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-149">ReferralPort (POX)</span></span>](referralport-pox.md) <br/> |<span data-ttu-id="567c4-150">指定用于获取目录检索的端口。</span><span class="sxs-lookup"><span data-stu-id="567c4-150">Specifies the port that is used to get a referral to a directory.</span></span>  <br/> |
|[<span data-ttu-id="567c4-151">ASUrl （POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-151">ASUrl (POX)</span></span>](asurl-pox.md) <br/> |<span data-ttu-id="567c4-152">指定已启用邮件的用户的 Exchange Web 服务最佳实例的 URL。</span><span class="sxs-lookup"><span data-stu-id="567c4-152">Specifies the URL of the best instance of the Exchange Web Services for a mail-enabled user.</span></span>  <br/> |
|[<span data-ttu-id="567c4-153">Mailbox.ewsurl （POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-153">EwsUrl (POX)</span></span>](ewsurl-pox.md) <br/> |<span data-ttu-id="567c4-154">指定已启用邮件的用户的 Exchange Web 服务（EWS）的最佳终结点实例的 URL。</span><span class="sxs-lookup"><span data-stu-id="567c4-154">Specifies the URL of the best endpoint instance for Exchange Web Services (EWS) for a mail-enabled user.</span></span>  <br/> |
|[<span data-ttu-id="567c4-155">EmwsUrl （POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-155">EmwsUrl (POX)</span></span>](emwsurl-pox.md) <br/> |<span data-ttu-id="567c4-156">指定已启用邮件的用户的 Exchange Web 服务（EWS）的最佳终结点实例的 URL。</span><span class="sxs-lookup"><span data-stu-id="567c4-156">Specifies the URL of the best endpoint instance for Exchange Web Services (EWS) for a mail-enabled user.</span></span>  <br/> |
|[<span data-ttu-id="567c4-157">SharingUrl （POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-157">SharingUrl (POX)</span></span>](sharingurl-pox.md) <br/> |<span data-ttu-id="567c4-158">包含用于跨组织共享日历和联系人的共享服务器的 URL。</span><span class="sxs-lookup"><span data-stu-id="567c4-158">Contains the URL of the sharing server used for cross-organization sharing of calendars and contacts.</span></span>  <br/> |
|[<span data-ttu-id="567c4-159">EcpUrl （POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-159">EcpUrl (POX)</span></span>](ecpurl-pox.md) <br/> |<span data-ttu-id="567c4-160">指定已启用邮件的用户的 Exchange 控制面板的 URL。</span><span class="sxs-lookup"><span data-stu-id="567c4-160">Specifies the URL of the Exchange Control Panel for a mail-enabled user.</span></span>  <br/> |
|[<span data-ttu-id="567c4-161">EcpUrl-um （POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-161">EcpUrl-um (POX)</span></span>](ecpurl-um-pox.md) <br/> |<span data-ttu-id="567c4-162">指定可与[EcpUrl （POX）](ecpurl-pox.md)元素的值组合在一起的部分 url，以生成可用于访问启用邮件的用户的语音邮件设置的 URL。</span><span class="sxs-lookup"><span data-stu-id="567c4-162">Specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access voice mail settings for a mail-enabled user.</span></span>  <br/> |
|[<span data-ttu-id="567c4-163">EcpUrl-aggr （POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-163">EcpUrl-aggr (POX)</span></span>](ecpurl-aggr-pox.md) <br/> |<span data-ttu-id="567c4-164">指定可与[EcpUrl （POX）](ecpurl-pox.md)元素的值组合在一起的部分 url，以生成可用于访问启用邮件的用户的电子邮件聚合设置的 URL。</span><span class="sxs-lookup"><span data-stu-id="567c4-164">Specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access email aggregation settings for a mail-enabled user.</span></span>  <br/> |
|[<span data-ttu-id="567c4-165">EcpUrl-mt （POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-165">EcpUrl-mt (POX)</span></span>](ecpurl-mt-pox.md) <br/> |<span data-ttu-id="567c4-166">指定可与[EcpUrl （POX）](ecpurl-pox.md)元素的值结合使用的部分 url，以生成可用于访问启用邮件的用户的电子邮件跟踪设置的 URL。</span><span class="sxs-lookup"><span data-stu-id="567c4-166">Specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access email message tracking settings for a mail-enabled user.</span></span>  <br/> |
|[<span data-ttu-id="567c4-167">EcpUrl-ret （POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-167">EcpUrl-ret (POX)</span></span>](ecpurl-ret-pox.md) <br/> |<span data-ttu-id="567c4-168">指定可与[EcpUrl （POX）](ecpurl-pox.md)元素的值组合在一起的部分 url，以生成可用于访问启用邮件的用户的保留标记设置的 URL。</span><span class="sxs-lookup"><span data-stu-id="567c4-168">Specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access retention tag settings for a mail-enabled user.</span></span>  <br/> |
|[<span data-ttu-id="567c4-169">EcpUrl-sms （POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-169">EcpUrl-sms (POX)</span></span>](ecpurl-sms-pox.md) <br/> |<span data-ttu-id="567c4-170">指定可与[EcpUrl （POX）](ecpurl-pox.md)元素的值组合在一起的部分 url，以生成可用于为启用邮件的用户访问短信服务（SMS）设置的 URL。</span><span class="sxs-lookup"><span data-stu-id="567c4-170">Specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access Short Message Service (SMS) settings for a mail-enabled user.</span></span>  <br/> |
|[<span data-ttu-id="567c4-171">EcpUrl-发布（POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-171">EcpUrl-publish (POX)</span></span>](ecpurl-publish-pox.md) <br/> |<span data-ttu-id="567c4-172">指定可与[EcpUrl （POX）](ecpurl-pox.md)元素的值组合在一起的部分 url，以生成可用于访问启用邮件的用户的日历发布设置的 URL。</span><span class="sxs-lookup"><span data-stu-id="567c4-172">Specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access calendar publishing settings for a mail-enabled user.</span></span>  <br/> |
|[<span data-ttu-id="567c4-173">EcpUrl-photo （POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-173">EcpUrl-photo (POX)</span></span>](ecpurl-photo-pox.md) <br/> |<span data-ttu-id="567c4-174">指定可与[EcpUrl （POX）](ecpurl-pox.md)元素的值结合使用的部分 url，以生成可用于查看或更改已启用邮件的用户的当前照片的 URL。</span><span class="sxs-lookup"><span data-stu-id="567c4-174">Specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to view or change a mail-enabled user's current photo.</span></span>  <br/> |
|[<span data-ttu-id="567c4-175">EcpUrl-tm （POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-175">EcpUrl-tm (POX)</span></span>](ecpurl-tm-pox.md) <br/> |<span data-ttu-id="567c4-176">指定可与[EcpUrl （POX）](ecpurl-pox.md)元素的值结合使用的部分 url，以生成一个 url，该 url 可用于访问已启用邮件的用户当前为其成员的所有站点邮箱的列表。</span><span class="sxs-lookup"><span data-stu-id="567c4-176">Specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access a list of all site mailboxes of which a mail-enabled user is currently a member.</span></span>  <br/> |
|[<span data-ttu-id="567c4-177">EcpUrl-tmCreating （POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-177">EcpUrl-tmCreating (POX)</span></span>](ecpurl-tmcreating-pox.md) <br/> |<span data-ttu-id="567c4-178">指定可与[EcpUrl （POX）](ecpurl-pox.md)元素的值组合在一起以生成可用于创建新网站邮箱的 url 的部分 URL。</span><span class="sxs-lookup"><span data-stu-id="567c4-178">Specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to create a new site mailbox.</span></span>  <br/> |
|[<span data-ttu-id="567c4-179">EcpUrl-tmHiding （POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-179">EcpUrl-tmHiding (POX)</span></span>](ecpurl-tmhiding-pox.md) <br/> |<span data-ttu-id="567c4-180">指定可与[EcpUrl （POX）](ecpurl-pox.md)元素的值组合在一起的部分 url，以生成可用于从网站邮箱取消订阅用户的 URL。</span><span class="sxs-lookup"><span data-stu-id="567c4-180">Specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to unsubscribe the user from a site mailbox.</span></span>  <br/> |
|[<span data-ttu-id="567c4-181">EcpUrl-tmEditing （POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-181">EcpUrl-tmEditing (POX)</span></span>](ecpurl-tmediting-pox.md) <br/> |<span data-ttu-id="567c4-182">指定可与[EcpUrl （POX）](ecpurl-pox.md)元素的值组合在一起以生成可用于编辑现有网站邮箱的 url 的部分 url。</span><span class="sxs-lookup"><span data-stu-id="567c4-182">Specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to edit an existing site mailbox.</span></span>  <br/> |
|[<span data-ttu-id="567c4-183">EcpUrl-extinstall （POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-183">EcpUrl-extinstall (POX)</span></span>](ecpurl-extinstall-pox.md) <br/> |<span data-ttu-id="567c4-184">指定可与[EcpUrl （POX）](ecpurl-pox.md)元素的值组合在一起的部分 url，以生成可用于查看或更改当前安装在用户邮箱中的邮件应用程序的 url。</span><span class="sxs-lookup"><span data-stu-id="567c4-184">Specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to view or change the mail apps currently installed in the user's mailbox.</span></span>  <br/> |
|[<span data-ttu-id="567c4-185">OOFUrl （POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-185">OOFUrl (POX)</span></span>](oofurl-pox.md) <br/> |<span data-ttu-id="567c4-186">指定已启用邮件的用户的可用性服务的最佳实例的 URL。</span><span class="sxs-lookup"><span data-stu-id="567c4-186">Specifies the URL of the best instance of the Availability service for a mail-enabled user.</span></span>  <br/> |
|[<span data-ttu-id="567c4-187">OABUrl （POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-187">OABUrl (POX)</span></span>](oaburl-pox.md) <br/> |<span data-ttu-id="567c4-188">指定 Exchange 拓扑的脱机通讯簿配置服务器 URL。</span><span class="sxs-lookup"><span data-stu-id="567c4-188">Specifies the Offline Address Book configuration server URL for an Exchange topology.</span></span>  <br/> |
|[<span data-ttu-id="567c4-189">UMUrl （POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-189">UMUrl (POX)</span></span>](umurl-pox.md) <br/> |<span data-ttu-id="567c4-190">指定已启用邮件的用户的统一消息 Web 服务的最佳实例的 URL。</span><span class="sxs-lookup"><span data-stu-id="567c4-190">Specifies the URL of the best instance of the Unified Messaging Web service for a mail-enabled user.</span></span>  <br/> |
|[<span data-ttu-id="567c4-191">EwsPartnerUrl （POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-191">EwsPartnerUrl (POX)</span></span>](ewspartnerurl-pox.md) <br/> |<span data-ttu-id="567c4-192">指定已启用邮件的用户的 Exchange Web 服务（EWS）的最佳终结点实例的 URL。</span><span class="sxs-lookup"><span data-stu-id="567c4-192">Specifies the URL of the best endpoint instance for Exchange Web Services (EWS) for a mail-enabled user.</span></span>  <br/> |
|[<span data-ttu-id="567c4-193">Person.loginname （POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-193">LoginName (POX)</span></span>](loginname-pox.md) <br/> |<span data-ttu-id="567c4-194">指定用户的登录名。</span><span class="sxs-lookup"><span data-stu-id="567c4-194">Specifies the user's logon name.</span></span>  <br/> |
|[<span data-ttu-id="567c4-195">DomainRequired （POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-195">DomainRequired (POX)</span></span>](domainrequired-pox.md) <br/> |<span data-ttu-id="567c4-196">指示是否需要域进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="567c4-196">Indicates whether the domain is required for authentication.</span></span>  <br/> |
|[<span data-ttu-id="567c4-197">DomainName （POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-197">DomainName (POX)</span></span>](domainname-pox.md) <br/> |<span data-ttu-id="567c4-198">指定用户的域。</span><span class="sxs-lookup"><span data-stu-id="567c4-198">Specifies the user's domain.</span></span>  <br/> |
|[<span data-ttu-id="567c4-199">SPA （POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-199">SPA (POX)</span></span>](spa-pox.md) <br/> |<span data-ttu-id="567c4-200">指示是否需要安全密码身份验证。</span><span class="sxs-lookup"><span data-stu-id="567c4-200">Indicates whether secure password authentication is required.</span></span>  <br/> |
|[<span data-ttu-id="567c4-201">AuthPackage （POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-201">AuthPackage (POX)</span></span>](authpackage-pox.md) <br/> |<span data-ttu-id="567c4-202">指定在对安装了邮箱服务器角色的 Exchange 2007 计算机进行身份验证时使用的身份验证方案。</span><span class="sxs-lookup"><span data-stu-id="567c4-202">Specifies the authentication scheme that is used when authenticating against the Exchange 2007 computer that has the Mailbox server role installed.</span></span>  <br/> |
|[<span data-ttu-id="567c4-203">CertPrincipalName （POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-203">CertPrincipalName (POX)</span></span>](certprincipalname-pox.md) <br/> |<span data-ttu-id="567c4-204">指定使用 SSL 连接到 Microsoft Exchange 组织所需的安全套接字层（SSL）证书主体名称。</span><span class="sxs-lookup"><span data-stu-id="567c4-204">Specifies the Secure Sockets Layer (SSL) certificate principal name that is required to connect to the Microsoft Exchange organization by using SSL.</span></span>  <br/> |
|[<span data-ttu-id="567c4-205">SSL （POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-205">SSL (POX)</span></span>](ssl-pox.md) <br/> |<span data-ttu-id="567c4-206">指定是否需要安全登录。</span><span class="sxs-lookup"><span data-stu-id="567c4-206">Specifies whether secure logon is needed.</span></span>  <br/> |
|[<span data-ttu-id="567c4-207">Resolver.rst.authrequired （POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-207">AuthRequired (POX)</span></span>](authrequired-pox.md) <br/> |<span data-ttu-id="567c4-208">指定是否需要身份验证。</span><span class="sxs-lookup"><span data-stu-id="567c4-208">Specifies whether authentication is required.</span></span>  <br/> |
|[<span data-ttu-id="567c4-209">UsePOPAuth （POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-209">UsePOPAuth (POX)</span></span>](usepopauth-pox.md) <br/> |<span data-ttu-id="567c4-210">指示是否还将为 POP3 帐户类型提供的身份验证信息用于简单邮件传输协议（SMTP）。</span><span class="sxs-lookup"><span data-stu-id="567c4-210">Indicates whether the authentication information that is provided for a POP3 type of account is also used for Simple Mail Transfer Protocol (SMTP).</span></span>  <br/> |
|[<span data-ttu-id="567c4-211">SMTPLast （POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-211">SMTPLast (POX)</span></span>](smtplast-pox.md) <br/> |<span data-ttu-id="567c4-212">指定 SMTP 服务器是否要求先下载电子邮件，然后再使用 SMTP 服务器发送电子邮件。</span><span class="sxs-lookup"><span data-stu-id="567c4-212">Specifies whether the SMTP server requires that e-mail be downloaded before it sends e-mail by using the SMTP server.</span></span>  <br/> |
|[<span data-ttu-id="567c4-213">NetworkRequirements （POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-213">NetworkRequirements (POX)</span></span>](networkrequirements-pox.md) <br/> |<span data-ttu-id="567c4-214">包含用于确定客户端计算机是否位于满足 Internet 服务提供商要求以连接到服务器的网络上的条件。</span><span class="sxs-lookup"><span data-stu-id="567c4-214">Contains the criteria that are used to determine whether the client computer is on a network that meets the Internet Service Provider's requirements to connect to the server.</span></span>  <br/> |
|[<span data-ttu-id="567c4-215">AddressBook （POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-215">AddressBook (POX)</span></span>](addressbook-pox.md) <br/> |<span data-ttu-id="567c4-216">包含使用 MAPI/HTTP 协议将客户端连接到通讯簿服务器的规范。</span><span class="sxs-lookup"><span data-stu-id="567c4-216">Contains the specifications for connecting a client to the address book server by using the MAPI/HTTP protocol.</span></span> <span data-ttu-id="567c4-217">仅当**Protocol**元素的**Type**属性存在并将其设置为 "mapi" 时，才会出现此元素。</span><span class="sxs-lookup"><span data-stu-id="567c4-217">This element is only present if the **Type** attribute on the **Protocol** element is present and set to "mapiHttp".</span></span> <span data-ttu-id="567c4-218">**AddressBook**元素适用于实现 MAPI/HTTP 协议和目标 exchange Online 的客户端，以及从15.00.0847.032 开始的 exchange 版本。</span><span class="sxs-lookup"><span data-stu-id="567c4-218">The **AddressBook** element is applicable to clients that implement the MAPI/HTTP protocol and target Exchange Online and versions of Exchange starting with 15.00.0847.032.</span></span>  <br/> |
|[<span data-ttu-id="567c4-219">MailStore （POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-219">MailStore (POX)</span></span>](mailstore-pox.md) <br/> |<span data-ttu-id="567c4-220">包含使用 MAPI/HTTP 协议将客户端连接到用户邮箱的规范。</span><span class="sxs-lookup"><span data-stu-id="567c4-220">Contains the specifications for connecting a client to the user's mailbox by using the MAPI/HTTP protocol.</span></span> <span data-ttu-id="567c4-221">仅当**Protocol**元素的**Type**属性存在并将其设置为 "mapi" 时，才会出现此元素。</span><span class="sxs-lookup"><span data-stu-id="567c4-221">This element is only present if the **Type** attribute on the **Protocol** element is present and set to "mapiHttp".</span></span> <span data-ttu-id="567c4-222">**MailStore**元素适用于实现 MAPI/HTTP 协议和目标 exchange Online 的客户端，以及从15.00.0847.032 开始的 exchange 版本。</span><span class="sxs-lookup"><span data-stu-id="567c4-222">The **MailStore** element is applicable to clients that implement the MAPI/HTTP protocol and target Exchange Online and versions of Exchange starting with 15.00.0847.032.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="567c4-223">父元素</span><span class="sxs-lookup"><span data-stu-id="567c4-223">Parent elements</span></span>

|<span data-ttu-id="567c4-224">**元素**</span><span class="sxs-lookup"><span data-stu-id="567c4-224">**Element**</span></span>|<span data-ttu-id="567c4-225">**说明**</span><span class="sxs-lookup"><span data-stu-id="567c4-225">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="567c4-226">帐户（POX）</span><span class="sxs-lookup"><span data-stu-id="567c4-226">Account (POX)</span></span>](account-pox.md) <br/> |<span data-ttu-id="567c4-227">指定用户的帐户设置。</span><span class="sxs-lookup"><span data-stu-id="567c4-227">Specifies account settings for the user.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="567c4-228">备注</span><span class="sxs-lookup"><span data-stu-id="567c4-228">Remarks</span></span>

<span data-ttu-id="567c4-229">**Protocol**元素存在于响应中，该响应具有与**设置**相等的[操作（POX）](action-pox.md)值。</span><span class="sxs-lookup"><span data-stu-id="567c4-229">The **Protocol** element is present in a response that has an [Action (POX)](action-pox.md) value that is equal to **settings**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="567c4-230">另请参阅</span><span class="sxs-lookup"><span data-stu-id="567c4-230">See also</span></span>



[<span data-ttu-id="567c4-231">Exchange 的 POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="567c4-231">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

