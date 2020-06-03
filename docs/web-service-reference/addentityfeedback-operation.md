---
title: AddEntityFeedback 操作
manager: luken
ms.date: 4/18/2016
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 00e40197-5794-4268-b937-bd65aa044890
description: AddEntityFeedback 操作将返回对应于服务器端问题的错误消息。
ms.openlocfilehash: a1027a0a1ee06cf3e83833b1d84c13d77b07c0b9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458437"
---
# <a name="addentityfeedback-operation"></a><span data-ttu-id="4e2e1-103">AddEntityFeedback 操作</span><span class="sxs-lookup"><span data-stu-id="4e2e1-103">AddEntityFeedback operation</span></span>

<span data-ttu-id="4e2e1-104">**AddEntityFeedback**操作将返回对应于服务器端问题的错误消息。</span><span class="sxs-lookup"><span data-stu-id="4e2e1-104">The **AddEntityFeedback** operation returns error information corresponding to server-side issues.</span></span> 
  
<span data-ttu-id="4e2e1-105">此操作取决于所记录的事件的类型。</span><span class="sxs-lookup"><span data-stu-id="4e2e1-105">This operation relies on the type of event being logged.</span></span> <span data-ttu-id="4e2e1-106">最重要的事件之一是**EntityAdded**，它对应于所选的实体。</span><span class="sxs-lookup"><span data-stu-id="4e2e1-106">One of the most important events is **EntityAdded**, which corresponds to an entity being selected.</span></span> <span data-ttu-id="4e2e1-107">此操作是批处理操作，因此可用于在单个请求中记录批次条目。</span><span class="sxs-lookup"><span data-stu-id="4e2e1-107">This operation is batch, so it can be used to log batches of entries in a single request.</span></span> 
  
## <a name="findpeople-request-examples"></a><span data-ttu-id="4e2e1-108">FindPeople 请求示例</span><span class="sxs-lookup"><span data-stu-id="4e2e1-108">FindPeople request examples</span></span>

<span data-ttu-id="4e2e1-109">**AddEntityFeedback**操作提供一种方法，使客户端可以记录与服务返回的实体进行交互的详细信息。</span><span class="sxs-lookup"><span data-stu-id="4e2e1-109">The **AddEntityFeedback** operation provides a way for clients to log details of interaction with entities returned by the service.</span></span> <span data-ttu-id="4e2e1-110">这可用作提高每个客户端的幕后相关性的信号。</span><span class="sxs-lookup"><span data-stu-id="4e2e1-110">This can be used as a signal to improve relevance behind the scenes for each client.</span></span> <span data-ttu-id="4e2e1-111">例如，客户端可以使用此操作提供对**FindPeople**返回的人员实体的反馈。</span><span class="sxs-lookup"><span data-stu-id="4e2e1-111">E.g., Clients can use this operation to provide feedback on people entities returned from **FindPeople**.</span></span>
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
                             xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                             xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:AddEntityFeedback>
            <m:EntityFeedbackEntries>
                  <t:EntityFeedbackEntry>
                        <t:ClientEventTimeUTC> 2015-07-05T22:16:18+00:00</t:ClientEventTimeUTC>
                        <t:ClientEventTimeLocal> 2015-07-05T22:16:18+00:00</t:ClientEventTimeLocal>
                        <t:ClientSessionId>00000000-0000-0000-0000-000000000012</t:ClientSessionId>
                        <t:ClientVersion>15.01.0101.01</t:ClientVersion>
                        <t:ClientId>Web</t:ClientId>
                        <t:TransactionId>123456789</t:TransactionId>
                        <t:EventType>EntityAdded</t:EventType>
                        <t:TargetEntityList>["a","b","c"]</t:TargetEntityList>
                        <t:SourceOfEntityAdded></t:SourceOfEntityAdded>
                        <t:JSONPropertyBag></t:JSONPropertyBag>
                  </t:EntityFeedbackEntry>
                  <t:EntityFeedbackEntry>
                  …
                  </t:EntityFeedbackEntry>
            </m:EntityFeedbackEntries>
      </m:AddEntityFeedback>
   </soap:Body>
</soap:Envelope>

