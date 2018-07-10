---
title: GetHoldOnMailboxes 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9157f329-80b4-4cd0-a158-378064966ae6
description: 查找信息 GetHoldOnMailboxes EWS 操作。
ms.openlocfilehash: 1d0bc2f9d26e11d8d2710693d67843ad2f339a5d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754574"
---
# <a name="getholdonmailboxes-operation"></a><span data-ttu-id="088ce-103">GetHoldOnMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="088ce-103">GetHoldOnMailboxes operation</span></span>

<span data-ttu-id="088ce-104">查找有关**GetHoldOnMailboxes** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="088ce-104">Find information about the **GetHoldOnMailboxes** EWS operation.</span></span> 
  
<span data-ttu-id="088ce-105">**GetHoldOnMailboxes**操作获取正在对特定保留项的邮箱和关联的保留查询。</span><span class="sxs-lookup"><span data-stu-id="088ce-105">The **GetHoldOnMailboxes** operation gets the mailboxes that are under a specific hold and the associated hold query.</span></span> 
  
<span data-ttu-id="088ce-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="088ce-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getholdonmailboxes-operation"></a><span data-ttu-id="088ce-107">使用 GetHoldOnMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="088ce-107">Using the GetHoldOnMailboxes operation</span></span>

<span data-ttu-id="088ce-108">**GetHoldOnMailboxes**操作提供了有关哪些邮箱置于下，特定保留项、 有关与每个保留，如果适用，关联的保留查询的信息和有关每个邮箱的保留状态信息的客户端信息。</span><span class="sxs-lookup"><span data-stu-id="088ce-108">The **GetHoldOnMailboxes** operation gives the client information about which mailboxes are placed under a specific hold, information about the hold query associated with each hold, if applicable, and information about the hold status for each mailbox.</span></span> <span data-ttu-id="088ce-109">有关邮箱保留，包括基于查询的保留项，请参阅 TechNet 上的[就地保留](http://technet.microsoft.com/zh-cn/library/ff637980%28v=exchg.150%29)。</span><span class="sxs-lookup"><span data-stu-id="088ce-109">For more information about mailbox holds, including query-based holds, see [In-Place Hold](http://technet.microsoft.com/zh-cn/library/ff637980%28v=exchg.150%29) on TechNet.</span></span> 
  
### <a name="getholdonmailboxes-operation-soap-headers"></a><span data-ttu-id="088ce-110">GetHoldOnMailboxes 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="088ce-110">GetHoldOnMailboxes operation SOAP headers</span></span>

<span data-ttu-id="088ce-111">**GetHoldOnMailboxes**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="088ce-111">The **GetHoldOnMailboxes** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="088ce-112">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="088ce-112">**Header name**</span></span>|<span data-ttu-id="088ce-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="088ce-113">**Element**</span></span>|<span data-ttu-id="088ce-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="088ce-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="088ce-115">**ManagementRole**</span><span class="sxs-lookup"><span data-stu-id="088ce-115">**ManagementRole**</span></span> <br/> |[<span data-ttu-id="088ce-116">ManagementRole</span><span class="sxs-lookup"><span data-stu-id="088ce-116">ManagementRole</span></span>](managementrole.md) <br/> |<span data-ttu-id="088ce-117">标识服务器角色所需顺序呼叫者发出请求。</span><span class="sxs-lookup"><span data-stu-id="088ce-117">Identifies the server roles that are necessary in order for the caller to make the request.</span></span> <span data-ttu-id="088ce-118">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="088ce-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="088ce-119">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="088ce-119">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="088ce-120">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="088ce-120">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="088ce-121">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="088ce-121">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="088ce-122">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="088ce-122">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="088ce-123">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="088ce-123">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="088ce-124">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="088ce-124">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="088ce-125">标识响应该请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="088ce-125">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="088ce-126">适用于响应此标头。</span><span class="sxs-lookup"><span data-stu-id="088ce-126">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getholdonmailboxes-operation-request-example-get-mailbox-hold-information"></a><span data-ttu-id="088ce-127">GetHoldOnMailboxes 操作请求示例： 获取邮箱保留信息</span><span class="sxs-lookup"><span data-stu-id="088ce-127">GetHoldOnMailboxes operation request example: Get mailbox hold information</span></span>

<span data-ttu-id="088ce-128">**GetHoldOnMailboxes**操作请求的下面的示例演示如何获取 HoldId2 邮箱保留的邮箱保留信息。</span><span class="sxs-lookup"><span data-stu-id="088ce-128">The following example of a **GetHoldOnMailboxes** operation request shows how to get the mailbox hold information for the HoldId2 mailbox hold.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="088ce-129">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="088ce-129">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="088ce-130">GetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="088ce-130">GetHoldOnMailboxes</span></span>](getholdonmailboxes.md)
    
- [<span data-ttu-id="088ce-131">HoldId</span><span class="sxs-lookup"><span data-stu-id="088ce-131">HoldId</span></span>](holdid.md)
    
## <a name="successful-getholdonmailboxes-operation-response"></a><span data-ttu-id="088ce-132">成功 GetHoldOnMailboxes 操作响应</span><span class="sxs-lookup"><span data-stu-id="088ce-132">Successful GetHoldOnMailboxes operation response</span></span>

