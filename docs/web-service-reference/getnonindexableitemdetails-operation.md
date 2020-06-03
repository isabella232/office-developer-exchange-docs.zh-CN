---
title: GetNonIndexableItemDetails 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9279c3ad-f7c8-4bbc-b0a7-2c78416cb39a
description: 查找有关 GetNonIndexableItemDetails EWS 操作的信息。
ms.openlocfilehash: a443e04b0622ddbaaeb1bc8c04bfd05679c6207e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530209"
---
# <a name="getnonindexableitemdetails-operation"></a><span data-ttu-id="f0204-103">GetNonIndexableItemDetails 操作</span><span class="sxs-lookup"><span data-stu-id="f0204-103">GetNonIndexableItemDetails operation</span></span>

<span data-ttu-id="f0204-104">查找有关**GetNonIndexableItemDetails** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="f0204-104">Find information about the **GetNonIndexableItemDetails** EWS operation.</span></span> 
  
<span data-ttu-id="f0204-105">**GetNonIndexableItemDetails**操作检索有关无法编制索引的项目的详细信息。</span><span class="sxs-lookup"><span data-stu-id="f0204-105">The **GetNonIndexableItemDetails** operation retrieves details about items that cannot be indexed.</span></span> <span data-ttu-id="f0204-106">这包括但不限于项目标识符、错误代码、错误说明、对项目编制索引时，以及有关文件的其他信息。</span><span class="sxs-lookup"><span data-stu-id="f0204-106">This includes, but is not limited to, the item identifier, an error code, an error description, when an attempt was made to index the item, and additional information about the file.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f0204-107">虽然架构指示可以搜索多个邮箱，但在 Exchange 2013 的初始发行版中，该服务仅支持获取单个邮箱中 nonindexable 项目的项目详细信息。</span><span class="sxs-lookup"><span data-stu-id="f0204-107">Although the schema indicates that more than one mailbox can be searched, in the initial release version of Exchange 2013, the service only supports getting item details for nonindexable items in a single mailbox.</span></span> 
  
<span data-ttu-id="f0204-108">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="f0204-108">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getnonindexableitemdetails-operation"></a><span data-ttu-id="f0204-109">使用 GetNonIndexableItemDetails 操作</span><span class="sxs-lookup"><span data-stu-id="f0204-109">Using the GetNonIndexableItemDetails operation</span></span>

<span data-ttu-id="f0204-110">**GetNonIndexableItemDetails**操作标识无法编制索引的邮箱项目，并提供有关无法对这些项目编制索引的原因的信息。</span><span class="sxs-lookup"><span data-stu-id="f0204-110">The **GetNonIndexableItemDetails** operation identifies mailbox items that cannot be indexed and provides information about why the items cannot be indexed.</span></span> <span data-ttu-id="f0204-111">在发现搜索过程中不会搜索无法编制索引的项目。</span><span class="sxs-lookup"><span data-stu-id="f0204-111">Items that cannot be indexed are not searched during a discovery search.</span></span> 
  
### <a name="getnonindexableitemdetails-operation-soap-headers"></a><span data-ttu-id="f0204-112">GetNonIndexableItemDetails 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="f0204-112">GetNonIndexableItemDetails operation SOAP headers</span></span>

<span data-ttu-id="f0204-113">**GetNonIndexableItemDetails**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="f0204-113">The **GetNonIndexableItemDetails** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="f0204-114">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="f0204-114">**Header name**</span></span>|<span data-ttu-id="f0204-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="f0204-115">**Element**</span></span>|<span data-ttu-id="f0204-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="f0204-116">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f0204-117">**Get-managementrole**</span><span class="sxs-lookup"><span data-stu-id="f0204-117">**ManagementRole**</span></span> <br/> |[<span data-ttu-id="f0204-118">Get-managementrole</span><span class="sxs-lookup"><span data-stu-id="f0204-118">ManagementRole</span></span>](managementrole.md) <br/> |<span data-ttu-id="f0204-119">标识调用方发出请求所需的服务器角色。</span><span class="sxs-lookup"><span data-stu-id="f0204-119">Identifies the server roles that are necessary in order for the caller to make the request.</span></span> <span data-ttu-id="f0204-120">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="f0204-120">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="f0204-121">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="f0204-121">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="f0204-122">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="f0204-122">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="f0204-123">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="f0204-123">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="f0204-124">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="f0204-124">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="f0204-125">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="f0204-125">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="f0204-126">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="f0204-126">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="f0204-127">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="f0204-127">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="f0204-128">此标头适用于响应。</span><span class="sxs-lookup"><span data-stu-id="f0204-128">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getnonindexableitemdetails-operation-request-example-get-the-details-of-an-item-that-cannot-be-indexed"></a><span data-ttu-id="f0204-129">GetNonIndexableItemDetails 操作请求示例：获取无法编制索引的项目的详细信息</span><span class="sxs-lookup"><span data-stu-id="f0204-129">GetNonIndexableItemDetails operation request example: Get the details of an item that cannot be indexed</span></span>

