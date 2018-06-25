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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826926"
---
# <a name="protocol-pox"></a><span data-ttu-id="4e963-103">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-103">Protocol (POX)</span></span>

<span data-ttu-id="4e963-104">**协议**元素包含客户端连接到运行 Exchange Server 已安装了客户端访问服务器角色的计算机的规格。</span><span class="sxs-lookup"><span data-stu-id="4e963-104">The **Protocol** element contains the specifications for connecting a client to the computer that is running Exchange Server that has the Client Access server role installed.</span></span> 
  
[<span data-ttu-id="4e963-105">自动发现 (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="4e963-106">响应 (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="4e963-107">帐户 (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="4e963-108">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-108">Protocol (POX)</span></span>](protocol-pox.md)
  
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

## <a name="attributes-and-elements"></a><span data-ttu-id="4e963-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4e963-109">Attributes and elements</span></span>

<span data-ttu-id="4e963-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4e963-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4e963-111">属性</span><span class="sxs-lookup"><span data-stu-id="4e963-111">Attributes</span></span>

|<span data-ttu-id="4e963-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="4e963-112">**Attribute**</span></span>|<span data-ttu-id="4e963-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="4e963-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4e963-114">类型</span><span class="sxs-lookup"><span data-stu-id="4e963-114">Type</span></span>  <br/> |<span data-ttu-id="4e963-115">指示此**协议**元素所述的协议类型。</span><span class="sxs-lookup"><span data-stu-id="4e963-115">Indicates the type of protocol described by this **Protocol** element.</span></span> <span data-ttu-id="4e963-116">唯一有效的值，此属性是"mapiHttp"。</span><span class="sxs-lookup"><span data-stu-id="4e963-116">The only valid value for this attribute is "mapiHttp".</span></span> <span data-ttu-id="4e963-117">此属性是仅存在如果自动发现请求的对应于此响应[包含 X MapiHttpCapability 标头](pox-autodiscover-request-for-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="4e963-117">This attribute is only present if the Autodiscover request that corresponds to this response [included an X-MapiHttpCapability header](pox-autodiscover-request-for-exchange.md).</span></span> <span data-ttu-id="4e963-118">此属性是适用于实现的 MAPI/HTTP 协议和目标 Exchange Online、 Exchange Online 作为 Office 365 的一部分的客户端或开头的 Exchange 内部部署版本生成 15.00.0847.032 (Exchange Server 2013 SP1)。</span><span class="sxs-lookup"><span data-stu-id="4e963-118">This attribute is applicable to clients that implement the MAPI/HTTP protocol and target Exchange Online, Exchange Online as part of Office 365, or on-premises versions of Exchange starting with build 15.00.0847.032 (Exchange Server 2013 SP1).</span></span>  <br/> |
|<span data-ttu-id="4e963-119">版本</span><span class="sxs-lookup"><span data-stu-id="4e963-119">Version</span></span>  <br/> |<span data-ttu-id="4e963-120">指示此**协议**元素所述的协议的版本。</span><span class="sxs-lookup"><span data-stu-id="4e963-120">Indicates the version of the protocol described by this **Protocol** element.</span></span> <span data-ttu-id="4e963-121">此属性仅有效值为"1"。</span><span class="sxs-lookup"><span data-stu-id="4e963-121">The only valid value for this attribute is "1".</span></span> <span data-ttu-id="4e963-122">此属性才存在，则自动发现请求对应于此响应包含**X MapiHttpCapability**标头。</span><span class="sxs-lookup"><span data-stu-id="4e963-122">This attribute is only present if the Autodiscover request that corresponds to this response included an **X-MapiHttpCapability** header.</span></span> <span data-ttu-id="4e963-123">此属性是适用于实现的 MAPI/HTTP 协议和目标 Exchange Online、 Exchange Online 作为 Office 365 的一部分的客户端或开头的 Exchange 内部部署版本生成 15.00.0847.032 (Exchange Server 2013 SP1)。</span><span class="sxs-lookup"><span data-stu-id="4e963-123">This attribute is applicable to clients that implement the MAPI/HTTP protocol and target Exchange Online, Exchange Online as part of Office 365, or on-premises versions of Exchange starting with build 15.00.0847.032 (Exchange Server 2013 SP1).</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4e963-124">子元素</span><span class="sxs-lookup"><span data-stu-id="4e963-124">Child elements</span></span>

|<span data-ttu-id="4e963-125">**元素**</span><span class="sxs-lookup"><span data-stu-id="4e963-125">**Element**</span></span>|<span data-ttu-id="4e963-126">**说明**</span><span class="sxs-lookup"><span data-stu-id="4e963-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4e963-127">类型 (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-127">Type (POX)</span></span>](type-pox.md) <br/> |<span data-ttu-id="4e963-128">标识配置的邮件帐户的类型。</span><span class="sxs-lookup"><span data-stu-id="4e963-128">Identifies the type of the configured mail account.</span></span>  <br/> |
|[<span data-ttu-id="4e963-129">内部 (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-129">Internal (POX)</span></span>](internal-pox.md) <br/> |<span data-ttu-id="4e963-130">包含客户端可以使用连接到从 Exchange 组织的网络内的 Url 的集合。</span><span class="sxs-lookup"><span data-stu-id="4e963-130">Contains a collection of URLs that a client can use to connect to Exchange from inside the organization's network.</span></span>  <br/> |
|[<span data-ttu-id="4e963-131">外部 (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-131">External (POX)</span></span>](external-pox.md) <br/> |<span data-ttu-id="4e963-132">包含客户端可以使用连接到从 Exchange 组织的网络之外的 Url 的集合。</span><span class="sxs-lookup"><span data-stu-id="4e963-132">Contains a collection of URLs that a client can use to connect to Exchange from outside of the organization's network.</span></span>  <br/> |
|[<span data-ttu-id="4e963-133">TTL (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-133">TTL (POX)</span></span>](ttl-pox.md) <br/> |<span data-ttu-id="4e963-134">指定的时间生存，以小时，在此期间设置一直保持有效。</span><span class="sxs-lookup"><span data-stu-id="4e963-134">Specifies the Time to Live, in hours, during which the settings remain valid.</span></span>  <br/> |
|[<span data-ttu-id="4e963-135">服务器 (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-135">Server (POX)</span></span>](server-pox.md) <br/> |<span data-ttu-id="4e963-136">指定的邮件服务器的名称。</span><span class="sxs-lookup"><span data-stu-id="4e963-136">Specifies the name of the mail server.</span></span>  <br/> |
|[<span data-ttu-id="4e963-137">ServerDN (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-137">ServerDN (POX)</span></span>](serverdn-pox.md) <br/> |<span data-ttu-id="4e963-138">指定 Exchange 服务器可分辨的名称。</span><span class="sxs-lookup"><span data-stu-id="4e963-138">Specifies the Exchange Server distinguished name.</span></span>  <br/> |
|[<span data-ttu-id="4e963-139">ServerVersion (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-139">ServerVersion (POX)</span></span>](serverversion-pox.md) <br/> |<span data-ttu-id="4e963-140">表示 Exchange Server 版本数。</span><span class="sxs-lookup"><span data-stu-id="4e963-140">Represents the Exchange Server version number.</span></span>  <br/> |
|[<span data-ttu-id="4e963-141">MdbDN (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-141">MdbDN (POX)</span></span>](mdbdn-pox.md) <br/> |<span data-ttu-id="4e963-142">表示的邮箱数据库的可分辨的名称。</span><span class="sxs-lookup"><span data-stu-id="4e963-142">Represents the distinguished name of the mailbox database.</span></span>  <br/> |
|[<span data-ttu-id="4e963-143">PublicFolderServer (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-143">PublicFolderServer (POX)</span></span>](publicfolderserver-pox.md) <br/> |<span data-ttu-id="4e963-144">包含的完全限定域名 (FQDN) 的公用文件夹服务器的用户。</span><span class="sxs-lookup"><span data-stu-id="4e963-144">Contains the fully-qualified domain name (FQDN) of the public folder server for the user.</span></span>  <br/> |
|[<span data-ttu-id="4e963-145">端口 (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-145">Port (POX)</span></span>](port-pox.md) <br/> |<span data-ttu-id="4e963-146">指定用于连接到存储的端口。</span><span class="sxs-lookup"><span data-stu-id="4e963-146">Specifies the port that is used to connect to the store.</span></span>  <br/> |
|[<span data-ttu-id="4e963-147">DirectoryPort (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-147">DirectoryPort (POX)</span></span>](directoryport-pox.md) <br/> |<span data-ttu-id="4e963-148">指定用于连接到目录时使用的名称服务提供程序界面 (NSPI) 协议的端口。</span><span class="sxs-lookup"><span data-stu-id="4e963-148">Specifies the port that is used to connect to the directory when the Name Service Provider Interface (NSPI) protocol is used.</span></span>  <br/> |
|[<span data-ttu-id="4e963-149">ReferralPort (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-149">ReferralPort (POX)</span></span>](referralport-pox.md) <br/> |<span data-ttu-id="4e963-150">指定用于获取目录引用的端口。</span><span class="sxs-lookup"><span data-stu-id="4e963-150">Specifies the port that is used to get a referral to a directory.</span></span>  <br/> |
|[<span data-ttu-id="4e963-151">ASUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-151">ASUrl (POX)</span></span>](asurl-pox.md) <br/> |<span data-ttu-id="4e963-152">指定已启用邮件的用户的 Exchange Web 服务的最佳实例的 URL。</span><span class="sxs-lookup"><span data-stu-id="4e963-152">Specifies the URL of the best instance of the Exchange Web Services for a mail-enabled user.</span></span>  <br/> |
|[<span data-ttu-id="4e963-153">EwsUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-153">EwsUrl (POX)</span></span>](ewsurl-pox.md) <br/> |<span data-ttu-id="4e963-154">指定已启用邮件的用户的最佳的终结点实例的 URL 为 Exchange Web 服务 (EWS)。</span><span class="sxs-lookup"><span data-stu-id="4e963-154">Specifies the URL of the best endpoint instance for Exchange Web Services (EWS) for a mail-enabled user.</span></span>  <br/> |
|[<span data-ttu-id="4e963-155">EmwsUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-155">EmwsUrl (POX)</span></span>](emwsurl-pox.md) <br/> |<span data-ttu-id="4e963-156">指定已启用邮件的用户的最佳的终结点实例的 URL 为 Exchange Web 服务 (EWS)。</span><span class="sxs-lookup"><span data-stu-id="4e963-156">Specifies the URL of the best endpoint instance for Exchange Web Services (EWS) for a mail-enabled user.</span></span>  <br/> |
|[<span data-ttu-id="4e963-157">SharingUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-157">SharingUrl (POX)</span></span>](sharingurl-pox.md) <br/> |<span data-ttu-id="4e963-158">包含用于跨组织共享日历和联系人信息的共享服务器的 URL。</span><span class="sxs-lookup"><span data-stu-id="4e963-158">Contains the URL of the sharing server used for cross-organization sharing of calendars and contacts.</span></span>  <br/> |
|[<span data-ttu-id="4e963-159">EcpUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-159">EcpUrl (POX)</span></span>](ecpurl-pox.md) <br/> |<span data-ttu-id="4e963-160">指定已启用邮件的用户的 Exchange 控制面板的 URL。</span><span class="sxs-lookup"><span data-stu-id="4e963-160">Specifies the URL of the Exchange Control Panel for a mail-enabled user.</span></span>  <br/> |
|[<span data-ttu-id="4e963-161">EcpUrl-um (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-161">EcpUrl-um (POX)</span></span>](ecpurl-um-pox.md) <br/> |<span data-ttu-id="4e963-162">指定可以结合使用[EcpUrl (POX)](ecpurl-pox.md)元素的值生成一个 URL，可用于访问已启用邮件的用户的语音邮件设置的部分 URL。</span><span class="sxs-lookup"><span data-stu-id="4e963-162">Specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access voice mail settings for a mail-enabled user.</span></span>  <br/> |
|[<span data-ttu-id="4e963-163">EcpUrl aggr (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-163">EcpUrl-aggr (POX)</span></span>](ecpurl-aggr-pox.md) <br/> |<span data-ttu-id="4e963-164">指定可以结合使用[EcpUrl (POX)](ecpurl-pox.md)元素的值生成一个 URL，可用于访问电子邮件的启用邮件的用户的聚合设置的部分 URL。</span><span class="sxs-lookup"><span data-stu-id="4e963-164">Specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access email aggregation settings for a mail-enabled user.</span></span>  <br/> |
|[<span data-ttu-id="4e963-165">EcpUrl 黑 (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-165">EcpUrl-mt (POX)</span></span>](ecpurl-mt-pox.md) <br/> |<span data-ttu-id="4e963-166">指定可以结合使用[EcpUrl (POX)](ecpurl-pox.md)元素的值生成一个 URL，可用于访问电子邮件跟踪已启用邮件的用户设置的部分 URL。</span><span class="sxs-lookup"><span data-stu-id="4e963-166">Specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access email message tracking settings for a mail-enabled user.</span></span>  <br/> |
|[<span data-ttu-id="4e963-167">EcpUrl 寄信人 (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-167">EcpUrl-ret (POX)</span></span>](ecpurl-ret-pox.md) <br/> |<span data-ttu-id="4e963-168">指定可以结合使用[EcpUrl (POX)](ecpurl-pox.md)元素的值生成一个 URL，可用于访问已启用邮件的用户的保留标记设置的部分 URL。</span><span class="sxs-lookup"><span data-stu-id="4e963-168">Specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access retention tag settings for a mail-enabled user.</span></span>  <br/> |
|[<span data-ttu-id="4e963-169">EcpUrl sms (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-169">EcpUrl-sms (POX)</span></span>](ecpurl-sms-pox.md) <br/> |<span data-ttu-id="4e963-170">指定可以结合使用[EcpUrl (POX)](ecpurl-pox.md)元素的值生成一个 URL，可用于访问已启用邮件的用户的短信服务 (SMS) 设置的部分 URL。</span><span class="sxs-lookup"><span data-stu-id="4e963-170">Specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access Short Message Service (SMS) settings for a mail-enabled user.</span></span>  <br/> |
|[<span data-ttu-id="4e963-171">EcpUrl 发布 (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-171">EcpUrl-publish (POX)</span></span>](ecpurl-publish-pox.md) <br/> |<span data-ttu-id="4e963-172">指定可以结合使用[EcpUrl (POX)](ecpurl-pox.md)元素的值生成一个 URL，可用于访问日历发布已启用邮件的用户设置的部分 URL。</span><span class="sxs-lookup"><span data-stu-id="4e963-172">Specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access calendar publishing settings for a mail-enabled user.</span></span>  <br/> |
|[<span data-ttu-id="4e963-173">EcpUrl 照片 (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-173">EcpUrl-photo (POX)</span></span>](ecpurl-photo-pox.md) <br/> |<span data-ttu-id="4e963-174">指定可以结合使用[EcpUrl (POX)](ecpurl-pox.md)元素的值生成一个 URL，可用于查看或更改已启用邮件的用户的当前照片的部分 URL。</span><span class="sxs-lookup"><span data-stu-id="4e963-174">Specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to view or change a mail-enabled user's current photo.</span></span>  <br/> |
|[<span data-ttu-id="4e963-175">EcpUrl tm (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-175">EcpUrl-tm (POX)</span></span>](ecpurl-tm-pox.md) <br/> |<span data-ttu-id="4e963-176">指定可以结合使用[EcpUrl (POX)](ecpurl-pox.md)元素的值生成一个可用于访问其中的所有站点邮箱的已启用邮件的用户是当前成员的列表的 URL 的部分 URL。</span><span class="sxs-lookup"><span data-stu-id="4e963-176">Specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access a list of all site mailboxes of which a mail-enabled user is currently a member.</span></span>  <br/> |
|[<span data-ttu-id="4e963-177">EcpUrl tmCreating (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-177">EcpUrl-tmCreating (POX)</span></span>](ecpurl-tmcreating-pox.md) <br/> |<span data-ttu-id="4e963-178">指定可以结合使用[EcpUrl (POX)](ecpurl-pox.md)元素的值生成一个 URL，可用于创建新的站点邮箱的部分 URL。</span><span class="sxs-lookup"><span data-stu-id="4e963-178">Specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to create a new site mailbox.</span></span>  <br/> |
|[<span data-ttu-id="4e963-179">EcpUrl tmHiding (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-179">EcpUrl-tmHiding (POX)</span></span>](ecpurl-tmhiding-pox.md) <br/> |<span data-ttu-id="4e963-180">指定可以结合使用[EcpUrl (POX)](ecpurl-pox.md)元素的值生成一个 URL，可用来取消订阅的站点邮箱用户的部分 URL。</span><span class="sxs-lookup"><span data-stu-id="4e963-180">Specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to unsubscribe the user from a site mailbox.</span></span>  <br/> |
|[<span data-ttu-id="4e963-181">EcpUrl tmEditing (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-181">EcpUrl-tmEditing (POX)</span></span>](ecpurl-tmediting-pox.md) <br/> |<span data-ttu-id="4e963-182">指定可以结合使用[EcpUrl (POX)](ecpurl-pox.md)元素的值生成一个 URL，可用于编辑现有的网站邮箱的部分 URL。</span><span class="sxs-lookup"><span data-stu-id="4e963-182">Specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to edit an existing site mailbox.</span></span>  <br/> |
|[<span data-ttu-id="4e963-183">EcpUrl extinstall (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-183">EcpUrl-extinstall (POX)</span></span>](ecpurl-extinstall-pox.md) <br/> |<span data-ttu-id="4e963-184">指定可以结合使用[EcpUrl (POX)](ecpurl-pox.md)元素的值生成一个可用于查看或更改当前用户的邮箱中安装邮件应用程序的 URL 的部分 URL。</span><span class="sxs-lookup"><span data-stu-id="4e963-184">Specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to view or change the mail apps currently installed in the user's mailbox.</span></span>  <br/> |
|[<span data-ttu-id="4e963-185">OOFUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-185">OOFUrl (POX)</span></span>](oofurl-pox.md) <br/> |<span data-ttu-id="4e963-186">指定已启用邮件的用户的可用性服务的最佳实例的 URL。</span><span class="sxs-lookup"><span data-stu-id="4e963-186">Specifies the URL of the best instance of the Availability service for a mail-enabled user.</span></span>  <br/> |
|[<span data-ttu-id="4e963-187">OABUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-187">OABUrl (POX)</span></span>](oaburl-pox.md) <br/> |<span data-ttu-id="4e963-188">指定 Exchange 拓扑的脱机通讯簿配置服务器 URL。</span><span class="sxs-lookup"><span data-stu-id="4e963-188">Specifies the Offline Address Book configuration server URL for an Exchange topology.</span></span>  <br/> |
|[<span data-ttu-id="4e963-189">UMUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-189">UMUrl (POX)</span></span>](umurl-pox.md) <br/> |<span data-ttu-id="4e963-190">指定已启用邮件的用户的统一消息 Web 服务的最佳实例的 URL。</span><span class="sxs-lookup"><span data-stu-id="4e963-190">Specifies the URL of the best instance of the Unified Messaging Web service for a mail-enabled user.</span></span>  <br/> |
|[<span data-ttu-id="4e963-191">EwsPartnerUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-191">EwsPartnerUrl (POX)</span></span>](ewspartnerurl-pox.md) <br/> |<span data-ttu-id="4e963-192">指定已启用邮件的用户的最佳的终结点实例的 URL 为 Exchange Web 服务 (EWS)。</span><span class="sxs-lookup"><span data-stu-id="4e963-192">Specifies the URL of the best endpoint instance for Exchange Web Services (EWS) for a mail-enabled user.</span></span>  <br/> |
|[<span data-ttu-id="4e963-193">使用 LoginName (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-193">LoginName (POX)</span></span>](loginname-pox.md) <br/> |<span data-ttu-id="4e963-194">指定用户的登录名。</span><span class="sxs-lookup"><span data-stu-id="4e963-194">Specifies the user's logon name.</span></span>  <br/> |
|[<span data-ttu-id="4e963-195">DomainRequired (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-195">DomainRequired (POX)</span></span>](domainrequired-pox.md) <br/> |<span data-ttu-id="4e963-196">指示是否需要身份验证的域。</span><span class="sxs-lookup"><span data-stu-id="4e963-196">Indicates whether the domain is required for authentication.</span></span>  <br/> |
|[<span data-ttu-id="4e963-197">DomainName (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-197">DomainName (POX)</span></span>](domainname-pox.md) <br/> |<span data-ttu-id="4e963-198">指定用户的域。</span><span class="sxs-lookup"><span data-stu-id="4e963-198">Specifies the user's domain.</span></span>  <br/> |
|[<span data-ttu-id="4e963-199">SPA (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-199">SPA (POX)</span></span>](spa-pox.md) <br/> |<span data-ttu-id="4e963-200">指示是否需要安全密码身份验证。</span><span class="sxs-lookup"><span data-stu-id="4e963-200">Indicates whether secure password authentication is required.</span></span>  <br/> |
|[<span data-ttu-id="4e963-201">AuthPackage (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-201">AuthPackage (POX)</span></span>](authpackage-pox.md) <br/> |<span data-ttu-id="4e963-202">指定对已安装了邮箱服务器角色的 Exchange 2007 计算机时所使用的身份验证方案。</span><span class="sxs-lookup"><span data-stu-id="4e963-202">Specifies the authentication scheme that is used when authenticating against the Exchange 2007 computer that has the Mailbox server role installed.</span></span>  <br/> |
|[<span data-ttu-id="4e963-203">CertPrincipalName (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-203">CertPrincipalName (POX)</span></span>](certprincipalname-pox.md) <br/> |<span data-ttu-id="4e963-204">指定需要使用 SSL 连接到 Microsoft Exchange 组织的安全套接字层 (SSL) 证书主体名称。</span><span class="sxs-lookup"><span data-stu-id="4e963-204">Specifies the Secure Sockets Layer (SSL) certificate principal name that is required to connect to the Microsoft Exchange organization by using SSL.</span></span>  <br/> |
|[<span data-ttu-id="4e963-205">SSL (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-205">SSL (POX)</span></span>](ssl-pox.md) <br/> |<span data-ttu-id="4e963-206">指定是否需要安全登录。</span><span class="sxs-lookup"><span data-stu-id="4e963-206">Specifies whether secure logon is needed.</span></span>  <br/> |
|[<span data-ttu-id="4e963-207">AuthRequired (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-207">AuthRequired (POX)</span></span>](authrequired-pox.md) <br/> |<span data-ttu-id="4e963-208">指定是否需要身份验证。</span><span class="sxs-lookup"><span data-stu-id="4e963-208">Specifies whether authentication is required.</span></span>  <br/> |
|[<span data-ttu-id="4e963-209">UsePOPAuth (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-209">UsePOPAuth (POX)</span></span>](usepopauth-pox.md) <br/> |<span data-ttu-id="4e963-210">指示是否提供 POP3 类型的帐户的身份验证信息也使用的简单邮件传输协议 (SMTP)。</span><span class="sxs-lookup"><span data-stu-id="4e963-210">Indicates whether the authentication information that is provided for a POP3 type of account is also used for Simple Mail Transfer Protocol (SMTP).</span></span>  <br/> |
|[<span data-ttu-id="4e963-211">SMTPLast (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-211">SMTPLast (POX)</span></span>](smtplast-pox.md) <br/> |<span data-ttu-id="4e963-212">指定的 SMTP 服务器是否需要使用 SMTP 服务器发送电子邮件之前下载的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="4e963-212">Specifies whether the SMTP server requires that e-mail be downloaded before it sends e-mail by using the SMTP server.</span></span>  <br/> |
|[<span data-ttu-id="4e963-213">NetworkRequirements (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-213">NetworkRequirements (POX)</span></span>](networkrequirements-pox.md) <br/> |<span data-ttu-id="4e963-214">包含用于确定客户端计算机是否满足 Internet 服务提供商的要求，以连接到服务器的网络上的条件。</span><span class="sxs-lookup"><span data-stu-id="4e963-214">Contains the criteria that are used to determine whether the client computer is on a network that meets the Internet Service Provider's requirements to connect to the server.</span></span>  <br/> |
|[<span data-ttu-id="4e963-215">通讯簿 (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-215">AddressBook (POX)</span></span>](addressbook-pox.md) <br/> |<span data-ttu-id="4e963-216">包含使用 MAPI/HTTP 协议客户端连接到通讯簿服务器的规范。</span><span class="sxs-lookup"><span data-stu-id="4e963-216">Contains the specifications for connecting a client to the address book server by using the MAPI/HTTP protocol.</span></span> <span data-ttu-id="4e963-217">此元素是仅存在**协议**元素的**Type**属性是否存在并将设置为"mapiHttp"。</span><span class="sxs-lookup"><span data-stu-id="4e963-217">This element is only present if the **Type** attribute on the **Protocol** element is present and set to "mapiHttp".</span></span> <span data-ttu-id="4e963-218">适用于实现的 MAPI/HTTP 协议和目标 Exchange Online 和 Exchange 开头 15.00.0847.032 版本的客户端的**通讯簿**元素。</span><span class="sxs-lookup"><span data-stu-id="4e963-218">The **AddressBook** element is applicable to clients that implement the MAPI/HTTP protocol and target Exchange Online and versions of Exchange starting with 15.00.0847.032.</span></span>  <br/> |
|[<span data-ttu-id="4e963-219">MailStore (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-219">MailStore (POX)</span></span>](mailstore-pox.md) <br/> |<span data-ttu-id="4e963-220">包含使用 MAPI/HTTP 协议来连接到用户邮箱的客户端的规范。</span><span class="sxs-lookup"><span data-stu-id="4e963-220">Contains the specifications for connecting a client to the user's mailbox by using the MAPI/HTTP protocol.</span></span> <span data-ttu-id="4e963-221">此元素是仅存在**协议**元素的**Type**属性是否存在并将设置为"mapiHttp"。</span><span class="sxs-lookup"><span data-stu-id="4e963-221">This element is only present if the **Type** attribute on the **Protocol** element is present and set to "mapiHttp".</span></span> <span data-ttu-id="4e963-222">适用于客户端实现的 MAPI/HTTP 协议和 Exchange Online 的目标和版本的 Exchange 开头 15.00.0847.032 **MailStore**元素。</span><span class="sxs-lookup"><span data-stu-id="4e963-222">The **MailStore** element is applicable to clients that implement the MAPI/HTTP protocol and target Exchange Online and versions of Exchange starting with 15.00.0847.032.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4e963-223">父元素</span><span class="sxs-lookup"><span data-stu-id="4e963-223">Parent elements</span></span>

|<span data-ttu-id="4e963-224">**元素**</span><span class="sxs-lookup"><span data-stu-id="4e963-224">**Element**</span></span>|<span data-ttu-id="4e963-225">**说明**</span><span class="sxs-lookup"><span data-stu-id="4e963-225">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4e963-226">帐户 (POX)</span><span class="sxs-lookup"><span data-stu-id="4e963-226">Account (POX)</span></span>](account-pox.md) <br/> |<span data-ttu-id="4e963-227">指定用户帐户的设置。</span><span class="sxs-lookup"><span data-stu-id="4e963-227">Specifies account settings for the user.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4e963-228">注解</span><span class="sxs-lookup"><span data-stu-id="4e963-228">Remarks</span></span>

<span data-ttu-id="4e963-229">其[操作 (POX)](action-pox.md)值，它等于**设置**的响应中存在**协议**元素。</span><span class="sxs-lookup"><span data-stu-id="4e963-229">The **Protocol** element is present in a response that has an [Action (POX)](action-pox.md) value that is equal to **settings**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4e963-230">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4e963-230">See also</span></span>



[<span data-ttu-id="4e963-231">Exchange POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="4e963-231">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

