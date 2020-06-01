---
title: GetConversationItems 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8ae00a99-b37b-4194-829c-fe300db6ab99
description: 查找有关 GetConversationItems 操作的信息。
ms.openlocfilehash: ddeb5386e56653a32ca2e6d212518704cd0f0c58
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457779"
---
# <a name="getconversationitems-operation"></a><span data-ttu-id="557f4-103">GetConversationItems 操作</span><span class="sxs-lookup"><span data-stu-id="557f4-103">GetConversationItems operation</span></span>

<span data-ttu-id="557f4-104">查找有关**GetConversationItems**操作的信息。</span><span class="sxs-lookup"><span data-stu-id="557f4-104">Find information about the **GetConversationItems** operation.</span></span> 
  
<span data-ttu-id="557f4-105">**GetConversationItems**操作获取组织到对话中的节点的一组或多组项目。</span><span class="sxs-lookup"><span data-stu-id="557f4-105">The **GetConversationItems** operation gets one or more sets of items that are organized in to nodes in a conversation.</span></span> 
  
<span data-ttu-id="557f4-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="557f4-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getconversationitems-operation"></a><span data-ttu-id="557f4-107">使用 GetConversationItems 操作</span><span class="sxs-lookup"><span data-stu-id="557f4-107">Using the GetConversationItems operation</span></span>

<span data-ttu-id="557f4-108">您可以使用**GetConversationItems**操作获取主邮箱和存档邮箱的会话中的项目。</span><span class="sxs-lookup"><span data-stu-id="557f4-108">You can use the **GetConversationItems** operation to get items in conversations for both primary and archive mailboxes.</span></span> 
  
### <a name="getconversationitems-operation-soap-headers"></a><span data-ttu-id="557f4-109">GetConversationItems 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="557f4-109">GetConversationItems operation SOAP headers</span></span>

<span data-ttu-id="557f4-110">**GetConversationItems**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="557f4-110">The **GetConversationItems** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="557f4-111">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="557f4-111">**Header name**</span></span>|<span data-ttu-id="557f4-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="557f4-112">**Element**</span></span>|<span data-ttu-id="557f4-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="557f4-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="557f4-114">**模拟**</span><span class="sxs-lookup"><span data-stu-id="557f4-114">**Impersonation**</span></span> <br/> |[<span data-ttu-id="557f4-115">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="557f4-115">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="557f4-116">标识客户端应用程序模拟的用户。</span><span class="sxs-lookup"><span data-stu-id="557f4-116">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="557f4-117">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="557f4-117">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="557f4-118">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="557f4-118">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="557f4-119">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="557f4-119">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="557f4-120">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="557f4-120">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="557f4-121">此元素的最小值为**Exchange2013**。</span><span class="sxs-lookup"><span data-stu-id="557f4-121">The minimum value for this element is **Exchange2013**.</span></span> <span data-ttu-id="557f4-122">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="557f4-122">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="557f4-123">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="557f4-123">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="557f4-124">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="557f4-124">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="557f4-125">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="557f4-125">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="557f4-126">此标头适用于响应。</span><span class="sxs-lookup"><span data-stu-id="557f4-126">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getconversationitems-operation-request-example-get-items-in-a-single-conversation"></a><span data-ttu-id="557f4-127">GetConversationItems 操作请求示例：获取单个对话中的项目</span><span class="sxs-lookup"><span data-stu-id="557f4-127">GetConversationItems operation request example: Get items in a single conversation</span></span>

<span data-ttu-id="557f4-128">下面的**GetConversationItems**操作请求示例演示如何在单个对话中获取所有对话项目，但 "已删除邮件" 和 "草稿" 文件夹中的项目除外。</span><span class="sxs-lookup"><span data-stu-id="557f4-128">The following example of a **GetConversationItems** operation request shows how to get all conversation items in a single conversation, with the exception of items located in the Deleted Items and Drafts folders.</span></span> <span data-ttu-id="557f4-129">响应中返回的每个项目都将包含一个项目标识符、一个主题以及在邮箱中接收项目的时间。</span><span class="sxs-lookup"><span data-stu-id="557f4-129">Each item returned in the response will contain an item identifier, a subject, and the time that the item was received in the mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="557f4-130">本文中的所有项目标识符和更改密钥都已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="557f4-130">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
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

