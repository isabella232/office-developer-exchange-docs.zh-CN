---
title: RemoveContactFromImList 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 28ec96c3-45af-48ff-9f17-718a527dc0ad
description: 查找有关 RemoveContactFromImList EWS 操作的信息。
ms.openlocfilehash: 8b3d83a0b53bad169d9f3478540e5087901f3a12
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458465"
---
# <a name="removecontactfromimlist-operation"></a><span data-ttu-id="04f5c-103">RemoveContactFromImList 操作</span><span class="sxs-lookup"><span data-stu-id="04f5c-103">RemoveContactFromImList operation</span></span>

<span data-ttu-id="04f5c-104">查找有关**RemoveContactFromImList** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="04f5c-104">Find information about the **RemoveContactFromImList** EWS operation.</span></span> 
  
<span data-ttu-id="04f5c-105">当 Lync 使用联系人存储库的 Exchange 时， **RemoveContactFromImList**操作将从 lync 即时消息（IM）列表中删除联系人。</span><span class="sxs-lookup"><span data-stu-id="04f5c-105">The **RemoveContactFromImList** operation removes contacts from the Lync instant messaging (IM) list when Lync uses Exchange for the contact store.</span></span> 
  
<span data-ttu-id="04f5c-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="04f5c-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-removecontactfromimlist-operation"></a><span data-ttu-id="04f5c-107">使用 RemoveContactFromImList 操作</span><span class="sxs-lookup"><span data-stu-id="04f5c-107">Using the RemoveContactFromImList operation</span></span>

<span data-ttu-id="04f5c-108">**RemoveContactFromImList**操作接受单个参数，该参数标识要从存储在 Exchange 服务器上的 Lync 联系人列表中删除的联系人。</span><span class="sxs-lookup"><span data-stu-id="04f5c-108">The **RemoveContactFromImList** operation accepts a single argument that identifies a contact to remove from the Lync contact list stored on an Exchange server.</span></span> <span data-ttu-id="04f5c-109">此操作所指向的联系人列表在 Outlook 2013 中称为**Lync 联系人**。</span><span class="sxs-lookup"><span data-stu-id="04f5c-109">The list of contacts that this operation targets is called **Lync Contacts** in Outlook 2013.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="04f5c-110">请勿使用[DeleteItem 操作](deleteitem-operation.md)从联系人列表中删除联系人。</span><span class="sxs-lookup"><span data-stu-id="04f5c-110">Do not use the [DeleteItem operation](deleteitem-operation.md) to remove contacts from a contact list.</span></span> <span data-ttu-id="04f5c-111">若要支持从**Lync 联系人**列表中删除联系人，可能需要进行其他服务器端处理。</span><span class="sxs-lookup"><span data-stu-id="04f5c-111">Additional server-side processing might have to occur to support removing a contact from the **Lync Contacts** list.</span></span> <span data-ttu-id="04f5c-112">请注意， **Lync 联系人**列表是默认**Lync 联系人**邮箱文件夹的概念性等效项。</span><span class="sxs-lookup"><span data-stu-id="04f5c-112">Note that the **Lync Contacts** list is the conceptual equivalent of the default **Lync Contacts** mailbox folder.</span></span> 
  
### <a name="removecontactfromimlist-operation-soap-headers"></a><span data-ttu-id="04f5c-113">RemoveContactFromImList 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="04f5c-113">RemoveContactFromImList operation SOAP headers</span></span>

