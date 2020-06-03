---
title: GetDiscoverySearchConfiguration 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8a54a6dc-110c-4972-a8bc-5ddb43c4b857
description: 查找有关 GetDiscoverySearchConfiguration EWS 操作的信息。
ms.openlocfilehash: 4db435988a9954b921e7851986b6f92ffedbad94
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461021"
---
# <a name="getdiscoverysearchconfiguration-operation"></a><span data-ttu-id="ff262-103">GetDiscoverySearchConfiguration 操作</span><span class="sxs-lookup"><span data-stu-id="ff262-103">GetDiscoverySearchConfiguration operation</span></span>

<span data-ttu-id="ff262-104">查找有关**GetDiscoverySearchConfiguration** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="ff262-104">Find information about the **GetDiscoverySearchConfiguration** EWS operation.</span></span> 
  
<span data-ttu-id="ff262-105">**GetDiscoverySearchConfiguration**操作返回就地保留的配置信息、已保存的发现搜索以及为发现搜索启用的邮箱。</span><span class="sxs-lookup"><span data-stu-id="ff262-105">The **GetDiscoverySearchConfiguration** operation returns configuration information for in-place holds, saved discovery searches, and the mailboxes that are enabled for discovery search.</span></span> 
  
<span data-ttu-id="ff262-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="ff262-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getdiscoverysearchconfiguration-operation"></a><span data-ttu-id="ff262-107">使用 GetDiscoverySearchConfiguration 操作</span><span class="sxs-lookup"><span data-stu-id="ff262-107">Using the GetDiscoverySearchConfiguration operation</span></span>

<span data-ttu-id="ff262-108">**GetDiscoverySearchConfiguration**操作提供发现搜索的配置信息。</span><span class="sxs-lookup"><span data-stu-id="ff262-108">The **GetDiscoverySearchConfiguration** operation provides configuration information for discovery search.</span></span> <span data-ttu-id="ff262-109">请求可以包含以下一个或多个参数：</span><span class="sxs-lookup"><span data-stu-id="ff262-109">Requests can contain one or more of the following arguments:</span></span> 
  
1. <span data-ttu-id="ff262-110">[SearchId](searchid.md) —标识已保存的发现搜索。</span><span class="sxs-lookup"><span data-stu-id="ff262-110">[SearchId](searchid.md) — Identifies a saved discovery search.</span></span> <span data-ttu-id="ff262-111">如果在请求中发送此参数，则忽略其他参数的值。</span><span class="sxs-lookup"><span data-stu-id="ff262-111">If this argument is sent in the request, the values of the other arguments are ignored.</span></span> 
    
2. <span data-ttu-id="ff262-112">[ExpandGroupMembership](expandgroupmembership.md) —指示是否在响应中展开组成员资格。</span><span class="sxs-lookup"><span data-stu-id="ff262-112">[ExpandGroupMembership](expandgroupmembership.md) — Indicates whether group membership is expanded in the response.</span></span> <span data-ttu-id="ff262-113">值**为 true**表示组成员身份已展开，以便在响应中返回所有可搜索的邮箱。</span><span class="sxs-lookup"><span data-stu-id="ff262-113">A value of **true** indicates that group membership is expanded so that all searchable mailboxes are returned in the response.</span></span> <span data-ttu-id="ff262-114">**如果值为 false** ，则表示只在响应中返回组。</span><span class="sxs-lookup"><span data-stu-id="ff262-114">A value of **false** indicates that only the group is returned in the response.</span></span> 
    
3. <span data-ttu-id="ff262-115">[InPlaceHoldConfigurationOnly](inplaceholdconfigurationonly.md) —指示除了就地保留配置之外，是否还返回所有可搜索的邮箱。</span><span class="sxs-lookup"><span data-stu-id="ff262-115">[InPlaceHoldConfigurationOnly](inplaceholdconfigurationonly.md) — Indicates whether all searchable mailboxes are returned in addition to the in-place hold configuration.</span></span> <span data-ttu-id="ff262-116">**True**值表示仅返回就地保留配置。</span><span class="sxs-lookup"><span data-stu-id="ff262-116">A value of **true** indicates that only the in-place hold configurations are returned.</span></span> <span data-ttu-id="ff262-117">**如果值为 false** ，则表示除了就地保留标识符之外，还返回所有可搜索的邮箱标识符。</span><span class="sxs-lookup"><span data-stu-id="ff262-117">A value of **false** indicates that all searchable mailbox identifiers are returned in addition to the in-place hold identifiers.</span></span> <span data-ttu-id="ff262-118">如果此元素不存在，则默认行为等效于值**false**。</span><span class="sxs-lookup"><span data-stu-id="ff262-118">If this element is not present, the default behavior is the equivalent of the value **false**.</span></span> 
    
