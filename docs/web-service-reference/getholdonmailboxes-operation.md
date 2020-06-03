---
title: GetHoldOnMailboxes 操作
manager: sethgros
ms.date: 01/24/2020
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9157f329-80b4-4cd0-a158-378064966ae6
description: 查找有关 GetHoldOnMailboxes EWS 操作的信息。
ms.openlocfilehash: 867f38be87e60af8708eeb0b9d0e3ac8eee6ff64
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457730"
---
# <a name="getholdonmailboxes-operation"></a><span data-ttu-id="67f7b-103">GetHoldOnMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="67f7b-103">GetHoldOnMailboxes operation</span></span>

> [!IMPORTANT]
> <span data-ttu-id="67f7b-104">从2020年4月1日起，GetHoldOnMailboxes 操作将不再在 Exchange Online 中可用。</span><span class="sxs-lookup"><span data-stu-id="67f7b-104">Starting on April 1, 2020, the GetHoldOnMailboxes operation will no longer be available in Exchange Online.</span></span> <span data-ttu-id="67f7b-105">此操作不会受到 Exchange Server 内部部署版本的影响。</span><span class="sxs-lookup"><span data-stu-id="67f7b-105">This operation won't be affected in on-premises versions of Exchange Server.</span></span> <span data-ttu-id="67f7b-106">有关详细信息，请参阅[在 Exchange Online 中停用旧版电子数据展示工具](https://docs.microsoft.com/microsoft-365/compliance/legacy-ediscovery-retirement#getsearchablemailboxes-setholdonmailboxes-and-getholdonmailboxes-operations-in-the-ews-api)。</span><span class="sxs-lookup"><span data-stu-id="67f7b-106">For more information, see [Retirement of legacy eDiscovery tools in Exchange Online](https://docs.microsoft.com/microsoft-365/compliance/legacy-ediscovery-retirement#getsearchablemailboxes-setholdonmailboxes-and-getholdonmailboxes-operations-in-the-ews-api).</span></span>

<span data-ttu-id="67f7b-107">查找有关**GetHoldOnMailboxes** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="67f7b-107">Find information about the **GetHoldOnMailboxes** EWS operation.</span></span> 
  
<span data-ttu-id="67f7b-108">**GetHoldOnMailboxes**操作获取特定保留中的邮箱和关联的保留查询。</span><span class="sxs-lookup"><span data-stu-id="67f7b-108">The **GetHoldOnMailboxes** operation gets the mailboxes that are under a specific hold and the associated hold query.</span></span> 
  
<span data-ttu-id="67f7b-109">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="67f7b-109">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getholdonmailboxes-operation"></a><span data-ttu-id="67f7b-110">使用 GetHoldOnMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="67f7b-110">Using the GetHoldOnMailboxes operation</span></span>

