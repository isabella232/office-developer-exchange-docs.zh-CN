---
title: SetHoldOnMailboxes 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9015a0d8-3495-461b-aa79-797d23169585
description: 查找信息 SetHoldOnMailboxes EWS 操作。
ms.openlocfilehash: 1091ed14ceb25dfd275499b9db47ae4e41b5f1a0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827412"
---
# <a name="setholdonmailboxes-operation"></a><span data-ttu-id="0c8fa-103">SetHoldOnMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="0c8fa-103">SetHoldOnMailboxes operation</span></span>

<span data-ttu-id="0c8fa-104">查找有关**SetHoldOnMailboxes** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="0c8fa-104">Find information about the **SetHoldOnMailboxes** EWS operation.</span></span> 
  
<span data-ttu-id="0c8fa-105">**SetHoldOnMailboxes**操作邮箱上设置邮箱保留策略。</span><span class="sxs-lookup"><span data-stu-id="0c8fa-105">The **SetHoldOnMailboxes** operation sets a mailbox hold policy on mailboxes.</span></span> 
  
<span data-ttu-id="0c8fa-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="0c8fa-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-setholdonmailboxes-operation"></a><span data-ttu-id="0c8fa-107">使用 SetHoldOnMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="0c8fa-107">Using the SetHoldOnMailboxes operation</span></span>

<span data-ttu-id="0c8fa-108">**SetHoldOnMailboxes**操作将在邮箱保留设置为一个或多个邮箱。</span><span class="sxs-lookup"><span data-stu-id="0c8fa-108">The **SetHoldOnMailboxes** operation sets a mailbox hold on to one or more mailboxes.</span></span> 
  
### <a name="setholdonmailboxes-operation-soap-headers"></a><span data-ttu-id="0c8fa-109">SetHoldOnMailboxes 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="0c8fa-109">SetHoldOnMailboxes operation SOAP headers</span></span>

<span data-ttu-id="0c8fa-110">**SetHoldOnMailboxes**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="0c8fa-110">The **SetHoldOnMailboxes** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="0c8fa-111">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="0c8fa-111">**Header name**</span></span>|<span data-ttu-id="0c8fa-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="0c8fa-112">**Element**</span></span>|<span data-ttu-id="0c8fa-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="0c8fa-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0c8fa-114">**ManagementRole**</span><span class="sxs-lookup"><span data-stu-id="0c8fa-114">**ManagementRole**</span></span> <br/> |[<span data-ttu-id="0c8fa-115">ManagementRole</span><span class="sxs-lookup"><span data-stu-id="0c8fa-115">ManagementRole</span></span>](managementrole.md) <br/> |<span data-ttu-id="0c8fa-116">标识服务器角色所需顺序呼叫者发出请求。</span><span class="sxs-lookup"><span data-stu-id="0c8fa-116">Identifies the server roles that are necessary in order for the caller to make the request.</span></span> <span data-ttu-id="0c8fa-117">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="0c8fa-117">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="0c8fa-118">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="0c8fa-118">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="0c8fa-119">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="0c8fa-119">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="0c8fa-120">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="0c8fa-120">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="0c8fa-121">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="0c8fa-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="0c8fa-122">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="0c8fa-122">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="0c8fa-123">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="0c8fa-123">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="0c8fa-124">标识响应该请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="0c8fa-124">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="0c8fa-125">适用于响应此标头。</span><span class="sxs-lookup"><span data-stu-id="0c8fa-125">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="setholdonmailboxes-operation-request-example-apply-a-hold-on-a-mailbox"></a><span data-ttu-id="0c8fa-126">SetHoldOnMailboxes 操作请求示例： 对邮箱应用保留</span><span class="sxs-lookup"><span data-stu-id="0c8fa-126">SetHoldOnMailboxes operation request example: Apply a hold on a mailbox</span></span>

