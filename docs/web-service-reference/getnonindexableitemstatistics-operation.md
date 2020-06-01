---
title: GetNonIndexableItemStatistics 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ed077877-9d98-4434-b8b6-a4a905e7f7a6
description: 查找有关 GetNonIndexableItemStatistics EWS 操作的信息。
ms.openlocfilehash: c7d49f9e0d7b4191c7403cb4d1a20e70a96c3882
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44452816"
---
# <a name="getnonindexableitemstatistics-operation"></a><span data-ttu-id="e6b78-103">GetNonIndexableItemStatistics 操作</span><span class="sxs-lookup"><span data-stu-id="e6b78-103">GetNonIndexableItemStatistics operation</span></span>

<span data-ttu-id="e6b78-104">查找有关**GetNonIndexableItemStatistics** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="e6b78-104">Find information about the **GetNonIndexableItemStatistics** EWS operation.</span></span> 
  
<span data-ttu-id="e6b78-105">**GetNonIndexableItemStatistics**操作检索邮箱中无法编制索引的项目数。</span><span class="sxs-lookup"><span data-stu-id="e6b78-105">The **GetNonIndexableItemStatistics** operation retrieves the count of items that cannot be indexed in a mailbox.</span></span> 
  
<span data-ttu-id="e6b78-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="e6b78-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getnonindexableitemstatistics-operation"></a><span data-ttu-id="e6b78-107">使用 GetNonIndexableItemStatistics 操作</span><span class="sxs-lookup"><span data-stu-id="e6b78-107">Using the GetNonIndexableItemStatistics operation</span></span>

<span data-ttu-id="e6b78-108">**GetNonIndexableItemStatistics**操作对无法编制索引的邮箱项目计数。</span><span class="sxs-lookup"><span data-stu-id="e6b78-108">The **GetNonIndexableItemStatistics** operation counts mailbox items that cannot be indexed.</span></span> <span data-ttu-id="e6b78-109">在发现搜索过程中不会搜索无法编制索引的项目。</span><span class="sxs-lookup"><span data-stu-id="e6b78-109">Items that cannot be indexed are not searched during a discovery search.</span></span> 
  
### <a name="getnonindexableitemstatistics-operation-soap-headers"></a><span data-ttu-id="e6b78-110">GetNonIndexableItemStatistics 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="e6b78-110">GetNonIndexableItemStatistics operation SOAP headers</span></span>

<span data-ttu-id="e6b78-111">**GetNonIndexableItemStatistics**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="e6b78-111">The **GetNonIndexableItemStatistics** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="e6b78-112">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="e6b78-112">**Header name**</span></span>|<span data-ttu-id="e6b78-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="e6b78-113">**Element**</span></span>|<span data-ttu-id="e6b78-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="e6b78-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e6b78-115">**Get-managementrole**</span><span class="sxs-lookup"><span data-stu-id="e6b78-115">**ManagementRole**</span></span> <br/> |[<span data-ttu-id="e6b78-116">Get-managementrole</span><span class="sxs-lookup"><span data-stu-id="e6b78-116">ManagementRole</span></span>](managementrole.md) <br/> |<span data-ttu-id="e6b78-117">标识调用方发出请求所需的服务器角色。</span><span class="sxs-lookup"><span data-stu-id="e6b78-117">Identifies the server roles that are necessary in order for the caller to make the request.</span></span> <span data-ttu-id="e6b78-118">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="e6b78-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="e6b78-119">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="e6b78-119">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="e6b78-120">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="e6b78-120">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="e6b78-121">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="e6b78-121">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="e6b78-122">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="e6b78-122">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="e6b78-123">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="e6b78-123">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="e6b78-124">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="e6b78-124">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="e6b78-125">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="e6b78-125">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="e6b78-126">此标头适用于响应。</span><span class="sxs-lookup"><span data-stu-id="e6b78-126">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getnonindexableitemstatistics-operation-request-example-get-the-count-of-items-that-cannot-be-indexed-in-a-mailbox"></a><span data-ttu-id="e6b78-127">GetNonIndexableItemStatistics 操作请求示例：获取邮箱中无法编制索引的项的计数</span><span class="sxs-lookup"><span data-stu-id="e6b78-127">GetNonIndexableItemStatistics operation request example: Get the count of items that cannot be indexed in a mailbox</span></span>

<span data-ttu-id="e6b78-128">以下示例的**GetNonIndexableItemStatistics**操作请求显示如何请求邮箱中无法编制索引的项目数。</span><span class="sxs-lookup"><span data-stu-id="e6b78-128">The following example of a **GetNonIndexableItemStatistics** operation request shows how to request the count of items that cannot be indexed in a mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e6b78-129">此示例中的所有旧版域名都将被缩短以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="e6b78-129">All legacy domain names in this example have be shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:GetNonIndexableItemStatistics>
         <m:Mailboxes>
            <t:LegacyDN>/o=First Organization/ou=Exchange Administrative Group (FYDIDLT)/cn=Recipients/cn=3518cf-Steve</t:LegacyDN>
         </m:Mailboxes>
         <m:SearchArchiveOnly>false</m:SearchArchiveOnly>
      </m:GetNonIndexableItemStatistics>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="e6b78-130">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="e6b78-130">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="e6b78-131">GetNonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="e6b78-131">GetNonIndexableItemStatistics</span></span>](getnonindexableitemstatistics.md)
    
- [<span data-ttu-id="e6b78-132">邮箱（NonEmptyArrayOfLegacyDNsType）</span><span class="sxs-lookup"><span data-stu-id="e6b78-132">Mailboxes (NonEmptyArrayOfLegacyDNsType)</span></span>](mailboxes-nonemptyarrayoflegacydnstype.md)
    
