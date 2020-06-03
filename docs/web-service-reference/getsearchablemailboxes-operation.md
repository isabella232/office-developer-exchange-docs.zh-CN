---
title: GetSearchableMailboxes 操作
manager: sethgros
ms.date: 01/24/2020
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 47f8ff57-4835-4d2d-9136-44afb31a4cbe
description: 查找有关 GetSearchableMailboxes EWS 操作的信息。
ms.openlocfilehash: e893a66eb1b638479eeccc6bd7548cb020f37243
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530837"
---
# <a name="getsearchablemailboxes-operation"></a><span data-ttu-id="7a2c5-103">GetSearchableMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="7a2c5-103">GetSearchableMailboxes operation</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7a2c5-104">从2020年4月1日起，GetSearchableMailboxes 操作将不再在 Exchange Online 中可用。</span><span class="sxs-lookup"><span data-stu-id="7a2c5-104">Starting on April 1, 2020, the GetSearchableMailboxes operation will no longer be available in Exchange Online.</span></span> <span data-ttu-id="7a2c5-105">此操作不会受到 Exchange Server 内部部署版本的影响。</span><span class="sxs-lookup"><span data-stu-id="7a2c5-105">This operation won't be affected in on-premises versions of Exchange Server.</span></span> <span data-ttu-id="7a2c5-106">有关详细信息，请参阅[在 Exchange Online 中停用旧版电子数据展示工具](https://docs.microsoft.com/microsoft-365/compliance/legacy-ediscovery-retirement#getsearchablemailboxes-setholdonmailboxes-and-getholdonmailboxes-operations-in-the-ews-api)。</span><span class="sxs-lookup"><span data-stu-id="7a2c5-106">For more information, see [Retirement of legacy eDiscovery tools in Exchange Online](https://docs.microsoft.com/microsoft-365/compliance/legacy-ediscovery-retirement#getsearchablemailboxes-setholdonmailboxes-and-getholdonmailboxes-operations-in-the-ews-api).</span></span>

<span data-ttu-id="7a2c5-107">查找有关**GetSearchableMailboxes** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="7a2c5-107">Find information about the **GetSearchableMailboxes** EWS operation.</span></span> 
  
<span data-ttu-id="7a2c5-108">**GetSearchableMailboxes**操作获取用于发现搜索的可搜索邮箱的范围集合。</span><span class="sxs-lookup"><span data-stu-id="7a2c5-108">The **GetSearchableMailboxes** operation gets a scoped set of searchable mailboxes for discovery searches.</span></span> <span data-ttu-id="7a2c5-109">响应中返回的可搜索邮箱的范围由搜索筛选器和是否扩展通讯组成员资格决定。</span><span class="sxs-lookup"><span data-stu-id="7a2c5-109">The scope of searchable mailboxes returned in the response is determined by the search filter and whether distribution group membership is expanded.</span></span> 

> [!NOTE] 
> <span data-ttu-id="7a2c5-110">此操作旨在用于搜索筛选器，并仅检索前几千位;它并不用于详尽的检索。</span><span class="sxs-lookup"><span data-stu-id="7a2c5-110">This operation is intended to be used with the search filter and to retrieve only the first few thousands; it's not intended for exhaustive retrieval.</span></span>
  
<span data-ttu-id="7a2c5-111">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="7a2c5-111">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getsearchablemailboxes-operation"></a><span data-ttu-id="7a2c5-112">使用 GetSearchableMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="7a2c5-112">Using the GetSearchableMailboxes operation</span></span>

<span data-ttu-id="7a2c5-113">**GetSearchableMailboxes**操作获取有关可搜索邮箱的信息。</span><span class="sxs-lookup"><span data-stu-id="7a2c5-113">The **GetSearchableMailboxes** operation gets information about searchable mailboxes.</span></span> <span data-ttu-id="7a2c5-114">可以在请求中传递以下参数：</span><span class="sxs-lookup"><span data-stu-id="7a2c5-114">The following arguments can be passed in the request:</span></span> 
  
- <span data-ttu-id="7a2c5-115">[过滤](searchfilter.md)-接受一个电子邮件别名作为参数。</span><span class="sxs-lookup"><span data-stu-id="7a2c5-115">[SearchFilter](searchfilter.md) - Accepts a single email alias as an argument.</span></span> 
    
- <span data-ttu-id="7a2c5-116">[ExpandGroupMembership](expandgroupmembership.md) -指示是否在响应中返回的结果中扩展通讯组成员资格。</span><span class="sxs-lookup"><span data-stu-id="7a2c5-116">[ExpandGroupMembership](expandgroupmembership.md) - Indicates whether the distribution group membership is expanded in the results returned in the response.</span></span> 
    
