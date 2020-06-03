---
title: SetHoldOnMailboxes 操作
manager: sethgros
ms.date: 01/24/2020
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9015a0d8-3495-461b-aa79-797d23169585
description: 查找有关 SetHoldOnMailboxes EWS 操作的信息。
ms.openlocfilehash: 4d79ba9f616974b9415ae9eae23b8f5fdb0ab205
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44448392"
---
# <a name="setholdonmailboxes-operation"></a><span data-ttu-id="8fc7a-103">SetHoldOnMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="8fc7a-103">SetHoldOnMailboxes operation</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8fc7a-104">从2020年4月1日起，SetHoldOnMailboxes 操作将不再在 Exchange Online 中可用。</span><span class="sxs-lookup"><span data-stu-id="8fc7a-104">Starting on April 1, 2020, the SetHoldOnMailboxes operation will no longer be available in Exchange Online.</span></span> <span data-ttu-id="8fc7a-105">此操作不会受到 Exchange Server 内部部署版本的影响。</span><span class="sxs-lookup"><span data-stu-id="8fc7a-105">This operation won't be affected in on-premises versions of Exchange Server.</span></span> <span data-ttu-id="8fc7a-106">有关详细信息，请参阅[在 Exchange Online 中停用旧版电子数据展示工具](https://docs.microsoft.com/microsoft-365/compliance/legacy-ediscovery-retirement#getsearchablemailboxes-setholdonmailboxes-and-getholdonmailboxes-operations-in-the-ews-api)。</span><span class="sxs-lookup"><span data-stu-id="8fc7a-106">For more information, see [Retirement of legacy eDiscovery tools in Exchange Online](https://docs.microsoft.com/microsoft-365/compliance/legacy-ediscovery-retirement#getsearchablemailboxes-setholdonmailboxes-and-getholdonmailboxes-operations-in-the-ews-api).</span></span>

<span data-ttu-id="8fc7a-107">查找有关**SetHoldOnMailboxes** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="8fc7a-107">Find information about the **SetHoldOnMailboxes** EWS operation.</span></span> 
  
<span data-ttu-id="8fc7a-108">**SetHoldOnMailboxes**操作设置邮箱的邮箱保留策略。</span><span class="sxs-lookup"><span data-stu-id="8fc7a-108">The **SetHoldOnMailboxes** operation sets a mailbox hold policy on mailboxes.</span></span> 
  
<span data-ttu-id="8fc7a-109">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="8fc7a-109">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-setholdonmailboxes-operation"></a><span data-ttu-id="8fc7a-110">使用 SetHoldOnMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="8fc7a-110">Using the SetHoldOnMailboxes operation</span></span>

<span data-ttu-id="8fc7a-111">**SetHoldOnMailboxes**操作将邮箱保留在一个或多个邮箱上。</span><span class="sxs-lookup"><span data-stu-id="8fc7a-111">The **SetHoldOnMailboxes** operation sets a mailbox hold on to one or more mailboxes.</span></span> 
  
### <a name="setholdonmailboxes-operation-soap-headers"></a><span data-ttu-id="8fc7a-112">SetHoldOnMailboxes 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="8fc7a-112">SetHoldOnMailboxes operation SOAP headers</span></span>

<span data-ttu-id="8fc7a-113">**SetHoldOnMailboxes**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="8fc7a-113">The **SetHoldOnMailboxes** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="8fc7a-114">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="8fc7a-114">**Header name**</span></span>|<span data-ttu-id="8fc7a-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="8fc7a-115">**Element**</span></span>|<span data-ttu-id="8fc7a-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="8fc7a-116">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8fc7a-117">**Get-managementrole**</span><span class="sxs-lookup"><span data-stu-id="8fc7a-117">**ManagementRole**</span></span> <br/> |[<span data-ttu-id="8fc7a-118">Get-managementrole</span><span class="sxs-lookup"><span data-stu-id="8fc7a-118">ManagementRole</span></span>](managementrole.md) <br/> |<span data-ttu-id="8fc7a-119">标识调用方发出请求所需的服务器角色。</span><span class="sxs-lookup"><span data-stu-id="8fc7a-119">Identifies the server roles that are necessary in order for the caller to make the request.</span></span> <span data-ttu-id="8fc7a-120">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="8fc7a-120">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="8fc7a-121">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="8fc7a-121">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="8fc7a-122">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="8fc7a-122">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="8fc7a-123">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="8fc7a-123">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="8fc7a-124">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="8fc7a-124">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="8fc7a-125">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="8fc7a-125">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="8fc7a-126">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="8fc7a-126">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="8fc7a-127">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="8fc7a-127">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="8fc7a-128">此标头适用于响应。</span><span class="sxs-lookup"><span data-stu-id="8fc7a-128">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="setholdonmailboxes-operation-request-example-apply-a-hold-on-a-mailbox"></a><span data-ttu-id="8fc7a-129">SetHoldOnMailboxes 操作请求示例：对邮箱应用保留</span><span class="sxs-lookup"><span data-stu-id="8fc7a-129">SetHoldOnMailboxes operation request example: Apply a hold on a mailbox</span></span>