<span data-ttu-id="0c8fa-127">**SetHoldOnMailboxes**操作请求的下面的示例演示如何在两个邮箱应用保留。</span><span class="sxs-lookup"><span data-stu-id="0c8fa-127">The following example of a **SetHoldOnMailboxes** operation request shows how to apply a hold on two mailboxes.</span></span> <span data-ttu-id="0c8fa-128">使用[New-mailboxsearch](http://technet.microsoft.com/zh-cn/library/dd298064.aspx)命令创建邮箱保留项。</span><span class="sxs-lookup"><span data-stu-id="0c8fa-128">The mailbox hold was created by using the [New-MailboxSearch](http://technet.microsoft.com/zh-cn/library/dd298064.aspx) command.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="0c8fa-129">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="0c8fa-129">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="0c8fa-130">SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="0c8fa-130">SetHoldOnMailboxes</span></span>](setholdonmailboxes.md)
    
- [<span data-ttu-id="0c8fa-131">ActionType (HoldActionType)</span><span class="sxs-lookup"><span data-stu-id="0c8fa-131">ActionType (HoldActionType)</span></span>](actiontype-holdactiontype.md)
    
- [<span data-ttu-id="0c8fa-132">HoldId</span><span class="sxs-lookup"><span data-stu-id="0c8fa-132">HoldId</span></span>](holdid.md)
    
- [<span data-ttu-id="0c8fa-133">Query</span><span class="sxs-lookup"><span data-stu-id="0c8fa-133">Query</span></span>](query.md)
    
- [<span data-ttu-id="0c8fa-134">邮箱 (ArrayOfStringsType)</span><span class="sxs-lookup"><span data-stu-id="0c8fa-134">Mailboxes (ArrayOfStringsType)</span></span>](mailboxes-arrayofstringstype.md)
    
- [<span data-ttu-id="0c8fa-135">字符串</span><span class="sxs-lookup"><span data-stu-id="0c8fa-135">String</span></span>](string.md)
    
- [<span data-ttu-id="0c8fa-136">Language</span><span class="sxs-lookup"><span data-stu-id="0c8fa-136">Language</span></span>](language.md)
    
- [<span data-ttu-id="0c8fa-137">IncludeNonIndexableItems</span><span class="sxs-lookup"><span data-stu-id="0c8fa-137">IncludeNonIndexableItems</span></span>](includenonindexableitems.md)
    
- [<span data-ttu-id="0c8fa-138">消除</span><span class="sxs-lookup"><span data-stu-id="0c8fa-138">Deduplication</span></span>](deduplication.md)
    
## <a name="successful-setholdonmailboxes-operation-response"></a><span data-ttu-id="0c8fa-139">成功 SetHoldOnMailboxes 操作响应</span><span class="sxs-lookup"><span data-stu-id="0c8fa-139">Successful SetHoldOnMailboxes operation response</span></span>

<span data-ttu-id="0c8fa-140">下面的示例演示成功响应**SetHoldOnMailboxes**操作请求要将两个邮箱置于保留。</span><span class="sxs-lookup"><span data-stu-id="0c8fa-140">The following example shows a successful response to a **SetHoldOnMailboxes** operation request to put two mailboxes on hold.</span></span> 
  
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
      <SetHoldOnMailboxesResponse ResponseClass="Success" 
                                  xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <MailboxHoldResult>
            <HoldId xmlns="http://schemas.microsoft.com/exchange/services/2006/types">HoldId2</HoldId>
            <Query xmlns="http://schemas.microsoft.com/exchange/services/2006/types">test</Query>
            <MailboxHoldStatuses xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="0c8fa-141">响应 SOAP 正文中包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="0c8fa-141">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="0c8fa-142">SetHoldOnMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="0c8fa-142">SetHoldOnMailboxesResponse</span></span>](setholdonmailboxesresponse.md)
    
