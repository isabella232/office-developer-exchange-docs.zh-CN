---
title: SearchMailboxes 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8a67c1d8-d021-4e68-aa62-35f7d9c2edc7
description: 查找有关 SearchMailboxes EWS 操作的信息。
ms.openlocfilehash: 9ec7e9dd4ef17f22f236e64ca1fdbeb65e6e56fe
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456751"
---
# <a name="searchmailboxes-operation"></a><span data-ttu-id="43a9c-103">SearchMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="43a9c-103">SearchMailboxes operation</span></span>

> [!NOTE]
> <span data-ttu-id="43a9c-104">此操作已弃用，Microsoft 不再支持它。</span><span class="sxs-lookup"><span data-stu-id="43a9c-104">This operation is deprecated, and no longer supported by Microsoft.</span></span>  <span data-ttu-id="43a9c-105">作为替换，请使用[FindItem](finditem-operation.md)操作。</span><span class="sxs-lookup"><span data-stu-id="43a9c-105">As a replacement, please use the [FindItem](finditem-operation.md) operation.</span></span>

<span data-ttu-id="43a9c-106">查找有关**SearchMailboxes** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="43a9c-106">Find information about the **SearchMailboxes** EWS operation.</span></span> 
  
<span data-ttu-id="43a9c-107">**SearchMailboxes**操作在邮箱中搜索邮箱项目中出现的术语。</span><span class="sxs-lookup"><span data-stu-id="43a9c-107">The **SearchMailboxes** operation searches mailboxes for occurrences of terms in mailbox items.</span></span> 
  
<span data-ttu-id="43a9c-108">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="43a9c-108">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-searchmailboxes-operation"></a><span data-ttu-id="43a9c-109">使用 SearchMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="43a9c-109">Using the SearchMailboxes operation</span></span>

<span data-ttu-id="43a9c-110">**SearchMailboxes**操作可以使用多个同时进行的搜索查询对多个邮箱执行发现搜索。</span><span class="sxs-lookup"><span data-stu-id="43a9c-110">The **SearchMailboxes** operation can use many simultaneous search queries to perform discovery search on multiple mailboxes.</span></span> <span data-ttu-id="43a9c-111">结果可以是有关搜索词发生次数的统计信息，也可以是包含搜索词的项目的预览。</span><span class="sxs-lookup"><span data-stu-id="43a9c-111">The results can be either statistical information about the number of times search terms occur, or a preview of the items that contain the search terms.</span></span> 
  
### <a name="searchmailboxes-operation-soap-headers"></a><span data-ttu-id="43a9c-112">SearchMailboxes 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="43a9c-112">SearchMailboxes operation SOAP headers</span></span>

<span data-ttu-id="43a9c-113">**SearchMailboxes**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="43a9c-113">The **SearchMailboxes** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="43a9c-114">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="43a9c-114">**Header name**</span></span>|<span data-ttu-id="43a9c-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="43a9c-115">**Element**</span></span>|<span data-ttu-id="43a9c-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="43a9c-116">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="43a9c-117">**Get-managementrole**</span><span class="sxs-lookup"><span data-stu-id="43a9c-117">**ManagementRole**</span></span> <br/> |[<span data-ttu-id="43a9c-118">Get-managementrole</span><span class="sxs-lookup"><span data-stu-id="43a9c-118">ManagementRole</span></span>](managementrole.md) <br/> |<span data-ttu-id="43a9c-119">标识调用方发出请求所需的服务器角色。</span><span class="sxs-lookup"><span data-stu-id="43a9c-119">Identifies the server roles that are necessary in order for the caller to make the request.</span></span> <span data-ttu-id="43a9c-120">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="43a9c-120">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="43a9c-121">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="43a9c-121">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="43a9c-122">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="43a9c-122">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="43a9c-123">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="43a9c-123">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="43a9c-124">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="43a9c-124">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="43a9c-125">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="43a9c-125">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="43a9c-126">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="43a9c-126">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="43a9c-127">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="43a9c-127">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="43a9c-128">此标头适用于响应。</span><span class="sxs-lookup"><span data-stu-id="43a9c-128">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="searchmailboxes-operation-request-example-search-mailboxes-for-number-of-search-term-hits"></a><span data-ttu-id="43a9c-129">SearchMailboxes 操作请求示例：搜索邮箱中搜索词命中数</span><span class="sxs-lookup"><span data-stu-id="43a9c-129">SearchMailboxes operation request example: Search mailboxes for number of search term hits</span></span>

