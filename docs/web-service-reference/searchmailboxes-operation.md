---
title: SearchMailboxes 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8a67c1d8-d021-4e68-aa62-35f7d9c2edc7
description: 查找信息 SearchMailboxes EWS 操作。
ms.openlocfilehash: 141ea466a24f3cb400a8e0b63e2162c1eae5d7f8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827296"
---
# <a name="searchmailboxes-operation"></a><span data-ttu-id="5367a-103">SearchMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="5367a-103">SearchMailboxes operation</span></span>

<span data-ttu-id="5367a-104">查找有关**SearchMailboxes** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="5367a-104">Find information about the **SearchMailboxes** EWS operation.</span></span> 
  
<span data-ttu-id="5367a-105">**SearchMailboxes**操作搜索词的项的邮箱中的邮箱项目。</span><span class="sxs-lookup"><span data-stu-id="5367a-105">The **SearchMailboxes** operation searches mailboxes for occurrences of terms in mailbox items.</span></span> 
  
<span data-ttu-id="5367a-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="5367a-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-searchmailboxes-operation"></a><span data-ttu-id="5367a-107">使用 SearchMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="5367a-107">Using the SearchMailboxes operation</span></span>

<span data-ttu-id="5367a-108">**SearchMailboxes**操作可以使用多个同时搜索查询执行发现搜索在多个邮箱。</span><span class="sxs-lookup"><span data-stu-id="5367a-108">The **SearchMailboxes** operation can use many simultaneous search queries to perform discovery search on multiple mailboxes.</span></span> <span data-ttu-id="5367a-109">结果可以是任一统计信息的次数发生搜索词，也包含搜索词的项的预览。</span><span class="sxs-lookup"><span data-stu-id="5367a-109">The results can be either statistical information about the number of times search terms occur, or a preview of the items that contain the search terms.</span></span> 
  
### <a name="searchmailboxes-operation-soap-headers"></a><span data-ttu-id="5367a-110">SearchMailboxes 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="5367a-110">SearchMailboxes operation SOAP headers</span></span>

<span data-ttu-id="5367a-111">**SearchMailboxes**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="5367a-111">The **SearchMailboxes** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="5367a-112">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="5367a-112">**Header name**</span></span>|<span data-ttu-id="5367a-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="5367a-113">**Element**</span></span>|<span data-ttu-id="5367a-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="5367a-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5367a-115">**ManagementRole**</span><span class="sxs-lookup"><span data-stu-id="5367a-115">**ManagementRole**</span></span> <br/> |[<span data-ttu-id="5367a-116">ManagementRole</span><span class="sxs-lookup"><span data-stu-id="5367a-116">ManagementRole</span></span>](managementrole.md) <br/> |<span data-ttu-id="5367a-117">标识服务器角色所需顺序呼叫者发出请求。</span><span class="sxs-lookup"><span data-stu-id="5367a-117">Identifies the server roles that are necessary in order for the caller to make the request.</span></span> <span data-ttu-id="5367a-118">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="5367a-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="5367a-119">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="5367a-119">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="5367a-120">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="5367a-120">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="5367a-121">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="5367a-121">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="5367a-122">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="5367a-122">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="5367a-123">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="5367a-123">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="5367a-124">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="5367a-124">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="5367a-125">标识响应该请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="5367a-125">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="5367a-126">适用于响应此标头。</span><span class="sxs-lookup"><span data-stu-id="5367a-126">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="searchmailboxes-operation-request-example-search-mailboxes-for-number-of-search-term-hits"></a><span data-ttu-id="5367a-127">SearchMailboxes 操作请求示例： 搜索邮箱搜索术语命中数</span><span class="sxs-lookup"><span data-stu-id="5367a-127">SearchMailboxes operation request example: Search mailboxes for number of search term hits</span></span>

<span data-ttu-id="5367a-128">**SearchMailboxes**操作请求的下面的示例演示如何使用两个不同的查询搜索术语显示每个邮箱中有关多少次的统计信息的三个不同的邮箱。</span><span class="sxs-lookup"><span data-stu-id="5367a-128">The following example of a **SearchMailboxes** operation request shows how to use two different queries to search three different mailboxes for statistical information about how many times a term appears in each mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5367a-129">本示例中，[查询](query.md)元素是 intentionaly 留空。</span><span class="sxs-lookup"><span data-stu-id="5367a-129">In this example, the [Query](query.md) element is intentionaly left blank.</span></span> <span data-ttu-id="5367a-130">此时将显示如何成功的请求可包含错误条件，在每个邮箱搜索基础。</span><span class="sxs-lookup"><span data-stu-id="5367a-130">This shows how a successful request can contain error conditions on a per mailbox search basis.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="5367a-131">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="5367a-131">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="5367a-132">SearchMailboxes</span><span class="sxs-lookup"><span data-stu-id="5367a-132">SearchMailboxes</span></span>](searchmailboxes.md)
    
