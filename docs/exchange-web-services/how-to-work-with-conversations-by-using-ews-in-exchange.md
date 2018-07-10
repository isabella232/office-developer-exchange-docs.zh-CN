---
title: 通过在 Exchange 使用 EWS 来处理对话
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7750528c-acb2-43e5-a1e1-ee201c0e1730
description: 了解如何查找对话、 适用于对话的操作和 Exchange 使用 EWS 托管 API 或 EWS 对话中获取项。
ms.openlocfilehash: 71ef7674086607e1544111071928f3dd74073a77
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752911"
---
# <a name="work-with-conversations-by-using-ews-in-exchange"></a><span data-ttu-id="142c2-103">通过在 Exchange 使用 EWS 来处理对话</span><span class="sxs-lookup"><span data-stu-id="142c2-103">Work with conversations by using EWS in Exchange</span></span>

<span data-ttu-id="142c2-104">了解如何查找对话、 适用于对话的操作和 Exchange 使用 EWS 托管 API 或 EWS 对话中获取项。</span><span class="sxs-lookup"><span data-stu-id="142c2-104">Learn about how to find conversations, apply actions to conversations, and get items in conversations by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="142c2-105">在 Exchange 的上下文中，对话是一种方式进行分组和管理一组相关的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="142c2-105">In the context of Exchange, conversations are a way to group and manage a related set of email messages.</span></span> <span data-ttu-id="142c2-106">他们还可以提供一种方法查看相关的邮件。</span><span class="sxs-lookup"><span data-stu-id="142c2-106">They can also provide a way to view related messages.</span></span> <span data-ttu-id="142c2-107">Exchange 定义基于线程中的第一个电子邮件**消息 ID**值的对话。</span><span class="sxs-lookup"><span data-stu-id="142c2-107">Exchange defines conversations based on the **Message-ID** value of the first email message in a thread.</span></span> <span data-ttu-id="142c2-108">全部答复和相关的消息引用其**引用**中的原始消息的**消息 ID**标头和 **-答复**邮件头。</span><span class="sxs-lookup"><span data-stu-id="142c2-108">All replies and related messages reference the original message's **Message-ID** header in their **References** and **In-Reply-To** headers.</span></span> 
  
<span data-ttu-id="142c2-109">此外，在 SOAP 信封，为每个邮箱中接收的消息 Exchange 将设置特定的属性和元素。</span><span class="sxs-lookup"><span data-stu-id="142c2-109">Additionally, inside the SOAP envelope, for each message received in a mailbox, Exchange sets specific properties and elements.</span></span>
  
<span data-ttu-id="142c2-110">**表 1。对话属性和元素上所有电子邮件设置**</span><span class="sxs-lookup"><span data-stu-id="142c2-110">**Table 1. Conversation properties and elements set on all email messages**</span></span>