### <a name="getdiscoverysearchconfiguration-operation-soap-headers"></a><span data-ttu-id="ff262-119">GetDiscoverySearchConfiguration 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="ff262-119">GetDiscoverySearchConfiguration operation SOAP headers</span></span>

<span data-ttu-id="ff262-120">**GetDiscoverySearchConfiguration**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="ff262-120">The **GetDiscoverySearchConfiguration** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="ff262-121">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="ff262-121">**Header name**</span></span>|<span data-ttu-id="ff262-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="ff262-122">**Element**</span></span>|<span data-ttu-id="ff262-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="ff262-123">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ff262-124">**Get-managementrole**</span><span class="sxs-lookup"><span data-stu-id="ff262-124">**ManagementRole**</span></span> <br/> |[<span data-ttu-id="ff262-125">Get-managementrole</span><span class="sxs-lookup"><span data-stu-id="ff262-125">ManagementRole</span></span>](managementrole.md) <br/> |<span data-ttu-id="ff262-126">标识调用方发出请求所需的服务器角色。</span><span class="sxs-lookup"><span data-stu-id="ff262-126">Identifies the server roles that are necessary in order for the caller to make the request.</span></span> <span data-ttu-id="ff262-127">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="ff262-127">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="ff262-128">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="ff262-128">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="ff262-129">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="ff262-129">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="ff262-130">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="ff262-130">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="ff262-131">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="ff262-131">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="ff262-132">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="ff262-132">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="ff262-133">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="ff262-133">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="ff262-134">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="ff262-134">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="ff262-135">此标头适用于响应。</span><span class="sxs-lookup"><span data-stu-id="ff262-135">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getdiscoverysearchconfiguration-operation-request-example-get-the-discovery-search-configuration-for-a-saved-search"></a><span data-ttu-id="ff262-136">GetDiscoverySearchConfiguration 操作请求示例：获取保存的搜索的发现搜索配置</span><span class="sxs-lookup"><span data-stu-id="ff262-136">GetDiscoverySearchConfiguration operation request example: Get the discovery search configuration for a saved search</span></span>

<span data-ttu-id="ff262-137">以下示例的**GetDiscoverySearchConfiguration**操作请求显示如何请求配置名为 "MyDiscSearchFor-sbrown" 的已保存搜索。</span><span class="sxs-lookup"><span data-stu-id="ff262-137">The following example of a **GetDiscoverySearchConfiguration** operation request shows how to request the configuration of a saved search called "MyDiscSearchFor-sbrown".</span></span> <span data-ttu-id="ff262-138">[ExpandGroupMembership](expandgroupmembership.md)和[InPlaceHoldConfigurationOnly](inplaceholdconfigurationonly.md)元素的参数将被忽略。</span><span class="sxs-lookup"><span data-stu-id="ff262-138">The arguments for the [ExpandGroupMembership](expandgroupmembership.md) and [InPlaceHoldConfigurationOnly](inplaceholdconfigurationonly.md) elements are ignored.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:GetDiscoverySearchConfiguration>
         <m:SearchId>MyDiscSearchFor-sbrown</m:SearchId>
         <m:ExpandGroupMembership>true</m:ExpandGroupMembership>
         <m:InPlaceHoldConfigurationOnly>false</m:InPlaceHoldConfigurationOnly>
      </m:GetDiscoverySearchConfiguration>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="ff262-139">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="ff262-139">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="ff262-140">GetDiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff262-140">GetDiscoverySearchConfiguration</span></span>](getdiscoverysearchconfiguration.md)
    
- [<span data-ttu-id="ff262-141">SearchId</span><span class="sxs-lookup"><span data-stu-id="ff262-141">SearchId</span></span>](searchid.md)
    
- [<span data-ttu-id="ff262-142">ExpandGroupMembership</span><span class="sxs-lookup"><span data-stu-id="ff262-142">ExpandGroupMembership</span></span>](expandgroupmembership.md)
    