<span data-ttu-id="557f4-131">此**GetConversationItems**请求的示例中不包含以下选项：</span><span class="sxs-lookup"><span data-stu-id="557f4-131">This example of a **GetConversationItems** request does not include the following options:</span></span> 
  
- <span data-ttu-id="557f4-132">[MaxItemsToReturn](maxitemstoreturn.md)元素，该元素设置响应中返回的最大项目数。</span><span class="sxs-lookup"><span data-stu-id="557f4-132">The [MaxItemsToReturn](maxitemstoreturn.md) element, which sets the maximum number of items to return in the response.</span></span> 
    
- <span data-ttu-id="557f4-133">[MailboxScope](mailboxscope.md)元素，它通过指示是否要对主邮箱、存档邮箱或这两个邮箱执行**GetConversationItems**操作来设置邮箱作用域。</span><span class="sxs-lookup"><span data-stu-id="557f4-133">The [MailboxScope](mailboxscope.md) element, which sets the mailbox scope by indicating whether the **GetConversationItems** operation is to be performed on the primary mailbox, the archive mailbox, or both mailboxes.</span></span> 
    
- <span data-ttu-id="557f4-134">[SyncState （base64Binary）](syncstate-base64binary.md)元素，该元素将同步状态设置为仅获取会话中新的或已更新的对话项目。</span><span class="sxs-lookup"><span data-stu-id="557f4-134">The [SyncState (base64Binary)](syncstate-base64binary.md) element, which sets the synchronization state to only get conversation items that are new or updated in the conversation.</span></span> <span data-ttu-id="557f4-135">此元素是为每个对话设置的。</span><span class="sxs-lookup"><span data-stu-id="557f4-135">This element is set for each conversation.</span></span> 
    
<span data-ttu-id="557f4-136">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="557f4-136">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="557f4-137">GetConversationItems</span><span class="sxs-lookup"><span data-stu-id="557f4-137">GetConversationItems</span></span>](getconversationitems.md)
    
- [<span data-ttu-id="557f4-138">ItemShape</span><span class="sxs-lookup"><span data-stu-id="557f4-138">ItemShape</span></span>](itemshape.md)
    
- [<span data-ttu-id="557f4-139">BaseShape</span><span class="sxs-lookup"><span data-stu-id="557f4-139">BaseShape</span></span>](baseshape.md)
    
- [<span data-ttu-id="557f4-140">AdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="557f4-140">AdditionalProperties</span></span>](additionalproperties.md)
    
- [<span data-ttu-id="557f4-141">FieldURI</span><span class="sxs-lookup"><span data-stu-id="557f4-141">FieldURI</span></span>](fielduri.md)
    
- [<span data-ttu-id="557f4-142">FoldersToIgnore</span><span class="sxs-lookup"><span data-stu-id="557f4-142">FoldersToIgnore</span></span>](folderstoignore.md)
    
- [<span data-ttu-id="557f4-143">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="557f4-143">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="557f4-144">SortOrder （ConversationNodeSortOrder）</span><span class="sxs-lookup"><span data-stu-id="557f4-144">SortOrder (ConversationNodeSortOrder)</span></span>](sortorder-conversationnodesortorder.md)
    
- [<span data-ttu-id="557f4-145">对话</span><span class="sxs-lookup"><span data-stu-id="557f4-145">Conversations</span></span>](conversations-ex15websvcsotherref.md)
    
- [<span data-ttu-id="557f4-146">对话（ConversationRequestType）</span><span class="sxs-lookup"><span data-stu-id="557f4-146">Conversation (ConversationRequestType)</span></span>](conversation-conversationrequesttype.md)
    
- [<span data-ttu-id="557f4-147">ConversationId</span><span class="sxs-lookup"><span data-stu-id="557f4-147">ConversationId</span></span>](conversationid.md)
    
## <a name="successful-getconversationitems-operation-response"></a><span data-ttu-id="557f4-148">成功的 GetConversationItems 操作响应</span><span class="sxs-lookup"><span data-stu-id="557f4-148">Successful GetConversationItems operation response</span></span>