<span data-ttu-id="8fc7a-130">以下示例的**SetHoldOnMailboxes**操作请求显示如何对两个邮箱应用保留。</span><span class="sxs-lookup"><span data-stu-id="8fc7a-130">The following example of a **SetHoldOnMailboxes** operation request shows how to apply a hold on two mailboxes.</span></span> <span data-ttu-id="8fc7a-131">邮箱保留是使用[new-mailboxsearch](https://technet.microsoft.com/library/dd298064.aspx)命令创建的。</span><span class="sxs-lookup"><span data-stu-id="8fc7a-131">The mailbox hold was created by using the [New-MailboxSearch](https://technet.microsoft.com/library/dd298064.aspx) command.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:SetHoldOnMailboxes>
         <m:ActionType>Create</m:ActionType>
         <m:HoldId>HoldId2</m:HoldId>
         <m:Query>test</m:Query>
         <m:Mailboxes>
            <t:String>/o=First/ou=Exchange(DLT)/cn=Recipients/cn=1fa441ff5e4749ba43ecc0fd94c21adf-Willi</t:String>
            <t:String>/o=First/ou=Exchange(DLT)/cn=Recipients/cn=aed2346adaa34ffc9f0f339917e8de95-Micha</t:String>
         </m:Mailboxes>
         <m:Language>English</m:Language>
         <m:IncludeNonIndexableItems>false</m:IncludeNonIndexableItems>
         <m:Deduplication>true</m:Deduplication>
      </m:SetHoldOnMailboxes>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="8fc7a-132">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="8fc7a-132">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="8fc7a-133">SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="8fc7a-133">SetHoldOnMailboxes</span></span>](setholdonmailboxes.md)
    
- [<span data-ttu-id="8fc7a-134">ActionType （HoldActionType）</span><span class="sxs-lookup"><span data-stu-id="8fc7a-134">ActionType (HoldActionType)</span></span>](actiontype-holdactiontype.md)
    
- [<span data-ttu-id="8fc7a-135">HoldId</span><span class="sxs-lookup"><span data-stu-id="8fc7a-135">HoldId</span></span>](holdid.md)
    
- [<span data-ttu-id="8fc7a-136">Query</span><span class="sxs-lookup"><span data-stu-id="8fc7a-136">Query</span></span>](query.md)
    
- [<span data-ttu-id="8fc7a-137">邮箱（ArrayOfStringsType）</span><span class="sxs-lookup"><span data-stu-id="8fc7a-137">Mailboxes (ArrayOfStringsType)</span></span>](mailboxes-arrayofstringstype.md)
    
- [<span data-ttu-id="8fc7a-138">String</span><span class="sxs-lookup"><span data-stu-id="8fc7a-138">String</span></span>](string.md)
    
- [<span data-ttu-id="8fc7a-139">Language</span><span class="sxs-lookup"><span data-stu-id="8fc7a-139">Language</span></span>](language.md)
    
- [<span data-ttu-id="8fc7a-140">IncludeNonIndexableItems</span><span class="sxs-lookup"><span data-stu-id="8fc7a-140">IncludeNonIndexableItems</span></span>](includenonindexableitems.md)
    
- [<span data-ttu-id="8fc7a-141">项</span><span class="sxs-lookup"><span data-stu-id="8fc7a-141">Deduplication</span></span>](deduplication.md)
    
## <a name="successful-setholdonmailboxes-operation-response"></a><span data-ttu-id="8fc7a-142">成功的 SetHoldOnMailboxes 操作响应</span><span class="sxs-lookup"><span data-stu-id="8fc7a-142">Successful SetHoldOnMailboxes operation response</span></span>

<span data-ttu-id="8fc7a-143">下面的示例演示对**SetHoldOnMailboxes**操作请求的成功响应，以将两个邮箱置于保留状态。</span><span class="sxs-lookup"><span data-stu-id="8fc7a-143">The following example shows a successful response to a **SetHoldOnMailboxes** operation request to put two mailboxes on hold.</span></span> 
  
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
      <SetHoldOnMailboxesResponse ResponseClass="Success" 
                                  xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <MailboxHoldResult>
            <HoldId xmlns="https://schemas.microsoft.com/exchange/services/2006/types">HoldId2</HoldId>
            <Query xmlns="https://schemas.microsoft.com/exchange/services/2006/types">test</Query>
            <MailboxHoldStatuses xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <MailboxHoldStatus>
                  <Mailbox>o=First/ou=Exchange(DLT)/cn=Recipients/cn=1fa441ff5e4749ba43ecc0fd94c21adf-Willi</Mailbox>
                  <Status>Pending</Status>
                  <AdditionalInfo/>
               </MailboxHoldStatus>
               <MailboxHoldStatus>
                  <Mailbox>/o=First/ou=Exchange(DLT)/cn=Recipients/cn=aed2346adaa34ffc9f0f339917e8de95-Micha</Mailbox>
                  <Status>Pending</Status>
                  <AdditionalInfo/>
               </MailboxHoldStatus>
            </MailboxHoldStatuses>
         </MailboxHoldResult>
      </SetHoldOnMailboxesResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="8fc7a-144">响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="8fc7a-144">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="8fc7a-145">SetHoldOnMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="8fc7a-145">SetHoldOnMailboxesResponse</span></span>](setholdonmailboxesresponse.md)
    
