---
title: GetSearchableMailboxes 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 47f8ff57-4835-4d2d-9136-44afb31a4cbe
description: 查找信息 GetSearchableMailboxes EWS 操作。
ms.openlocfilehash: 5e14288280b23e2555eea4fce0f77743d7d210ce
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754678"
---
# <a name="getsearchablemailboxes-operation"></a><span data-ttu-id="e2efb-103">GetSearchableMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="e2efb-103">GetSearchableMailboxes operation</span></span>

<span data-ttu-id="e2efb-104">查找有关**GetSearchableMailboxes** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="e2efb-104">Find information about the **GetSearchableMailboxes** EWS operation.</span></span> 
  
<span data-ttu-id="e2efb-105">**GetSearchableMailboxes**操作获取一作用域的可搜索发现搜索邮箱。</span><span class="sxs-lookup"><span data-stu-id="e2efb-105">The **GetSearchableMailboxes** operation gets a scoped set of searchable mailboxes for discovery searches.</span></span> <span data-ttu-id="e2efb-106">可搜索的邮箱在响应中返回的范围是取决于的搜索筛选器和是否展开通讯组成员身份。</span><span class="sxs-lookup"><span data-stu-id="e2efb-106">The scope of searchable mailboxes returned in the response is determined by the search filter and whether distribution group membership is expanded.</span></span> 
  
<span data-ttu-id="e2efb-107">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="e2efb-107">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getsearchablemailboxes-operation"></a><span data-ttu-id="e2efb-108">使用 GetSearchableMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="e2efb-108">Using the GetSearchableMailboxes operation</span></span>

<span data-ttu-id="e2efb-109">**GetSearchableMailboxes**操作获取有关可搜索的邮箱的信息。</span><span class="sxs-lookup"><span data-stu-id="e2efb-109">The **GetSearchableMailboxes** operation gets information about searchable mailboxes.</span></span> <span data-ttu-id="e2efb-110">可以在请求中传递的以下参数：</span><span class="sxs-lookup"><span data-stu-id="e2efb-110">The following arguments can be passed in the request:</span></span> 
  
- <span data-ttu-id="e2efb-111">[SearchFilter](searchfilter.md) — 接受作为参数的单个电子邮件别名。</span><span class="sxs-lookup"><span data-stu-id="e2efb-111">[SearchFilter](searchfilter.md) —Accepts a single email alias as an argument.</span></span> 
    
- <span data-ttu-id="e2efb-112">[ExpandGroupMembership](expandgroupmembership.md) — 指示是否在响应中返回的结果中展开通讯组成员身份。</span><span class="sxs-lookup"><span data-stu-id="e2efb-112">[ExpandGroupMembership](expandgroupmembership.md) — Indicates whether the distribution group membership is expanded in the results returned in the response.</span></span> 
    
<span data-ttu-id="e2efb-113">如果没有展开通讯组成员身份的搜索筛选器中设置电子邮件别名是通讯组，响应将包含通讯组的邮箱信息。</span><span class="sxs-lookup"><span data-stu-id="e2efb-113">If the email alias set in the search filter is a distribution group and the distribution group membership is not expanded, the response will contain the mailbox information for the distribution group.</span></span> <span data-ttu-id="e2efb-114">如果搜索筛选器中设置电子邮件别名是通讯组扩展的通讯组成员身份以及响应将包含通讯组的成员的每个邮箱的邮箱信息。</span><span class="sxs-lookup"><span data-stu-id="e2efb-114">If the email alias set in the search filter is a distribution group and the distribution group membership is expanded, the response will contain the mailbox information for each mailbox that is a member of the distribution group.</span></span> <span data-ttu-id="e2efb-115">如果搜索筛选器包含单个用户的别名，则响应将包含单个用户的邮箱信息。</span><span class="sxs-lookup"><span data-stu-id="e2efb-115">If the search filter contains a single user's alias, the response will contain the mailbox information for the single user.</span></span> <span data-ttu-id="e2efb-116">如果[GetSearchableMailboxes](getsearchablemailboxes.md)元素为空，则响应将包含所有可搜索的邮箱。</span><span class="sxs-lookup"><span data-stu-id="e2efb-116">The response will contain all searchable mailboxes if the [GetSearchableMailboxes](getsearchablemailboxes.md) element is empty.</span></span> <span data-ttu-id="e2efb-117">这是相同具有空[SearchFilter](searchfilter.md)元素和[ExpandGroupMembership](expandgroupmembership.md)元素设置为**false**。</span><span class="sxs-lookup"><span data-stu-id="e2efb-117">This is the same as having an empty [SearchFilter](searchfilter.md) element and the [ExpandGroupMembership](expandgroupmembership.md) element set to **false**.</span></span>
  