<span data-ttu-id="7a2c5-117">如果搜索筛选器中设置的电子邮件别名是通讯组，且通讯组成员身份未扩展，则响应将包含通讯组的邮箱信息。</span><span class="sxs-lookup"><span data-stu-id="7a2c5-117">If the email alias set in the search filter is a distribution group and the distribution group membership is not expanded, the response will contain the mailbox information for the distribution group.</span></span> <span data-ttu-id="7a2c5-118">如果搜索筛选器中设置的电子邮件别名是通讯组，并且展开了通讯组成员身份，则响应将包含作为通讯组成员的每个邮箱的邮箱信息。</span><span class="sxs-lookup"><span data-stu-id="7a2c5-118">If the email alias set in the search filter is a distribution group and the distribution group membership is expanded, the response will contain the mailbox information for each mailbox that is a member of the distribution group.</span></span> <span data-ttu-id="7a2c5-119">如果搜索筛选器包含单个用户的别名，则响应将包含单个用户的邮箱信息。</span><span class="sxs-lookup"><span data-stu-id="7a2c5-119">If the search filter contains a single user's alias, the response will contain the mailbox information for the single user.</span></span> <span data-ttu-id="7a2c5-120">如果[GetSearchableMailboxes](getsearchablemailboxes.md)元素为空，则响应将包含所有可搜索的邮箱。</span><span class="sxs-lookup"><span data-stu-id="7a2c5-120">The response will contain all searchable mailboxes if the [GetSearchableMailboxes](getsearchablemailboxes.md) element is empty.</span></span> <span data-ttu-id="7a2c5-121">这与将空的[过滤](searchfilter.md)元素和[ExpandGroupMembership](expandgroupmembership.md)元素设置为**false**相同。</span><span class="sxs-lookup"><span data-stu-id="7a2c5-121">This is the same as having an empty [SearchFilter](searchfilter.md) element and the [ExpandGroupMembership](expandgroupmembership.md) element set to **false**.</span></span>
  
### <a name="getsearchablemailboxes-operation-soap-headers"></a><span data-ttu-id="7a2c5-122">GetSearchableMailboxes 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="7a2c5-122">GetSearchableMailboxes operation SOAP headers</span></span>

<span data-ttu-id="7a2c5-123">**GetSearchableMailboxes**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="7a2c5-123">The **GetSearchableMailboxes** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="7a2c5-124">头名称</span><span class="sxs-lookup"><span data-stu-id="7a2c5-124">Header name</span></span>|<span data-ttu-id="7a2c5-125">元素</span><span class="sxs-lookup"><span data-stu-id="7a2c5-125">Element</span></span>|<span data-ttu-id="7a2c5-126">说明</span><span class="sxs-lookup"><span data-stu-id="7a2c5-126">Description</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7a2c5-127">**Get-managementrole**</span><span class="sxs-lookup"><span data-stu-id="7a2c5-127">**ManagementRole**</span></span> <br/> |[<span data-ttu-id="7a2c5-128">Get-managementrole</span><span class="sxs-lookup"><span data-stu-id="7a2c5-128">ManagementRole</span></span>](managementrole.md) <br/> |<span data-ttu-id="7a2c5-129">标识调用方发出请求所需的服务器角色。</span><span class="sxs-lookup"><span data-stu-id="7a2c5-129">Identifies the server roles that are necessary in order for the caller to make the request.</span></span> <span data-ttu-id="7a2c5-130">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="7a2c5-130">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="7a2c5-131">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="7a2c5-131">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="7a2c5-132">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="7a2c5-132">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="7a2c5-133">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="7a2c5-133">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="7a2c5-134">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="7a2c5-134">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="7a2c5-135">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="7a2c5-135">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="7a2c5-136">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="7a2c5-136">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="7a2c5-137">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="7a2c5-137">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="7a2c5-138">此标头适用于响应。</span><span class="sxs-lookup"><span data-stu-id="7a2c5-138">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getsearchablemailboxes-operation-request-example-request-information-about-a-distribution-group"></a><span data-ttu-id="7a2c5-139">GetSearchableMailboxes 操作请求示例：请求有关通讯组的信息</span><span class="sxs-lookup"><span data-stu-id="7a2c5-139">GetSearchableMailboxes operation request example: Request information about a distribution group</span></span>

