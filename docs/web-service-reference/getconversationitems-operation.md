---
title: GetConversationItems operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8ae00a99-b37b-4194-829c-fe300db6ab99
description: 查找有关 GetConversationItems 操作的信息。
ms.openlocfilehash: 9d9fb9cc04bcbb5846162c77c852defa51dff98b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754498"
---
# <a name="getconversationitems-operation"></a><span data-ttu-id="d943e-103">GetConversationItems operation</span><span class="sxs-lookup"><span data-stu-id="d943e-103">GetConversationItems operation</span></span>

<span data-ttu-id="d943e-104">查找有关**GetConversationItems**操作的信息。</span><span class="sxs-lookup"><span data-stu-id="d943e-104">Find information about the **GetConversationItems** operation.</span></span> 
  
<span data-ttu-id="d943e-105">**GetConversationItems**操作获取对话中的节点到组织中的项目的一个或多个的设置。</span><span class="sxs-lookup"><span data-stu-id="d943e-105">The **GetConversationItems** operation gets one or more sets of items that are organized in to nodes in a conversation.</span></span> 
  
<span data-ttu-id="d943e-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="d943e-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getconversationitems-operation"></a><span data-ttu-id="d943e-107">使用 GetConversationItems 操作</span><span class="sxs-lookup"><span data-stu-id="d943e-107">Using the GetConversationItems operation</span></span>

<span data-ttu-id="d943e-108">您可以使用**GetConversationItems**操作获取的两个主对话和存档邮箱中的项目。</span><span class="sxs-lookup"><span data-stu-id="d943e-108">You can use the **GetConversationItems** operation to get items in conversations for both primary and archive mailboxes.</span></span> 
  
### <a name="getconversationitems-operation-soap-headers"></a><span data-ttu-id="d943e-109">GetConversationItems 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="d943e-109">GetConversationItems operation SOAP headers</span></span>