- [<span data-ttu-id="ff262-143">InPlaceHoldConfigurationOnly</span><span class="sxs-lookup"><span data-stu-id="ff262-143">InPlaceHoldConfigurationOnly</span></span>](inplaceholdconfigurationonly.md)
    
## <a name="successful-getdiscoverysearchconfiguration-operation-response-request-for-a-single-saved-search"></a><span data-ttu-id="ff262-144">成功的 GetDiscoverySearchConfiguration 操作响应：请求单个已保存的搜索</span><span class="sxs-lookup"><span data-stu-id="ff262-144">Successful GetDiscoverySearchConfiguration operation response: Request for a single saved search</span></span>

<span data-ttu-id="ff262-145">下面的示例演示对**GetDiscoverySearchConfiguration**操作请求的成功响应，以获取名为 "MyDiscSearchFor-sbrown" 的已保存搜索的配置。</span><span class="sxs-lookup"><span data-stu-id="ff262-145">The following example shows a successful response to a **GetDiscoverySearchConfiguration** operation request to get the configuration of a saved search called "MyDiscSearchFor-sbrown".</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="526" MinorBuildNumber="0" Version="Exchange2013" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetDiscoverySearchConfigurationResponse ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <DiscoverySearchConfigurations>
        <DiscoverySearchConfiguration xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <SearchId>MyDiscSearchFor-sbrown</SearchId>
          <SearchQuery>test item</SearchQuery>
          <SearchableMailboxes>
            <SearchableMailbox>
              <Guid>3c620d04-8b22-432e-92be-5b9321599576</Guid>
              <PrimarySmtpAddress>SBrown@contoso.com</PrimarySmtpAddress>
              <IsExternalMailbox>false</IsExternalMailbox>
              <ExternalEmailAddress/>
              <DisplayName>Steven Brown</DisplayName>
              <IsMembershipGroup>false</IsMembershipGroup>
              <ReferenceId>/o=First/ou=Exchange(FYDILT)/cn=Recipients/cn=313ecf-Steve</ReferenceId>
            </SearchableMailbox>
          </SearchableMailboxes>
        </DiscoverySearchConfiguration>
      </DiscoverySearchConfigurations>
    </GetDiscoverySearchConfigurationResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="ff262-146">响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="ff262-146">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="ff262-147">GetDiscoverySearchConfigurationResponse</span><span class="sxs-lookup"><span data-stu-id="ff262-147">GetDiscoverySearchConfigurationResponse</span></span>](getdiscoverysearchconfigurationresponse.md)
    
- [<span data-ttu-id="ff262-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ff262-148">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="ff262-149">DiscoverySearchConfigurations</span><span class="sxs-lookup"><span data-stu-id="ff262-149">DiscoverySearchConfigurations</span></span>](discoverysearchconfigurations.md)
    