<span data-ttu-id="7a2c5-140">以下示例的**GetSearchableMailboxes**操作请求显示如何获取 lolgroup 通讯组的邮箱信息。</span><span class="sxs-lookup"><span data-stu-id="7a2c5-140">The following example of a **GetSearchableMailboxes** operation request shows how to get the mailbox information for the lolgroup distribution group.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:GetSearchableMailboxes>
         <m:SearchFilter>lolgroup</m:SearchFilter>
         <m:ExpandGroupMembership>false</m:ExpandGroupMembership>
      </m:GetSearchableMailboxes>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="7a2c5-141">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="7a2c5-141">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="7a2c5-142">GetSearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="7a2c5-142">GetSearchableMailboxes</span></span>](getsearchablemailboxes.md)   
- [<span data-ttu-id="7a2c5-143">过滤</span><span class="sxs-lookup"><span data-stu-id="7a2c5-143">SearchFilter</span></span>](searchfilter.md)    
- [<span data-ttu-id="7a2c5-144">ExpandGroupMembership</span><span class="sxs-lookup"><span data-stu-id="7a2c5-144">ExpandGroupMembership</span></span>](expandgroupmembership.md)
    
## <a name="successful-getsearchablemailboxes-operation-response-get-information-about-a-distribution-group"></a><span data-ttu-id="7a2c5-145">成功的 GetSearchableMailboxes 操作响应：获取有关通讯组的信息</span><span class="sxs-lookup"><span data-stu-id="7a2c5-145">Successful GetSearchableMailboxes operation response: Get information about a distribution group</span></span>

<span data-ttu-id="7a2c5-146">下面的示例演示对**GetSearchableMailboxes**操作请求的成功响应，以获取 lolgroup 通讯组的发现信息。</span><span class="sxs-lookup"><span data-stu-id="7a2c5-146">The following example shows a successful response to a **GetSearchableMailboxes** operation request to get the discovery information for the lolgroup distribution group.</span></span> 
  
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
      <GetSearchableMailboxesResponse ResponseClass="Success" 
                                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <SearchableMailboxes>
            <SearchableMailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <Guid>33a408fe-2574-4e3b-49f5-5e1e000a3035</Guid>
               <PrimarySmtpAddress>LOLgroup@contoso.com</PrimarySmtpAddress>
               <IsExternalMailbox>false</IsExternalMailbox>
               <ExternalEmailAddress/>
               <DisplayName>LOLgroup</DisplayName>
               <IsMembershipGroup>true</IsMembershipGroup>
               <ReferenceId>/o=First/ou=Exchange(FYLT)/cn=Recipients/cn=81213b958a0b5295b13b3f02b812bf1bc-LOLgroup</ReferenceId>
            </SearchableMailbox>
         </SearchableMailboxes>
      </GetSearchableMailboxesResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="7a2c5-147">响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="7a2c5-147">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="7a2c5-148">GetSearchableMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="7a2c5-148">GetSearchableMailboxesResponse</span></span>](getsearchablemailboxesresponse.md)   
- [<span data-ttu-id="7a2c5-149">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="7a2c5-149">ResponseCode</span></span>](responsecode.md)   
- [<span data-ttu-id="7a2c5-150">SearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="7a2c5-150">SearchableMailboxes</span></span>](searchablemailboxes.md)    
- [<span data-ttu-id="7a2c5-151">SearchableMailbox</span><span class="sxs-lookup"><span data-stu-id="7a2c5-151">SearchableMailbox</span></span>](searchablemailbox.md)    
- [<span data-ttu-id="7a2c5-152">Guid</span><span class="sxs-lookup"><span data-stu-id="7a2c5-152">Guid</span></span>](guid-ex15websvcsotherref.md)    
- [<span data-ttu-id="7a2c5-153">PrimarySmtpAddress</span><span class="sxs-lookup"><span data-stu-id="7a2c5-153">PrimarySmtpAddress</span></span>](primarysmtpaddress.md)    
- [<span data-ttu-id="7a2c5-154">IsExternalMailbox</span><span class="sxs-lookup"><span data-stu-id="7a2c5-154">IsExternalMailbox</span></span>](isexternalmailbox.md)   
- [<span data-ttu-id="7a2c5-155">ExternalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="7a2c5-155">ExternalEmailAddress</span></span>](externalemailaddress.md)    
- [<span data-ttu-id="7a2c5-156">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="7a2c5-156">DisplayName (string)</span></span>](displayname-string.md)    
- [<span data-ttu-id="7a2c5-157">IsMembershipGroup</span><span class="sxs-lookup"><span data-stu-id="7a2c5-157">IsMembershipGroup</span></span>](ismembershipgroup.md)    
- [<span data-ttu-id="7a2c5-158">ReferenceId</span><span class="sxs-lookup"><span data-stu-id="7a2c5-158">ReferenceId</span></span>](referenceid.md)
    