### <a name="getsearchablemailboxes-operation-soap-headers"></a><span data-ttu-id="e2efb-118">GetSearchableMailboxes 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="e2efb-118">GetSearchableMailboxes operation SOAP headers</span></span>

<span data-ttu-id="e2efb-119">**GetSearchableMailboxes**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="e2efb-119">The **GetSearchableMailboxes** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="e2efb-120">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="e2efb-120">**Header name**</span></span>|<span data-ttu-id="e2efb-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="e2efb-121">**Element**</span></span>|<span data-ttu-id="e2efb-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="e2efb-122">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e2efb-123">**ManagementRole**</span><span class="sxs-lookup"><span data-stu-id="e2efb-123">**ManagementRole**</span></span> <br/> |[<span data-ttu-id="e2efb-124">ManagementRole</span><span class="sxs-lookup"><span data-stu-id="e2efb-124">ManagementRole</span></span>](managementrole.md) <br/> |<span data-ttu-id="e2efb-125">标识服务器角色所需顺序呼叫者发出请求。</span><span class="sxs-lookup"><span data-stu-id="e2efb-125">Identifies the server roles that are necessary in order for the caller to make the request.</span></span> <span data-ttu-id="e2efb-126">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="e2efb-126">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="e2efb-127">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="e2efb-127">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="e2efb-128">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="e2efb-128">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="e2efb-129">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="e2efb-129">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="e2efb-130">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="e2efb-130">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="e2efb-131">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="e2efb-131">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="e2efb-132">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="e2efb-132">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="e2efb-133">标识响应该请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="e2efb-133">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="e2efb-134">适用于响应此标头。</span><span class="sxs-lookup"><span data-stu-id="e2efb-134">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getsearchablemailboxes-operation-request-example-request-information-about-a-distribution-group"></a><span data-ttu-id="e2efb-135">GetSearchableMailboxes 操作请求示例： 请求信息的通讯组</span><span class="sxs-lookup"><span data-stu-id="e2efb-135">GetSearchableMailboxes operation request example: Request information about a distribution group</span></span>

<span data-ttu-id="e2efb-136">**GetSearchableMailboxes**操作请求的下面的示例演示如何获取 lolgroup 通讯组的邮箱信息。</span><span class="sxs-lookup"><span data-stu-id="e2efb-136">The following example of a **GetSearchableMailboxes** operation request shows how to get the mailbox information for the lolgroup distribution group.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="e2efb-137">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="e2efb-137">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="e2efb-138">GetSearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="e2efb-138">GetSearchableMailboxes</span></span>](getsearchablemailboxes.md)
    
- [<span data-ttu-id="e2efb-139">SearchFilter</span><span class="sxs-lookup"><span data-stu-id="e2efb-139">SearchFilter</span></span>](searchfilter.md)
    
- [<span data-ttu-id="e2efb-140">ExpandGroupMembership</span><span class="sxs-lookup"><span data-stu-id="e2efb-140">ExpandGroupMembership</span></span>](expandgroupmembership.md)
    
## <a name="successful-getsearchablemailboxes-operation-response-get-information-about-a-distribution-group"></a><span data-ttu-id="e2efb-141">成功 GetSearchableMailboxes 操作响应： 获取有关通讯组的信息</span><span class="sxs-lookup"><span data-stu-id="e2efb-141">Successful GetSearchableMailboxes operation response: Get information about a distribution group</span></span>

<span data-ttu-id="e2efb-142">下面的示例演示对**GetSearchableMailboxes**操作请求以获得 lolgroup 通讯组的发现信息的成功响应。</span><span class="sxs-lookup"><span data-stu-id="e2efb-142">The following example shows a successful response to a **GetSearchableMailboxes** operation request to get the discovery information for the lolgroup distribution group.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="526" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetSearchableMailboxesResponse ResponseClass="Success" 
                                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <SearchableMailboxes>
            <SearchableMailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="e2efb-143">响应 SOAP 正文中包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="e2efb-143">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="e2efb-144">GetSearchableMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="e2efb-144">GetSearchableMailboxesResponse</span></span>](getsearchablemailboxesresponse.md)
    
