---
title: FindConversation 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindConversation
api_type:
- schema
ms.assetid: 2384908a-c203-45b6-98aa-efd6a4c23aac
description: FindConversation 操作枚举文件夹中的对话列表。
ms.openlocfilehash: ef768807431ff3e02c6af7277c1c2a750607ed92
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462652"
---
# <a name="findconversation-operation"></a><span data-ttu-id="0929c-103">FindConversation 操作</span><span class="sxs-lookup"><span data-stu-id="0929c-103">FindConversation operation</span></span>

<span data-ttu-id="0929c-104">**FindConversation**操作枚举文件夹中的对话列表。</span><span class="sxs-lookup"><span data-stu-id="0929c-104">The **FindConversation** operation enumerates a list of conversations in a folder.</span></span> 
  
## <a name="findconversation-request-example"></a><span data-ttu-id="0929c-105">FindConversation 请求示例</span><span class="sxs-lookup"><span data-stu-id="0929c-105">FindConversation request example</span></span>

### <a name="description"></a><span data-ttu-id="0929c-106">说明</span><span class="sxs-lookup"><span data-stu-id="0929c-106">Description</span></span>

<span data-ttu-id="0929c-107">以下示例的**FindConversation**请求显示如何在 "收件箱" 文件夹中形成查找第一个对话的请求。</span><span class="sxs-lookup"><span data-stu-id="0929c-107">The following example of a **FindConversation** request shows how to form a request to find the first conversation in the Inbox folder.</span></span> 
  
### <a name="code"></a><span data-ttu-id="0929c-108">代码</span><span class="sxs-lookup"><span data-stu-id="0929c-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010_SP1" />
  </soap:Header>
  <soap:Body>
    <m:FindConversation>
      <m:IndexedPageItemView BasePoint="Beginning" MaxEntriesReturned="1" Offset="0"/>
      <m:ParentFolderId>
        <t:DistinguishedFolderId Id ="inbox"/>
      </m:ParentFolderId>
    </m:FindConversation>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="0929c-109">Request 元素</span><span class="sxs-lookup"><span data-stu-id="0929c-109">Request elements</span></span>

<span data-ttu-id="0929c-110">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="0929c-110">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="0929c-111">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="0929c-111">RequestServerVersion</span></span>](requestserverversion.md)
    
- [<span data-ttu-id="0929c-112">FindConversation</span><span class="sxs-lookup"><span data-stu-id="0929c-112">FindConversation</span></span>](findconversation.md)
    
- [<span data-ttu-id="0929c-113">IndexedPageItemView</span><span class="sxs-lookup"><span data-stu-id="0929c-113">IndexedPageItemView</span></span>](indexedpageitemview.md)
    
- [<span data-ttu-id="0929c-114">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="0929c-114">ParentFolderId</span></span>](parentfolderid.md)
    