```

### <a name="the-request-soap-body-contents"></a><span data-ttu-id="4e2e1-112">请求 SOAP 正文内容</span><span class="sxs-lookup"><span data-stu-id="4e2e1-112">The request SOAP body contents</span></span>

<span data-ttu-id="4e2e1-113">Soap 请求包含单个元素**EntityFeedbackEntries**。</span><span class="sxs-lookup"><span data-stu-id="4e2e1-113">The soap request contains a single element **EntityFeedbackEntries**.</span></span> <span data-ttu-id="4e2e1-114">这反过来又包含**EntityFeedbackEntry**对象的数组。</span><span class="sxs-lookup"><span data-stu-id="4e2e1-114">This in turn contains an array of **EntityFeedbackEntry** objects.</span></span> <span data-ttu-id="4e2e1-115">数组中的每个条目都可以包含以下元素。</span><span class="sxs-lookup"><span data-stu-id="4e2e1-115">Each entry in the array can contain the following elements.</span></span> 
  
|<span data-ttu-id="4e2e1-116">**请求参数**</span><span class="sxs-lookup"><span data-stu-id="4e2e1-116">**Request Parameters**</span></span>|<span data-ttu-id="4e2e1-117">**必需**</span><span class="sxs-lookup"><span data-stu-id="4e2e1-117">**Required**</span></span>|<span data-ttu-id="4e2e1-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="4e2e1-118">**Description**</span></span>|<span data-ttu-id="4e2e1-119">**类型**</span><span class="sxs-lookup"><span data-stu-id="4e2e1-119">**Type**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4e2e1-120">**ClientEventTimeUtc**</span><span class="sxs-lookup"><span data-stu-id="4e2e1-120">**ClientEventTimeUtc**</span></span> <br/> |<span data-ttu-id="4e2e1-121">是</span><span class="sxs-lookup"><span data-stu-id="4e2e1-121">Yes</span></span>  <br/> |<span data-ttu-id="4e2e1-122">在客户端上事件发生时的 UTC 时间。</span><span class="sxs-lookup"><span data-stu-id="4e2e1-122">The UTC time the event occurred on the client-side.</span></span>  <br/> |<span data-ttu-id="4e2e1-123">日期/时间</span><span class="sxs-lookup"><span data-stu-id="4e2e1-123">DateTime</span></span>  <br/> |
|<span data-ttu-id="4e2e1-124">**ClientEventTimeLocal**</span><span class="sxs-lookup"><span data-stu-id="4e2e1-124">**ClientEventTimeLocal**</span></span> <br/> |<span data-ttu-id="4e2e1-125">是</span><span class="sxs-lookup"><span data-stu-id="4e2e1-125">Yes</span></span>  <br/> |<span data-ttu-id="4e2e1-126">在客户端上发生事件的本地时间。</span><span class="sxs-lookup"><span data-stu-id="4e2e1-126">The local time the event occurred on the client side.</span></span>  <br/> |<span data-ttu-id="4e2e1-127">日期/时间</span><span class="sxs-lookup"><span data-stu-id="4e2e1-127">DateTime</span></span>  <br/> |
|<span data-ttu-id="4e2e1-128">**ClientId**</span><span class="sxs-lookup"><span data-stu-id="4e2e1-128">**ClientId**</span></span> <br/> |<span data-ttu-id="4e2e1-129">是</span><span class="sxs-lookup"><span data-stu-id="4e2e1-129">Yes</span></span>  <br/> |<span data-ttu-id="4e2e1-130">客户端的类型（例如，Outlook、OWA 等）。</span><span class="sxs-lookup"><span data-stu-id="4e2e1-130">Type of Client (E.g., Outlook, OWA, etc.).</span></span>  <br/> |<span data-ttu-id="4e2e1-131">ClientIDType 枚举</span><span class="sxs-lookup"><span data-stu-id="4e2e1-131">ClientIDType Enumeration</span></span>  <br/> |
|<span data-ttu-id="4e2e1-132">**ClientSessionId**</span><span class="sxs-lookup"><span data-stu-id="4e2e1-132">**ClientSessionId**</span></span> <br/> |<span data-ttu-id="4e2e1-133">是</span><span class="sxs-lookup"><span data-stu-id="4e2e1-133">Yes</span></span>  <br/> |<span data-ttu-id="4e2e1-134">标识会话 ID 的 GUID。</span><span class="sxs-lookup"><span data-stu-id="4e2e1-134">GUID Identifying the session ID.</span></span> <span data-ttu-id="4e2e1-135">在客户端上生成。</span><span class="sxs-lookup"><span data-stu-id="4e2e1-135">Generated on the client.</span></span>  <br/> |<span data-ttu-id="4e2e1-136">GUID</span><span class="sxs-lookup"><span data-stu-id="4e2e1-136">GUID</span></span>  <br/> |
|<span data-ttu-id="4e2e1-137">**ClientVersion**</span><span class="sxs-lookup"><span data-stu-id="4e2e1-137">**ClientVersion**</span></span> <br/> |<span data-ttu-id="4e2e1-138">是</span><span class="sxs-lookup"><span data-stu-id="4e2e1-138">Yes</span></span>  <br/> |<span data-ttu-id="4e2e1-139">客户端的版本（例如，15.01.0101.000）。</span><span class="sxs-lookup"><span data-stu-id="4e2e1-139">Version of the client (E.g., 15.01.0101.000).</span></span>  <br/> |<span data-ttu-id="4e2e1-140">String</span><span class="sxs-lookup"><span data-stu-id="4e2e1-140">String</span></span>  <br/> |
|<span data-ttu-id="4e2e1-141">**EntityAddSource**</span><span class="sxs-lookup"><span data-stu-id="4e2e1-141">**EntityAddSource**</span></span> <br/> |<span data-ttu-id="4e2e1-142">否</span><span class="sxs-lookup"><span data-stu-id="4e2e1-142">No</span></span>  <br/> |<span data-ttu-id="4e2e1-143">EntityAded 的源（例如，EntityRelevanceAPI、类型、粘贴）。</span><span class="sxs-lookup"><span data-stu-id="4e2e1-143">Source for EntityAded (E.g., EntityRelevanceAPI, types, pasted).</span></span>  <br/> |<span data-ttu-id="4e2e1-144">EntityAddSource 枚举</span><span class="sxs-lookup"><span data-stu-id="4e2e1-144">EntityAddSource Enumeration</span></span>  <br/> |
|<span data-ttu-id="4e2e1-145">**EntrySequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="4e2e1-145">**EntrySequenceNumber**</span></span> <br/> |<span data-ttu-id="4e2e1-146">是</span><span class="sxs-lookup"><span data-stu-id="4e2e1-146">Yes</span></span>  <br/> |<span data-ttu-id="4e2e1-147">每个客户端会话递增整数。</span><span class="sxs-lookup"><span data-stu-id="4e2e1-147">An incremental integer per client session.</span></span> <span data-ttu-id="4e2e1-148">用于检测数据丢失。</span><span class="sxs-lookup"><span data-stu-id="4e2e1-148">Used for detecting data loss.</span></span>  <br/> |<span data-ttu-id="4e2e1-149">Int</span><span class="sxs-lookup"><span data-stu-id="4e2e1-149">Int</span></span>  <br/> |
|<span data-ttu-id="4e2e1-150">**EventType**</span><span class="sxs-lookup"><span data-stu-id="4e2e1-150">**EventType**</span></span> <br/> |<span data-ttu-id="4e2e1-151">是</span><span class="sxs-lookup"><span data-stu-id="4e2e1-151">Yes</span></span>  <br/> |<span data-ttu-id="4e2e1-152">事件类型（例如，添加实体，删除实体）。</span><span class="sxs-lookup"><span data-stu-id="4e2e1-152">Type of event (E.g., Entity Added, Entity Removed).</span></span>  <br/> |<span data-ttu-id="4e2e1-153">String</span><span class="sxs-lookup"><span data-stu-id="4e2e1-153">String</span></span>  <br/> |
|<span data-ttu-id="4e2e1-154">**JSONPropertyBag**</span><span class="sxs-lookup"><span data-stu-id="4e2e1-154">**JSONPropertyBag**</span></span> <br/> |<span data-ttu-id="4e2e1-155">否</span><span class="sxs-lookup"><span data-stu-id="4e2e1-155">No</span></span>  <br/> |<span data-ttu-id="4e2e1-156">与事件关联的其他属性（JSON blob 的键/值对）。</span><span class="sxs-lookup"><span data-stu-id="4e2e1-156">Additional properties associated with the event (JSON blob of key/value pairs).</span></span>  <br/> |<span data-ttu-id="4e2e1-157">JSON Blob</span><span class="sxs-lookup"><span data-stu-id="4e2e1-157">JSON Blob</span></span>  <br/> |
|<span data-ttu-id="4e2e1-158">**TargetEntityList**</span><span class="sxs-lookup"><span data-stu-id="4e2e1-158">**TargetEntityList**</span></span> <br/> |<span data-ttu-id="4e2e1-159">否</span><span class="sxs-lookup"><span data-stu-id="4e2e1-159">No</span></span>  <br/> |<span data-ttu-id="4e2e1-160">与事件关联的实体的列表。</span><span class="sxs-lookup"><span data-stu-id="4e2e1-160">List of entities associated with the event.</span></span>  <br/> |<span data-ttu-id="4e2e1-161">JSON 字符串</span><span class="sxs-lookup"><span data-stu-id="4e2e1-161">JSON String</span></span>  <br/> |
|<span data-ttu-id="4e2e1-162">**TransactionId**</span><span class="sxs-lookup"><span data-stu-id="4e2e1-162">**TransactionId**</span></span> <br/> |<span data-ttu-id="4e2e1-163">否</span><span class="sxs-lookup"><span data-stu-id="4e2e1-163">No</span></span>  <br/> |<span data-ttu-id="4e2e1-164">ID （GUID），用于关联查询日志中的 ID。</span><span class="sxs-lookup"><span data-stu-id="4e2e1-164">ID (GUID) correlating the ID in query logs.</span></span>  <br/> |<span data-ttu-id="4e2e1-165">String</span><span class="sxs-lookup"><span data-stu-id="4e2e1-165">String</span></span>  <br/> |
   
### <a name="successful-addentityfeedback-operation-response"></a><span data-ttu-id="4e2e1-166">成功的 AddEntityFeedback 操作响应</span><span class="sxs-lookup"><span data-stu-id="4e2e1-166">Successful AddEntityFeedback operation response</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Header>
        <h:ServerVersionInfo MajorVersion="15" 
                                MinorVersion="1" 
                                MajorBuildNumber="228" 
                                MinorBuildNumber="0" 
                                Version="V2_49" 
                                xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                                xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                                xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
    </s:Header>
    <s:Body>
        <AddEntityFeedbackResponse ResponseClass="Success" 
                                                              xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                                              xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                                                              xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
            <ResponseCode>NoError</ResponseCode>
            <ErrorCount>0</ErrorCount>
            <ErrorDetails />
        </AddEntityFeedbackResponse>
    </s:Body>
</s:Envelope> 

```