<span data-ttu-id="d943e-110">**GetConversationItems**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="d943e-110">The **GetConversationItems** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="d943e-111">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="d943e-111">**Header name**</span></span>|<span data-ttu-id="d943e-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="d943e-112">**Element**</span></span>|<span data-ttu-id="d943e-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="d943e-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d943e-114">**模拟**</span><span class="sxs-lookup"><span data-stu-id="d943e-114">**Impersonation**</span></span> <br/> |[<span data-ttu-id="d943e-115">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="d943e-115">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="d943e-116">标识模拟客户端应用程序的用户。</span><span class="sxs-lookup"><span data-stu-id="d943e-116">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="d943e-117">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="d943e-117">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="d943e-118">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="d943e-118">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="d943e-119">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="d943e-119">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="d943e-120">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="d943e-120">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="d943e-121">此元素的最小值是**Exchange2013**。</span><span class="sxs-lookup"><span data-stu-id="d943e-121">The minimum value for this element is **Exchange2013**.</span></span> <span data-ttu-id="d943e-122">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="d943e-122">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="d943e-123">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="d943e-123">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="d943e-124">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="d943e-124">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="d943e-125">标识响应该请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="d943e-125">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="d943e-126">适用于响应此标头。</span><span class="sxs-lookup"><span data-stu-id="d943e-126">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getconversationitems-operation-request-example-get-items-in-a-single-conversation"></a><span data-ttu-id="d943e-127">GetConversationItems 操作请求示例： 单个会话中获取项</span><span class="sxs-lookup"><span data-stu-id="d943e-127">GetConversationItems operation request example: Get items in a single conversation</span></span>

<span data-ttu-id="d943e-128">**GetConversationItems**操作请求的下面的示例演示如何在单个对话中，项目中的已删除邮件和草稿文件夹位于除外获取对话的所有项目。</span><span class="sxs-lookup"><span data-stu-id="d943e-128">The following example of a **GetConversationItems** operation request shows how to get all conversation items in a single conversation, with the exception of items located in the Deleted Items and Drafts folders.</span></span> <span data-ttu-id="d943e-129">项标识符、 主题和项目的邮箱中接收的时间，将包含响应中返回每个项目。</span><span class="sxs-lookup"><span data-stu-id="d943e-129">Each item returned in the response will contain an item identifier, a subject, and the time that the item was received in the mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d943e-130">所有项目标识符，本文中的更改项具有已截短要保留可读性。</span><span class="sxs-lookup"><span data-stu-id="d943e-130">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body>
      <m:GetConversationItems>
         <m:ItemShape>
            <t:BaseShape>IdOnly</t:BaseShape>
            <t:AdditionalProperties>
               <t:FieldURI FieldURI="item:Subject" />
               <t:FieldURI FieldURI="item:DateTimeReceived" />
            </t:AdditionalProperties>
         </m:ItemShape>
         <m:FoldersToIgnore>
            <t:DistinguishedFolderId Id="deleteditems" />
            <t:DistinguishedFolderId Id="drafts" />
         </m:FoldersToIgnore>
         <m:SortOrder>TreeOrderDescending</m:SortOrder>
         <m:Conversations>
            <t:Conversation>
               <t:ConversationId Id="AAQkADEzOTExYjJkakJCs=" />
            </t:Conversation>
         </m:Conversations>
      </m:GetConversationItems>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="d943e-131">**GetConversationItems**请求此示例不包括以下选项：</span><span class="sxs-lookup"><span data-stu-id="d943e-131">This example of a **GetConversationItems** request does not include the following options:</span></span> 
  
- <span data-ttu-id="d943e-132">[MaxItemsToReturn](maxitemstoreturn.md)元素，设置要在响应中返回的项的最大数目。</span><span class="sxs-lookup"><span data-stu-id="d943e-132">The [MaxItemsToReturn](maxitemstoreturn.md) element, which sets the maximum number of items to return in the response.</span></span> 
    
- <span data-ttu-id="d943e-133">[MailboxScope](mailboxscope.md)元素，它通过指示**GetConversationItems**操作是否执行主邮箱、 存档邮箱中或两个邮箱上设置邮箱范围。</span><span class="sxs-lookup"><span data-stu-id="d943e-133">The [MailboxScope](mailboxscope.md) element, which sets the mailbox scope by indicating whether the **GetConversationItems** operation is to be performed on the primary mailbox, the archive mailbox, or both mailboxes.</span></span> 
    
- <span data-ttu-id="d943e-134">[SyncState (base64Binary)](syncstate-base64binary.md)元素，设置要仅获取对话项目的新的或更新对话中的同步状态。</span><span class="sxs-lookup"><span data-stu-id="d943e-134">The [SyncState (base64Binary)](syncstate-base64binary.md) element, which sets the synchronization state to only get conversation items that are new or updated in the conversation.</span></span> <span data-ttu-id="d943e-135">此元素设置为每个对话。</span><span class="sxs-lookup"><span data-stu-id="d943e-135">This element is set for each conversation.</span></span> 
    
<span data-ttu-id="d943e-136">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="d943e-136">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="d943e-137">GetConversationItems</span><span class="sxs-lookup"><span data-stu-id="d943e-137">GetConversationItems</span></span>](getconversationitems.md)
    
- [<span data-ttu-id="d943e-138">ItemShape</span><span class="sxs-lookup"><span data-stu-id="d943e-138">ItemShape</span></span>](itemshape.md)
    
- [<span data-ttu-id="d943e-139">BaseShape</span><span class="sxs-lookup"><span data-stu-id="d943e-139">BaseShape</span></span>](baseshape.md)
    
- [<span data-ttu-id="d943e-140">AdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="d943e-140">AdditionalProperties</span></span>](additionalproperties.md)
    
- [<span data-ttu-id="d943e-141">FieldURI</span><span class="sxs-lookup"><span data-stu-id="d943e-141">FieldURI</span></span>](fielduri.md)
    
- [<span data-ttu-id="d943e-142">FoldersToIgnore</span><span class="sxs-lookup"><span data-stu-id="d943e-142">FoldersToIgnore</span></span>](folderstoignore.md)
    
- [<span data-ttu-id="d943e-143">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="d943e-143">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="d943e-144">SortOrder (ConversationNodeSortOrder)</span><span class="sxs-lookup"><span data-stu-id="d943e-144">SortOrder (ConversationNodeSortOrder)</span></span>](sortorder-conversationnodesortorder.md)
    
- [<span data-ttu-id="d943e-145">Conversations</span><span class="sxs-lookup"><span data-stu-id="d943e-145">Conversations</span></span>](conversations-ex15websvcsotherref.md)
    
- [<span data-ttu-id="d943e-146">对话 (ConversationRequestType)</span><span class="sxs-lookup"><span data-stu-id="d943e-146">Conversation (ConversationRequestType)</span></span>](conversation-conversationrequesttype.md)
    