<span data-ttu-id="43a9c-130">下面的**SearchMailboxes**操作请求示例演示如何使用两个不同的查询来搜索三个不同的邮箱，以获取有关每个邮箱中某个术语出现次数的统计信息。</span><span class="sxs-lookup"><span data-stu-id="43a9c-130">The following example of a **SearchMailboxes** operation request shows how to use two different queries to search three different mailboxes for statistical information about how many times a term appears in each mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="43a9c-131">在此示例中，将 intentionaly 的[查询](query.md)元素留空。</span><span class="sxs-lookup"><span data-stu-id="43a9c-131">In this example, the [Query](query.md) element is intentionaly left blank.</span></span> <span data-ttu-id="43a9c-132">这说明了成功的请求如何基于每个邮箱搜索来包含错误条件。</span><span class="sxs-lookup"><span data-stu-id="43a9c-132">This shows how a successful request can contain error conditions on a per mailbox search basis.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:SearchMailboxes>
         <m:SearchQueries>
            <t:MailboxQuery>
               <t:Query>Test Item</t:Query>
               <t:MailboxSearchScopes>
                  <t:MailboxSearchScope>
                     <t:Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYDLT)/cn=Recipients/cn=12311a742f0e47e392c8201a60d13ecf-Steve</t:Mailbox>
                     <t:SearchScope>All</t:SearchScope>
                  </t:MailboxSearchScope>
                  <t:MailboxSearchScope>
                     <t:Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYDLT)/cn=Recipients/cn=f00c9f70539844beb52341d8f40c572e-Antho</t:Mailbox>
                     <t:SearchScope>PrimaryOnly</t:SearchScope>
                  </t:MailboxSearchScope>
               </t:MailboxSearchScopes>
            </t:MailboxQuery>
            <t:MailboxQuery>
               <t:Query></t:Query>
               <t:MailboxSearchScopes>
                  <t:MailboxSearchScope>
                     <t:Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYDLT)/cn=Recipients/cn=accba4fd5ddf12214a0e82ce1645f4e-Danie</t:Mailbox>
                     <t:SearchScope>ArchiveOnly</t:SearchScope>
                  </t:MailboxSearchScope>
               </t:MailboxSearchScopes>
            </t:MailboxQuery>
         </m:SearchQueries>
         <m:ResultType>StatisticsOnly</m:ResultType>
      </m:SearchMailboxes>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="43a9c-133">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="43a9c-133">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="43a9c-134">SearchMailboxes</span><span class="sxs-lookup"><span data-stu-id="43a9c-134">SearchMailboxes</span></span>](searchmailboxes.md)
    
- [<span data-ttu-id="43a9c-135">SearchQueries</span><span class="sxs-lookup"><span data-stu-id="43a9c-135">SearchQueries</span></span>](searchqueries.md)
    
- [<span data-ttu-id="43a9c-136">MailboxQuery</span><span class="sxs-lookup"><span data-stu-id="43a9c-136">MailboxQuery</span></span>](mailboxquery.md)
    
- [<span data-ttu-id="43a9c-137">Query</span><span class="sxs-lookup"><span data-stu-id="43a9c-137">Query</span></span>](query.md)
    
- [<span data-ttu-id="43a9c-138">MailboxSearchScopes</span><span class="sxs-lookup"><span data-stu-id="43a9c-138">MailboxSearchScopes</span></span>](mailboxsearchscopes.md)
    
- [<span data-ttu-id="43a9c-139">MailboxSearchScope</span><span class="sxs-lookup"><span data-stu-id="43a9c-139">MailboxSearchScope</span></span>](mailboxsearchscope.md)
    