### <a name="the-response-soap-body-contains-the-following-elements"></a><span data-ttu-id="4e2e1-167">响应 SOAP 正文包含以下元素</span><span class="sxs-lookup"><span data-stu-id="4e2e1-167">The response SOAP body contains the following elements</span></span>

#### <a name="errors"></a><span data-ttu-id="4e2e1-168">错误</span><span class="sxs-lookup"><span data-stu-id="4e2e1-168">Errors</span></span> 
  
<span data-ttu-id="4e2e1-169">API 可以记录一批反馈条目，我们记录了我们所能做的一切。</span><span class="sxs-lookup"><span data-stu-id="4e2e1-169">The API can log a batch of feedback entries, we log all that we can.</span></span> <span data-ttu-id="4e2e1-170">此字段表示未记录的错误条目数。</span><span class="sxs-lookup"><span data-stu-id="4e2e1-170">This field represents the number of error entries that were not logged.</span></span>
    
#### <a name="errordetails"></a><span data-ttu-id="4e2e1-171">ErrorDetails</span><span class="sxs-lookup"><span data-stu-id="4e2e1-171">ErrorDetails</span></span>
  
<span data-ttu-id="4e2e1-172">与以上分隔的错误相关的详细信息 `;` 。</span><span class="sxs-lookup"><span data-stu-id="4e2e1-172">Details pertaining to the errors above separates by `;`.</span></span>
    