## <a name="successful-getsearchablemailboxes-operation-response-get-information-about-an-expanded-distribution-group"></a><span data-ttu-id="7a2c5-159">成功的 GetSearchableMailboxes 操作响应：获取有关展开的通讯组的信息</span><span class="sxs-lookup"><span data-stu-id="7a2c5-159">Successful GetSearchableMailboxes operation response: Get information about an expanded distribution group</span></span>

<span data-ttu-id="7a2c5-160">下面的示例演示对**GetSearchableMailboxes**操作请求的成功响应，以获取有关已展开的 lolgroup 通讯组的成员的发现信息。</span><span class="sxs-lookup"><span data-stu-id="7a2c5-160">The following example shows a successful response to a **GetSearchableMailboxes** operation request to get the discovery information about members of the expanded lolgroup distribution group.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="526" MinorBuildNumber="0" Version="Exchange2013" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetSearchableMailboxesResponse ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <SearchableMailboxes>
        <SearchableMailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <Guid>e2d42cdf-a227-1ec3-486b-6fa0ebaadb9f5</Guid>
          <PrimarySmtpAddress>JSmith@contoso.com</PrimarySmtpAddress>
          <IsExternalMailbox>false</IsExternalMailbox>
          <ExternalEmailAddress/>
          <DisplayName>Julia Smith</DisplayName>
          <IsMembershipGroup>false</IsMembershipGroup>
          <ReferenceId>/o=First Organization/ou=Exchange Administrative Group (FYDLT)/cn=Recipients/cn=0a1fc86f883846152405d60956dd02e7-Julia</ReferenceId>
        </SearchableMailbox>
        <SearchableMailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <Guid>45d0fff1-6541-459a-a343-52453b30e12ca</Guid>
          <PrimarySmtpAddress>LMoore@contoso.com</PrimarySmtpAddress>
          <IsExternalMailbox>false</IsExternalMailbox>
          <ExternalEmailAddress/>
          <DisplayName>Laura Moore</DisplayName>
          <IsMembershipGroup>false</IsMembershipGroup>
          <ReferenceId>/o=First Organization/ou=Exchange Administrative Group (FYDLT)/cn=Recipients/cn=2910d8f8316f4378bbf9338d8f9d714b-Laura</ReferenceId>
        </SearchableMailbox>
        <SearchableMailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <Guid>3c620d04-8b33-435a-95be-5b939375576</Guid>
          <PrimarySmtpAddress>SBrown@contoso.com</PrimarySmtpAddress>
          <IsExternalMailbox>false</IsExternalMailbox>
          <ExternalEmailAddress/>
          <DisplayName>Steven Brown</DisplayName>
          <IsMembershipGroup>false</IsMembershipGroup>
          <ReferenceId>/o=First Organization/ou=Exchange Administrative Group (FYDLT)/cn=Recipients/cn=90312341a742f0e47e392c80a60d13ecf-Steve</ReferenceId>
        </SearchableMailbox>
      </SearchableMailboxes>
    </GetSearchableMailboxesResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="7a2c5-161">响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="7a2c5-161">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="7a2c5-162">GetSearchableMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="7a2c5-162">GetSearchableMailboxesResponse</span></span>](getsearchablemailboxesresponse.md)    
- [<span data-ttu-id="7a2c5-163">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="7a2c5-163">ResponseCode</span></span>](responsecode.md)   
- [<span data-ttu-id="7a2c5-164">SearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="7a2c5-164">SearchableMailboxes</span></span>](searchablemailboxes.md)    
- [<span data-ttu-id="7a2c5-165">SearchableMailbox</span><span class="sxs-lookup"><span data-stu-id="7a2c5-165">SearchableMailbox</span></span>](searchablemailbox.md)    
- [<span data-ttu-id="7a2c5-166">Guid</span><span class="sxs-lookup"><span data-stu-id="7a2c5-166">Guid</span></span>](guid-ex15websvcsotherref.md)    
- [<span data-ttu-id="7a2c5-167">PrimarySmtpAddress</span><span class="sxs-lookup"><span data-stu-id="7a2c5-167">PrimarySmtpAddress</span></span>](primarysmtpaddress.md)    
- [<span data-ttu-id="7a2c5-168">IsExternalMailbox</span><span class="sxs-lookup"><span data-stu-id="7a2c5-168">IsExternalMailbox</span></span>](isexternalmailbox.md)    
- [<span data-ttu-id="7a2c5-169">ExternalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="7a2c5-169">ExternalEmailAddress</span></span>](externalemailaddress.md)    
- [<span data-ttu-id="7a2c5-170">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="7a2c5-170">DisplayName (string)</span></span>](displayname-string.md)    
- [<span data-ttu-id="7a2c5-171">IsMembershipGroup</span><span class="sxs-lookup"><span data-stu-id="7a2c5-171">IsMembershipGroup</span></span>](ismembershipgroup.md)    
- [<span data-ttu-id="7a2c5-172">ReferenceId</span><span class="sxs-lookup"><span data-stu-id="7a2c5-172">ReferenceId</span></span>](referenceid.md)
    