- [<span data-ttu-id="43a9c-140">邮箱 (字符串)</span><span class="sxs-lookup"><span data-stu-id="43a9c-140">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="43a9c-141">SearchScope</span><span class="sxs-lookup"><span data-stu-id="43a9c-141">SearchScope</span></span>](searchscope.md)
    
- [<span data-ttu-id="43a9c-142">ResultType</span><span class="sxs-lookup"><span data-stu-id="43a9c-142">ResultType</span></span>](resulttype.md)
    
## <a name="successful-searchmailboxes-operation-response"></a><span data-ttu-id="43a9c-143">成功的 SearchMailboxes 操作响应</span><span class="sxs-lookup"><span data-stu-id="43a9c-143">Successful SearchMailboxes operation response</span></span>

<span data-ttu-id="43a9c-144">下面的示例演示对**SearchMailboxes**操作请求的成功响应，以获取有关在目标邮箱中找到的搜索词次数的统计信息。</span><span class="sxs-lookup"><span data-stu-id="43a9c-144">The following example shows a successful response to a **SearchMailboxes** operation request to get statistical information about the number of times search terms are found in the target mailboxes.</span></span> <span data-ttu-id="43a9c-145">最后一个查询包含一个空的**查询**元素，该元素显示失败的邮箱搜索。</span><span class="sxs-lookup"><span data-stu-id="43a9c-145">The last query contains an empty **Query** element, which shows a failed mailbox search.</span></span> 
  
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
      <m:SearchMailboxesResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:SearchMailboxesResponseMessage ResponseClass="Success">
               <m:ResponseCode>NoError</m:ResponseCode>
               <m:SearchMailboxesResult>
                  <t:SearchQueries>
                     <t:MailboxQuery>
                        <t:Query>Test Item</t:Query>
                        <t:MailboxSearchScopes>
                           <t:MailboxSearchScope>
                              <t:Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYPDLT)/cn=Recipients/cn=35181a94327e392c8201a60d13ecf-Steve</t:Mailbox>
                              <t:SearchScope>All</t:SearchScope>
                           </t:MailboxSearchScope>
                           <t:MailboxSearchScope>
                              <t:Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYPDLT)/cn=Recipients/cn=f00c9f789572-beb04001d8f40c572e-Antho</t:Mailbox>
                              <t:SearchScope>PrimaryOnly</t:SearchScope>
                           </t:MailboxSearchScope>
                        </t:MailboxSearchScopes>
                     </t:MailboxQuery>
                  </t:SearchQueries>
                  <t:ResultType>StatisticsOnly</t:ResultType>
                  <t:ItemCount>2</t:ItemCount>
                  <t:Size>20206</t:Size>
                  <t:PageItemCount>0</t:PageItemCount>
                  <t:PageItemSize>0</t:PageItemSize>
                  <t:KeywordStats>
                     <t:KeywordStat>
                        <t:Keyword>Test Item</t:Keyword>
                        <t:ItemHits>2</t:ItemHits>
                        <t:Size>20206</t:Size>
                     </t:KeywordStat>
                  </t:KeywordStats>
                  <t:FailedMailboxes>
                     <t:FailedMailbox>
                        <t:Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYPDLT)/cn=Recipients/cn=accba4as3df234234a0e82ce1645f4e-Danie</t:Mailbox>
                        <t:ErrorCode>0</t:ErrorCode>
                        <t:ErrorMessage>The search query can't be empty.</t:ErrorMessage>
                        <t:IsArchive>true</t:IsArchive>
                     </t:FailedMailbox>
                  </t:FailedMailboxes>
               </m:SearchMailboxesResult>
            </m:SearchMailboxesResponseMessage>
         </m:ResponseMessages>
      </m:SearchMailboxesResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="43a9c-146">响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="43a9c-146">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="43a9c-147">SearchMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="43a9c-147">SearchMailboxesResponse</span></span>](searchmailboxesresponse.md)
    
- [<span data-ttu-id="43a9c-148">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="43a9c-148">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="43a9c-149">SearchMailboxesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="43a9c-149">SearchMailboxesResponseMessage</span></span>](searchmailboxesresponsemessage.md)
    