- [<span data-ttu-id="5367a-133">SearchQueries</span><span class="sxs-lookup"><span data-stu-id="5367a-133">SearchQueries</span></span>](searchqueries.md)
    
- [<span data-ttu-id="5367a-134">MailboxQuery</span><span class="sxs-lookup"><span data-stu-id="5367a-134">MailboxQuery</span></span>](mailboxquery.md)
    
- [<span data-ttu-id="5367a-135">Query</span><span class="sxs-lookup"><span data-stu-id="5367a-135">Query</span></span>](query.md)
    
- [<span data-ttu-id="5367a-136">MailboxSearchScopes</span><span class="sxs-lookup"><span data-stu-id="5367a-136">MailboxSearchScopes</span></span>](mailboxsearchscopes.md)
    
- [<span data-ttu-id="5367a-137">MailboxSearchScope</span><span class="sxs-lookup"><span data-stu-id="5367a-137">MailboxSearchScope</span></span>](mailboxsearchscope.md)
    
- [<span data-ttu-id="5367a-138">邮箱 (字符串)</span><span class="sxs-lookup"><span data-stu-id="5367a-138">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="5367a-139">SearchScope</span><span class="sxs-lookup"><span data-stu-id="5367a-139">SearchScope</span></span>](searchscope.md)
    
- [<span data-ttu-id="5367a-140">ResultType</span><span class="sxs-lookup"><span data-stu-id="5367a-140">ResultType</span></span>](resulttype.md)
    
## <a name="successful-searchmailboxes-operation-response"></a><span data-ttu-id="5367a-141">成功 SearchMailboxes 操作响应</span><span class="sxs-lookup"><span data-stu-id="5367a-141">Successful SearchMailboxes operation response</span></span>

<span data-ttu-id="5367a-142">下面的示例演示成功响应**SearchMailboxes**操作请求获取统计信息的目标邮箱中找到搜索词的次数。</span><span class="sxs-lookup"><span data-stu-id="5367a-142">The following example shows a successful response to a **SearchMailboxes** operation request to get statistical information about the number of times search terms are found in the target mailboxes.</span></span> <span data-ttu-id="5367a-143">上一次查询包含空的**Query**元素，其中显示失败的邮箱搜索。</span><span class="sxs-lookup"><span data-stu-id="5367a-143">The last query contains an empty **Query** element, which shows a failed mailbox search.</span></span> 
  
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
      <m:SearchMailboxesResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="5367a-144">响应 SOAP 正文中包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="5367a-144">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="5367a-145">SearchMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="5367a-145">SearchMailboxesResponse</span></span>](searchmailboxesresponse.md)
    
- [<span data-ttu-id="5367a-146">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="5367a-146">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="5367a-147">SearchMailboxesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="5367a-147">SearchMailboxesResponseMessage</span></span>](searchmailboxesresponsemessage.md)
    