<span data-ttu-id="67f7b-111">**GetHoldOnMailboxes**操作提供了有关在特定保留下放置了哪些邮箱的客户端信息、有关与每个保留关联的保留查询的信息（如果适用）以及有关每个邮箱的保留状态的信息。</span><span class="sxs-lookup"><span data-stu-id="67f7b-111">The **GetHoldOnMailboxes** operation gives the client information about which mailboxes are placed under a specific hold, information about the hold query associated with each hold, if applicable, and information about the hold status for each mailbox.</span></span> <span data-ttu-id="67f7b-112">有关邮箱保留（包括基于查询的保留）的详细信息，请参阅 TechNet 上的[就地保留](https://technet.microsoft.com/library/ff637980%28v=exchg.150%29)。</span><span class="sxs-lookup"><span data-stu-id="67f7b-112">For more information about mailbox holds, including query-based holds, see [In-Place Hold](https://technet.microsoft.com/library/ff637980%28v=exchg.150%29) on TechNet.</span></span> 
  
### <a name="getholdonmailboxes-operation-soap-headers"></a><span data-ttu-id="67f7b-113">GetHoldOnMailboxes 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="67f7b-113">GetHoldOnMailboxes operation SOAP headers</span></span>

<span data-ttu-id="67f7b-114">**GetHoldOnMailboxes**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="67f7b-114">The **GetHoldOnMailboxes** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="67f7b-115">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="67f7b-115">**Header name**</span></span>|<span data-ttu-id="67f7b-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="67f7b-116">**Element**</span></span>|<span data-ttu-id="67f7b-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="67f7b-117">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="67f7b-118">**Get-managementrole**</span><span class="sxs-lookup"><span data-stu-id="67f7b-118">**ManagementRole**</span></span> <br/> |[<span data-ttu-id="67f7b-119">Get-managementrole</span><span class="sxs-lookup"><span data-stu-id="67f7b-119">ManagementRole</span></span>](managementrole.md) <br/> |<span data-ttu-id="67f7b-120">标识调用方发出请求所需的服务器角色。</span><span class="sxs-lookup"><span data-stu-id="67f7b-120">Identifies the server roles that are necessary in order for the caller to make the request.</span></span> <span data-ttu-id="67f7b-121">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="67f7b-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="67f7b-122">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="67f7b-122">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="67f7b-123">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="67f7b-123">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="67f7b-124">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="67f7b-124">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="67f7b-125">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="67f7b-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="67f7b-126">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="67f7b-126">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="67f7b-127">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="67f7b-127">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="67f7b-128">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="67f7b-128">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="67f7b-129">此标头适用于响应。</span><span class="sxs-lookup"><span data-stu-id="67f7b-129">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getholdonmailboxes-operation-request-example-get-mailbox-hold-information"></a><span data-ttu-id="67f7b-130">GetHoldOnMailboxes 操作请求示例：获取邮箱保留信息</span><span class="sxs-lookup"><span data-stu-id="67f7b-130">GetHoldOnMailboxes operation request example: Get mailbox hold information</span></span>

<span data-ttu-id="67f7b-131">以下示例的**GetHoldOnMailboxes**操作请求显示如何获取 HoldId2 邮箱保留的邮箱保留信息。</span><span class="sxs-lookup"><span data-stu-id="67f7b-131">The following example of a **GetHoldOnMailboxes** operation request shows how to get the mailbox hold information for the HoldId2 mailbox hold.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:GetHoldOnMailboxes>
         <m:HoldId>HoldId2</m:HoldId>
      </m:GetHoldOnMailboxes>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="67f7b-132">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="67f7b-132">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="67f7b-133">GetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="67f7b-133">GetHoldOnMailboxes</span></span>](getholdonmailboxes.md)
    
- [<span data-ttu-id="67f7b-134">HoldId</span><span class="sxs-lookup"><span data-stu-id="67f7b-134">HoldId</span></span>](holdid.md)
    
## <a name="successful-getholdonmailboxes-operation-response"></a><span data-ttu-id="67f7b-135">成功的 GetHoldOnMailboxes 操作响应</span><span class="sxs-lookup"><span data-stu-id="67f7b-135">Successful GetHoldOnMailboxes operation response</span></span>

<span data-ttu-id="67f7b-136">下面的示例演示对**GetHoldOnMailboxes**操作请求的成功响应，以获取 HoldId2 邮箱保留的邮箱保留信息。</span><span class="sxs-lookup"><span data-stu-id="67f7b-136">The following example shows a successful response to a **GetHoldOnMailboxes** operation request to get the mailbox hold information for the HoldId2 mailbox hold.</span></span> 
  
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
      <GetHoldOnMailboxesResponse ResponseClass="Success" 
                                  xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <MailboxHoldResult>
            <HoldId xmlns="https://schemas.microsoft.com/exchange/services/2006/types">HoldId2</HoldId>
            <Query xmlns="https://schemas.microsoft.com/exchange/services/2006/types">test</Query>
            <MailboxHoldStatuses xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <MailboxHoldStatus>
                  <Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYDIBPDLT)/cn=Recipients/cn=ecc0fd98c2cadf-Willi</Mailbox>
                  <Status>OnHold</Status>
                  <AdditionalInfo/>
               </MailboxHoldStatus>
               <MailboxHoldStatus>
                  <Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYDIBPDLT)/cn=Recipients/cn=dasdat341q8de95-Micha</Mailbox>
                  <Status>OnHold</Status>
                  <AdditionalInfo/>
               </MailboxHoldStatus>
            </MailboxHoldStatuses>
         </MailboxHoldResult>
      </GetHoldOnMailboxesResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="67f7b-137">响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="67f7b-137">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="67f7b-138">GetHoldOnMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="67f7b-138">GetHoldOnMailboxesResponse</span></span>](getholdonmailboxesresponse.md)
    
- [<span data-ttu-id="67f7b-139">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="67f7b-139">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="67f7b-140">MailboxHoldResult</span><span class="sxs-lookup"><span data-stu-id="67f7b-140">MailboxHoldResult</span></span>](mailboxholdresult.md)
    