- [<span data-ttu-id="43a9c-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="43a9c-150">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="43a9c-151">SearchMailboxesResult</span><span class="sxs-lookup"><span data-stu-id="43a9c-151">SearchMailboxesResult</span></span>](searchmailboxesresult.md)
    
- [<span data-ttu-id="43a9c-152">SearchQueries</span><span class="sxs-lookup"><span data-stu-id="43a9c-152">SearchQueries</span></span>](searchqueries.md)
    
- [<span data-ttu-id="43a9c-153">MailboxQuery</span><span class="sxs-lookup"><span data-stu-id="43a9c-153">MailboxQuery</span></span>](mailboxquery.md)
    
- [<span data-ttu-id="43a9c-154">Query</span><span class="sxs-lookup"><span data-stu-id="43a9c-154">Query</span></span>](query.md)
    
- [<span data-ttu-id="43a9c-155">MailboxSearchScopes</span><span class="sxs-lookup"><span data-stu-id="43a9c-155">MailboxSearchScopes</span></span>](mailboxsearchscopes.md)
    
- [<span data-ttu-id="43a9c-156">MailboxSearchScope</span><span class="sxs-lookup"><span data-stu-id="43a9c-156">MailboxSearchScope</span></span>](mailboxsearchscope.md)
    
- [<span data-ttu-id="43a9c-157">邮箱 (字符串)</span><span class="sxs-lookup"><span data-stu-id="43a9c-157">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="43a9c-158">SearchScope</span><span class="sxs-lookup"><span data-stu-id="43a9c-158">SearchScope</span></span>](searchscope.md)
    
- [<span data-ttu-id="43a9c-159">ResultType</span><span class="sxs-lookup"><span data-stu-id="43a9c-159">ResultType</span></span>](resulttype.md)
    
- [<span data-ttu-id="43a9c-160">ItemCount</span><span class="sxs-lookup"><span data-stu-id="43a9c-160">ItemCount</span></span>](itemcount.md)
    
- [<span data-ttu-id="43a9c-161">大小（long）</span><span class="sxs-lookup"><span data-stu-id="43a9c-161">Size (long)</span></span>](size-long.md)
    
- [<span data-ttu-id="43a9c-162">PageItemCount</span><span class="sxs-lookup"><span data-stu-id="43a9c-162">PageItemCount</span></span>](pageitemcount.md)
    
- [<span data-ttu-id="43a9c-163">KeywordStats</span><span class="sxs-lookup"><span data-stu-id="43a9c-163">KeywordStats</span></span>](keywordstats.md)
    
- [<span data-ttu-id="43a9c-164">KeywordStat</span><span class="sxs-lookup"><span data-stu-id="43a9c-164">KeywordStat</span></span>](keywordstat.md)
    
- [<span data-ttu-id="43a9c-165">关键字</span><span class="sxs-lookup"><span data-stu-id="43a9c-165">Keyword</span></span>](keyword.md)
    
- [<span data-ttu-id="43a9c-166">ItemHits</span><span class="sxs-lookup"><span data-stu-id="43a9c-166">ItemHits</span></span>](itemhits.md)
    
- [<span data-ttu-id="43a9c-167">FailedMailboxes</span><span class="sxs-lookup"><span data-stu-id="43a9c-167">FailedMailboxes</span></span>](failedmailboxes.md)
    
- [<span data-ttu-id="43a9c-168">FailedMailbox</span><span class="sxs-lookup"><span data-stu-id="43a9c-168">FailedMailbox</span></span>](failedmailbox.md)
    
- [<span data-ttu-id="43a9c-169">邮箱 (字符串)</span><span class="sxs-lookup"><span data-stu-id="43a9c-169">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="43a9c-170">错误代码 (int)</span><span class="sxs-lookup"><span data-stu-id="43a9c-170">ErrorCode (int)</span></span>](errorcode-int.md)
    
- [<span data-ttu-id="43a9c-171">ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="43a9c-171">ErrorMessage</span></span>](errormessage.md)
    
- [<span data-ttu-id="43a9c-172">IsArchive</span><span class="sxs-lookup"><span data-stu-id="43a9c-172">IsArchive</span></span>](isarchive.md)
    
## <a name="searchmailboxes-operation-error-response"></a><span data-ttu-id="43a9c-173">SearchMailboxes 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="43a9c-173">SearchMailboxes operation error response</span></span>

<span data-ttu-id="43a9c-174">下面的示例演示对**SearchMailboxes**操作请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="43a9c-174">The following example shows an error response to a **SearchMailboxes** operation request.</span></span> <span data-ttu-id="43a9c-175">这是对邮箱标识符不正确时搜索邮箱的请求的响应。</span><span class="sxs-lookup"><span data-stu-id="43a9c-175">This is a response to a request to search a mailbox when the mailbox identifier is incorrect.</span></span> 
  
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
      <m:SearchMailboxesResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:SearchMailboxesResponseMessage ResponseClass="Error">
               <m:MessageText>No mailbox is specified for search operation. If specified in the request, 
               then it could be due to permission issue.</m:MessageText>
               <m:ResponseCode>ErrorInvalidOperation</m:ResponseCode>
               <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
               <m:SearchMailboxesResult>
                  <t:SearchQueries>
                     <t:MailboxQuery>
                        <t:Query>subject:Test Item</t:Query>
                        <t:MailboxSearchScopes>
                           <t:MailboxSearchScope>
                              <t:Mailbox>sbrown@contoso.com</t:Mailbox>
                              <t:SearchScope>All</t:SearchScope>
                           </t:MailboxSearchScope>
                        </t:MailboxSearchScopes>
                     </t:MailboxQuery>
                  </t:SearchQueries>
                  <t:ResultType>StatisticsOnly</t:ResultType>
                  <t:ItemCount>0</t:ItemCount>
                  <t:Size>0</t:Size>
                  <t:PageItemCount>0</t:PageItemCount>
                  <t:PageItemSize>0</t:PageItemSize>
                  <t:FailedMailboxes>
                     <t:FailedMailbox>
                        <t:Mailbox>sbrown@contoso.com</t:Mailbox>
                        <t:ErrorCode>0</t:ErrorCode>
                        <t:ErrorMessage>No mailbox is specified for search operation. If specified in the request, 
                        then it could be due to permission issue.</t:ErrorMessage>
                        <t:IsArchive>false</t:IsArchive>
                     </t:FailedMailbox>
                  </t:FailedMailboxes>
               </m:SearchMailboxesResult>
            </m:SearchMailboxesResponseMessage>
         </m:ResponseMessages>
      </m:SearchMailboxesResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="43a9c-176">错误响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="43a9c-176">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="43a9c-177">SearchMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="43a9c-177">SearchMailboxesResponse</span></span>](searchmailboxesresponse.md)
    