- [<span data-ttu-id="0c8fa-143">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0c8fa-143">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="0c8fa-144">MailboxHoldResult</span><span class="sxs-lookup"><span data-stu-id="0c8fa-144">MailboxHoldResult</span></span>](mailboxholdresult.md)
    
- [<span data-ttu-id="0c8fa-145">HoldId</span><span class="sxs-lookup"><span data-stu-id="0c8fa-145">HoldId</span></span>](holdid.md)
    
- [<span data-ttu-id="0c8fa-146">Query</span><span class="sxs-lookup"><span data-stu-id="0c8fa-146">Query</span></span>](query.md)
    
- [<span data-ttu-id="0c8fa-147">MailboxHoldStatuses</span><span class="sxs-lookup"><span data-stu-id="0c8fa-147">MailboxHoldStatuses</span></span>](mailboxholdstatuses.md)
    
- [<span data-ttu-id="0c8fa-148">MailboxHoldStatus</span><span class="sxs-lookup"><span data-stu-id="0c8fa-148">MailboxHoldStatus</span></span>](mailboxholdstatus.md)
    
- [<span data-ttu-id="0c8fa-149">邮箱 (字符串)</span><span class="sxs-lookup"><span data-stu-id="0c8fa-149">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="0c8fa-150">状态 (HoldStatusType)</span><span class="sxs-lookup"><span data-stu-id="0c8fa-150">Status (HoldStatusType)</span></span>](status-holdstatustype.md)
    
- [<span data-ttu-id="0c8fa-151">AdditionalInfo</span><span class="sxs-lookup"><span data-stu-id="0c8fa-151">AdditionalInfo</span></span>](additionalinfo.md)
    
## <a name="setholdonmailboxes-operation-error-response"></a><span data-ttu-id="0c8fa-152">SetHoldOnMailboxes 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="0c8fa-152">SetHoldOnMailboxes operation error response</span></span>

<span data-ttu-id="0c8fa-153">下面的示例演示对**SetHoldOnMailboxes**操作请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="0c8fa-153">The following example shows an error response to a **SetHoldOnMailboxes** operation request.</span></span> <span data-ttu-id="0c8fa-154">这是包含正确指定的邮箱标识符请求的响应。</span><span class="sxs-lookup"><span data-stu-id="0c8fa-154">This is a response to a request that contains an incorrectly specified mailbox identifier.</span></span> 
  
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
      <SetHoldOnMailboxesResponse ResponseClass="Error" 
                                  xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>No mailbox is specified for hold operation. If specified in the request, then it could be the object does not exist in AD or is a Distribution Group.</MessageText>
         <ResponseCode>ErrorInvalidOperation</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </SetHoldOnMailboxesResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="0c8fa-155">错误响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="0c8fa-155">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="0c8fa-156">SetHoldOnMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="0c8fa-156">SetHoldOnMailboxesResponse</span></span>](setholdonmailboxesresponse.md)
    
- [<span data-ttu-id="0c8fa-157">MessageText</span><span class="sxs-lookup"><span data-stu-id="0c8fa-157">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="0c8fa-158">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0c8fa-158">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="0c8fa-159">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="0c8fa-159">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="0c8fa-160">通用到 EWS 且特定于此操作的其他错误代码，请参阅[ResponseCode](responsecode.md)。</span><span class="sxs-lookup"><span data-stu-id="0c8fa-160">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0c8fa-161">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0c8fa-161">See also</span></span>

- [<span data-ttu-id="0c8fa-162">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="0c8fa-162">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="0c8fa-163">GetSearchableMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="0c8fa-163">GetSearchableMailboxes operation</span></span>](getsearchablemailboxes-operation.md)
    
- [<span data-ttu-id="0c8fa-164">SearchMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="0c8fa-164">SearchMailboxes operation</span></span>](searchmailboxes-operation.md)
    
- [<span data-ttu-id="0c8fa-165">GetHoldOnMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="0c8fa-165">GetHoldOnMailboxes operation</span></span>](getholdonmailboxes-operation.md)
    
- [<span data-ttu-id="0c8fa-166">GetDiscoverySearchConfiguration 操作</span><span class="sxs-lookup"><span data-stu-id="0c8fa-166">GetDiscoverySearchConfiguration operation</span></span>](getdiscoverysearchconfiguration-operation.md)
    
- [<span data-ttu-id="0c8fa-167">GetNonIndexableItemDetails 操作</span><span class="sxs-lookup"><span data-stu-id="0c8fa-167">GetNonIndexableItemDetails operation</span></span>](getnonindexableitemdetails-operation.md)
    
- [<span data-ttu-id="0c8fa-168">GetNonIndexableItemStatistics 操作</span><span class="sxs-lookup"><span data-stu-id="0c8fa-168">GetNonIndexableItemStatistics operation</span></span>](getnonindexableitemstatistics-operation.md)
    