|<span data-ttu-id="142c2-111">**EWS 托管 API 属性**</span><span class="sxs-lookup"><span data-stu-id="142c2-111">**EWS Managed API property**</span></span>|<span data-ttu-id="142c2-112">**EWS 元素**</span><span class="sxs-lookup"><span data-stu-id="142c2-112">**EWS element**</span></span>|<span data-ttu-id="142c2-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="142c2-113">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="142c2-114">ConversationTopic</span><span class="sxs-lookup"><span data-stu-id="142c2-114">ConversationTopic</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.emailmessage.conversationtopic%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="142c2-115">ConversationTopic</span><span class="sxs-lookup"><span data-stu-id="142c2-115">ConversationTopic</span></span>](http://msdn.microsoft.com/library/46cacf42-4039-4c8a-9b20-c42cdd9f2760%28Office.15%29.aspx) <br/> |<span data-ttu-id="142c2-116">包含对原始邮件已设置主题值的规范化窗体。</span><span class="sxs-lookup"><span data-stu-id="142c2-116">Contains a normalized form of the subject value that was set on the original message.</span></span> <span data-ttu-id="142c2-117">这是**线程主题**邮件头相同。</span><span class="sxs-lookup"><span data-stu-id="142c2-117">This is the same as the **Thread-Topic** message header.</span></span> <span data-ttu-id="142c2-118">此值是只读的。</span><span class="sxs-lookup"><span data-stu-id="142c2-118">This value is read-only.</span></span>  <br/> |
|[<span data-ttu-id="142c2-119">ConversationIndex</span><span class="sxs-lookup"><span data-stu-id="142c2-119">ConversationIndex</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.emailmessage.conversationindex%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="142c2-120">ConversationIndex</span><span class="sxs-lookup"><span data-stu-id="142c2-120">ConversationIndex</span></span>](http://msdn.microsoft.com/library/fdf47e22-8d93-4ae4-883b-0c9f07f48724%28Office.15%29.aspx) <br/> |<span data-ttu-id="142c2-121">代表会话中的项的位置。</span><span class="sxs-lookup"><span data-stu-id="142c2-121">Represents the position of the item in the conversation.</span></span> <span data-ttu-id="142c2-122">这是**线程索引**邮件头相同。</span><span class="sxs-lookup"><span data-stu-id="142c2-122">This is the same as the **Thread-Index** message header.</span></span> <span data-ttu-id="142c2-123">此值是只读的。</span><span class="sxs-lookup"><span data-stu-id="142c2-123">This value is read-only.</span></span>  <br/> |
   
<span data-ttu-id="142c2-124">Exchange 相同的**ConversationTopic**值应用于回复到第一条消息，然后更新**ConversationIndex**值，表示相对于原始邮件消息的位置。</span><span class="sxs-lookup"><span data-stu-id="142c2-124">Exchange applies the same **ConversationTopic** value to replies to the first message and then updates the **ConversationIndex** value to represent the message's position relative to the original message.</span></span> <span data-ttu-id="142c2-125">如果发生更改的电子邮件线程主题，Exchange 将新**ConversationTopic**值和新的**ConversationIndex**值适用于新的对话。</span><span class="sxs-lookup"><span data-stu-id="142c2-125">If the subject of the email thread changes, Exchange applies a new **ConversationTopic** value and new **ConversationIndex** values to the new conversation.</span></span> 
  
<span data-ttu-id="142c2-126">**表 2。EWS 托管 API 方法和用于处理的对话的 EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="142c2-126">**Table 2. EWS Managed API methods and EWS operations for working with conversations**</span></span>

|<span data-ttu-id="142c2-127">**若要...**</span><span class="sxs-lookup"><span data-stu-id="142c2-127">**In order to…**</span></span>|<span data-ttu-id="142c2-128">**使用此 EWS 托管 API 方法**</span><span class="sxs-lookup"><span data-stu-id="142c2-128">**Use this EWS Managed API method or methods**</span></span>|<span data-ttu-id="142c2-129">**使用此 EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="142c2-129">**Use this EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="142c2-130">查找对话</span><span class="sxs-lookup"><span data-stu-id="142c2-130">Find conversations</span></span>  <br/> |[<span data-ttu-id="142c2-131">ExchangeService.FindConversation</span><span class="sxs-lookup"><span data-stu-id="142c2-131">ExchangeService.FindConversation</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.findconversation%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="142c2-132">FindConversation</span><span class="sxs-lookup"><span data-stu-id="142c2-132">FindConversation</span></span>](http://msdn.microsoft.com/library/2384908a-c203-45b6-98aa-efd6a4c23aac%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="142c2-133">应用对话操作</span><span class="sxs-lookup"><span data-stu-id="142c2-133">Apply conversation actions</span></span>  <br/> |[<span data-ttu-id="142c2-134">Conversation.EnableAlwaysCategorizeItems</span><span class="sxs-lookup"><span data-stu-id="142c2-134">Conversation.EnableAlwaysCategorizeItems</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.conversation.enablealwayscategorizeitems%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="142c2-135">Conversation.EnableAlwaysDeleteItems</span><span class="sxs-lookup"><span data-stu-id="142c2-135">Conversation.EnableAlwaysDeleteItems</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.conversation.enablealwaysdeleteitems%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="142c2-136">Conversation.EnableAlwaysMoveItems</span><span class="sxs-lookup"><span data-stu-id="142c2-136">Conversation.EnableAlwaysMoveItems</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.conversation.enablealwaysmoveitems%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="142c2-137">ExchangeService.CopyItemsInConversations</span><span class="sxs-lookup"><span data-stu-id="142c2-137">ExchangeService.CopyItemsInConversations</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.copyitemsinconversations%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="142c2-138">ExchangeService.DeleteItemsInConversations</span><span class="sxs-lookup"><span data-stu-id="142c2-138">ExchangeService.DeleteItemsInConversations</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.deleteitemsinconversations%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="142c2-139">ExchangeService.DisableAlwaysCategorizeItemsInConversations</span><span class="sxs-lookup"><span data-stu-id="142c2-139">ExchangeService.DisableAlwaysCategorizeItemsInConversations</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.disablealwayscategorizeitemsinconversations%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="142c2-140">ExchangeService.DisableAlwaysDeleteItemsInConversations</span><span class="sxs-lookup"><span data-stu-id="142c2-140">ExchangeService.DisableAlwaysDeleteItemsInConversations</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.disablealwaysdeleteitemsinconversations%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="142c2-141">ExchangeService.DisableAlwaysMoveItemsInConversations</span><span class="sxs-lookup"><span data-stu-id="142c2-141">ExchangeService.DisableAlwaysMoveItemsInConversations</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.disablealwaysmoveitemsinconversations%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="142c2-142">ExchangeService.EnableAlwaysCategorizeItemsInConversations</span><span class="sxs-lookup"><span data-stu-id="142c2-142">ExchangeService.EnableAlwaysCategorizeItemsInConversations</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.enablealwayscategorizeitemsinconversations%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="142c2-143">ExchangeService.EnableAlwaysDeleteItemsInConversations</span><span class="sxs-lookup"><span data-stu-id="142c2-143">ExchangeService.EnableAlwaysDeleteItemsInConversations</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.enablealwaysdeleteitemsinconversations%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="142c2-144">ExchangeService.EnableAlwaysMoveItemsInConversations</span><span class="sxs-lookup"><span data-stu-id="142c2-144">ExchangeService.EnableAlwaysMoveItemsInConversations</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.enablealwaysmoveitemsinconversations%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="142c2-145">ExchangeService.MoveItemsInConversations</span><span class="sxs-lookup"><span data-stu-id="142c2-145">ExchangeService.MoveItemsInConversations</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.moveitemsinconversations%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="142c2-146">ExchangeService.SetFlagStatusForItemsInConversations</span><span class="sxs-lookup"><span data-stu-id="142c2-146">ExchangeService.SetFlagStatusForItemsInConversations</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.setflagstatusforitemsinconversations%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="142c2-147">ExchangeService.SetReadStateForItemsInConversations</span><span class="sxs-lookup"><span data-stu-id="142c2-147">ExchangeService.SetReadStateForItemsInConversations</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.setreadstateforitemsinconversations%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="142c2-148">ExchangeService.SetRetentionPolicyForItemsInConversations</span><span class="sxs-lookup"><span data-stu-id="142c2-148">ExchangeService.SetRetentionPolicyForItemsInConversations</span></span>](http://msdn.microsoft.com/zh-cn/library/office/microsoft.exchange.webservices.data.exchangeservice.setretentionpolicyforitemsinconversations%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="142c2-149">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="142c2-149">ApplyConversationAction</span></span>](http://msdn.microsoft.com/library/73d7943d-d361-4f8b-9948-d85f886efa1a%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="142c2-150">获取一个或多个对话中的项</span><span class="sxs-lookup"><span data-stu-id="142c2-150">Get items in one or more conversations</span></span>  <br/> |[<span data-ttu-id="142c2-151">ExchangeService.GetConversationItems</span><span class="sxs-lookup"><span data-stu-id="142c2-151">ExchangeService.GetConversationItems</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.getconversationitems%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="142c2-152">GetConversationItems</span><span class="sxs-lookup"><span data-stu-id="142c2-152">GetConversationItems</span></span>](http://msdn.microsoft.com/library/8ae00a99-b37b-4194-829c-fe300db6ab99%28Office.15%29.aspx) <br/> |

<span data-ttu-id="142c2-153"><a name="bk_findewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="142c2-153"></span></span>

## <a name="find-a-conversation-by-using-the-ews-managed-api"></a><span data-ttu-id="142c2-154">使用 EWS 托管 API 来查找对话</span><span class="sxs-lookup"><span data-stu-id="142c2-154">Find a conversation by using the EWS Managed API</span></span>

<span data-ttu-id="142c2-155">下面的示例中所示，您可以通过使用[ExchangeService.FindConversation](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.findconversation%28v=exchg.80%29.aspx) EWS 托管 API 方法中，找到对话。</span><span class="sxs-lookup"><span data-stu-id="142c2-155">You can find conversations by using the [ExchangeService.FindConversation](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.findconversation%28v=exchg.80%29.aspx) EWS Managed API method, as shown in the following example.</span></span> <span data-ttu-id="142c2-156">此示例获取主题包含单词收件箱文件夹的前 10 的对话"新闻"。</span><span class="sxs-lookup"><span data-stu-id="142c2-156">This example gets the first 10 conversations in the Inbox folder that have a subject that contains the word "news".</span></span> <span data-ttu-id="142c2-157">该示例然后将写入到控制台窗口的对话主题、 传递上次和全局唯一的收件人列表。</span><span class="sxs-lookup"><span data-stu-id="142c2-157">The example then writes the conversation topic, last delivery time, and global unique recipient list to the console window.</span></span> 
  
<span data-ttu-id="142c2-158">此示例假定 **service** 是有效的 [ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，并且已向 Exchange 服务器对该用户进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="142c2-158">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
static void FindConversation(ExchangeService service)
{
    // Create the view of conversations returned in the response. This view will return at most 10 results.
    ConversationIndexedItemView view = new ConversationIndexedItemView(10);
    // Create the query string to search for.
    String queryString = "subject:news";
    // Search the Inbox for conversations and return a results set with the specified view.
    // This method call results in a FindConversation call to EWS. 
    ICollection<Conversation> conversations = service.FindConversation(view, WellKnownFolderName.Inbox, queryString);
    // Examine properties on each conversation returned in the response.
    foreach (Conversation conversation in conversations)
    {
        Console.WriteLine("Conversation Topic: " + conversation.Topic);
        Console.WriteLine("Last Delivered: " + conversation.LastDeliveryTime.ToString());
        ApplyConversationActions(service, conversation);
        foreach (string GlUniqRec in conversation.GlobalUniqueRecipients)
        {
            Console.WriteLine("Global Unique Recipient: " + GlUniqRec);
        }
        Console.WriteLine("");
    }
}
```

<span data-ttu-id="142c2-159"><a name="bk_findews"> </a></span><span class="sxs-lookup"><span data-stu-id="142c2-159"></span></span>

## <a name="find-a-conversation-by-using-ews"></a><span data-ttu-id="142c2-160">使用 EWS 查找对话</span><span class="sxs-lookup"><span data-stu-id="142c2-160">Find a conversation by using EWS</span></span>

<span data-ttu-id="142c2-161">下面的示例中所示，您可以使用[FindConversation](http://msdn.microsoft.com/library/2384908a-c203-45b6-98aa-efd6a4c23aac%28Office.15%29.aspx) EWS 操作中，找到对话。</span><span class="sxs-lookup"><span data-stu-id="142c2-161">You can find conversations by using the [FindConversation](http://msdn.microsoft.com/library/2384908a-c203-45b6-98aa-efd6a4c23aac%28Office.15%29.aspx) EWS operation, as shown in the following example.</span></span> <span data-ttu-id="142c2-162">此示例获取主题包含单词收件箱文件夹的前 10 个对话"新闻"。</span><span class="sxs-lookup"><span data-stu-id="142c2-162">This example gets the first ten conversations in the Inbox folder that have a subject that contains the word "news".</span></span> <span data-ttu-id="142c2-163">这也是使用 EWS 托管 API 对[查找对话](#bk_findewsma)时，将发送 EWS 托管 API 的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="142c2-163">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [find a conversation](#bk_findewsma).</span></span>
  
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
    <m:FindConversation>
      <m:IndexedPageItemView MaxEntriesReturned="10"
                             Offset="0"
                             BasePoint="Beginning" />
      <m:ParentFolderId>
        <t:DistinguishedFolderId Id="inbox" />
      </m:ParentFolderId>
      <m:QueryString>subject:news</m:QueryString>
    </m:FindConversation>
  </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="142c2-164">服务器响应**FindConversation**请求[FindConversationResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx)邮件包含[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)值**NoError**以指示操作成功完成。</span><span class="sxs-lookup"><span data-stu-id="142c2-164">The server responds to the **FindConversation** request with a [FindConversationResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError** to indicate that the operation completed successfully.</span></span> <span data-ttu-id="142c2-165">响应还包括具有主题包含单词"新闻"的邮箱中的唯一的对话。</span><span class="sxs-lookup"><span data-stu-id="142c2-165">The response also includes the only conversation in the mailbox that has a subject that contains the word "news".</span></span> 
  
<span data-ttu-id="142c2-166">为便于阅读变短了**ItemId**、**更改密钥**和**ConversationId**元素。</span><span class="sxs-lookup"><span data-stu-id="142c2-166">The **ItemId**, **ChangeKey**, and **ConversationId** elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="883"
                         MinorBuildNumber="10"
                         Version="V2_10"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <FindConversationResponse ResponseClass="Success"
                              xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <Conversations>
        <Conversation xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <ConversationId Id="aO2NM+Q=" />
          <ConversationTopic>Today's top news headlines</ConversationTopic>
          <UniqueRecipients>
            <String>Sadie Daniels</String>
          </UniqueRecipients>
          <GlobalUniqueRecipients>
            <String>Sadie Daniels</String>
          </GlobalUniqueRecipients>
          <UniqueUnreadSenders>
            <String>Ronnie Sturgis</String>
          </UniqueUnreadSenders>
          <GlobalUniqueUnreadSenders>
            <String>Ronnie Sturgis</String>
          </GlobalUniqueUnreadSenders>
          <UniqueSenders>
            <String>Ronnie Sturgis</String>
          </UniqueSenders>
          <GlobalUniqueSenders>
            <String>Ronnie Sturgis</String>
          </GlobalUniqueSenders>
          <LastDeliveryTime>2014-02-18T20:42:26Z</LastDeliveryTime>
          <GlobalLastDeliveryTime>2014-02-18T20:42:26Z</GlobalLastDeliveryTime>
          <HasAttachments>false</HasAttachments>
          <GlobalHasAttachments>false</GlobalHasAttachments>
          <MessageCount>1</MessageCount>
          <GlobalMessageCount>1</GlobalMessageCount>
          <UnreadCount>1</UnreadCount>
          <GlobalUnreadCount>1</GlobalUnreadCount>
          <Size>9330</Size>
          <GlobalSize>9330</GlobalSize>
          <ItemClasses>
            <ItemClass>IPM.Note</ItemClass>
          </ItemClasses>
          <GlobalItemClasses>
            <ItemClass>IPM.Note</ItemClass>
          </GlobalItemClasses>
          <Importance>Normal</Importance>
          <GlobalImportance>Normal</GlobalImportance>
          <ItemIds>
            <ItemId Id="sVCyAAA="
                    ChangeKey="CQAAAA==" />
          </ItemIds>
          <GlobalItemIds>
            <ItemId Id="sVCyAAA="
                    ChangeKey="CQAAAA==" />
          </GlobalItemIds>
          <LastModifiedTime>2014-02-18T20:42:26Z</LastModifiedTime>
          <InstanceKey>AQAAAAAAAQABAAAACbFYggAAAAA=</InstanceKey>
          <HasIrm>false</HasIrm>
          <GlobalHasIrm>false</GlobalHasIrm>
        </Conversation>
      </Conversations>
      <TotalConversationsInView>1</TotalConversationsInView>
      <IndexedOffset>1</IndexedOffset>
    </FindConversationResponse>
  </s:Body>
</s:Envelope>

```

<span data-ttu-id="142c2-167"><a name="bk_applyewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="142c2-167"></span></span>

## <a name="apply-conversation-actions-by-using-the-ews-managed-api"></a><span data-ttu-id="142c2-168">使用 EWS 托管 API 应用对话操作</span><span class="sxs-lookup"><span data-stu-id="142c2-168">Apply conversation actions by using the EWS Managed API</span></span>

<span data-ttu-id="142c2-169">下面的示例中所示，可以应用于对话使用大量 EWS 托管 API 方法的对话操作。</span><span class="sxs-lookup"><span data-stu-id="142c2-169">You can apply conversation actions to a conversation by using a number of EWS Managed API methods, as shown in the following example.</span></span> <span data-ttu-id="142c2-170">本示例将类别添加到现有对话中的项目，并将相同的类别应用于对话中的未来项目。</span><span class="sxs-lookup"><span data-stu-id="142c2-170">This example adds categories to existing items in a conversation and applies the same categories to future items in the conversation.</span></span> <span data-ttu-id="142c2-171">它还会显示如何启用自动进入对话中的项目的文件夹。</span><span class="sxs-lookup"><span data-stu-id="142c2-171">It also shows how to enable the automatic moving of items in the conversation to a folder.</span></span> <span data-ttu-id="142c2-172">本示例中，项目移动到草稿文件夹中。</span><span class="sxs-lookup"><span data-stu-id="142c2-172">In this example, items are moved to the Drafts folder.</span></span>
  
<span data-ttu-id="142c2-173">此示例假定 **service** 是有效的 [ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，并且已向 Exchange 服务器对该用户进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="142c2-173">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
<span data-ttu-id="142c2-174">应用对话操作的方法的完整列表，请参阅表 2。</span><span class="sxs-lookup"><span data-stu-id="142c2-174">For a complete list of methods that apply conversation actions, see Table 2.</span></span>
  
```cs
static void ApplyConversationActions(ExchangeService service, Conversation conversation)
{
   // Create a list of categories to apply to a conversation.
   List<string> categories = new List<string>();
   categories.Add("Customer");
   categories.Add("System Integrator");
   // Apply categorization to all items in the conversation and process the request
   // synchronously after enabling this rule and after all item categorization has been applied. 
   // This method call results in an ApplyConversationAction call to EWS.
   conversation.EnableAlwaysCategorizeItems(categories, true);
   // Apply an always move rule to all items in the conversation and move the items
   // to the Drafts folder. Process the request asynchronously and return the response. 
   // immediately. This method call results in an ApplyConversationAction call to EWS.
   conversation.EnableAlwaysMoveItems(WellKnownFolderName.Drafts, false);
}

```

<span data-ttu-id="142c2-175"><a name="bk_applyews"> </a></span><span class="sxs-lookup"><span data-stu-id="142c2-175"></span></span>

## <a name="apply-conversation-actions-by-using-ews"></a><span data-ttu-id="142c2-176">使用 EWS 应用对话操作</span><span class="sxs-lookup"><span data-stu-id="142c2-176">Apply conversation actions by using EWS</span></span>

<span data-ttu-id="142c2-177">您可以应用对话操作、 如分类、 删除和移动，请使用[ApplyConversationAction](http://msdn.microsoft.com/library/73d7943d-d361-4f8b-9948-d85f886efa1a%28Office.15%29.aspx)操作，如下面的示例中所示。</span><span class="sxs-lookup"><span data-stu-id="142c2-177">You can apply conversation actions, such as categorize, delete, and move, by using the [ApplyConversationAction](http://msdn.microsoft.com/library/73d7943d-d361-4f8b-9948-d85f886efa1a%28Office.15%29.aspx) operation, as shown in the following example.</span></span> <span data-ttu-id="142c2-178">本示例将类别添加到现有对话中的项目，并将相同的类别应用于对话中的未来项目。</span><span class="sxs-lookup"><span data-stu-id="142c2-178">This example adds categories to existing items in a conversation and applies the same categories to future items in the conversation.</span></span> <span data-ttu-id="142c2-179">它还会显示如何启用自动进入对话中的项目的文件夹。本示例中，项目移动到草稿文件夹中。</span><span class="sxs-lookup"><span data-stu-id="142c2-179">It also shows how to enable the automatic moving of items in the conversation to a folder; in this example, items are moved to the Drafts folder.</span></span> <span data-ttu-id="142c2-180">这也是使用 EWS 托管 API[应用对话操作](#bk_applyewsma)时，将发送 EWS 托管 API 的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="142c2-180">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [apply conversation actions](#bk_applyewsma).</span></span>
  
<span data-ttu-id="142c2-181">为便于阅读缩短了**ConversationId**元素。</span><span class="sxs-lookup"><span data-stu-id="142c2-181">The **ConversationId** element has been shortened for readability.</span></span> 
  
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
    <m:ApplyConversationAction>
      <m:ConversationActions>
        <t:ConversationAction>
          <t:Action>AlwaysMove</t:Action>
          <t:ConversationId Id="jG6WVpg=" />
          <t:ProcessRightAway>false</t:ProcessRightAway>
          <t:DestinationFolderId>
            <t:DistinguishedFolderId Id="drafts" />
          </t:DestinationFolderId>
        </t:ConversationAction>
      </m:ConversationActions>
    </m:ApplyConversationAction>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="142c2-182">服务器响应**ApplyConversationAction**请求[ApplyConversationActionResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx)邮件包含[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)值**NoError**以指示操作成功完成。</span><span class="sxs-lookup"><span data-stu-id="142c2-182">The server responds to the **ApplyConversationAction** request with a [ApplyConversationActionResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError** to indicate that the operation completed successfully.</span></span> 

<span data-ttu-id="142c2-183"><a name="bk_getitemssingleewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="142c2-183"></span></span>

## <a name="get-items-in-a-single-conversation-by-using-the-conversation-identifier-in-the-ews-managed-api"></a><span data-ttu-id="142c2-184">通过使用 EWS 托管 API 中的对话标识符单个会话中获取项</span><span class="sxs-lookup"><span data-stu-id="142c2-184">Get items in a single conversation by using the conversation identifier in the EWS Managed API</span></span>

<span data-ttu-id="142c2-185">使用[ExchangeService.GetConversationItems](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.getconversationitems%28v=exchg.80%29.aspx) EWS 托管 API 方法，可以在对话中获取项。</span><span class="sxs-lookup"><span data-stu-id="142c2-185">You can get items in a conversation by using the [ExchangeService.GetConversationItems](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.getconversationitems%28v=exchg.80%29.aspx) EWS Managed API method.</span></span> <span data-ttu-id="142c2-186">该示例提供的收件箱中的第一个对话的对话节点集。</span><span class="sxs-lookup"><span data-stu-id="142c2-186">This example provides the set of conversation nodes for the first conversation in the Inbox.</span></span> <span data-ttu-id="142c2-187">在响应中，以及对话索引和 parent 对话索引属性返回的项标识符、 主题和每个项目的接收的时间。</span><span class="sxs-lookup"><span data-stu-id="142c2-187">The item identifier, subject, and received time for each item are returned in the response, along with the conversation index and parent conversation index properties.</span></span> <span data-ttu-id="142c2-188">您可以使用对话索引属性重新构造节点层次结构。</span><span class="sxs-lookup"><span data-stu-id="142c2-188">You can use the conversation index properties to reconstruct the node hierarchy.</span></span> 
  
<span data-ttu-id="142c2-189">本示例中，默认已删除邮件和草稿文件夹中的所有对话项目将被都忽略。</span><span class="sxs-lookup"><span data-stu-id="142c2-189">In this example, all conversation items in the default Deleted Items and Drafts folders are ignored.</span></span>
  
<span data-ttu-id="142c2-190">此示例假定 **service** 是有效的 [ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，并且已向 Exchange 服务器对该用户进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="142c2-190">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
static void GetConversationItemsSingleConversation(ExchangeService service)
{
   try
   {
      // Find the first item in the mailbox.
      // This method call results in an FindItem call to EWS.
      FindItemsResults<Item> results = service.FindItems(WellKnownFolderName.Inbox,
                                                         new ItemView(1));
      // Get the conversation identifier of the item. 
      ConversationId convId = results.Items[0].ConversationId;
      // Specify the properties that will be 
      // returned for the items in the conversation.
      PropertySet properties = new PropertySet(BasePropertySet.IdOnly,
                                                ItemSchema.Subject,
                                                ItemSchema.DateTimeReceived);
      // Identify the folders to ignore.
      Collection<FolderId> foldersToIgnore = new Collection<FolderId>() 
          { WellKnownFolderName.DeletedItems, WellKnownFolderName.Drafts };
      // Request the conversation items.
      // This method call results in an GetConversationItems call to EWS.
      ConversationResponse response = service.GetConversationItems(convId,
                                                   properties,
                                                  null,
                                                  foldersToIgnore,
                                                  ConversationSortOrder.TreeOrderDescending);
      // Get the synchronization state of the conversation.
      Console.WriteLine("SyncState: " + response.SyncState);
      Collection<Item> items = new Collection<Item>();
      // Process each node of conversation items.
      foreach (ConversationNode node in response.ConversationNodes)
      {
         Console.WriteLine("Parent conversation index: " + node.ParentConversationIndex);
         Console.WriteLine("Conversation index: " + node.ConversationIndex);
         Console.WriteLine("Conversation node items:");
         // Process each item in the conversation node.
         foreach (Item item in node.Items)
         {
            Console.WriteLine("   Item ID: " + item.Id.UniqueId);
            Console.WriteLine("   Subject: " + item.Subject);
            Console.WriteLine("   Received: " + item.DateTimeReceived);
            items.Add(item);
         }
      }
   }
   // This exception occurs if there is an error with the service.
   catch (ServiceResponseException srException)
   {
      Console.WriteLine(srException);
   }
}

```

<span data-ttu-id="142c2-191">我们建议您缓存后续请求会话中获取项的**SyncState**属性。</span><span class="sxs-lookup"><span data-stu-id="142c2-191">We recommend that you cache the **SyncState** property for subsequent requests to get items in the conversation.</span></span> 

<span data-ttu-id="142c2-192"><a name="bk_getitemsmanyewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="142c2-192"></span></span>

## <a name="get-items-in-many-conversations-by-using-the-conversationrequest-object-in-the-ews-managed-api"></a><span data-ttu-id="142c2-193">通过使用 EWS 托管 API 中的 ConversationRequest 对象在很多对话中获取项</span><span class="sxs-lookup"><span data-stu-id="142c2-193">Get items in many conversations by using the ConversationRequest object in the EWS Managed API</span></span>

<span data-ttu-id="142c2-194">您可以使用[ConversationRequest](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.conversationrequest%28v=exchg.80%29.aspx)对象和[ExchangeService.GetConversationItems](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.getconversationitems%28v=exchg.80%29.aspx) EWS 托管 API 方法获取两个或多个对话中的项。</span><span class="sxs-lookup"><span data-stu-id="142c2-194">You can use the [ConversationRequest](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.conversationrequest%28v=exchg.80%29.aspx) object and the [ExchangeService.GetConversationItems](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.getconversationitems%28v=exchg.80%29.aspx) EWS Managed API method to get items from two or more conversations.</span></span> <span data-ttu-id="142c2-195">此示例在收件箱中的前两个对话提供一组对话节点。</span><span class="sxs-lookup"><span data-stu-id="142c2-195">This example provides a set of conversation nodes for the first two conversations in the Inbox.</span></span> <span data-ttu-id="142c2-196">将在响应中，以及对话索引和 parent 对话索引属性返回的项标识符、 主题和接收的时间为每个项目。</span><span class="sxs-lookup"><span data-stu-id="142c2-196">The item identifier, subject, and the received time for each item will be returned in the response, along with the conversation index and parent conversation index properties.</span></span> <span data-ttu-id="142c2-197">您可以使用对话索引属性重新构造节点层次结构。</span><span class="sxs-lookup"><span data-stu-id="142c2-197">You can use the conversation index properties to reconstruct the node hierarchy.</span></span> <span data-ttu-id="142c2-198">本示例假定收件箱中的前两个项目的不同的对话。</span><span class="sxs-lookup"><span data-stu-id="142c2-198">This example assumes that the first two items in the Inbox are from different conversations.</span></span> 
  
<span data-ttu-id="142c2-199">本示例中，默认已删除邮件和草稿文件夹中的所有对话项目将被都忽略。</span><span class="sxs-lookup"><span data-stu-id="142c2-199">In this example, all conversation items in the default Deleted Items and Drafts folders are ignored.</span></span>
  
<span data-ttu-id="142c2-200">此示例假定 **service** 是有效的 [ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，并且已向 Exchange 服务器对该用户进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="142c2-200">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
static void GetConversationItemsManyConversations(ExchangeService service)
{
   try
   {
      // Find the first two items in the Inbox. This item will be used to call the GetConversationItems operation.
      // This method call results in an FindItem call to EWS.
      FindItemsResults<Item> results = service.FindItems(WellKnownFolderName.Inbox, new ItemView(2));
      // Get the conversation identifier of the first two items in the Inbox. 
      ConversationId convId1 = results.Items[0].ConversationId;
      ConversationId convId2 = results.Items[1].ConversationId;
      
      // Identify two conversation requests. 
      ConversationRequest convR1 = new ConversationRequest();
      convR1.ConversationId = convId1;
      ConversationRequest convR2 = new ConversationRequest();
      convR2.ConversationId = convId2;
      // Create a collection of conversations to fetch. 
      Collection<ConversationRequest> conversations = new Collection<ConversationRequest>();
      conversations.Add(convR1);
      conversations.Add(convR2);
      // Specify the properties that will be returned for the items in the conversation.
      PropertySet properties = new PropertySet(BasePropertySet.IdOnly,
                                                ItemSchema.Subject,
                                                ItemSchema.DateTimeReceived);
      // Identify the folders to ignore.
      Collection<FolderId> foldersToIgnore = new Collection<FolderId>() 
          { WellKnownFolderName.DeletedItems, WellKnownFolderName.Drafts };
      // Request the conversation items.
      // This method call results in an GetConversationItems call to EWS.
      ServiceResponseCollection<GetConversationItemsResponse> responses = 
          service.GetConversationItems(conversations, properties, foldersToIgnore, 
          ConversationSortOrder.TreeOrderDescending);
      // Process each conversation.
      foreach (GetConversationItemsResponse resp in responses)
      {
         // Identify the synchronization state of the conversation.
         Console.WriteLine("Sync State: " + resp.Conversation.SyncState);
         // Process each node in the conversation.
         foreach (ConversationNode node in resp.Conversation.ConversationNodes)
         {
            Console.WriteLine("Parent conversation index: " + node.ParentConversationIndex);
            Console.WriteLine("Conversation index: " + node.ConversationIndex);
            Console.WriteLine("Conversation node items:");
            // Process each item in the conversation node.
            foreach (Item item in node.Items)
            {
               Console.WriteLine("   Item ID: " + item.Id.UniqueId);
               Console.WriteLine("   Subject: " + item.Subject);
               Console.WriteLine("   Received: " + item.DateTimeReceived);
            }
         }
      }
   }
   // This exception occurs if there is an error with the service.
   catch (ServiceResponseException srException)
   { 
      Console.WriteLine(srException);
   }
}

```

<span data-ttu-id="142c2-201">作为最佳实践，我们建议您返回仅属性的客户端应用程序要求，而不是使用**FirstClassProperties**选项**BasePropertySet**类。</span><span class="sxs-lookup"><span data-stu-id="142c2-201">As a best practice, we recommend that you return only the properties that the client application requires, rather than using the **FirstClassProperties** option for the **BasePropertySet** class.</span></span> <span data-ttu-id="142c2-202">我们建议您缓存后续请求会话中获取项的**SyncState**属性。</span><span class="sxs-lookup"><span data-stu-id="142c2-202">We recommend that you cache the **SyncState** property for subsequent requests to get items in the conversation.</span></span> 

<span data-ttu-id="142c2-203"><a name="bk_getitemsews"> </a></span><span class="sxs-lookup"><span data-stu-id="142c2-203"></span></span>

## <a name="get-items-in-conversations-by-using-the-conversation-identifier-in-ews"></a><span data-ttu-id="142c2-204">通过使用 EWS 中的对话标识符对话中获取项</span><span class="sxs-lookup"><span data-stu-id="142c2-204">Get items in conversations by using the conversation identifier in EWS</span></span>

<span data-ttu-id="142c2-205">使用[GetConversationItems](http://msdn.microsoft.com/library/8ae00a99-b37b-4194-829c-fe300db6ab99%28Office.15%29.aspx) EWS 操作，可以在对话中获取项。</span><span class="sxs-lookup"><span data-stu-id="142c2-205">You can get items in a conversation by using the [GetConversationItems](http://msdn.microsoft.com/library/8ae00a99-b37b-4194-829c-fe300db6ab99%28Office.15%29.aspx) EWS operation.</span></span> <span data-ttu-id="142c2-206">该示例提供一的组对话节点的收件箱中的第一个对话。</span><span class="sxs-lookup"><span data-stu-id="142c2-206">This example provides a set of conversation nodes for the first conversation in the Inbox.</span></span> <span data-ttu-id="142c2-207">在响应中，以及对话索引和 parent 对话索引属性返回的项标识符、 主题和每个项目的接收的时间。</span><span class="sxs-lookup"><span data-stu-id="142c2-207">The item identifier, subject, and received time for each item are returned in the response, along with the conversation index and parent conversation index properties.</span></span> <span data-ttu-id="142c2-208">您可以使用对话索引属性重新构造节点层次结构。</span><span class="sxs-lookup"><span data-stu-id="142c2-208">You can use the conversation index properties to reconstruct the node hierarchy.</span></span> 
  
<span data-ttu-id="142c2-209">本示例中，默认已删除邮件和草稿文件夹中的所有对话项目将被都忽略。</span><span class="sxs-lookup"><span data-stu-id="142c2-209">In this example, all conversation items in the default Deleted Items and Drafts folders are ignored.</span></span>
  
<span data-ttu-id="142c2-210">为便于阅读缩短了**ConversationId**元素。</span><span class="sxs-lookup"><span data-stu-id="142c2-210">The **ConversationId** element has been shortened for readability.</span></span> 
  
<span data-ttu-id="142c2-211">从多个对话中获取项，包括其他**对话**元素。</span><span class="sxs-lookup"><span data-stu-id="142c2-211">To get items from more than one conversation, include additional **Conversation** elements.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m=http://schemas.microsoft.com/exchange/services/2006/messages
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
          <t:ConversationId Id="LUQFH6Q=" />
        </t:Conversation>
      </m:Conversations>
    </m:GetConversationItems>
  </soap:Body>
</soap:Envelope>
```

服务器响应**GetConversationItems**请求[GetConversationItemsResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx)邮件包含[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)值**NoError**以指示操作成功完成。 <span data-ttu-id="142c2-213">响应还包括[ConversationNodes](http://msdn.microsoft.com/library/5c8a35b8-a940-4b3e-8768-9ba95766fd79%28Office.15%29.aspx)对话中。</span><span class="sxs-lookup"><span data-stu-id="142c2-213">The response also includes the [ConversationNodes](http://msdn.microsoft.com/library/5c8a35b8-a940-4b3e-8768-9ba95766fd79%28Office.15%29.aspx) in the conversation.</span></span> 
  
<span data-ttu-id="142c2-214">为便于阅读变短了**ItemId**、 **SyncState**和**ConversationId**元素。</span><span class="sxs-lookup"><span data-stu-id="142c2-214">The **ItemId**, **SyncState**, and **ConversationId** elements have been shortened for readability.</span></span> 
  
```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="873"
                         MinorBuildNumber="9"
                         Version="V2_9"
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
            <t:ConversationId Id="LUQFH6Q=" />
            <t:SyncState>AAAAYAm1</t:SyncState>
            <t:ConversationNodes>
              <t:ConversationNode>
                <t:InternetMessageId>&amp;lt;994051d7c1a346efbfce8dec2cbad509
                    @SN2SR01MB006.com&amp;gt;</t:InternetMessageId>
                <t:ParentInternetMessageId>&amp;lt;faa2b1df30074380abe3527b0cd18ca5
                    @SN2SR01MB001.com&amp;gt;</t:ParentInternetMessageId>
                <t:Items>
                  <t:Message>
                    <t:ItemId Id="AYB1NAAA="
                              ChangeKey="CQAAABYAAAD/oydcA+SPQZGbKWNyvNIZAAAAYCHq" />
                    <t:Subject>RE: Review Proposal for Tailspin Toys</t:Subject>
                    <t:DateTimeReceived>2014-01-02T13:15:00Z</t:DateTimeReceived>
                  </t:Message>
                </t:Items>
              </t:ConversationNode>
              <t:ConversationNode>
                <t:InternetMessageId>&amp;lt;faa2b1df30074380abe3527b0cd18ca5
                    @SN2SR01MB001.com&amp;gt;</t:InternetMessageId>
                <t:ParentInternetMessageId>&amp;lt;6a8e7658524b41cda7cdc3f23c1074a5
                    @SN2SR01MB001.com&amp;gt;</t:ParentInternetMessageId>
                <t:Items>
                  <t:Message>
                    <t:ItemId Id="lQAAAA=="
                              ChangeKey="CQAAABYAAAD/oydcA+SPQZGbKWNyvNIZAAAAYAu8" />
                    <t:Subject>RE: Review Proposal for Tailspin Toys</t:Subject>
                    <t:DateTimeReceived>2014-01-02T10:02:08Z</t:DateTimeReceived>
                  </t:Message>
                </t:Items>
              </t:ConversationNode>
              <t:ConversationNode>
                <t:InternetMessageId>&amp;lt;bcdb185495834370a874a1e7ebedbb96
                    @SN2SR01MB005.com&amp;gt;</t:InternetMessageId>
                <t:ParentInternetMessageId>&amp;lt;e52a4de6b98d484887e141da094a2ce6
                    @SN2SR01MB006.com&amp;gt;</t:ParentInternetMessageId>
                <t:Items>
                  <t:Message>
                    <t:ItemId Id="igAAAA=="
                              ChangeKey="CQAAABYAAAD/oydcA+SPQZGbKWNyvNIZAAAAYAuj" />
                    <t:Subject>RE: Review Proposal for Tailspin Toys</t:Subject>
                    <t:DateTimeReceived>2014-01-02T16:20:10Z</t:DateTimeReceived>
                  </t:Message>
                </t:Items>
              </t:ConversationNode>
              <t:ConversationNode>
                <t:InternetMessageId>&amp;lt;e52a4de6b98d484887e141da094a2ce6
                    @SN2SR01MB006.com&amp;gt;</t:InternetMessageId>
                <t:ParentInternetMessageId>&amp;lt;f0db3ead01db4fe087d98022149aa16f
                    @SN2SR01MB001.com&amp;gt;</t:ParentInternetMessageId>
                <t:Items>
                  <t:Message>
                    <t:ItemId Id="iwAAAA=="
                              ChangeKey="CQAAABYAAAD/oydcA+SPQZGbKWNyvNIZAAAAYAul" />
                    <t:Subject>RE: Review Proposal for Tailspin Toys</t:Subject>
                    <t:DateTimeReceived>2014-01-02T15:30:10Z</t:DateTimeReceived>
                  </t:Message>
                </t:Items>
              </t:ConversationNode>
              <t:ConversationNode>
                <t:InternetMessageId>&amp;lt;f0db3ead01db4fe087d98022149aa16f
                    @SN2SR01MB001.com&amp;gt;</t:InternetMessageId>
                <t:ParentInternetMessageId>&amp;lt;88b1884ecaaa4f68b081c009d827e8c6
                    @SN2SR01MB003.com&amp;gt;</t:ParentInternetMessageId>
                <t:Items>
                  <t:Message>
                    <t:ItemId Id="jQAAAA=="
                              ChangeKey="CQAAABYAAAD/oydcA+SPQZGbKWNyvNIZAAAAYAuq" />
                    <t:Subject>RE: Review Proposal for Tailspin Toys</t:Subject>
                    <t:DateTimeReceived>2014-01-02T14:20:10Z</t:DateTimeReceived>
                  </t:Message>
                </t:Items>
              </t:ConversationNode>
              <t:ConversationNode>
                <t:InternetMessageId>&amp;lt;88b1884ecaaa4f68b081c009d827e8c6
                    @SN2SR01MB003.com&amp;gt;</t:InternetMessageId>
                <t:ParentInternetMessageId>&amp;lt;faa2b1df30074380abe3527b0cd18ca5
                    @SN2SR01MB001.com&amp;gt;</t:ParentInternetMessageId>
                <t:Items>
                  <t:Message>
                    <t:ItemId Id="kAAAAA=="
                              ChangeKey="CQAAABYAAAD/oydcA+SPQZGbKWNyvNIZAAAAYAux" />
                    <t:Subject>RE: Review Proposal for Tailspin Toys</t:Subject>
                    <t:DateTimeReceived>2014-01-02T12:52:09Z</t:DateTimeReceived>
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

<span data-ttu-id="142c2-215"><a name="bk_versiondiffs"> </a></span><span class="sxs-lookup"><span data-stu-id="142c2-215"></span></span>

## <a name="version-differences"></a><span data-ttu-id="142c2-216">版本差异</span><span class="sxs-lookup"><span data-stu-id="142c2-216">Version differences</span></span>

<span data-ttu-id="142c2-217">当您使用 Exchange Server 2010 Service Pack 1 (SP1) 时， [FindConversation](http://msdn.microsoft.com/zh-cn/library/office/jj220668%28v=exchg.80%29.aspx)方法具有较少的可用选项和[FindConversation](http://msdn.microsoft.com/library/2384908a-c203-45b6-98aa-efd6a4c23aac%28Office.15%29.aspx)操作中请求具有较少的元素。</span><span class="sxs-lookup"><span data-stu-id="142c2-217">When you are using Exchange Server 2010 Service Pack 1 (SP1), the [FindConversation](http://msdn.microsoft.com/zh-cn/library/office/jj220668%28v=exchg.80%29.aspx) method has fewer options available, and the [FindConversation](http://msdn.microsoft.com/library/2384908a-c203-45b6-98aa-efd6a4c23aac%28Office.15%29.aspx) operation has fewer elements in the request.</span></span> 
  
<span data-ttu-id="142c2-218">**表 3。Exchange 2010 SP1 版本支持 FindConversation**</span><span class="sxs-lookup"><span data-stu-id="142c2-218">**Table 3. Exchange 2010 SP1 version support for FindConversation**</span></span>

|<span data-ttu-id="142c2-219">**EWS 托管的 API 方法**</span><span class="sxs-lookup"><span data-stu-id="142c2-219">**EWS Managed API method**</span></span>|<span data-ttu-id="142c2-220">**EWS 元素**</span><span class="sxs-lookup"><span data-stu-id="142c2-220">**EWS elements**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="142c2-221">FindConversation （ViewBase，文件夹 Id）</span><span class="sxs-lookup"><span data-stu-id="142c2-221">FindConversation (ViewBase, FolderId)</span></span>](http://msdn.microsoft.com/zh-cn/library/office/jj220668%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="142c2-222">IndexedPageItemView</span><span class="sxs-lookup"><span data-stu-id="142c2-222">IndexedPageItemView</span></span>](http://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) <br/> [<span data-ttu-id="142c2-223">SortOrder</span><span class="sxs-lookup"><span data-stu-id="142c2-223">SortOrder</span></span>](http://msdn.microsoft.com/library/c2413f0b-8c03-46ae-9990-13338b3c53a6%28Office.15%29.aspx) <br/> [<span data-ttu-id="142c2-224">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="142c2-224">ParentFolderId</span></span>](http://msdn.microsoft.com/library/0e3e6e5f-06d0-499b-8ca4-d36036521658%28Office.15%29.aspx) <br/> |
   
<span data-ttu-id="142c2-225">[GetConversationItems](http://msdn.microsoft.com/zh-cn/library/office/microsoft.exchange.webservices.data.exchangeservice.getconversationitems%28v=exchg.80%29.aspx) EWS 托管 API 方法和[GetConversationItems](http://msdn.microsoft.com/library/8ae00a99-b37b-4194-829c-fe300db6ab99%28Office.15%29.aspx) EWS 操作是在 Exchange Server 2013 中引入的。</span><span class="sxs-lookup"><span data-stu-id="142c2-225">The [GetConversationItems](http://msdn.microsoft.com/zh-cn/library/office/microsoft.exchange.webservices.data.exchangeservice.getconversationitems%28v=exchg.80%29.aspx) EWS Managed API method and the [GetConversationItems](http://msdn.microsoft.com/library/8ae00a99-b37b-4194-829c-fe300db6ab99%28Office.15%29.aspx) EWS operation were introduced in Exchange Server 2013.</span></span> <span data-ttu-id="142c2-226">表 2 中所列，针对早期版本 Exchange 的应用程序仅可加入对话，应用对话操作。</span><span class="sxs-lookup"><span data-stu-id="142c2-226">Applications that target earlier versions of Exchange can only apply conversation actions to conversations, as listed in Table 2.</span></span> 
  
<span data-ttu-id="142c2-227">**FindConversation** EWS 托管 API 方法和**FindConversation** EWS 方法不在 Exchange 2007 或 Exchange 2010 的初始发行版中可用。</span><span class="sxs-lookup"><span data-stu-id="142c2-227">The **FindConversation** EWS Managed API method and the **FindConversation** EWS method are not available in the initial release version of Exchange 2010 or in Exchange 2007.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="142c2-228">另请参阅</span><span class="sxs-lookup"><span data-stu-id="142c2-228">See also</span></span>

- [<span data-ttu-id="142c2-229">电子邮件和 Exchange 中的 EWS</span><span class="sxs-lookup"><span data-stu-id="142c2-229">Email and EWS in Exchange</span></span>](email-and-ews-in-exchange.md)
- [<span data-ttu-id="142c2-230">在 Exchange 中使用 EWS 使用搜索筛选器</span><span class="sxs-lookup"><span data-stu-id="142c2-230">Use search filters with EWS in Exchange</span></span>](how-to-use-search-filters-with-ews-in-exchange.md)   
- [<span data-ttu-id="142c2-231">Exchange 2013： 查找对话在邮箱中以编程方式</span><span class="sxs-lookup"><span data-stu-id="142c2-231">Exchange 2013: Find conversations in mailboxes programmatically</span></span>](http://code.msdn.microsoft.com/exchange/Exchange-2013-Find-d4b6b3af)    
- [<span data-ttu-id="142c2-232">Exchange 2013： 应用操作来管理邮箱中的对话</span><span class="sxs-lookup"><span data-stu-id="142c2-232">Exchange 2013: Apply actions to manage conversations in a mailbox</span></span>](http://code.msdn.microsoft.com/exchange/Exchange-2013-Apply-accde0b5)
    