- [<span data-ttu-id="43a9c-178">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="43a9c-178">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="43a9c-179">SearchMailboxesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="43a9c-179">SearchMailboxesResponseMessage</span></span>](searchmailboxesresponsemessage.md)
    
- [<span data-ttu-id="43a9c-180">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="43a9c-180">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="43a9c-181">SearchMailboxesResult</span><span class="sxs-lookup"><span data-stu-id="43a9c-181">SearchMailboxesResult</span></span>](searchmailboxesresult.md)
    
- [<span data-ttu-id="43a9c-182">SearchQueries</span><span class="sxs-lookup"><span data-stu-id="43a9c-182">SearchQueries</span></span>](searchqueries.md)
    
- [<span data-ttu-id="43a9c-183">MailboxQuery</span><span class="sxs-lookup"><span data-stu-id="43a9c-183">MailboxQuery</span></span>](mailboxquery.md)
    
- [<span data-ttu-id="43a9c-184">Query</span><span class="sxs-lookup"><span data-stu-id="43a9c-184">Query</span></span>](query.md)
    
- [<span data-ttu-id="43a9c-185">MailboxSearchScopes</span><span class="sxs-lookup"><span data-stu-id="43a9c-185">MailboxSearchScopes</span></span>](mailboxsearchscopes.md)
    
- [<span data-ttu-id="43a9c-186">MailboxSearchScope</span><span class="sxs-lookup"><span data-stu-id="43a9c-186">MailboxSearchScope</span></span>](mailboxsearchscope.md)
    