- [<span data-ttu-id="5367a-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="5367a-148">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="5367a-149">SearchMailboxesResult</span><span class="sxs-lookup"><span data-stu-id="5367a-149">SearchMailboxesResult</span></span>](searchmailboxesresult.md)
    
- [<span data-ttu-id="5367a-150">SearchQueries</span><span class="sxs-lookup"><span data-stu-id="5367a-150">SearchQueries</span></span>](searchqueries.md)
    
- [<span data-ttu-id="5367a-151">MailboxQuery</span><span class="sxs-lookup"><span data-stu-id="5367a-151">MailboxQuery</span></span>](mailboxquery.md)
    
- [<span data-ttu-id="5367a-152">Query</span><span class="sxs-lookup"><span data-stu-id="5367a-152">Query</span></span>](query.md)
    
- [<span data-ttu-id="5367a-153">MailboxSearchScopes</span><span class="sxs-lookup"><span data-stu-id="5367a-153">MailboxSearchScopes</span></span>](mailboxsearchscopes.md)
    
- [<span data-ttu-id="5367a-154">MailboxSearchScope</span><span class="sxs-lookup"><span data-stu-id="5367a-154">MailboxSearchScope</span></span>](mailboxsearchscope.md)
    
- [<span data-ttu-id="5367a-155">邮箱 (字符串)</span><span class="sxs-lookup"><span data-stu-id="5367a-155">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="5367a-156">SearchScope</span><span class="sxs-lookup"><span data-stu-id="5367a-156">SearchScope</span></span>](searchscope.md)
    
- [<span data-ttu-id="5367a-157">ResultType</span><span class="sxs-lookup"><span data-stu-id="5367a-157">ResultType</span></span>](resulttype.md)
    
- [<span data-ttu-id="5367a-158">ItemCount</span><span class="sxs-lookup"><span data-stu-id="5367a-158">ItemCount</span></span>](itemcount.md)
    
- [<span data-ttu-id="5367a-159">大小 (long)</span><span class="sxs-lookup"><span data-stu-id="5367a-159">Size (long)</span></span>](size-long.md)
    
- [<span data-ttu-id="5367a-160">PageItemCount</span><span class="sxs-lookup"><span data-stu-id="5367a-160">PageItemCount</span></span>](pageitemcount.md)
    
- [<span data-ttu-id="5367a-161">KeywordStats</span><span class="sxs-lookup"><span data-stu-id="5367a-161">KeywordStats</span></span>](keywordstats.md)
    
- [<span data-ttu-id="5367a-162">KeywordStat</span><span class="sxs-lookup"><span data-stu-id="5367a-162">KeywordStat</span></span>](keywordstat.md)
    
- [<span data-ttu-id="5367a-163">关键字</span><span class="sxs-lookup"><span data-stu-id="5367a-163">Keyword</span></span>](keyword.md)
    
- [<span data-ttu-id="5367a-164">ItemHits</span><span class="sxs-lookup"><span data-stu-id="5367a-164">ItemHits</span></span>](itemhits.md)
    
- [<span data-ttu-id="5367a-165">FailedMailboxes</span><span class="sxs-lookup"><span data-stu-id="5367a-165">FailedMailboxes</span></span>](failedmailboxes.md)
    
- [<span data-ttu-id="5367a-166">FailedMailbox</span><span class="sxs-lookup"><span data-stu-id="5367a-166">FailedMailbox</span></span>](failedmailbox.md)
    
- [<span data-ttu-id="5367a-167">邮箱 (字符串)</span><span class="sxs-lookup"><span data-stu-id="5367a-167">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="5367a-168">错误代码 (int)</span><span class="sxs-lookup"><span data-stu-id="5367a-168">ErrorCode (int)</span></span>](errorcode-int.md)
    
- [<span data-ttu-id="5367a-169">ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="5367a-169">ErrorMessage</span></span>](errormessage.md)
    
- [<span data-ttu-id="5367a-170">IsArchive</span><span class="sxs-lookup"><span data-stu-id="5367a-170">IsArchive</span></span>](isarchive.md)
    
## <a name="searchmailboxes-operation-error-response"></a><span data-ttu-id="5367a-171">SearchMailboxes 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="5367a-171">SearchMailboxes operation error response</span></span>

<span data-ttu-id="5367a-172">下面的示例演示对**SearchMailboxes**操作请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="5367a-172">The following example shows an error response to a **SearchMailboxes** operation request.</span></span> <span data-ttu-id="5367a-173">这是对搜索邮箱的邮箱标识符时不正确的请求的响应。</span><span class="sxs-lookup"><span data-stu-id="5367a-173">This is a response to a request to search a mailbox when the mailbox identifier is incorrect.</span></span> 
  
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
      <m:SearchMailboxesResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="5367a-174">错误响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="5367a-174">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="5367a-175">SearchMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="5367a-175">SearchMailboxesResponse</span></span>](searchmailboxesresponse.md)
    
- [<span data-ttu-id="5367a-176">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="5367a-176">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="5367a-177">SearchMailboxesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="5367a-177">SearchMailboxesResponseMessage</span></span>](searchmailboxesresponsemessage.md)
    
- [<span data-ttu-id="5367a-178">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="5367a-178">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="5367a-179">SearchMailboxesResult</span><span class="sxs-lookup"><span data-stu-id="5367a-179">SearchMailboxesResult</span></span>](searchmailboxesresult.md)
    
- [<span data-ttu-id="5367a-180">SearchQueries</span><span class="sxs-lookup"><span data-stu-id="5367a-180">SearchQueries</span></span>](searchqueries.md)
    
- [<span data-ttu-id="5367a-181">MailboxQuery</span><span class="sxs-lookup"><span data-stu-id="5367a-181">MailboxQuery</span></span>](mailboxquery.md)
    