- [<span data-ttu-id="e2efb-145">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e2efb-145">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="e2efb-146">SearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="e2efb-146">SearchableMailboxes</span></span>](searchablemailboxes.md)
    
- [<span data-ttu-id="e2efb-147">SearchableMailbox</span><span class="sxs-lookup"><span data-stu-id="e2efb-147">SearchableMailbox</span></span>](searchablemailbox.md)
    
- [<span data-ttu-id="e2efb-148">Guid</span><span class="sxs-lookup"><span data-stu-id="e2efb-148">Guid</span></span>](guid-ex15websvcsotherref.md)
    
- [<span data-ttu-id="e2efb-149">PrimarySmtpAddress</span><span class="sxs-lookup"><span data-stu-id="e2efb-149">PrimarySmtpAddress</span></span>](primarysmtpaddress.md)
    
- [<span data-ttu-id="e2efb-150">IsExternalMailbox</span><span class="sxs-lookup"><span data-stu-id="e2efb-150">IsExternalMailbox</span></span>](isexternalmailbox.md)
    
- [<span data-ttu-id="e2efb-151">ExternalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="e2efb-151">ExternalEmailAddress</span></span>](externalemailaddress.md)
    
- [<span data-ttu-id="e2efb-152">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="e2efb-152">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="e2efb-153">IsMembershipGroup</span><span class="sxs-lookup"><span data-stu-id="e2efb-153">IsMembershipGroup</span></span>](ismembershipgroup.md)
    
- [<span data-ttu-id="e2efb-154">相同引用</span><span class="sxs-lookup"><span data-stu-id="e2efb-154">ReferenceId</span></span>](referenceid.md)
    
## <a name="successful-getsearchablemailboxes-operation-response-get-information-about-an-expanded-distribution-group"></a><span data-ttu-id="e2efb-155">成功 GetSearchableMailboxes 操作响应： 获取有关扩展的通讯组的信息</span><span class="sxs-lookup"><span data-stu-id="e2efb-155">Successful GetSearchableMailboxes operation response: Get information about an expanded distribution group</span></span>

<span data-ttu-id="e2efb-156">下面的示例演示对**GetSearchableMailboxes**操作请求以获取有关扩展的 lolgroup 通讯组的成员的发现信息的成功响应。</span><span class="sxs-lookup"><span data-stu-id="e2efb-156">The following example shows a successful response to a **GetSearchableMailboxes** operation request to get the discovery information about members of the expanded lolgroup distribution group.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="526" MinorBuildNumber="0" Version="Exchange2013" xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" xmlns="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetSearchableMailboxesResponse ResponseClass="Success" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <SearchableMailboxes>
        <SearchableMailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <Guid>e2d42cdf-a227-1ec3-486b-6fa0ebaadb9f5</Guid>
          <PrimarySmtpAddress>JSmith@contoso.com</PrimarySmtpAddress>
          <IsExternalMailbox>false</IsExternalMailbox>
          <ExternalEmailAddress/>
          <DisplayName>Julia Smith</DisplayName>
          <IsMembershipGroup>false</IsMembershipGroup>
          <ReferenceId>/o=First Organization/ou=Exchange Administrative Group (FYDLT)/cn=Recipients/cn=0a1fc86f883846152405d60956dd02e7-Julia</ReferenceId>
        </SearchableMailbox>
        <SearchableMailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <Guid>45d0fff1-6541-459a-a343-52453b30e12ca</Guid>
          <PrimarySmtpAddress>LMoore@contoso.com</PrimarySmtpAddress>
          <IsExternalMailbox>false</IsExternalMailbox>
          <ExternalEmailAddress/>
          <DisplayName>Laura Moore</DisplayName>
          <IsMembershipGroup>false</IsMembershipGroup>
          <ReferenceId>/o=First Organization/ou=Exchange Administrative Group (FYDLT)/cn=Recipients/cn=2910d8f8316f4378bbf9338d8f9d714b-Laura</ReferenceId>
        </SearchableMailbox>
        <SearchableMailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="e2efb-157">响应 SOAP 正文中包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="e2efb-157">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="e2efb-158">GetSearchableMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="e2efb-158">GetSearchableMailboxesResponse</span></span>](getsearchablemailboxesresponse.md)
    