- [<span data-ttu-id="d943e-147">ConversationId</span><span class="sxs-lookup"><span data-stu-id="d943e-147">ConversationId</span></span>](conversationid.md)
    
## <a name="successful-getconversationitems-operation-response"></a><span data-ttu-id="d943e-148">成功 GetConversationItems 操作响应</span><span class="sxs-lookup"><span data-stu-id="d943e-148">Successful GetConversationItems operation response</span></span>

<span data-ttu-id="d943e-149">下面的示例演示了单个会话中获取项的**GetConversationItems**操作请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="d943e-149">The following example shows a successful response to a **GetConversationItems** operation request to get items in a single conversation.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15"
                           MinorVersion="0"
                           MajorBuildNumber="545"
                           MinorBuildNumber="11"
                           Version="Exchange2013"
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:GetConversationItemsResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:GetConversationItemsResponseMessage ResponseClass="Success">
               <m:ResponseCode>NoError</m:ResponseCode>
               <m:Conversation>
                  <t:ConversationId Id="AAQkADEzOTExYjJkakJCs=" />
                  <t:SyncState>AQIAAABNVkUwAgIAAABhHqHUAwIAAABNVkUxBAIAAABhHqHfBAIAAABhHqHV</t:SyncState>
                  <t:ConversationNodes>
                     <t:ConversationNode>
                        <t:InternetMessageId>6a4838fa804045e09d40c1a39b9ea916@contoso.com</t:InternetMessageId>
                        <t:ParentInternetMessageId>15a56698d503438fbdaa18186d5b81b7@contoso.com</t:ParentInternetMessageId>
                        <t:Items>
                           <t:Message>
                              <t:ItemId Id="AAMkADEzOTQrAABhHqHfAAA=" ChangeKey="CQAAABYAAACYAABhPpaq" />
                              <t:Subject>RE: Daily issue scrub</t:Subject>
                              <t:DateTimeReceived>2012-10-30T18:42:27Z</t:DateTimeReceived>
                           </t:Message>
                        </t:Items>
                     </t:ConversationNode>
                     <t:ConversationNode>
                        <t:InternetMessageId>2695d2b837954d68846b0c30491f5af1@contoso.com</t:InternetMessageId>
                        <t:ParentInternetMessageId>15a56698d503438fbdaa18186d5b81b7@contoso.com</t:ParentInternetMessageId>
                        <t:Items>
                           <t:Message>
                              <t:ItemId Id="AAMkADEzOTExYjJkLTYxZDAt" ChangeKey="CQAAABQrAABhPpaP" />
                              <t:Subject>RE: Daily issue scrub</t:Subject>
                              <t:DateTimeReceived>2012-10-30T17:38:26Z</t:DateTimeReceived>
                           </t:Message>
                        </t:Items>
                     </t:ConversationNode>
                     <t:ConversationNode>
                        <t:InternetMessageId>15a56698d503438fbdaa18186d5b81b7@contoso.com</t:InternetMessageId>
                        <t:ParentInternetMessageId>d3113e59c89c4288ae13100d033f8dbc@contoso.com</t:ParentInternetMessageId>
                        <t:Items>
                           <t:Message>
                              <t:ItemId Id="AAMkADEzOTFNVkUxAAA=" ChangeKey="CQAAABY4QrAABhPvYK" />
                              <t:Subject>RE: Daily issue scrub</t:Subject>
                              <t:DateTimeReceived>2012-10-30T17:37:00Z</t:DateTimeReceived>
                           </t:Message>
                        </t:Items>
                     </t:ConversationNode>
                     <t:ConversationNode>
                        <t:InternetMessageId>d3113e59c89c4288ae13100d033f8dbc@contoso.com</t:InternetMessageId>
                        <t:ParentInternetMessageId>189b712056c2430dbce334b40496ad00@contoso.com</t:ParentInternetMessageId>
                        <t:Items>
                           <t:Message>
                              <t:ItemId Id="AAMkm4QrAABhHqHUAAA=" ChangeKey="CQAAABQrAABhPpaN" />
                              <t:Subject>RE: Daily issue scrub</t:Subject>
                              <t:DateTimeReceived>2012-10-30T17:37:05Z</t:DateTimeReceived>
                           </t:Message>
                        </t:Items>
                     </t:ConversationNode>
                     <t:ConversationNode>
                        <t:InternetMessageId>189b712056c2430dbce334b40496ad00@contoso.com</t:InternetMessageId>
                        <t:Items>
                           <t:Message>
                              <t:ItemId Id="AAMkArAABNVkUwAAA=" ChangeKey="CQAAABm4QrAABhPvYJ" />
                              <t:Subject>Daily issue scrub</t:Subject>
                              <t:DateTimeReceived>2012-10-30T17:36:00Z</t:DateTimeReceived>
                           </t:Message>
                        </t:Items>
                     </t:ConversationNode>
                  </t:ConversationNodes>
               </m:Conversation>
            </m:GetConversationItemsResponseMessage>
         </m:ResponseMessages>
      </m:GetConversationItemsResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="d943e-150">我们建议您保存的后续**GetConversationItems**操作请求 SyncState。</span><span class="sxs-lookup"><span data-stu-id="d943e-150">We recommend that you save the SyncState for subsequent **GetConversationItems** operation requests.</span></span> 
  
