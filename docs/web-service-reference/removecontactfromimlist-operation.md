---
title: RemoveContactFromImList 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 28ec96c3-45af-48ff-9f17-718a527dc0ad
description: 查找信息 RemoveContactFromImList EWS 操作。
ms.openlocfilehash: 036b295a84e86ad74c467572cc52fdf6bbae5191
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827080"
---
# <a name="removecontactfromimlist-operation"></a><span data-ttu-id="6a1df-103">RemoveContactFromImList 操作</span><span class="sxs-lookup"><span data-stu-id="6a1df-103">RemoveContactFromImList operation</span></span>

<span data-ttu-id="6a1df-104">查找有关**RemoveContactFromImList** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="6a1df-104">Find information about the **RemoveContactFromImList** EWS operation.</span></span> 
  
<span data-ttu-id="6a1df-105">当 Lync 的联系人存储库中使用 Exchange **RemoveContactFromImList**操作从 Lync 即时消息 (IM) 列表中删除联系人。</span><span class="sxs-lookup"><span data-stu-id="6a1df-105">The **RemoveContactFromImList** operation removes contacts from the Lync instant messaging (IM) list when Lync uses Exchange for the contact store.</span></span> 
  
<span data-ttu-id="6a1df-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="6a1df-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-removecontactfromimlist-operation"></a><span data-ttu-id="6a1df-107">使用 RemoveContactFromImList 操作</span><span class="sxs-lookup"><span data-stu-id="6a1df-107">Using the RemoveContactFromImList operation</span></span>

<span data-ttu-id="6a1df-108">**RemoveContactFromImList**操作接受单个参数标识要从 Exchange 服务器上存储的 Lync 联系人列表中删除的联系人。</span><span class="sxs-lookup"><span data-stu-id="6a1df-108">The **RemoveContactFromImList** operation accepts a single argument that identifies a contact to remove from the Lync contact list stored on an Exchange server.</span></span> <span data-ttu-id="6a1df-109">此操作目标调用 Outlook 2013 中**的 Lync 联系人**的联系人的列表。</span><span class="sxs-lookup"><span data-stu-id="6a1df-109">The list of contacts that this operation targets is called **Lync Contacts** in Outlook 2013.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="6a1df-110">不要使用[删除项操作](deleteitem-operation.md)来从联系人列表中删除联系人。</span><span class="sxs-lookup"><span data-stu-id="6a1df-110">Do not use the [DeleteItem operation](deleteitem-operation.md) to remove contacts from a contact list.</span></span> <span data-ttu-id="6a1df-111">其他服务器端处理，可能必须发生以支持**Lync 联系人**列表中删除联系人。</span><span class="sxs-lookup"><span data-stu-id="6a1df-111">Additional server-side processing might have to occur to support removing a contact from the **Lync Contacts** list.</span></span> <span data-ttu-id="6a1df-112">请注意， **Lync 联系人**列表的默认的**Lync 联系人**邮箱文件夹的概念等效。</span><span class="sxs-lookup"><span data-stu-id="6a1df-112">Note that the **Lync Contacts** list is the conceptual equivalent of the default **Lync Contacts** mailbox folder.</span></span> 
  
### <a name="removecontactfromimlist-operation-soap-headers"></a><span data-ttu-id="6a1df-113">RemoveContactFromImList 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="6a1df-113">RemoveContactFromImList operation SOAP headers</span></span>

<span data-ttu-id="6a1df-114">**RemoveContactFromImList**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="6a1df-114">The **RemoveContactFromImList** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="6a1df-115">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="6a1df-115">**Header name**</span></span>|<span data-ttu-id="6a1df-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="6a1df-116">**Element**</span></span>|<span data-ttu-id="6a1df-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="6a1df-117">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6a1df-118">**模拟**</span><span class="sxs-lookup"><span data-stu-id="6a1df-118">**Impersonation**</span></span> <br/> |[<span data-ttu-id="6a1df-119">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="6a1df-119">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="6a1df-120">标识模拟客户端应用程序的用户。</span><span class="sxs-lookup"><span data-stu-id="6a1df-120">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="6a1df-121">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="6a1df-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="6a1df-122">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="6a1df-122">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="6a1df-123">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="6a1df-123">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="6a1df-124">定义 RFC 3066 中，"标记的标识的语言"，以用于访问邮箱标识与的区域性。</span><span class="sxs-lookup"><span data-stu-id="6a1df-124">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="6a1df-125">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="6a1df-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="6a1df-126">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="6a1df-126">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="6a1df-127">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="6a1df-127">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="6a1df-128">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="6a1df-128">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="6a1df-129">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="6a1df-129">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="6a1df-130">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="6a1df-130">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="6a1df-131">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="6a1df-131">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="6a1df-132">标识响应该请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="6a1df-132">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="6a1df-133">适用于响应此标头。</span><span class="sxs-lookup"><span data-stu-id="6a1df-133">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="removecontactfromimlist-operation-request-example-remove-a-contact-from-the-lync-contacts-list"></a><span data-ttu-id="6a1df-134">RemoveContactFromImList 操作请求示例： 从 Lync 联系人列表中删除联系人</span><span class="sxs-lookup"><span data-stu-id="6a1df-134">RemoveContactFromImList operation request example: Remove a contact from the Lync Contacts list</span></span>