### <a name="currently-supported-values"></a><span data-ttu-id="4e2e1-173">当前支持的值</span><span class="sxs-lookup"><span data-stu-id="4e2e1-173">Currently supported values</span></span>

|<span data-ttu-id="4e2e1-174">**ClientIdType 枚举**</span><span class="sxs-lookup"><span data-stu-id="4e2e1-174">**ClientIdType Enumeration**</span></span>|
|:-----|
|<span data-ttu-id="4e2e1-175">桌面</span><span class="sxs-lookup"><span data-stu-id="4e2e1-175">Desktop</span></span>  <br/> |
|<span data-ttu-id="4e2e1-176">Exchange</span><span class="sxs-lookup"><span data-stu-id="4e2e1-176">Exchange</span></span>  <br/> |
|<span data-ttu-id="4e2e1-177">IMAP4</span><span class="sxs-lookup"><span data-stu-id="4e2e1-177">IMAP4</span></span>  <br/> |
|<span data-ttu-id="4e2e1-178">Lync</span><span class="sxs-lookup"><span data-stu-id="4e2e1-178">Lync</span></span>  <br/> |
|<span data-ttu-id="4e2e1-179">MacMail</span><span class="sxs-lookup"><span data-stu-id="4e2e1-179">MacMail</span></span>  <br/> |
|<span data-ttu-id="4e2e1-180">MacOutlook</span><span class="sxs-lookup"><span data-stu-id="4e2e1-180">MacOutlook</span></span>  <br/> |
|<span data-ttu-id="4e2e1-181">移动设备</span><span class="sxs-lookup"><span data-stu-id="4e2e1-181">Mobile</span></span>  <br/> |
|<span data-ttu-id="4e2e1-182">其他</span><span class="sxs-lookup"><span data-stu-id="4e2e1-182">Other</span></span>  <br/> |
|<span data-ttu-id="4e2e1-183">Outlook</span><span class="sxs-lookup"><span data-stu-id="4e2e1-183">Outlook</span></span>  <br/> |
|<span data-ttu-id="4e2e1-184">Outlookservice.swift</span><span class="sxs-lookup"><span data-stu-id="4e2e1-184">OutlookService</span></span>  <br/> |
|<span data-ttu-id="4e2e1-185">POP3</span><span class="sxs-lookup"><span data-stu-id="4e2e1-185">POP3</span></span>  <br/> |
|<span data-ttu-id="4e2e1-186">平板电脑</span><span class="sxs-lookup"><span data-stu-id="4e2e1-186">Tablet</span></span>  <br/> |
|<span data-ttu-id="4e2e1-187">Web</span><span class="sxs-lookup"><span data-stu-id="4e2e1-187">Web</span></span>  <br/> |
   