- [<span data-ttu-id="e2efb-159">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e2efb-159">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="e2efb-160">SearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="e2efb-160">SearchableMailboxes</span></span>](searchablemailboxes.md)
    
- [<span data-ttu-id="e2efb-161">SearchableMailbox</span><span class="sxs-lookup"><span data-stu-id="e2efb-161">SearchableMailbox</span></span>](searchablemailbox.md)
    
- [<span data-ttu-id="e2efb-162">Guid</span><span class="sxs-lookup"><span data-stu-id="e2efb-162">Guid</span></span>](guid-ex15websvcsotherref.md)
    
- [<span data-ttu-id="e2efb-163">PrimarySmtpAddress</span><span class="sxs-lookup"><span data-stu-id="e2efb-163">PrimarySmtpAddress</span></span>](primarysmtpaddress.md)
    
- [<span data-ttu-id="e2efb-164">IsExternalMailbox</span><span class="sxs-lookup"><span data-stu-id="e2efb-164">IsExternalMailbox</span></span>](isexternalmailbox.md)
    
- [<span data-ttu-id="e2efb-165">ExternalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="e2efb-165">ExternalEmailAddress</span></span>](externalemailaddress.md)
    
- [<span data-ttu-id="e2efb-166">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="e2efb-166">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="e2efb-167">IsMembershipGroup</span><span class="sxs-lookup"><span data-stu-id="e2efb-167">IsMembershipGroup</span></span>](ismembershipgroup.md)
    
- [<span data-ttu-id="e2efb-168">相同引用</span><span class="sxs-lookup"><span data-stu-id="e2efb-168">ReferenceId</span></span>](referenceid.md)
    
## <a name="getsearchablemailboxes-operation-error-response"></a><span data-ttu-id="e2efb-169">GetSearchableMailboxes 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="e2efb-169">GetSearchableMailboxes operation error response</span></span>

<span data-ttu-id="e2efb-170">下面的示例演示对**GetSearchableMailboxes**操作请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="e2efb-170">The following example shows an error response to a **GetSearchableMailboxes** operation request.</span></span> <span data-ttu-id="e2efb-171">这是对**ExpandGroupMembership**参数设置为**true**时，收到所有可搜索的邮箱的请求的响应。</span><span class="sxs-lookup"><span data-stu-id="e2efb-171">This is a response to a request to get all searchable mailboxes when the **ExpandGroupMembership** argument is set to **true**.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="526"
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetSearchableMailboxesResponse ResponseClass="Error" 
                                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Cannot use wildcard or empty query when auto group expansion is enabled.</MessageText>
         <ResponseCode>ErrorInvalidArgument</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
         <SearchableMailboxes/>
      </GetSearchableMailboxesResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="e2efb-172">错误响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="e2efb-172">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="e2efb-173">GetSearchableMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="e2efb-173">GetSearchableMailboxesResponse</span></span>](getsearchablemailboxesresponse.md)
    
- [<span data-ttu-id="e2efb-174">MessageText</span><span class="sxs-lookup"><span data-stu-id="e2efb-174">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="e2efb-175">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e2efb-175">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="e2efb-176">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="e2efb-176">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="e2efb-177">SearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="e2efb-177">SearchableMailboxes</span></span>](searchablemailboxes.md)
    
<span data-ttu-id="e2efb-178">通用到 EWS 且特定于此操作的其他错误代码，请参阅[ResponseCode](responsecode.md)。</span><span class="sxs-lookup"><span data-stu-id="e2efb-178">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e2efb-179">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e2efb-179">See also</span></span>

- [<span data-ttu-id="e2efb-180">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="e2efb-180">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="e2efb-181">SetHoldOnMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="e2efb-181">SetHoldOnMailboxes operation</span></span>](setholdonmailboxes-operation.md)
    
- [<span data-ttu-id="e2efb-182">SearchMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="e2efb-182">SearchMailboxes operation</span></span>](searchmailboxes-operation.md)
    
- [<span data-ttu-id="e2efb-183">GetHoldOnMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="e2efb-183">GetHoldOnMailboxes operation</span></span>](getholdonmailboxes-operation.md)
    
- [<span data-ttu-id="e2efb-184">GetDiscoverySearchConfiguration 操作</span><span class="sxs-lookup"><span data-stu-id="e2efb-184">GetDiscoverySearchConfiguration operation</span></span>](getdiscoverysearchconfiguration-operation.md)
    
- [<span data-ttu-id="e2efb-185">GetNonIndexableItemDetails 操作</span><span class="sxs-lookup"><span data-stu-id="e2efb-185">GetNonIndexableItemDetails operation</span></span>](getnonindexableitemdetails-operation.md)
    
- [<span data-ttu-id="e2efb-186">GetNonIndexableItemStatistics 操作</span><span class="sxs-lookup"><span data-stu-id="e2efb-186">GetNonIndexableItemStatistics operation</span></span>](getnonindexableitemstatistics-operation.md)
    