- [<span data-ttu-id="8fc7a-146">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="8fc7a-146">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="8fc7a-147">MailboxHoldResult</span><span class="sxs-lookup"><span data-stu-id="8fc7a-147">MailboxHoldResult</span></span>](mailboxholdresult.md)
    
- [<span data-ttu-id="8fc7a-148">HoldId</span><span class="sxs-lookup"><span data-stu-id="8fc7a-148">HoldId</span></span>](holdid.md)
    
- [<span data-ttu-id="8fc7a-149">Query</span><span class="sxs-lookup"><span data-stu-id="8fc7a-149">Query</span></span>](query.md)
    
- [<span data-ttu-id="8fc7a-150">MailboxHoldStatuses</span><span class="sxs-lookup"><span data-stu-id="8fc7a-150">MailboxHoldStatuses</span></span>](mailboxholdstatuses.md)
    
- [<span data-ttu-id="8fc7a-151">MailboxHoldStatus</span><span class="sxs-lookup"><span data-stu-id="8fc7a-151">MailboxHoldStatus</span></span>](mailboxholdstatus.md)
    
- [<span data-ttu-id="8fc7a-152">邮箱 (字符串)</span><span class="sxs-lookup"><span data-stu-id="8fc7a-152">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="8fc7a-153">状态（HoldStatusType）</span><span class="sxs-lookup"><span data-stu-id="8fc7a-153">Status (HoldStatusType)</span></span>](status-holdstatustype.md)
    
- [<span data-ttu-id="8fc7a-154">AdditionalInfo</span><span class="sxs-lookup"><span data-stu-id="8fc7a-154">AdditionalInfo</span></span>](additionalinfo.md)
    
## <a name="setholdonmailboxes-operation-error-response"></a><span data-ttu-id="8fc7a-155">SetHoldOnMailboxes 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="8fc7a-155">SetHoldOnMailboxes operation error response</span></span>

<span data-ttu-id="8fc7a-156">下面的示例演示对**SetHoldOnMailboxes**操作请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="8fc7a-156">The following example shows an error response to a **SetHoldOnMailboxes** operation request.</span></span> <span data-ttu-id="8fc7a-157">这是对包含错误指定的邮箱标识符的请求的响应。</span><span class="sxs-lookup"><span data-stu-id="8fc7a-157">This is a response to a request that contains an incorrectly specified mailbox identifier.</span></span> 
  
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
      <SetHoldOnMailboxesResponse ResponseClass="Error" 
                                  xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>No mailbox is specified for hold operation. If specified in the request, then it could be the object does not exist in AD or is a Distribution Group.</MessageText>
         <ResponseCode>ErrorInvalidOperation</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </SetHoldOnMailboxesResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="8fc7a-158">错误响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="8fc7a-158">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="8fc7a-159">SetHoldOnMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="8fc7a-159">SetHoldOnMailboxesResponse</span></span>](setholdonmailboxesresponse.md)
    
- [<span data-ttu-id="8fc7a-160">MessageText</span><span class="sxs-lookup"><span data-stu-id="8fc7a-160">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="8fc7a-161">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="8fc7a-161">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="8fc7a-162">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="8fc7a-162">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="8fc7a-163">有关对 EWS 通用的其他错误代码以及特定于此操作的错误代码，请参阅[ResponseCode](responsecode.md)。</span><span class="sxs-lookup"><span data-stu-id="8fc7a-163">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8fc7a-164">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8fc7a-164">See also</span></span>

- [<span data-ttu-id="8fc7a-165">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="8fc7a-165">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="8fc7a-166">GetSearchableMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="8fc7a-166">GetSearchableMailboxes operation</span></span>](getsearchablemailboxes-operation.md)
    
- [<span data-ttu-id="8fc7a-167">SearchMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="8fc7a-167">SearchMailboxes operation</span></span>](searchmailboxes-operation.md)
    
- [<span data-ttu-id="8fc7a-168">GetHoldOnMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="8fc7a-168">GetHoldOnMailboxes operation</span></span>](getholdonmailboxes-operation.md)
    
- [<span data-ttu-id="8fc7a-169">GetDiscoverySearchConfiguration 操作</span><span class="sxs-lookup"><span data-stu-id="8fc7a-169">GetDiscoverySearchConfiguration operation</span></span>](getdiscoverysearchconfiguration-operation.md)
    
- [<span data-ttu-id="8fc7a-170">GetNonIndexableItemDetails 操作</span><span class="sxs-lookup"><span data-stu-id="8fc7a-170">GetNonIndexableItemDetails operation</span></span>](getnonindexableitemdetails-operation.md)
    
- [<span data-ttu-id="8fc7a-171">GetNonIndexableItemStatistics 操作</span><span class="sxs-lookup"><span data-stu-id="8fc7a-171">GetNonIndexableItemStatistics operation</span></span>](getnonindexableitemstatistics-operation.md)
    