<span data-ttu-id="6a1df-135">**RemoveContactFromImList**操作请求的下面的示例演示如何从**Lync 联系人**列表中删除联系人。</span><span class="sxs-lookup"><span data-stu-id="6a1df-135">The following example of a **RemoveContactFromImList** operation request shows how to remove a contact from the **Lync Contacts** list.</span></span> <span data-ttu-id="6a1df-136">**RemoveContactFromImList**操作接受单个唯一联系人标识符，以确定从**Lync 联系人**列表中删除该联系人。</span><span class="sxs-lookup"><span data-stu-id="6a1df-136">The **RemoveContactFromImList** operation accepts a single unique contact identifier to identify the contact that is removed from the **Lync Contacts** list.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6a1df-137">所有项目标识符，本文中的更改项具有已截短要保留可读性。</span><span class="sxs-lookup"><span data-stu-id="6a1df-137">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> 
  
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
      <m:RemoveContactFromImList>
         <m:ContactId Id=""/>
      </m:RemoveContactFromImList>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="6a1df-138">请求 SOAP 正文中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="6a1df-138">The following elements are used in the request SOAP body:</span></span>
  
- [<span data-ttu-id="6a1df-139">RemoveContactFromImList</span><span class="sxs-lookup"><span data-stu-id="6a1df-139">RemoveContactFromImList</span></span>](removecontactfromimlist.md)
    
- [<span data-ttu-id="6a1df-140">ContactId</span><span class="sxs-lookup"><span data-stu-id="6a1df-140">ContactId</span></span>](contactid.md)
    
## <a name="successful-removecontactfromimlist-operation-response"></a><span data-ttu-id="6a1df-141">成功 RemoveContactFromImList 操作响应</span><span class="sxs-lookup"><span data-stu-id="6a1df-141">Successful RemoveContactFromImList operation response</span></span>

<span data-ttu-id="6a1df-142">下面的示例演示对**RemoveContactFromImList**操作请求以从**Lync 联系人**列表中删除联系人成功响应。</span><span class="sxs-lookup"><span data-stu-id="6a1df-142">The following example shows a successful response to a **RemoveContactFromImList** operation request to remove a contact from the **Lync Contacts** list.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="8" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <RemoveContactFromImListResponse ResponseClass="Success" 
                                       xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </RemoveContactFromImListResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="6a1df-143">SOAP 正文的响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="6a1df-143">The following elements are used in the response SOAP body:</span></span>
  
- [<span data-ttu-id="6a1df-144">RemoveContactFromImListResponse</span><span class="sxs-lookup"><span data-stu-id="6a1df-144">RemoveContactFromImListResponse</span></span>](removecontactfromimlistresponse.md)
    
- [<span data-ttu-id="6a1df-145">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="6a1df-145">ResponseCode</span></span>](responsecode.md)
    
## <a name="removecontactfromimlist-operation-error-response"></a><span data-ttu-id="6a1df-146">RemoveContactFromImList 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="6a1df-146">RemoveContactFromImList operation error response</span></span>

<span data-ttu-id="6a1df-147">下面的示例演示对**RemoveContactFromImList**操作请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="6a1df-147">The following example shows an error response to a **RemoveContactFromImList** operation request.</span></span> <span data-ttu-id="6a1df-148">这是要从**Lync 联系人**列表中删除某个联系人，联系人不再存在于列表时请求的响应。</span><span class="sxs-lookup"><span data-stu-id="6a1df-148">This is a response to a request to remove a contact from the **Lync Contacts** list when the contact no longer exists in the list.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="8" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <RemoveContactFromImListResponse ResponseClass="Error" 
                                       xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified object was not found in the store.</MessageText>
         <ResponseCode>ErrorItemNotFound</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </RemoveContactFromImListResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="6a1df-149">错误响应 SOAP 正文中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="6a1df-149">The following elements are used in the error response SOAP body:</span></span>
  
- [<span data-ttu-id="6a1df-150">RemoveContactFromImListResponse</span><span class="sxs-lookup"><span data-stu-id="6a1df-150">RemoveContactFromImListResponse</span></span>](removecontactfromimlistresponse.md)
    
- [<span data-ttu-id="6a1df-151">MessageText</span><span class="sxs-lookup"><span data-stu-id="6a1df-151">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="6a1df-152">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="6a1df-152">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="6a1df-153">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="6a1df-153">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="6a1df-154">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6a1df-154">See also</span></span>

- [<span data-ttu-id="6a1df-155">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="6a1df-155">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="6a1df-156">GetImItemList 操作</span><span class="sxs-lookup"><span data-stu-id="6a1df-156">GetImItemList operation</span></span>](getimitemlist-operation.md)
    