<span data-ttu-id="d943e-151">响应 SOAP 正文中包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="d943e-151">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="d943e-152">GetConversationItemsResponse</span><span class="sxs-lookup"><span data-stu-id="d943e-152">GetConversationItemsResponse</span></span>](getconversationitemsresponse.md)
    
- [<span data-ttu-id="d943e-153">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d943e-153">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="d943e-154">GetConversationItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d943e-154">GetConversationItemsResponseMessage</span></span>](getconversationitemsresponsemessage.md)
    
- [<span data-ttu-id="d943e-155">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d943e-155">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="d943e-156">对话 (ConversationResponseType)</span><span class="sxs-lookup"><span data-stu-id="d943e-156">Conversation (ConversationResponseType)</span></span>](conversation-conversationresponsetype.md)
    
- [<span data-ttu-id="d943e-157">ConversationId</span><span class="sxs-lookup"><span data-stu-id="d943e-157">ConversationId</span></span>](conversationid.md)
    
- [<span data-ttu-id="d943e-158">SyncState (base64Binary)</span><span class="sxs-lookup"><span data-stu-id="d943e-158">SyncState (base64Binary)</span></span>](syncstate-base64binary.md)
    
- [<span data-ttu-id="d943e-159">ConversationNodes</span><span class="sxs-lookup"><span data-stu-id="d943e-159">ConversationNodes</span></span>](conversationnodes.md)
    
- [<span data-ttu-id="d943e-160">ConversationNode</span><span class="sxs-lookup"><span data-stu-id="d943e-160">ConversationNode</span></span>](conversationnode.md)
    
- [<span data-ttu-id="d943e-161">InternetMessageId</span><span class="sxs-lookup"><span data-stu-id="d943e-161">InternetMessageId</span></span>](internetmessageid.md)
    
- [<span data-ttu-id="d943e-162">项目 (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="d943e-162">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
- [<span data-ttu-id="d943e-163">Message</span><span class="sxs-lookup"><span data-stu-id="d943e-163">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="d943e-164">ItemId</span><span class="sxs-lookup"><span data-stu-id="d943e-164">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="d943e-165">Subject</span><span class="sxs-lookup"><span data-stu-id="d943e-165">Subject</span></span>](subject.md)
    
- [<span data-ttu-id="d943e-166">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="d943e-166">DateTimeReceived</span></span>](datetimereceived.md)
    
## <a name="getconversationitems-operation-error-response"></a><span data-ttu-id="d943e-167">GetConversationItems 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="d943e-167">GetConversationItems operation error response</span></span>

<span data-ttu-id="d943e-168">下面的示例显示邮箱，或将被忽略的文件夹中，对话的所有项目都位于其中任一不再存在的会话中获取项的**GetConversationItems**操作请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="d943e-168">The following example shows an error response to a **GetConversationItems** operation request to get items in a conversation that either no longer exists in the mailbox, or for which all the conversation items are located in folders that are ignored.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="556" MinorBuildNumber="8" Version="Exchange2013" xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" xmlns="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetConversationItemsResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetConversationItemsResponseMessage ResponseClass="Error">
          <m:MessageText>The specified object was not found in the store.</m:MessageText>
          <m:ResponseCode>ErrorItemNotFound</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:GetConversationItemsResponseMessage>
      </m:ResponseMessages>
    </m:GetConversationItemsResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="d943e-169">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d943e-169">See also</span></span>

- [<span data-ttu-id="d943e-170">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="d943e-170">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="d943e-171">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="d943e-171">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)
    
- [<span data-ttu-id="d943e-172">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="d943e-172">FindConversation operation</span></span>](findconversation-operation.md)
    