|<span data-ttu-id="4e2e1-188">**EntityAddSource 枚举**</span><span class="sxs-lookup"><span data-stu-id="4e2e1-188">**EntityAddSource Enumeration**</span></span>|
|:-----|
|<span data-ttu-id="4e2e1-189">ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="4e2e1-189">ActiveDirectory</span></span>  <br/> |
|<span data-ttu-id="4e2e1-190">EntityRelevanceApi</span><span class="sxs-lookup"><span data-stu-id="4e2e1-190">EntityRelevanceApi</span></span>  <br/> |
|<span data-ttu-id="4e2e1-191">EntityRelevanceApiCache</span><span class="sxs-lookup"><span data-stu-id="4e2e1-191">EntityRelevanceApiCache</span></span>  <br/> |
|<span data-ttu-id="4e2e1-192">ExplicitTyping</span><span class="sxs-lookup"><span data-stu-id="4e2e1-192">ExplicitTyping</span></span>  <br/> |
|<span data-ttu-id="4e2e1-193">LocalCache</span><span class="sxs-lookup"><span data-stu-id="4e2e1-193">LocalCache</span></span>  <br/> |
|<span data-ttu-id="4e2e1-194">LocalCacheAndEntityRelevanceAPI</span><span class="sxs-lookup"><span data-stu-id="4e2e1-194">LocalCacheAndEntityRelevanceAPI</span></span>  <br/> |
|<span data-ttu-id="4e2e1-195">无</span><span class="sxs-lookup"><span data-stu-id="4e2e1-195">None</span></span>  <br/> |
|<span data-ttu-id="4e2e1-196">其他</span><span class="sxs-lookup"><span data-stu-id="4e2e1-196">Other</span></span>  <br/> |
|<span data-ttu-id="4e2e1-197">Paste</span><span class="sxs-lookup"><span data-stu-id="4e2e1-197">Paste</span></span>  <br/> |
   
### <a name="addentityfeedback-operation-error-response"></a><span data-ttu-id="4e2e1-198">AddEntityFeedback 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="4e2e1-198">AddEntityFeedback operation error response</span></span>

<span data-ttu-id="4e2e1-199">有关对 EWS 通用的错误代码，请参阅[ResponseCode](responsecode.md)。</span><span class="sxs-lookup"><span data-stu-id="4e2e1-199">For error codes that are generic to EWS, see [ResponseCode](responsecode.md).</span></span>
  
### <a name="example-of-addentityfeedback-in-conjunction-with-findpeople"></a><span data-ttu-id="4e2e1-200">AddEntityFeedback 与 FindPeople 结合使用的示例</span><span class="sxs-lookup"><span data-stu-id="4e2e1-200">Example of AddEntityFeedback in conjunction with FindPeople</span></span>