## <a name="getsearchablemailboxes-operation-error-response"></a><span data-ttu-id="7a2c5-173">GetSearchableMailboxes 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="7a2c5-173">GetSearchableMailboxes operation error response</span></span>

<span data-ttu-id="7a2c5-174">下面的示例演示对**GetSearchableMailboxes**操作请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="7a2c5-174">The following example shows an error response to a **GetSearchableMailboxes** operation request.</span></span> <span data-ttu-id="7a2c5-175">这是对在**ExpandGroupMembership**参数设置为**true**时获取所有可搜索邮箱的请求的响应。</span><span class="sxs-lookup"><span data-stu-id="7a2c5-175">This is a response to a request to get all searchable mailboxes when the **ExpandGroupMembership** argument is set to **true**.</span></span> 
  
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
      <GetSearchableMailboxesResponse ResponseClass="Error" 
                                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Cannot use wildcard or empty query when auto group expansion is enabled.</MessageText>
         <ResponseCode>ErrorInvalidArgument</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
         <SearchableMailboxes/>
      </GetSearchableMailboxesResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="7a2c5-176">错误响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="7a2c5-176">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="7a2c5-177">GetSearchableMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="7a2c5-177">GetSearchableMailboxesResponse</span></span>](getsearchablemailboxesresponse.md)  
- [<span data-ttu-id="7a2c5-178">MessageText</span><span class="sxs-lookup"><span data-stu-id="7a2c5-178">MessageText</span></span>](messagetext.md)   
- [<span data-ttu-id="7a2c5-179">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="7a2c5-179">ResponseCode</span></span>](responsecode.md)   
- [<span data-ttu-id="7a2c5-180">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="7a2c5-180">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) 
- [<span data-ttu-id="7a2c5-181">SearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="7a2c5-181">SearchableMailboxes</span></span>](searchablemailboxes.md)
    
<span data-ttu-id="7a2c5-182">有关对 EWS 通用的其他错误代码以及特定于此操作的错误代码，请参阅[ResponseCode](responsecode.md)。</span><span class="sxs-lookup"><span data-stu-id="7a2c5-182">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7a2c5-183">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7a2c5-183">See also</span></span>

- [<span data-ttu-id="7a2c5-184">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="7a2c5-184">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)   
- [<span data-ttu-id="7a2c5-185">SetHoldOnMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="7a2c5-185">SetHoldOnMailboxes operation</span></span>](setholdonmailboxes-operation.md)   
- [<span data-ttu-id="7a2c5-186">SearchMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="7a2c5-186">SearchMailboxes operation</span></span>](searchmailboxes-operation.md)   
- [<span data-ttu-id="7a2c5-187">GetHoldOnMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="7a2c5-187">GetHoldOnMailboxes operation</span></span>](getholdonmailboxes-operation.md)    
- [<span data-ttu-id="7a2c5-188">GetDiscoverySearchConfiguration 操作</span><span class="sxs-lookup"><span data-stu-id="7a2c5-188">GetDiscoverySearchConfiguration operation</span></span>](getdiscoverysearchconfiguration-operation.md)   
- [<span data-ttu-id="7a2c5-189">GetNonIndexableItemDetails 操作</span><span class="sxs-lookup"><span data-stu-id="7a2c5-189">GetNonIndexableItemDetails operation</span></span>](getnonindexableitemdetails-operation.md)   
- [<span data-ttu-id="7a2c5-190">GetNonIndexableItemStatistics 操作</span><span class="sxs-lookup"><span data-stu-id="7a2c5-190">GetNonIndexableItemStatistics operation</span></span>](getnonindexableitemstatistics-operation.md)
    