- [<span data-ttu-id="67f7b-141">HoldId</span><span class="sxs-lookup"><span data-stu-id="67f7b-141">HoldId</span></span>](holdid.md)
    
- [<span data-ttu-id="67f7b-142">Query</span><span class="sxs-lookup"><span data-stu-id="67f7b-142">Query</span></span>](query.md)
    
- [<span data-ttu-id="67f7b-143">MailboxHoldStatuses</span><span class="sxs-lookup"><span data-stu-id="67f7b-143">MailboxHoldStatuses</span></span>](mailboxholdstatuses.md)
    
- [<span data-ttu-id="67f7b-144">MailboxHoldStatus</span><span class="sxs-lookup"><span data-stu-id="67f7b-144">MailboxHoldStatus</span></span>](mailboxholdstatus.md)
    
- [<span data-ttu-id="67f7b-145">邮箱 (字符串)</span><span class="sxs-lookup"><span data-stu-id="67f7b-145">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="67f7b-146">状态（HoldStatusType）</span><span class="sxs-lookup"><span data-stu-id="67f7b-146">Status (HoldStatusType)</span></span>](status-holdstatustype.md)
    
- [<span data-ttu-id="67f7b-147">AdditionalInfo</span><span class="sxs-lookup"><span data-stu-id="67f7b-147">AdditionalInfo</span></span>](additionalinfo.md)
    
## <a name="getholdonmailboxes-operation-error-response"></a><span data-ttu-id="67f7b-148">GetHoldOnMailboxes 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="67f7b-148">GetHoldOnMailboxes operation error response</span></span>

<span data-ttu-id="67f7b-149">下面的示例演示对**GetHoldOnMailboxes**操作请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="67f7b-149">The following example shows an error response to a **GetHoldOnMailboxes** operation request.</span></span> <span data-ttu-id="67f7b-150">这是对获取已删除保留的请求的响应。</span><span class="sxs-lookup"><span data-stu-id="67f7b-150">This is a response to a request to get a hold that has been deleted.</span></span> 
  
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
      <GetHoldOnMailboxesResponse ResponseClass="Error" 
                                  xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specific query-based hold is not found.</MessageText>
         <ResponseCode>ErrorMailboxHoldNotFound</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </GetHoldOnMailboxesResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="67f7b-151">错误响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="67f7b-151">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="67f7b-152">GetHoldOnMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="67f7b-152">GetHoldOnMailboxesResponse</span></span>](getholdonmailboxesresponse.md)
    
- [<span data-ttu-id="67f7b-153">MessageText</span><span class="sxs-lookup"><span data-stu-id="67f7b-153">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="67f7b-154">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="67f7b-154">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="67f7b-155">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="67f7b-155">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="67f7b-156">有关对 EWS 通用的其他错误代码以及特定于此操作的错误代码，请参阅[ResponseCode](responsecode.md)。</span><span class="sxs-lookup"><span data-stu-id="67f7b-156">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="67f7b-157">另请参阅</span><span class="sxs-lookup"><span data-stu-id="67f7b-157">See also</span></span>

- [<span data-ttu-id="67f7b-158">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="67f7b-158">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="67f7b-159">GetSearchableMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="67f7b-159">GetSearchableMailboxes operation</span></span>](getsearchablemailboxes-operation.md)
    
- [<span data-ttu-id="67f7b-160">SearchMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="67f7b-160">SearchMailboxes operation</span></span>](searchmailboxes-operation.md)
    
- [<span data-ttu-id="67f7b-161">SetHoldOnMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="67f7b-161">SetHoldOnMailboxes operation</span></span>](setholdonmailboxes-operation.md)
    
- [<span data-ttu-id="67f7b-162">GetDiscoverySearchConfiguration 操作</span><span class="sxs-lookup"><span data-stu-id="67f7b-162">GetDiscoverySearchConfiguration operation</span></span>](getdiscoverysearchconfiguration-operation.md)
    
- [<span data-ttu-id="67f7b-163">GetNonIndexableItemDetails 操作</span><span class="sxs-lookup"><span data-stu-id="67f7b-163">GetNonIndexableItemDetails operation</span></span>](getnonindexableitemdetails-operation.md)
    
- [<span data-ttu-id="67f7b-164">GetNonIndexableItemStatistics 操作</span><span class="sxs-lookup"><span data-stu-id="67f7b-164">GetNonIndexableItemStatistics operation</span></span>](getnonindexableitemstatistics-operation.md)
    