<span data-ttu-id="f0204-130">以下示例的**GetNonIndexableItemDetails**操作请求显示如何请求无法为单个邮箱编制索引的项目的详细信息。</span><span class="sxs-lookup"><span data-stu-id="f0204-130">The following example of a **GetNonIndexableItemDetails** operation request shows how to request the details for items that cannot be indexed for a single mailbox.</span></span> <span data-ttu-id="f0204-131">同时在主邮箱和存档邮箱中执行搜索。</span><span class="sxs-lookup"><span data-stu-id="f0204-131">The search is performed across both primary and archive mailboxes.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f0204-132">此示例中的所有旧版域名都将被缩短以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="f0204-132">All legacy domain names in this example have be shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:GetNonIndexableItemDetails>
         <m:Mailboxes>
            <t:LegacyDN>/o=First Organization/ou=Exchange Administrative Group (FYT)/cn=Recipients/cn=35-Steve</t:LegacyDN>
         </m:Mailboxes>
         <m:SearchArchiveOnly>false</m:SearchArchiveOnly>
      </m:GetNonIndexableItemDetails>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="f0204-133">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="f0204-133">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="f0204-134">GetNonIndexableItemDetails</span><span class="sxs-lookup"><span data-stu-id="f0204-134">GetNonIndexableItemDetails</span></span>](getnonindexableitemdetails.md)
    
- [<span data-ttu-id="f0204-135">邮箱（NonEmptyArrayOfLegacyDNsType）</span><span class="sxs-lookup"><span data-stu-id="f0204-135">Mailboxes (NonEmptyArrayOfLegacyDNsType)</span></span>](mailboxes-nonemptyarrayoflegacydnstype.md)
    
- [<span data-ttu-id="f0204-136">LegacyDN</span><span class="sxs-lookup"><span data-stu-id="f0204-136">LegacyDN</span></span>](legacydn.md)
    
- [<span data-ttu-id="f0204-137">SearchArchiveOnly</span><span class="sxs-lookup"><span data-stu-id="f0204-137">SearchArchiveOnly</span></span>](searcharchiveonly.md)
    
## <a name="successful-getnonindexableitemdetails-operation-response"></a><span data-ttu-id="f0204-138">成功的 GetNonIndexableItemDetails 操作响应</span><span class="sxs-lookup"><span data-stu-id="f0204-138">Successful GetNonIndexableItemDetails operation response</span></span>

<span data-ttu-id="f0204-139">下面的示例演示对**GetNonIndexableItemDetails**操作请求的成功响应，以获取无法为单个邮箱编制索引的项目。</span><span class="sxs-lookup"><span data-stu-id="f0204-139">The following example shows a successful response to a **GetNonIndexableItemDetails** operation request to get items that cannot be indexed for a single mailbox.</span></span> <span data-ttu-id="f0204-140">此示例中无法编制索引的项目是 binaryfile 文件，该文件的格式未知。</span><span class="sxs-lookup"><span data-stu-id="f0204-140">The item in this example that cannot be indexed is the binaryfile.abc file, which is of an unknown format.</span></span> 
  
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
      <GetNonIndexableItemDetailsResponse ResponseClass="Success" 
                                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <NonIndexableItemDetailsResult>
            <Items xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <NonIndexableItemDetail>
                  <ItemId Id="AQMkAGVmNDAyOQAAAY2fUAAAAA==" ChangeKey="CQAAAA=="/>
                  <ErrorCode>DocumentParserFailure</ErrorCode>
                  <ErrorDescription>The document parser encountered a processing error.</ErrorDescription>
                  <IsPartiallyIndexed>false</IsPartiallyIndexed>
                  <IsPermanentFailure>true</IsPermanentFailure>
                  <SortValue>502511175756</SortValue>
                  <AttemptCount>0</AttemptCount>
                  <LastAttemptTime>2012-11-15T01:56:11Z</LastAttemptTime>
                  <AdditionalInfo> 301002 Error parsing document 'exchange://localhost/Attachment/d987b1f4-9aa7-42b3-aa8c-9515a35dfa1a/1f3047d4-c287-41e4-910c-feb70c1a59f0/ef402830-3d33-4a0d-a4e9-d8576900060d/85b83861-0026-418f-8464-be2036696333/502511175756.0/binaryfile.abc'. Document has an undetectable format and will not be parsed.</AdditionalInfo>
               </NonIndexableItemDetail>
            </Items>
         </NonIndexableItemDetailsResult>
      </GetNonIndexableItemDetailsResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="f0204-141">响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="f0204-141">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="f0204-142">GetNonIndexableItemDetailsResponse</span><span class="sxs-lookup"><span data-stu-id="f0204-142">GetNonIndexableItemDetailsResponse</span></span>](getnonindexableitemdetailsresponse.md)
    