- [<span data-ttu-id="ff262-150">DiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff262-150">DiscoverySearchConfiguration</span></span>](discoverysearchconfiguration.md)
    
- [<span data-ttu-id="ff262-151">SearchId</span><span class="sxs-lookup"><span data-stu-id="ff262-151">SearchId</span></span>](searchid.md)
    
- [<span data-ttu-id="ff262-152">SearchQuery</span><span class="sxs-lookup"><span data-stu-id="ff262-152">SearchQuery</span></span>](searchquery.md)
    
- [<span data-ttu-id="ff262-153">SearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="ff262-153">SearchableMailboxes</span></span>](searchablemailboxes.md)
    
- [<span data-ttu-id="ff262-154">SearchableMailbox</span><span class="sxs-lookup"><span data-stu-id="ff262-154">SearchableMailbox</span></span>](searchablemailbox.md)
    
- [<span data-ttu-id="ff262-155">Guid</span><span class="sxs-lookup"><span data-stu-id="ff262-155">Guid</span></span>](guid-ex15websvcsotherref.md)
    
- [<span data-ttu-id="ff262-156">PrimarySmtpAddress （字符串）</span><span class="sxs-lookup"><span data-stu-id="ff262-156">PrimarySmtpAddress (string)</span></span>](primarysmtpaddress-string.md)
    
- [<span data-ttu-id="ff262-157">IsExternalMailbox</span><span class="sxs-lookup"><span data-stu-id="ff262-157">IsExternalMailbox</span></span>](isexternalmailbox.md)
    
- [<span data-ttu-id="ff262-158">ExternalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="ff262-158">ExternalEmailAddress</span></span>](externalemailaddress.md)
    
- [<span data-ttu-id="ff262-159">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="ff262-159">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="ff262-160">IsMembershipGroup</span><span class="sxs-lookup"><span data-stu-id="ff262-160">IsMembershipGroup</span></span>](ismembershipgroup.md)
    
- [<span data-ttu-id="ff262-161">ReferenceId</span><span class="sxs-lookup"><span data-stu-id="ff262-161">ReferenceId</span></span>](referenceid.md)
    
## <a name="successful-getdiscoverysearchconfiguration-operation-response-request-for-in-place-holds"></a><span data-ttu-id="ff262-162">成功的 GetDiscoverySearchConfiguration 操作响应：就地保留请求</span><span class="sxs-lookup"><span data-stu-id="ff262-162">Successful GetDiscoverySearchConfiguration operation response: Request for in-place holds</span></span>

<span data-ttu-id="ff262-163">下面的示例演示对**GetDiscoverySearchConfiguration**操作请求的成功响应，仅获取就地保留。</span><span class="sxs-lookup"><span data-stu-id="ff262-163">The following example shows a successful response to a **GetDiscoverySearchConfiguration** operation request to only get in-place holds.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="526" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetDiscoverySearchConfigurationResponse ResponseClass="Success" 
                                               xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <DiscoverySearchConfigurations>
            <DiscoverySearchConfiguration xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <SearchId>MyDiscSearchFor-sbrown</SearchId>
               <SearchQuery>test item</SearchQuery>
               <InPlaceHoldIdentity>3f37d90f53144558a80814ef0272749a9</InPlaceHoldIdentity>
               <ManagedByOrganization/>
            </DiscoverySearchConfiguration>
            <DiscoverySearchConfiguration xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <SearchId>MyDiscSearch</SearchId>
               <SearchQuery>test</SearchQuery>
               <InPlaceHoldIdentity>6ea486f0f3f140efb044682a2e782abdf</InPlaceHoldIdentity>
               <ManagedByOrganization/>
            </DiscoverySearchConfiguration>
         </DiscoverySearchConfigurations>
      </GetDiscoverySearchConfigurationResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="ff262-164">响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="ff262-164">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="ff262-165">GetDiscoverySearchConfigurationResponse</span><span class="sxs-lookup"><span data-stu-id="ff262-165">GetDiscoverySearchConfigurationResponse</span></span>](getdiscoverysearchconfigurationresponse.md)
    