- [<span data-ttu-id="0929c-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="0929c-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
## <a name="successful-findconversation-response-example"></a><span data-ttu-id="0929c-116">成功的 FindConversation 响应示例</span><span class="sxs-lookup"><span data-stu-id="0929c-116">Successful FindConversation response example</span></span>

### <a name="description"></a><span data-ttu-id="0929c-117">说明</span><span class="sxs-lookup"><span data-stu-id="0929c-117">Description</span></span>

<span data-ttu-id="0929c-118">下面的示例演示对**FindConversation**请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="0929c-118">The following example shows a successful response to a **FindConversation** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="0929c-119">代码</span><span class="sxs-lookup"><span data-stu-id="0929c-119">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="1" 
                         MajorBuildNumber="91" 
                         MinorBuildNumber="0" 
                         Version="Exchange2010_SP1" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <FindConversationResponse ResponseClass="Success" 
                              xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <Conversations>
        <t:Conversation xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
          <t:ConversationId Id="AAQkADRlZDhjZDVlLzYtNDcyZi1i32hHpdc="/>
          <t:ConversationTopic>Have you heard about EWS?</t:ConversationTopic>
          <t:UniqueRecipients>
            <t:String>User1First User1Last</t:String>
          </t:UniqueRecipients>
          <t:GlobalUniqueRecipients>
            <t:String>User2First User2Last</t:String>
            <t:String>User1First User1Last</t:String>
          </t:GlobalUniqueRecipients>
          <t:UniqueSenders>
            <t:String>User2First User2Last</t:String>
          </t:UniqueSenders>
          <t:GlobalUniqueSenders>
            <t:String>User1First User1Last</t:String>
            <t:String>User2First User2Last</t:String>
          </t:GlobalUniqueSenders>
          <t:LastDeliveryTime>2010-02-09T02:20:49Z</t:LastDeliveryTime>
          <t:GlobalLastDeliveryTime>2010-02-09T02:21:01Z</t:GlobalLastDeliveryTime>
          <t:HasAttachments>false</t:HasAttachments>
          <t:GlobalHasAttachments>false</t:GlobalHasAttachments>
          <t:MessageCount>2</t:MessageCount>
          <t:GlobalMessageCount>5</t:GlobalMessageCount>
          <t:UnreadCount>0</t:UnreadCount>
          <t:Size>6474</t:Size>
          <t:GlobalSize>14497</t:GlobalSize>
          <t:ItemClasses>
            <t:ItemClass>IPM.Note</t:ItemClass>
          </t:ItemClasses>
          <t:GlobalItemClasses>
            <t:ItemClass>IPM.Note</t:ItemClass>
          </t:GlobalItemClasses>
          <t:Importance>Normal</t:Importance>
          <t:GlobalImportance>Normal</t:GlobalImportance>
          <t:ItemIds>
            <t:ItemId Id="AAMkADRlZDhjZDVlLTU3qaTQvcFtnmUZQY2FuFP93qPtAAAADXWyAAA=" ChangeKey="CQAAAA=="/>
            <t:ItemId Id="AAMkADRlZDhjZDVFtnmUZQY2vcFtnmUZQY2FuFP93qPtAAAADXWxAAA=" ChangeKey="CQAAAA=="/>
          </t:ItemIds>
          <t:GlobalItemIds>
            <t:ItemId Id="AAMkADRlZDhCQvcFtnmADU5PAACQvcFtnmUZQsdfFPPtAAAADad4AAA=" ChangeKey="CQAAAA=="/>
            <t:ItemId Id="AAqaTXQvcFtnmUZQAADU5NAACQvcFmUZQY2FuFP93qPtAAAADXWyAAA=" ChangeKey="CQAAAA=="/>
            <t:ItemId Id="AAMkFtnmUZQY2FuFP93qPtAAAADU5vcFtY2FuFP93qPtAAAADad3AAA=" ChangeKey="CQAAAA=="/>
            <t:ItemId Id="AAMkLTU3YzQvcFtnmUZQY2FuFP93qPtnmU2FuFP93qPtAAAADXWxAAA=" ChangeKey="CQAAAA=="/>
            <t:ItemId Id="AAMkADlLTU3YzYtNDAAAAAB1aGnYmUZQY2FPAmUZQY2FuqPtAAd2AAA=" ChangeKey="CQAAAA=="/>
          </t:GlobalItemIds>
        </t:Conversation>
      </Conversations>
    </FindConversationResponse>
  </s:Body>
</s:Envelope>
```

### <a name="comment"></a><span data-ttu-id="0929c-120">评论</span><span class="sxs-lookup"><span data-stu-id="0929c-120">Comment</span></span>

<span data-ttu-id="0929c-121">示例中的项和对话标识符已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="0929c-121">The item and conversation identifiers in the example have been shortened to preserve readability.</span></span>
  
### <a name="successful-response-elements"></a><span data-ttu-id="0929c-122">成功的响应元素</span><span class="sxs-lookup"><span data-stu-id="0929c-122">Successful response elements</span></span>

<span data-ttu-id="0929c-123">响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="0929c-123">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="0929c-124">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="0929c-124">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="0929c-125">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="0929c-125">FindConversationResponse</span></span>](findconversationresponse.md)
    
- [<span data-ttu-id="0929c-126">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0929c-126">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="0929c-127">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="0929c-127">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
    
- [<span data-ttu-id="0929c-128">ConversationId</span><span class="sxs-lookup"><span data-stu-id="0929c-128">ConversationId</span></span>](conversationid.md)
    
- [<span data-ttu-id="0929c-129">ConversationTopic</span><span class="sxs-lookup"><span data-stu-id="0929c-129">ConversationTopic</span></span>](conversationtopic.md)
    
- [<span data-ttu-id="0929c-130">UniqueRecipients</span><span class="sxs-lookup"><span data-stu-id="0929c-130">UniqueRecipients</span></span>](uniquerecipients.md)
    
- [<span data-ttu-id="0929c-131">String</span><span class="sxs-lookup"><span data-stu-id="0929c-131">String</span></span>](string.md)
    
- [<span data-ttu-id="0929c-132">GlobalUniqueRecipients</span><span class="sxs-lookup"><span data-stu-id="0929c-132">GlobalUniqueRecipients</span></span>](globaluniquerecipients.md)
    
- [<span data-ttu-id="0929c-133">UniqueSenders</span><span class="sxs-lookup"><span data-stu-id="0929c-133">UniqueSenders</span></span>](uniquesenders.md)
    
- [<span data-ttu-id="0929c-134">GlobalUniqueSenders</span><span class="sxs-lookup"><span data-stu-id="0929c-134">GlobalUniqueSenders</span></span>](globaluniquesenders.md)
    
- [<span data-ttu-id="0929c-135">LastDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="0929c-135">LastDeliveryTime</span></span>](lastdeliverytime.md)
    
- [<span data-ttu-id="0929c-136">GlobalLastDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="0929c-136">GlobalLastDeliveryTime</span></span>](globallastdeliverytime.md)
    
- [<span data-ttu-id="0929c-137">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="0929c-137">HasAttachments</span></span>](hasattachments.md)
    
- [<span data-ttu-id="0929c-138">GlobalHasAttachments</span><span class="sxs-lookup"><span data-stu-id="0929c-138">GlobalHasAttachments</span></span>](globalhasattachments.md)
    
- [<span data-ttu-id="0929c-139">MessageCount</span><span class="sxs-lookup"><span data-stu-id="0929c-139">MessageCount</span></span>](messagecount.md)
    
- [<span data-ttu-id="0929c-140">GlobalMessageCount</span><span class="sxs-lookup"><span data-stu-id="0929c-140">GlobalMessageCount</span></span>](globalmessagecount.md)
    
- [<span data-ttu-id="0929c-141">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="0929c-141">UnreadCount</span></span>](unreadcount.md)
    
- [<span data-ttu-id="0929c-142">大小</span><span class="sxs-lookup"><span data-stu-id="0929c-142">Size</span></span>](size.md)
    
- [<span data-ttu-id="0929c-143">GlobalSize</span><span class="sxs-lookup"><span data-stu-id="0929c-143">GlobalSize</span></span>](globalsize.md)
    
- [<span data-ttu-id="0929c-144">ItemClasses (ArrayOfItemClassType)</span><span class="sxs-lookup"><span data-stu-id="0929c-144">ItemClasses (ArrayOfItemClassType)</span></span>](itemclasses-arrayofitemclasstype.md)
    
- [<span data-ttu-id="0929c-145">ItemClass</span><span class="sxs-lookup"><span data-stu-id="0929c-145">ItemClass</span></span>](itemclass.md)
    
- [<span data-ttu-id="0929c-146">GlobalItemClasses</span><span class="sxs-lookup"><span data-stu-id="0929c-146">GlobalItemClasses</span></span>](globalitemclasses.md)
    
- [<span data-ttu-id="0929c-147">Importance</span><span class="sxs-lookup"><span data-stu-id="0929c-147">Importance</span></span>](importance.md)
    
- [<span data-ttu-id="0929c-148">GlobalImportance</span><span class="sxs-lookup"><span data-stu-id="0929c-148">GlobalImportance</span></span>](globalimportance.md)
    
- [<span data-ttu-id="0929c-149">ItemIds</span><span class="sxs-lookup"><span data-stu-id="0929c-149">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="0929c-150">ItemId</span><span class="sxs-lookup"><span data-stu-id="0929c-150">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="0929c-151">GlobalItemIds</span><span class="sxs-lookup"><span data-stu-id="0929c-151">GlobalItemIds</span></span>](globalitemids.md)
    
## <a name="findconversation-error-response-example"></a><span data-ttu-id="0929c-152">FindConversation 错误响应示例</span><span class="sxs-lookup"><span data-stu-id="0929c-152">FindConversation Error response example</span></span>

### <a name="description"></a><span data-ttu-id="0929c-153">说明</span><span class="sxs-lookup"><span data-stu-id="0929c-153">Description</span></span>

<span data-ttu-id="0929c-154">下面的示例演示对由架构验证错误导致的**FindConversation**请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="0929c-154">The following example shows an error response to the **FindConversation** request that was caused by a schema validation error.</span></span> 
  
### <a name="code"></a><span data-ttu-id="0929c-155">代码</span><span class="sxs-lookup"><span data-stu-id="0929c-155">Code</span></span>

```
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Body>
    <s:Fault>
      <faultcode xmlns:a="https://schemas.microsoft.com/exchange/services/2006/types">a:ErrorSchemaValidation</faultcode>
      <faultstring xml:lang="en-US">The request failed schema validation: The 'Id' attribute is invalid - The value 'inbox1' is invalid according to its datatype 'https://schemas.microsoft.com/exchange/services/2006/types:DistinguishedFolderIdNameType' - The Enumeration constraint failed.</faultstring>
      <detail>
        <e:ResponseCode xmlns:e="https://schemas.microsoft.com/exchange/services/2006/errors">ErrorSchemaValidation</e:ResponseCode>
        <e:Message xmlns:e="https://schemas.microsoft.com/exchange/services/2006/errors">The request failed schema validation.</e:Message>
        <t:MessageXml xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
          <t:LineNumber>14</t:LineNumber>
          <t:LinePosition>34</t:LinePosition>
          <t:Violation>The 'Id' attribute is invalid - The value 'inbox1' is invalid according to its datatype 'https://schemas.microsoft.com/exchange/services/2006/types:DistinguishedFolderIdNameType' - The Enumeration constraint failed.</t:Violation>
        </t:MessageXml>
      </detail>
    </s:Fault>
  </s:Body>
</s:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="0929c-156">错误响应元素</span><span class="sxs-lookup"><span data-stu-id="0929c-156">Error response elements</span></span>

<span data-ttu-id="0929c-157">错误响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="0929c-157">The following elements are used in the error response:</span></span>
  
- <span data-ttu-id="0929c-158">faultcode</span><span class="sxs-lookup"><span data-stu-id="0929c-158">faultcode</span></span>
    
- <span data-ttu-id="0929c-159">faultstring</span><span class="sxs-lookup"><span data-stu-id="0929c-159">faultstring</span></span>
    
- <span data-ttu-id="0929c-160">介绍</span><span class="sxs-lookup"><span data-stu-id="0929c-160">detail</span></span>
    
- [<span data-ttu-id="0929c-161">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0929c-161">ResponseCode</span></span>](responsecode.md)
    
- <span data-ttu-id="0929c-162">消息</span><span class="sxs-lookup"><span data-stu-id="0929c-162">Message</span></span>
    
- [<span data-ttu-id="0929c-163">MessageXml</span><span class="sxs-lookup"><span data-stu-id="0929c-163">MessageXml</span></span>](messagexml.md)
    
- <span data-ttu-id="0929c-164">LineNumber</span><span class="sxs-lookup"><span data-stu-id="0929c-164">LineNumber</span></span>
    
- <span data-ttu-id="0929c-165">LinePosition</span><span class="sxs-lookup"><span data-stu-id="0929c-165">LinePosition</span></span>
    
- <span data-ttu-id="0929c-166">非法</span><span class="sxs-lookup"><span data-stu-id="0929c-166">Violation</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0929c-167">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0929c-167">See also</span></span>



[<span data-ttu-id="0929c-168">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="0929c-168">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="0929c-169">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="0929c-169">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
  
- [<span data-ttu-id="0929c-170">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="0929c-170">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="0929c-171">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="0929c-171">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