- [<span data-ttu-id="f0204-143">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f0204-143">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="f0204-144">NonIndexableItemDetailsResult</span><span class="sxs-lookup"><span data-stu-id="f0204-144">NonIndexableItemDetailsResult</span></span>](nonindexableitemdetailsresult.md)
    
- [<span data-ttu-id="f0204-145">NonIndexableItemDetail</span><span class="sxs-lookup"><span data-stu-id="f0204-145">NonIndexableItemDetail</span></span>](nonindexableitemdetail.md)
    
- [<span data-ttu-id="f0204-146">ItemId</span><span class="sxs-lookup"><span data-stu-id="f0204-146">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="f0204-147">ErrorCode （ItemIndexErrorType）</span><span class="sxs-lookup"><span data-stu-id="f0204-147">ErrorCode (ItemIndexErrorType)</span></span>](errorcode-itemindexerrortype.md)
    
- [<span data-ttu-id="f0204-148">ErrorDescription</span><span class="sxs-lookup"><span data-stu-id="f0204-148">ErrorDescription</span></span>](errordescription.md)
    
- [<span data-ttu-id="f0204-149">IsPartiallyIndexed</span><span class="sxs-lookup"><span data-stu-id="f0204-149">IsPartiallyIndexed</span></span>](ispartiallyindexed.md)
    
- [<span data-ttu-id="f0204-150">IsPermanentFailure</span><span class="sxs-lookup"><span data-stu-id="f0204-150">IsPermanentFailure</span></span>](ispermanentfailure.md)
    
- [<span data-ttu-id="f0204-151">SortValue</span><span class="sxs-lookup"><span data-stu-id="f0204-151">SortValue</span></span>](sortvalue.md)
    
- [<span data-ttu-id="f0204-152">AttemptCount</span><span class="sxs-lookup"><span data-stu-id="f0204-152">AttemptCount</span></span>](attemptcount.md)
    
- [<span data-ttu-id="f0204-153">LastAttemptTime</span><span class="sxs-lookup"><span data-stu-id="f0204-153">LastAttemptTime</span></span>](lastattempttime.md)
    
- [<span data-ttu-id="f0204-154">AdditionalInfo</span><span class="sxs-lookup"><span data-stu-id="f0204-154">AdditionalInfo</span></span>](additionalinfo.md)
    
## <a name="getnonindexableitemdetails-operation-error-response"></a><span data-ttu-id="f0204-155">GetNonIndexableItemDetails 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="f0204-155">GetNonIndexableItemDetails operation error response</span></span>

<span data-ttu-id="f0204-156">下面的示例演示对**GetNonIndexableItemDetails**操作请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="f0204-156">The following example shows an error response to a **GetNonIndexableItemDetails** operation request.</span></span> <span data-ttu-id="f0204-157">这是对获取无法从多个邮箱编制索引的项目的项目详细信息的请求的响应。</span><span class="sxs-lookup"><span data-stu-id="f0204-157">This is a response to a request to get item details for items that cannot be indexed from more than one mailbox.</span></span> 
  
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
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetNonIndexableItemDetailsResponse ResponseClass="Error" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Multiple mailboxes is currently not supported, only single mailbox is supported.</MessageText>
         <ResponseCode>ErrorInvalidArgument</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </GetNonIndexableItemDetailsResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="f0204-158">错误响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="f0204-158">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="f0204-159">GetNonIndexableItemDetailsResponse</span><span class="sxs-lookup"><span data-stu-id="f0204-159">GetNonIndexableItemDetailsResponse</span></span>](getnonindexableitemdetailsresponse.md)
    
- [<span data-ttu-id="f0204-160">MessageText</span><span class="sxs-lookup"><span data-stu-id="f0204-160">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="f0204-161">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f0204-161">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="f0204-162">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="f0204-162">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="f0204-163">有关对 EWS 通用的其他错误代码以及特定于此操作的错误代码，请参阅[ResponseCode](responsecode.md)。</span><span class="sxs-lookup"><span data-stu-id="f0204-163">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f0204-164">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f0204-164">See also</span></span>

- [<span data-ttu-id="f0204-165">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="f0204-165">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="f0204-166">GetSearchableMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="f0204-166">GetSearchableMailboxes operation</span></span>](getsearchablemailboxes-operation.md)
    
- [<span data-ttu-id="f0204-167">SearchMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="f0204-167">SearchMailboxes operation</span></span>](searchmailboxes-operation.md)
    
- [<span data-ttu-id="f0204-168">GetHoldOnMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="f0204-168">GetHoldOnMailboxes operation</span></span>](getholdonmailboxes-operation.md)
    
- [<span data-ttu-id="f0204-169">SetHoldOnMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="f0204-169">SetHoldOnMailboxes operation</span></span>](setholdonmailboxes-operation.md)
    
- [<span data-ttu-id="f0204-170">GetDiscoverySearchConfiguration 操作</span><span class="sxs-lookup"><span data-stu-id="f0204-170">GetDiscoverySearchConfiguration operation</span></span>](getdiscoverysearchconfiguration-operation.md)
    
- [<span data-ttu-id="f0204-171">GetNonIndexableItemStatistics 操作</span><span class="sxs-lookup"><span data-stu-id="f0204-171">GetNonIndexableItemStatistics operation</span></span>](getnonindexableitemstatistics-operation.md)
    