- [<span data-ttu-id="e6b78-133">LegacyDN</span><span class="sxs-lookup"><span data-stu-id="e6b78-133">LegacyDN</span></span>](legacydn.md)
    
- [<span data-ttu-id="e6b78-134">SearchArchiveOnly</span><span class="sxs-lookup"><span data-stu-id="e6b78-134">SearchArchiveOnly</span></span>](searcharchiveonly.md)
    
## <a name="successful-getnonindexableitemstatistics-operation-response"></a><span data-ttu-id="e6b78-135">成功的 GetNonIndexableItemStatistics 操作响应</span><span class="sxs-lookup"><span data-stu-id="e6b78-135">Successful GetNonIndexableItemStatistics operation response</span></span>

<span data-ttu-id="e6b78-136">下面的示例演示对**GetNonIndexableItemStatistics**操作请求的成功响应，以获取无法在邮箱中编制索引的项的计数。</span><span class="sxs-lookup"><span data-stu-id="e6b78-136">The following example shows a successful response to a **GetNonIndexableItemStatistics** operation request to get the count of items that cannot be indexed in a mailbox.</span></span> 
  
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
      <GetNonIndexableItemStatisticsResponse ResponseClass="Success" 
                                             xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <NonIndexableItemStatistics>
            <NonIndexableItemStatistic xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYT)/cn=Recipients/cn=35181acf-Steve</Mailbox>
               <ItemCount>2</ItemCount>
            </NonIndexableItemStatistic>
         </NonIndexableItemStatistics>
      </GetNonIndexableItemStatisticsResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="e6b78-137">响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="e6b78-137">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="e6b78-138">GetNonIndexableItemStatisticsResponse</span><span class="sxs-lookup"><span data-stu-id="e6b78-138">GetNonIndexableItemStatisticsResponse</span></span>](getnonindexableitemstatisticsresponse.md)
    
- [<span data-ttu-id="e6b78-139">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e6b78-139">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="e6b78-140">NonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="e6b78-140">NonIndexableItemStatistics</span></span>](nonindexableitemstatistics.md)
    
- [<span data-ttu-id="e6b78-141">NonIndexableItemStatistic</span><span class="sxs-lookup"><span data-stu-id="e6b78-141">NonIndexableItemStatistic</span></span>](nonindexableitemstatistic.md)
    
- [<span data-ttu-id="e6b78-142">邮箱 (字符串)</span><span class="sxs-lookup"><span data-stu-id="e6b78-142">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="e6b78-143">ItemCount</span><span class="sxs-lookup"><span data-stu-id="e6b78-143">ItemCount</span></span>](itemcount.md)
    
## <a name="getnonindexableitemstatistics-operation-error-response"></a><span data-ttu-id="e6b78-144">GetNonIndexableItemStatistics 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="e6b78-144">GetNonIndexableItemStatistics operation error response</span></span>

<span data-ttu-id="e6b78-145">下面的示例演示对**GetNonIndexableItemStatistics**操作请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="e6b78-145">The following example shows an error response to a **GetNonIndexableItemStatistics** operation request.</span></span> <span data-ttu-id="e6b78-146">这是对获取无法从多个邮箱编制索引的项目数的请求的响应。</span><span class="sxs-lookup"><span data-stu-id="e6b78-146">This is a response to a request to get the count of items that cannot be indexed from more than one mailbox.</span></span> 
  
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
      <GetNonIndexableItemStatisticsResponse ResponseClass="Error" 
                                             xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Multiple mailboxes is currently not supported, only single mailbox is supported.</MessageText>
         <ResponseCode>ErrorInvalidArgument</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </GetNonIndexableItemStatisticsResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="e6b78-147">错误响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="e6b78-147">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="e6b78-148">GetNonIndexableItemStatisticsResponse</span><span class="sxs-lookup"><span data-stu-id="e6b78-148">GetNonIndexableItemStatisticsResponse</span></span>](getnonindexableitemstatisticsresponse.md)
    
- [<span data-ttu-id="e6b78-149">MessageText</span><span class="sxs-lookup"><span data-stu-id="e6b78-149">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="e6b78-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e6b78-150">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="e6b78-151">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="e6b78-151">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="e6b78-152">有关对 EWS 通用的其他错误代码以及特定于此操作的错误代码，请参阅[ResponseCode](responsecode.md)。</span><span class="sxs-lookup"><span data-stu-id="e6b78-152">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e6b78-153">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e6b78-153">See also</span></span>

- [<span data-ttu-id="e6b78-154">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="e6b78-154">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="e6b78-155">GetSearchableMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="e6b78-155">GetSearchableMailboxes operation</span></span>](getsearchablemailboxes-operation.md)
    
- [<span data-ttu-id="e6b78-156">SearchMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="e6b78-156">SearchMailboxes operation</span></span>](searchmailboxes-operation.md)
    
- [<span data-ttu-id="e6b78-157">GetHoldOnMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="e6b78-157">GetHoldOnMailboxes operation</span></span>](getholdonmailboxes-operation.md)
    
- [<span data-ttu-id="e6b78-158">SetHoldOnMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="e6b78-158">SetHoldOnMailboxes operation</span></span>](setholdonmailboxes-operation.md)
    
- [<span data-ttu-id="e6b78-159">GetDiscoverySearchConfiguration 操作</span><span class="sxs-lookup"><span data-stu-id="e6b78-159">GetDiscoverySearchConfiguration operation</span></span>](getdiscoverysearchconfiguration-operation.md)
    
- [<span data-ttu-id="e6b78-160">GetNonIndexableItemDetails 操作</span><span class="sxs-lookup"><span data-stu-id="e6b78-160">GetNonIndexableItemDetails operation</span></span>](getnonindexableitemdetails-operation.md)
    