- [<span data-ttu-id="ff262-166">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ff262-166">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="ff262-167">DiscoverySearchConfigurations</span><span class="sxs-lookup"><span data-stu-id="ff262-167">DiscoverySearchConfigurations</span></span>](discoverysearchconfigurations.md)
    
- [<span data-ttu-id="ff262-168">DiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff262-168">DiscoverySearchConfiguration</span></span>](discoverysearchconfiguration.md)
    
- [<span data-ttu-id="ff262-169">SearchId</span><span class="sxs-lookup"><span data-stu-id="ff262-169">SearchId</span></span>](searchid.md)
    
- [<span data-ttu-id="ff262-170">SearchQuery</span><span class="sxs-lookup"><span data-stu-id="ff262-170">SearchQuery</span></span>](searchquery.md)
    
- [<span data-ttu-id="ff262-171">InPlaceHoldIdentity</span><span class="sxs-lookup"><span data-stu-id="ff262-171">InPlaceHoldIdentity</span></span>](inplaceholdidentity.md)
    
- [<span data-ttu-id="ff262-172">ManagedByOrganization</span><span class="sxs-lookup"><span data-stu-id="ff262-172">ManagedByOrganization</span></span>](managedbyorganization.md)
    
## <a name="successful-getdiscoverysearchconfiguration-operation-response-request-for-all-saved-discovery-search-configurations"></a><span data-ttu-id="ff262-173">成功的 GetDiscoverySearchConfiguration 操作响应：请求所有已保存的发现搜索配置</span><span class="sxs-lookup"><span data-stu-id="ff262-173">Successful GetDiscoverySearchConfiguration operation response: Request for all saved discovery search configurations</span></span>

<span data-ttu-id="ff262-174">下面的示例演示对**GetDiscoverySearchConfiguration**操作请求的成功响应，以获取所有已保存的发现搜索。</span><span class="sxs-lookup"><span data-stu-id="ff262-174">The following example shows a successful response to a **GetDiscoverySearchConfiguration** operation request to get all saved discovery searches.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="526" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetDiscoverySearchConfigurationResponse ResponseClass="Success" 
                                               xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <DiscoverySearchConfigurations>
            <DiscoverySearchConfiguration xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <SearchId>MyDiscSearchFor-sbrown</SearchId>
               <SearchQuery>test item</SearchQuery>
               <SearchableMailboxes>
                  <SearchableMailbox>
                     <Guid>3c620d04-8b33-435e-95be-5b9351599576</Guid>
                     <PrimarySmtpAddress>SBrown@contoso.com</PrimarySmtpAddress>
                     <IsExternalMailbox>false</IsExternalMailbox>
                     <ExternalEmailAddress/>
                     <DisplayName>Steven Brown</DisplayName>
                     <IsMembershipGroup>false</IsMembershipGroup>
                     <ReferenceId>/o=First/ou=Exchange (FYLT)/cn=Recipients/cn=35381a742f0e47e395c8601a60d13ecz-Steve</ReferenceId>
                  </SearchableMailbox>
               </SearchableMailboxes>
            </DiscoverySearchConfiguration>
            <DiscoverySearchConfiguration xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <SearchId>MyDiscSearch</SearchId>
               <SearchQuery>test</SearchQuery>
               <SearchableMailboxes>
                  <SearchableMailbox>
                     <Guid>e788c4b0-54a2-458c-83b2-22d5bb02b23f</Guid>
                     <PrimarySmtpAddress>Administrator@contoso.com</PrimarySmtpAddress>
                     <IsExternalMailbox>false</IsExternalMailbox>
                     <ExternalEmailAddress/>
                     <DisplayName>Administrator</DisplayName>
                     <IsMembershipGroup>false</IsMembershipGroup>
                     <ReferenceId>/o=First/ou=Exchange (FYLT)/cn=Recipients/cn=ebez7871332d4595abe1c62962911a58-Admin</ReferenceId>
                  </SearchableMailbox>
                  <SearchableMailbox>
                     <Guid>6f6cff39-8967-4a60-b43f-328413c25199</Guid>
                     <PrimarySmtpAddress>ADavis@contoso.com</PrimarySmtpAddress>
                     <IsExternalMailbox>false</IsExternalMailbox>
                     <ExternalEmailAddress/>
                     <DisplayName>Anthony Davis</DisplayName>
                     <IsMembershipGroup>false</IsMembershipGroup>
                     <ReferenceId>/o=First/ou=Exchange (FYLT)/cn=Recipients/cn=f10c9f70519844beb04101d8f40c572z-Antho</ReferenceId>
                  </SearchableMailbox>
               </SearchableMailboxes>
            </DiscoverySearchConfiguration>
         </DiscoverySearchConfigurations>
      </GetDiscoverySearchConfigurationResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="ff262-175">响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="ff262-175">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="ff262-176">GetDiscoverySearchConfigurationResponse</span><span class="sxs-lookup"><span data-stu-id="ff262-176">GetDiscoverySearchConfigurationResponse</span></span>](getdiscoverysearchconfigurationresponse.md)
    
- [<span data-ttu-id="ff262-177">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ff262-177">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="ff262-178">DiscoverySearchConfigurations</span><span class="sxs-lookup"><span data-stu-id="ff262-178">DiscoverySearchConfigurations</span></span>](discoverysearchconfigurations.md)
    
- [<span data-ttu-id="ff262-179">DiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff262-179">DiscoverySearchConfiguration</span></span>](discoverysearchconfiguration.md)
    
- [<span data-ttu-id="ff262-180">SearchId</span><span class="sxs-lookup"><span data-stu-id="ff262-180">SearchId</span></span>](searchid.md)
    
- [<span data-ttu-id="ff262-181">SearchQuery</span><span class="sxs-lookup"><span data-stu-id="ff262-181">SearchQuery</span></span>](searchquery.md)
    
- [<span data-ttu-id="ff262-182">SearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="ff262-182">SearchableMailboxes</span></span>](searchablemailboxes.md)
    
- [<span data-ttu-id="ff262-183">SearchableMailbox</span><span class="sxs-lookup"><span data-stu-id="ff262-183">SearchableMailbox</span></span>](searchablemailbox.md)
    
- [<span data-ttu-id="ff262-184">Guid</span><span class="sxs-lookup"><span data-stu-id="ff262-184">Guid</span></span>](guid-ex15websvcsotherref.md)
    
- [<span data-ttu-id="ff262-185">PrimarySmtpAddress （字符串）</span><span class="sxs-lookup"><span data-stu-id="ff262-185">PrimarySmtpAddress (string)</span></span>](primarysmtpaddress-string.md)
    
- [<span data-ttu-id="ff262-186">IsExternalMailbox</span><span class="sxs-lookup"><span data-stu-id="ff262-186">IsExternalMailbox</span></span>](isexternalmailbox.md)
    
- [<span data-ttu-id="ff262-187">ExternalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="ff262-187">ExternalEmailAddress</span></span>](externalemailaddress.md)
    
- [<span data-ttu-id="ff262-188">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="ff262-188">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="ff262-189">IsMembershipGroup</span><span class="sxs-lookup"><span data-stu-id="ff262-189">IsMembershipGroup</span></span>](ismembershipgroup.md)
    
- [<span data-ttu-id="ff262-190">ReferenceId</span><span class="sxs-lookup"><span data-stu-id="ff262-190">ReferenceId</span></span>](referenceid.md)
    
## <a name="getdiscoverysearchconfiguration-operation-error-response"></a><span data-ttu-id="ff262-191">GetDiscoverySearchConfiguration 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="ff262-191">GetDiscoverySearchConfiguration operation error response</span></span>

<span data-ttu-id="ff262-192">下面的示例演示对**GetDiscoverySearchConfiguration**操作请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="ff262-192">The following example shows an error response to a **GetDiscoverySearchConfiguration** operation request.</span></span> <span data-ttu-id="ff262-193">这是对获取在服务器上找不到的已保存搜索的请求的响应。</span><span class="sxs-lookup"><span data-stu-id="ff262-193">This is a response to a request to get a saved search that is not found on the server.</span></span> 
  
```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="526" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetDiscoverySearchConfigurationResponse ResponseClass="Error" 
                                               xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Search configuration corresponding to the search id was not found.</MessageText>
         <ResponseCode>ErrorInvalidArgument</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
         <DiscoverySearchConfigurations/>
      </GetDiscoverySearchConfigurationResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="ff262-194">错误响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="ff262-194">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="ff262-195">GetDiscoverySearchConfigurationResponse</span><span class="sxs-lookup"><span data-stu-id="ff262-195">GetDiscoverySearchConfigurationResponse</span></span>](getdiscoverysearchconfigurationresponse.md)
    
- [<span data-ttu-id="ff262-196">MessageText</span><span class="sxs-lookup"><span data-stu-id="ff262-196">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="ff262-197">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ff262-197">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="ff262-198">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="ff262-198">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="ff262-199">DiscoverySearchConfigurations</span><span class="sxs-lookup"><span data-stu-id="ff262-199">DiscoverySearchConfigurations</span></span>](discoverysearchconfigurations.md)
    
<span data-ttu-id="ff262-200">有关对 EWS 通用的其他错误代码以及特定于此操作的错误代码，请参阅[ResponseCode](responsecode.md)。</span><span class="sxs-lookup"><span data-stu-id="ff262-200">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ff262-201">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ff262-201">See also</span></span>

- [<span data-ttu-id="ff262-202">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="ff262-202">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="ff262-203">GetSearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="ff262-203">GetSearchableMailboxes</span></span>](getsearchablemailboxes.md)
    
- [<span data-ttu-id="ff262-204">SearchMailboxes</span><span class="sxs-lookup"><span data-stu-id="ff262-204">SearchMailboxes</span></span>](searchmailboxes.md)
    
- [<span data-ttu-id="ff262-205">GetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="ff262-205">GetHoldOnMailboxes</span></span>](getholdonmailboxes.md)
    
- [<span data-ttu-id="ff262-206">SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="ff262-206">SetHoldOnMailboxes</span></span>](setholdonmailboxes.md)
    
- [<span data-ttu-id="ff262-207">GetNonIndexableItemDetails</span><span class="sxs-lookup"><span data-stu-id="ff262-207">GetNonIndexableItemDetails</span></span>](getnonindexableitemdetails.md)
    
- [<span data-ttu-id="ff262-208">GetNonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="ff262-208">GetNonIndexableItemStatistics</span></span>](getnonindexableitemstatistics.md)
    