- [<span data-ttu-id="43a9c-187">邮箱 (字符串)</span><span class="sxs-lookup"><span data-stu-id="43a9c-187">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="43a9c-188">SearchScope</span><span class="sxs-lookup"><span data-stu-id="43a9c-188">SearchScope</span></span>](searchscope.md)
    
- [<span data-ttu-id="43a9c-189">ResultType</span><span class="sxs-lookup"><span data-stu-id="43a9c-189">ResultType</span></span>](resulttype.md)
    
- [<span data-ttu-id="43a9c-190">ItemCount</span><span class="sxs-lookup"><span data-stu-id="43a9c-190">ItemCount</span></span>](itemcount.md)
    
- [<span data-ttu-id="43a9c-191">大小（long）</span><span class="sxs-lookup"><span data-stu-id="43a9c-191">Size (long)</span></span>](size-long.md)
    
- [<span data-ttu-id="43a9c-192">PageItemCount</span><span class="sxs-lookup"><span data-stu-id="43a9c-192">PageItemCount</span></span>](pageitemcount.md)
    
- [<span data-ttu-id="43a9c-193">PageItemSize</span><span class="sxs-lookup"><span data-stu-id="43a9c-193">PageItemSize</span></span>](pageitemsize.md)
    
- [<span data-ttu-id="43a9c-194">FailedMailboxes</span><span class="sxs-lookup"><span data-stu-id="43a9c-194">FailedMailboxes</span></span>](failedmailboxes.md)
    
- [<span data-ttu-id="43a9c-195">FailedMailbox</span><span class="sxs-lookup"><span data-stu-id="43a9c-195">FailedMailbox</span></span>](failedmailbox.md)
    
- [<span data-ttu-id="43a9c-196">邮箱 (字符串)</span><span class="sxs-lookup"><span data-stu-id="43a9c-196">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="43a9c-197">错误代码 (int)</span><span class="sxs-lookup"><span data-stu-id="43a9c-197">ErrorCode (int)</span></span>](errorcode-int.md)
    
- [<span data-ttu-id="43a9c-198">ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="43a9c-198">ErrorMessage</span></span>](errormessage.md)
    
- [<span data-ttu-id="43a9c-199">IsArchive</span><span class="sxs-lookup"><span data-stu-id="43a9c-199">IsArchive</span></span>](isarchive.md)
    
<span data-ttu-id="43a9c-200">有关对 EWS 通用的其他错误代码以及特定于此操作的错误代码，请参阅[ResponseCode](responsecode.md)。</span><span class="sxs-lookup"><span data-stu-id="43a9c-200">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="43a9c-201">另请参阅</span><span class="sxs-lookup"><span data-stu-id="43a9c-201">See also</span></span>

- [<span data-ttu-id="43a9c-202">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="43a9c-202">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="43a9c-203">GetSearchableMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="43a9c-203">GetSearchableMailboxes operation</span></span>](getsearchablemailboxes-operation.md)
    
- [<span data-ttu-id="43a9c-204">SetHoldOnMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="43a9c-204">SetHoldOnMailboxes operation</span></span>](setholdonmailboxes-operation.md)
    
- [<span data-ttu-id="43a9c-205">GetHoldOnMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="43a9c-205">GetHoldOnMailboxes operation</span></span>](getholdonmailboxes-operation.md)
    
- [<span data-ttu-id="43a9c-206">GetDiscoverySearchConfiguration 操作</span><span class="sxs-lookup"><span data-stu-id="43a9c-206">GetDiscoverySearchConfiguration operation</span></span>](getdiscoverysearchconfiguration-operation.md)
    
- [<span data-ttu-id="43a9c-207">GetNonIndexableItemDetails 操作</span><span class="sxs-lookup"><span data-stu-id="43a9c-207">GetNonIndexableItemDetails operation</span></span>](getnonindexableitemdetails-operation.md)
    
- [<span data-ttu-id="43a9c-208">GetNonIndexableItemStatistics 操作</span><span class="sxs-lookup"><span data-stu-id="43a9c-208">GetNonIndexableItemStatistics operation</span></span>](getnonindexableitemstatistics-operation.md)
    