<span data-ttu-id="557f4-149">下面的示例演示对**GetConversationItems**操作请求的成功响应，以获取单个对话中的项目。</span><span class="sxs-lookup"><span data-stu-id="557f4-149">The following example shows a successful response to a **GetConversationItems** operation request to get items in a single conversation.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15"
                           MinorVersion="0"
                           MajorBuildNumber="545"
                           MinorBuildNumber="11"
                           Version="Exchange2013"
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:GetConversationItemsResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="557f4-150">建议您为后续的**GetConversationItems**操作请求保存 SyncState。</span><span class="sxs-lookup"><span data-stu-id="557f4-150">We recommend that you save the SyncState for subsequent **GetConversationItems** operation requests.</span></span> 
  
<span data-ttu-id="557f4-151">响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="557f4-151">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="557f4-152">GetConversationItemsResponse</span><span class="sxs-lookup"><span data-stu-id="557f4-152">GetConversationItemsResponse</span></span>](getconversationitemsresponse.md)
    
- [<span data-ttu-id="557f4-153">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="557f4-153">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="557f4-154">GetConversationItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="557f4-154">GetConversationItemsResponseMessage</span></span>](getconversationitemsresponsemessage.md)
    
- [<span data-ttu-id="557f4-155">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="557f4-155">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="557f4-156">对话（ConversationResponseType）</span><span class="sxs-lookup"><span data-stu-id="557f4-156">Conversation (ConversationResponseType)</span></span>](conversation-conversationresponsetype.md)
    
- [<span data-ttu-id="557f4-157">ConversationId</span><span class="sxs-lookup"><span data-stu-id="557f4-157">ConversationId</span></span>](conversationid.md)
    
- [<span data-ttu-id="557f4-158">SyncState (base64Binary)</span><span class="sxs-lookup"><span data-stu-id="557f4-158">SyncState (base64Binary)</span></span>](syncstate-base64binary.md)
    
- [<span data-ttu-id="557f4-159">ConversationNodes</span><span class="sxs-lookup"><span data-stu-id="557f4-159">ConversationNodes</span></span>](conversationnodes.md)
    
- [<span data-ttu-id="557f4-160">ConversationNode</span><span class="sxs-lookup"><span data-stu-id="557f4-160">ConversationNode</span></span>](conversationnode.md)
    
- [<span data-ttu-id="557f4-161">InternetMessageId</span><span class="sxs-lookup"><span data-stu-id="557f4-161">InternetMessageId</span></span>](internetmessageid.md)
    
- [<span data-ttu-id="557f4-162">项目（NonEmptyArrayOfAllItemsType）</span><span class="sxs-lookup"><span data-stu-id="557f4-162">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
- [<span data-ttu-id="557f4-163">邮件</span><span class="sxs-lookup"><span data-stu-id="557f4-163">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="557f4-164">ItemId</span><span class="sxs-lookup"><span data-stu-id="557f4-164">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="557f4-165">主题</span><span class="sxs-lookup"><span data-stu-id="557f4-165">Subject</span></span>](subject.md)
    
- [<span data-ttu-id="557f4-166">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="557f4-166">DateTimeReceived</span></span>](datetimereceived.md)
    
## <a name="getconversationitems-operation-error-response"></a><span data-ttu-id="557f4-167">GetConversationItems 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="557f4-167">GetConversationItems operation error response</span></span>

<span data-ttu-id="557f4-168">下面的示例演示对**GetConversationItems**操作请求的错误响应，以获取对话中不再存在于邮箱中的项目，或在忽略的文件夹中的所有对话项目所在的位置。</span><span class="sxs-lookup"><span data-stu-id="557f4-168">The following example shows an error response to a **GetConversationItems** operation request to get items in a conversation that either no longer exists in the mailbox, or for which all the conversation items are located in folders that are ignored.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="556" MinorBuildNumber="8" Version="Exchange2013" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetConversationItemsResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="see-also"></a><span data-ttu-id="557f4-169">另请参阅</span><span class="sxs-lookup"><span data-stu-id="557f4-169">See also</span></span>

- [<span data-ttu-id="557f4-170">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="557f4-170">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="557f4-171">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="557f4-171">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)
    
- [<span data-ttu-id="557f4-172">FindConversation 操作</span><span class="sxs-lookup"><span data-stu-id="557f4-172">FindConversation operation</span></span>](findconversation-operation.md)
    