<span data-ttu-id="088ce-133">下面的示例演示对**GetHoldOnMailboxes**操作的成功响应请求以获取邮箱保留 HoldId2 邮箱保留的信息。</span><span class="sxs-lookup"><span data-stu-id="088ce-133">The following example shows a successful response to a **GetHoldOnMailboxes** operation request to get the mailbox hold information for the HoldId2 mailbox hold.</span></span> 
  
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
      <GetHoldOnMailboxesResponse ResponseClass="Success" 
                                  xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <MailboxHoldResult>
            <HoldId xmlns="http://schemas.microsoft.com/exchange/services/2006/types">HoldId2</HoldId>
            <Query xmlns="http://schemas.microsoft.com/exchange/services/2006/types">test</Query>
            <MailboxHoldStatuses xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="088ce-134">响应 SOAP 正文中包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="088ce-134">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="088ce-135">GetHoldOnMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="088ce-135">GetHoldOnMailboxesResponse</span></span>](getholdonmailboxesresponse.md)
    
- [<span data-ttu-id="088ce-136">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="088ce-136">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="088ce-137">MailboxHoldResult</span><span class="sxs-lookup"><span data-stu-id="088ce-137">MailboxHoldResult</span></span>](mailboxholdresult.md)
    
- [<span data-ttu-id="088ce-138">HoldId</span><span class="sxs-lookup"><span data-stu-id="088ce-138">HoldId</span></span>](holdid.md)
    
- [<span data-ttu-id="088ce-139">Query</span><span class="sxs-lookup"><span data-stu-id="088ce-139">Query</span></span>](query.md)
    
- [<span data-ttu-id="088ce-140">MailboxHoldStatuses</span><span class="sxs-lookup"><span data-stu-id="088ce-140">MailboxHoldStatuses</span></span>](mailboxholdstatuses.md)
    
- [<span data-ttu-id="088ce-141">MailboxHoldStatus</span><span class="sxs-lookup"><span data-stu-id="088ce-141">MailboxHoldStatus</span></span>](mailboxholdstatus.md)
    
- [<span data-ttu-id="088ce-142">邮箱 (字符串)</span><span class="sxs-lookup"><span data-stu-id="088ce-142">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="088ce-143">状态 (HoldStatusType)</span><span class="sxs-lookup"><span data-stu-id="088ce-143">Status (HoldStatusType)</span></span>](status-holdstatustype.md)
    
- [<span data-ttu-id="088ce-144">AdditionalInfo</span><span class="sxs-lookup"><span data-stu-id="088ce-144">AdditionalInfo</span></span>](additionalinfo.md)
    
## <a name="getholdonmailboxes-operation-error-response"></a><span data-ttu-id="088ce-145">GetHoldOnMailboxes 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="088ce-145">GetHoldOnMailboxes operation error response</span></span>

<span data-ttu-id="088ce-146">下面的示例演示对**GetHoldOnMailboxes**操作请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="088ce-146">The following example shows an error response to a **GetHoldOnMailboxes** operation request.</span></span> <span data-ttu-id="088ce-147">这是对请求以获取保留已删除的响应。</span><span class="sxs-lookup"><span data-stu-id="088ce-147">This is a response to a request to get a hold that has been deleted.</span></span> 
  
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
      <GetHoldOnMailboxesResponse ResponseClass="Error" 
                                  xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specific query-based hold is not found.</MessageText>
         <ResponseCode>ErrorMailboxHoldNotFound</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </GetHoldOnMailboxesResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="088ce-148">错误响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="088ce-148">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="088ce-149">GetHoldOnMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="088ce-149">GetHoldOnMailboxesResponse</span></span>](getholdonmailboxesresponse.md)
    
- [<span data-ttu-id="088ce-150">MessageText</span><span class="sxs-lookup"><span data-stu-id="088ce-150">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="088ce-151">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="088ce-151">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="088ce-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="088ce-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="088ce-153">通用到 EWS 且特定于此操作的其他错误代码，请参阅[ResponseCode](responsecode.md)。</span><span class="sxs-lookup"><span data-stu-id="088ce-153">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="088ce-154">另请参阅</span><span class="sxs-lookup"><span data-stu-id="088ce-154">See also</span></span>

- [<span data-ttu-id="088ce-155">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="088ce-155">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="088ce-156">GetSearchableMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="088ce-156">GetSearchableMailboxes operation</span></span>](getsearchablemailboxes-operation.md)
    
- [<span data-ttu-id="088ce-157">SearchMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="088ce-157">SearchMailboxes operation</span></span>](searchmailboxes-operation.md)
    
- [<span data-ttu-id="088ce-158">SetHoldOnMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="088ce-158">SetHoldOnMailboxes operation</span></span>](setholdonmailboxes-operation.md)
    
- [<span data-ttu-id="088ce-159">GetDiscoverySearchConfiguration 操作</span><span class="sxs-lookup"><span data-stu-id="088ce-159">GetDiscoverySearchConfiguration operation</span></span>](getdiscoverysearchconfiguration-operation.md)
    
- [<span data-ttu-id="088ce-160">GetNonIndexableItemDetails 操作</span><span class="sxs-lookup"><span data-stu-id="088ce-160">GetNonIndexableItemDetails operation</span></span>](getnonindexableitemdetails-operation.md)
    
- [<span data-ttu-id="088ce-161">GetNonIndexableItemStatistics 操作</span><span class="sxs-lookup"><span data-stu-id="088ce-161">GetNonIndexableItemStatistics operation</span></span>](getnonindexableitemstatistics-operation.md)
    