#### <a name="findpeople-request"></a><span data-ttu-id="4e2e1-201">FindPeople 请求</span><span class="sxs-lookup"><span data-stu-id="4e2e1-201">FindPeople request</span></span>
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
<soap:Body >
    <m:FindPeople>
      <m:IndexedPageItemView BasePoint="Beginning" MaxEntriesReturned="100" Offset="0"/>
      <m:QueryString>user1</m:QueryString>
      <m:SearchPeopleSuggestionIndex>true</m:SearchPeopleSuggestionIndex>
    </m:FindPeople>
  </soap:Body>
</soap:Envelope>    
    
```

#### <a name="findpeople-response"></a><span data-ttu-id="4e2e1-202">FindPeople 响应</span><span class="sxs-lookup"><span data-stu-id="4e2e1-202">FindPeople response</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Header>
        <h:ServerVersionInfo MajorVersion="15" MinorVersion="1" MajorBuildNumber="302" MinorBuildNumber="0" Version="V2_68" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
    </s:Header>
    <s:Body>
        <FindPeopleResponse ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
            <ResponseCode>NoError</ResponseCode>
            <People>
                <Persona xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
                    <PersonaId Id="AAUQAFjZ4UxX8SZCqSPFsmh0cSo=" />
                    <PersonaType>Person</PersonaType>
                    <CreationTime>2015-10-02T23:25:42</CreationTime>
                    <DisplayName>user2</DisplayName>
…
                  </Persona>
            </People>
            <TotalNumberOfPeopleInView>0</TotalNumberOfPeopleInView>
            <FirstMatchingRowIndex>0</FirstMatchingRowIndex>
            <FirstLoadedRowIndex>0</FirstLoadedRowIndex>
            <TransactionId>b56ad16e-5d5a-4574-90f8-b8dd57382be6</TransactionId>
        </FindPeopleResponse>
    </s:Body>
</s:Envelope>

```

#### <a name="addentityfeedback-request"></a><span data-ttu-id="4e2e1-203">AddEntityFeedback 请求</span><span class="sxs-lookup"><span data-stu-id="4e2e1-203">AddEntityFeedback request</span></span>

```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:AddEntityFeedback>
<m:EntityFeedbackEntries>
<t:EntityFeedbackEntry>
         <t:ClientEventTimeUtc>2015-07-05T22:16:18+00:00</t:ClientEventTimeUtc>
         <t:ClientEventTimeLocal>2015-07-05T22:16:18+00:00</t:ClientEventTimeLocal>
         <t:ClientSessionId>00000000-0000-0000-0000-000000000012</t:ClientSessionId>
         <t:ClientVersion>15.01.0101.01</t:ClientVersion>
         <t:ClientId>Web</t:ClientId>
         <t:TransactionId>b56ad16e-5d5a-4574-90f8-b8dd57382be6</t:TransactionId>
         <t:EventType>EntityAdded</t:EventType>
         <t:TargetEntityList>["user1@ms7.com"]</t:TargetEntityList>
         <t:SourceOfEntityAdded>EntityRelevanceApi</t:SourceOfEntityAdded>
         <t:JSONPropertyBag></t:JSONPropertyBag>
</t:EntityFeedbackEntry>
</m:EntityFeedbackEntries>
      </m:AddEntityFeedback>
   </soap:Body>
</soap:Envelope>

```

> [!NOTE]
> <span data-ttu-id="4e2e1-204">使用 FindPeople 响应事务 ID 作为 AddEntityFeedback 请求事务 ID。</span><span class="sxs-lookup"><span data-stu-id="4e2e1-204">Using FindPeople response transaction ID as the AddEntityFeedback request transaction ID.</span></span> 
  
#### <a name="addentityfeedback-response"></a><span data-ttu-id="4e2e1-205">AddEntityFeedback 响应</span><span class="sxs-lookup"><span data-stu-id="4e2e1-205">AddEntityFeedback response</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Header>
        <h:ServerVersionInfo MajorVersion="15" MinorVersion="1" MajorBuildNumber="302" MinorBuildNumber="0" Version="V2_68" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
    </s:Header>
    <s:Body>
        <AddEntityFeedbackResponse ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
            <ResponseCode>NoError</ResponseCode>
            <ErrorCount>0</ErrorCount>
            <ErrorDetails />
        </AddEntityFeedbackResponse>
    </s:Body>
</s:Envelope>

```