<span data-ttu-id="04f5c-114">**RemoveContactFromImList**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="04f5c-114">The **RemoveContactFromImList** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="04f5c-115">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="04f5c-115">**Header name**</span></span>|<span data-ttu-id="04f5c-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="04f5c-116">**Element**</span></span>|<span data-ttu-id="04f5c-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="04f5c-117">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="04f5c-118">**模拟**</span><span class="sxs-lookup"><span data-stu-id="04f5c-118">**Impersonation**</span></span> <br/> |[<span data-ttu-id="04f5c-119">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="04f5c-119">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="04f5c-120">标识客户端应用程序模拟的用户。</span><span class="sxs-lookup"><span data-stu-id="04f5c-120">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="04f5c-121">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="04f5c-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="04f5c-122">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="04f5c-122">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="04f5c-123">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="04f5c-123">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="04f5c-124">确定用于访问邮箱的区域性（如 RFC 3066 中定义的用于标识语言的标记）。</span><span class="sxs-lookup"><span data-stu-id="04f5c-124">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="04f5c-125">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="04f5c-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="04f5c-126">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="04f5c-126">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="04f5c-127">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="04f5c-127">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="04f5c-128">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="04f5c-128">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="04f5c-129">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="04f5c-129">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="04f5c-130">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="04f5c-130">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="04f5c-131">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="04f5c-131">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="04f5c-132">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="04f5c-132">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="04f5c-133">此标头适用于响应。</span><span class="sxs-lookup"><span data-stu-id="04f5c-133">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="removecontactfromimlist-operation-request-example-remove-a-contact-from-the-lync-contacts-list"></a><span data-ttu-id="04f5c-134">RemoveContactFromImList 操作请求示例：从 Lync 联系人列表中删除联系人</span><span class="sxs-lookup"><span data-stu-id="04f5c-134">RemoveContactFromImList operation request example: Remove a contact from the Lync Contacts list</span></span>

<span data-ttu-id="04f5c-135">以下示例的**RemoveContactFromImList**操作请求显示如何从**Lync 联系人**列表中删除联系人。</span><span class="sxs-lookup"><span data-stu-id="04f5c-135">The following example of a **RemoveContactFromImList** operation request shows how to remove a contact from the **Lync Contacts** list.</span></span> <span data-ttu-id="04f5c-136">**RemoveContactFromImList**操作接受单一的唯一联系人标识符，以标识从**Lync 联系人**列表中删除的联系人。</span><span class="sxs-lookup"><span data-stu-id="04f5c-136">The **RemoveContactFromImList** operation accepts a single unique contact identifier to identify the contact that is removed from the **Lync Contacts** list.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="04f5c-137">本文中的所有项目标识符和更改密钥都已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="04f5c-137">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> 
  
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
      <m:RemoveContactFromImList>
         <m:ContactId Id=""/>
      </m:RemoveContactFromImList>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="04f5c-138">请求 SOAP 正文中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="04f5c-138">The following elements are used in the request SOAP body:</span></span>
  
- [<span data-ttu-id="04f5c-139">RemoveContactFromImList</span><span class="sxs-lookup"><span data-stu-id="04f5c-139">RemoveContactFromImList</span></span>](removecontactfromimlist.md)
    
- [<span data-ttu-id="04f5c-140">ContactId</span><span class="sxs-lookup"><span data-stu-id="04f5c-140">ContactId</span></span>](contactid.md)
    
## <a name="successful-removecontactfromimlist-operation-response"></a><span data-ttu-id="04f5c-141">成功的 RemoveContactFromImList 操作响应</span><span class="sxs-lookup"><span data-stu-id="04f5c-141">Successful RemoveContactFromImList operation response</span></span>

<span data-ttu-id="04f5c-142">以下示例显示了对从**Lync 联系人**列表中删除联系人的**RemoveContactFromImList**操作请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="04f5c-142">The following example shows a successful response to a **RemoveContactFromImList** operation request to remove a contact from the **Lync Contacts** list.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="8" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <RemoveContactFromImListResponse ResponseClass="Success" 
                                       xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </RemoveContactFromImListResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="04f5c-143">响应 SOAP 正文中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="04f5c-143">The following elements are used in the response SOAP body:</span></span>
  
- [<span data-ttu-id="04f5c-144">RemoveContactFromImListResponse</span><span class="sxs-lookup"><span data-stu-id="04f5c-144">RemoveContactFromImListResponse</span></span>](removecontactfromimlistresponse.md)
    
- [<span data-ttu-id="04f5c-145">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="04f5c-145">ResponseCode</span></span>](responsecode.md)
    
## <a name="removecontactfromimlist-operation-error-response"></a><span data-ttu-id="04f5c-146">RemoveContactFromImList 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="04f5c-146">RemoveContactFromImList operation error response</span></span>

<span data-ttu-id="04f5c-147">下面的示例演示对**RemoveContactFromImList**操作请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="04f5c-147">The following example shows an error response to a **RemoveContactFromImList** operation request.</span></span> <span data-ttu-id="04f5c-148">这是对在联系人不再存在于列表中时从**Lync 联系人**列表中删除联系人的请求的响应。</span><span class="sxs-lookup"><span data-stu-id="04f5c-148">This is a response to a request to remove a contact from the **Lync Contacts** list when the contact no longer exists in the list.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="8" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <RemoveContactFromImListResponse ResponseClass="Error" 
                                       xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified object was not found in the store.</MessageText>
         <ResponseCode>ErrorItemNotFound</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </RemoveContactFromImListResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="04f5c-149">错误响应 SOAP 正文中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="04f5c-149">The following elements are used in the error response SOAP body:</span></span>
  
- [<span data-ttu-id="04f5c-150">RemoveContactFromImListResponse</span><span class="sxs-lookup"><span data-stu-id="04f5c-150">RemoveContactFromImListResponse</span></span>](removecontactfromimlistresponse.md)
    
- [<span data-ttu-id="04f5c-151">MessageText</span><span class="sxs-lookup"><span data-stu-id="04f5c-151">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="04f5c-152">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="04f5c-152">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="04f5c-153">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="04f5c-153">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="04f5c-154">另请参阅</span><span class="sxs-lookup"><span data-stu-id="04f5c-154">See also</span></span>

- [<span data-ttu-id="04f5c-155">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="04f5c-155">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="04f5c-156">GetImItemList 操作</span><span class="sxs-lookup"><span data-stu-id="04f5c-156">GetImItemList operation</span></span>](getimitemlist-operation.md)
    