- [<span data-ttu-id="5367a-182">Query</span><span class="sxs-lookup"><span data-stu-id="5367a-182">Query</span></span>](query.md)
    
- [<span data-ttu-id="5367a-183">MailboxSearchScopes</span><span class="sxs-lookup"><span data-stu-id="5367a-183">MailboxSearchScopes</span></span>](mailboxsearchscopes.md)
    
- [<span data-ttu-id="5367a-184">MailboxSearchScope</span><span class="sxs-lookup"><span data-stu-id="5367a-184">MailboxSearchScope</span></span>](mailboxsearchscope.md)
    
- [<span data-ttu-id="5367a-185">邮箱 (字符串)</span><span class="sxs-lookup"><span data-stu-id="5367a-185">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="5367a-186">SearchScope</span><span class="sxs-lookup"><span data-stu-id="5367a-186">SearchScope</span></span>](searchscope.md)
    
- [<span data-ttu-id="5367a-187">ResultType</span><span class="sxs-lookup"><span data-stu-id="5367a-187">ResultType</span></span>](resulttype.md)
    
- [<span data-ttu-id="5367a-188">ItemCount</span><span class="sxs-lookup"><span data-stu-id="5367a-188">ItemCount</span></span>](itemcount.md)
    
- [<span data-ttu-id="5367a-189">大小 (long)</span><span class="sxs-lookup"><span data-stu-id="5367a-189">Size (long)</span></span>](size-long.md)
    
- [<span data-ttu-id="5367a-190">PageItemCount</span><span class="sxs-lookup"><span data-stu-id="5367a-190">PageItemCount</span></span>](pageitemcount.md)
    
- [<span data-ttu-id="5367a-191">PageItemSize</span><span class="sxs-lookup"><span data-stu-id="5367a-191">PageItemSize</span></span>](pageitemsize.md)
    
- [<span data-ttu-id="5367a-192">FailedMailboxes</span><span class="sxs-lookup"><span data-stu-id="5367a-192">FailedMailboxes</span></span>](failedmailboxes.md)
    
- [<span data-ttu-id="5367a-193">FailedMailbox</span><span class="sxs-lookup"><span data-stu-id="5367a-193">FailedMailbox</span></span>](failedmailbox.md)
    
- [<span data-ttu-id="5367a-194">邮箱 (字符串)</span><span class="sxs-lookup"><span data-stu-id="5367a-194">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="5367a-195">错误代码 (int)</span><span class="sxs-lookup"><span data-stu-id="5367a-195">ErrorCode (int)</span></span>](errorcode-int.md)
    
- [<span data-ttu-id="5367a-196">ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="5367a-196">ErrorMessage</span></span>](errormessage.md)
    
- [<span data-ttu-id="5367a-197">IsArchive</span><span class="sxs-lookup"><span data-stu-id="5367a-197">IsArchive</span></span>](isarchive.md)
    
<span data-ttu-id="5367a-198">通用到 EWS 且特定于此操作的其他错误代码，请参阅[ResponseCode](responsecode.md)。</span><span class="sxs-lookup"><span data-stu-id="5367a-198">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5367a-199">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5367a-199">See also</span></span>

- [<span data-ttu-id="5367a-200">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="5367a-200">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="5367a-201">GetSearchableMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="5367a-201">GetSearchableMailboxes operation</span></span>](getsearchablemailboxes-operation.md)
    
- [<span data-ttu-id="5367a-202">SetHoldOnMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="5367a-202">SetHoldOnMailboxes operation</span></span>](setholdonmailboxes-operation.md)
    
- [<span data-ttu-id="5367a-203">GetHoldOnMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="5367a-203">GetHoldOnMailboxes operation</span></span>](getholdonmailboxes-operation.md)
    
- [<span data-ttu-id="5367a-204">GetDiscoverySearchConfiguration 操作</span><span class="sxs-lookup"><span data-stu-id="5367a-204">GetDiscoverySearchConfiguration operation</span></span>](getdiscoverysearchconfiguration-operation.md)
    
- [<span data-ttu-id="5367a-205">GetNonIndexableItemDetails 操作</span><span class="sxs-lookup"><span data-stu-id="5367a-205">GetNonIndexableItemDetails operation</span></span>](getnonindexableitemdetails-operation.md)
    
- [<span data-ttu-id="5367a-206">GetNonIndexableItemStatistics 操作</span><span class="sxs-lookup"><span data-stu-id="5367a-206">GetNonIndexableItemStatistics operation</span></span>](getnonindexableitemstatistics-operation.md)
    

