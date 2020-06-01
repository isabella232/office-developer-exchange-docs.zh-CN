---
title: RemoveDistributionGroupFromImList 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 252bddf2-98b6-4824-b548-2fba2bda5384
description: 查找有关 RemoveDistributionGroupFromImList EWS 操作的信息。
ms.openlocfilehash: 66220f0cab99f404e17136bbb7836ca13d569b53
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459600"
---
# <a name="removedistributiongroupfromimlist-operation"></a><span data-ttu-id="7ab10-103">RemoveDistributionGroupFromImList 操作</span><span class="sxs-lookup"><span data-stu-id="7ab10-103">RemoveDistributionGroupFromImList operation</span></span>

<span data-ttu-id="7ab10-104">查找有关**RemoveDistributionGroupFromImList** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="7ab10-104">Find information about the **RemoveDistributionGroupFromImList** EWS operation.</span></span> 
  
<span data-ttu-id="7ab10-105">当 Lync 使用联系人存储库的 Exchange 时， **RemoveDistributionGroupFromImList**操作将从 lync 即时消息（IM）列表中删除通讯组。</span><span class="sxs-lookup"><span data-stu-id="7ab10-105">The **RemoveDistributionGroupFromImList** operation removes a distribution group from the Lync instant messaging (IM) list when Lync uses Exchange for the contact store.</span></span> 
  
<span data-ttu-id="7ab10-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="7ab10-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-removedistributiongroupfromimlist-operation"></a><span data-ttu-id="7ab10-107">使用 RemoveDistributionGroupFromImList 操作</span><span class="sxs-lookup"><span data-stu-id="7ab10-107">Using the RemoveDistributionGroupFromImList operation</span></span>

<span data-ttu-id="7ab10-108">**RemoveDistributionGroupFromImList**操作接受单个参数，该参数标识要从存储在 Exchange 服务器上的 Lync IM 列表中删除的通讯组。</span><span class="sxs-lookup"><span data-stu-id="7ab10-108">The **RemoveDistributionGroupFromImList** operation accepts a single argument that identifies a distribution group to remove from the Lync IM list stored on an Exchange server.</span></span> 
  
### <a name="removedistributiongroupfromimlist-operation-soap-headers"></a><span data-ttu-id="7ab10-109">RemoveDistributionGroupFromImList 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="7ab10-109">RemoveDistributionGroupFromImList operation SOAP headers</span></span>

<span data-ttu-id="7ab10-110">**RemoveDistributionGroupFromImList**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="7ab10-110">The **RemoveDistributionGroupFromImList** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="7ab10-111">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="7ab10-111">**Header name**</span></span>|<span data-ttu-id="7ab10-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="7ab10-112">**Element**</span></span>|<span data-ttu-id="7ab10-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="7ab10-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7ab10-114">**模拟**</span><span class="sxs-lookup"><span data-stu-id="7ab10-114">**Impersonation**</span></span> <br/> |[<span data-ttu-id="7ab10-115">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="7ab10-115">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="7ab10-116">标识客户端应用程序模拟的用户。</span><span class="sxs-lookup"><span data-stu-id="7ab10-116">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="7ab10-117">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="7ab10-117">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="7ab10-118">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="7ab10-118">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="7ab10-119">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="7ab10-119">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="7ab10-120">确定用于访问邮箱的区域性（如 RFC 3066 中定义的用于标识语言的标记）。</span><span class="sxs-lookup"><span data-stu-id="7ab10-120">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="7ab10-121">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="7ab10-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="7ab10-122">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="7ab10-122">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="7ab10-123">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="7ab10-123">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="7ab10-124">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="7ab10-124">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="7ab10-125">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="7ab10-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="7ab10-126">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="7ab10-126">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="7ab10-127">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="7ab10-127">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="7ab10-128">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="7ab10-128">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="7ab10-129">此标头适用于响应。</span><span class="sxs-lookup"><span data-stu-id="7ab10-129">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="removedistributiongroupfromimlist-operation-request-example-remove-a-distribution-group-from-an-im-list"></a><span data-ttu-id="7ab10-130">RemoveDistributionGroupFromImList 操作请求示例：从 IM 列表中删除通讯组</span><span class="sxs-lookup"><span data-stu-id="7ab10-130">RemoveDistributionGroupFromImList operation request example: Remove a distribution group from an IM list</span></span>

<span data-ttu-id="7ab10-131">下面的**RemoveDistributionGroupFromImList**操作请求示例演示如何从 IM 组中删除通讯组。</span><span class="sxs-lookup"><span data-stu-id="7ab10-131">The following example of a **RemoveDistributionGroupFromImList** operation request shows how to remove a distribution group from an IM group.</span></span> <span data-ttu-id="7ab10-132">**RemoveDistributionGroupFromImList**操作接受唯一的组标识符，以标识要从 IM 列表中删除的通讯组。</span><span class="sxs-lookup"><span data-stu-id="7ab10-132">The **RemoveDistributionGroupFromImList** operation accepts the unique group identifier to identify the distribution group to remove from the IM list.</span></span> <span data-ttu-id="7ab10-133">在[GetImItemList 操作](getimitemlist-operation.md)和[AddDistributionGroupToImList 操作](adddistributiongrouptoimlist-operation.md)的响应中返回的[EXCHANGESTOREID](exchangestoreid.md)元素标识可从 IM 列表中删除的通讯组。</span><span class="sxs-lookup"><span data-stu-id="7ab10-133">The [ExchangeStoreId](exchangestoreid.md) element that is returned in the response for the [GetImItemList operation](getimitemlist-operation.md) and the [AddDistributionGroupToImList operation](adddistributiongrouptoimlist-operation.md) identifies distribution groups that can be removed from the IM list.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7ab10-134">本文中的所有项目标识符和更改密钥都已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="7ab10-134">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> 
  
```XML
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
      <t:MailboxCulture>en-US</t:MailboxCulture>
   </soap:Header>
   <soap:Body >
      <m:RemoveDistributionGroupFromImList>
         <m:GroupId Id="AAMkADEzO4QrAABmEh5oAAA="/>
      </m:RemoveDistributionGroupFromImList>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="7ab10-135">请求 SOAP 正文中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="7ab10-135">The following elements are used in the request SOAP body:</span></span>
  
- [<span data-ttu-id="7ab10-136">RemoveDistributionGroupFromImList</span><span class="sxs-lookup"><span data-stu-id="7ab10-136">RemoveDistributionGroupFromImList</span></span>](removedistributiongroupfromimlist.md)
    
- [<span data-ttu-id="7ab10-137">GroupId</span><span class="sxs-lookup"><span data-stu-id="7ab10-137">GroupId</span></span>](groupid.md)
    
## <a name="successful-removedistributiongroupfromimlist-operation-response"></a><span data-ttu-id="7ab10-138">成功的 RemoveDistributionGroupFromImList 操作响应</span><span class="sxs-lookup"><span data-stu-id="7ab10-138">Successful RemoveDistributionGroupFromImList operation response</span></span>

<span data-ttu-id="7ab10-139">下面的示例演示对从 IM 组中删除通讯组的**RemoveDistributionGroupFromImList**操作请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="7ab10-139">The following example shows a successful response to a **RemoveDistributionGroupFromImList** operation request to a remove a distribution group from an IM group.</span></span> 
  
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
      <RemoveDistributionGroupFromImListResponse ResponseClass="Success" 
                                                 xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </RemoveDistributionGroupFromImListResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="7ab10-140">响应 SOAP 正文中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="7ab10-140">The following elements are used in the response SOAP body:</span></span>
  
- [<span data-ttu-id="7ab10-141">RemoveDistributionGroupFromImListResponse</span><span class="sxs-lookup"><span data-stu-id="7ab10-141">RemoveDistributionGroupFromImListResponse</span></span>](removedistributiongroupfromimlistresponse.md)
    
- [<span data-ttu-id="7ab10-142">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="7ab10-142">ResponseCode</span></span>](responsecode.md)
    
## <a name="removedistributiongroupfromimlist-operation-error-response-example"></a><span data-ttu-id="7ab10-143">RemoveDistributionGroupFromImList 操作错误响应示例</span><span class="sxs-lookup"><span data-stu-id="7ab10-143">RemoveDistributionGroupFromImList operation error response example</span></span>

<span data-ttu-id="7ab10-144">下面的示例演示对**RemoveDistributionGroupFromImList**操作请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="7ab10-144">The following example shows an error response to a **RemoveDistributionGroupFromImList** operation request.</span></span> <span data-ttu-id="7ab10-145">这是对删除已从邮箱中删除的通讯组的请求的响应。</span><span class="sxs-lookup"><span data-stu-id="7ab10-145">This is a response to a request to remove a distribution group that has already been removed from the mailbox.</span></span> 
  
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
      <RemoveDistributionGroupFromImListResponse ResponseClass="Error" 
                                                 xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified object was not found in the store.</MessageText>
         <ResponseCode>ErrorItemNotFound</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </RemoveDistributionGroupFromImListResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="7ab10-146">错误响应 SOAP 正文中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="7ab10-146">The following elements are used in the error response SOAP body:</span></span>
  
- [<span data-ttu-id="7ab10-147">RemoveDistributionGroupFromImListResponse</span><span class="sxs-lookup"><span data-stu-id="7ab10-147">RemoveDistributionGroupFromImListResponse</span></span>](removedistributiongroupfromimlistresponse.md)
    
- [<span data-ttu-id="7ab10-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="7ab10-148">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="7ab10-149">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="7ab10-149">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="7ab10-150">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="7ab10-150">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="7ab10-151">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7ab10-151">See also</span></span>

- [<span data-ttu-id="7ab10-152">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="7ab10-152">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="7ab10-153">GetImItemList 操作</span><span class="sxs-lookup"><span data-stu-id="7ab10-153">GetImItemList operation</span></span>](getimitemlist-operation.md)
    
- [<span data-ttu-id="7ab10-154">AddDistributionGroupToImList 操作</span><span class="sxs-lookup"><span data-stu-id="7ab10-154">AddDistributionGroupToImList operation</span></span>](adddistributiongrouptoimlist-operation.md)
    
- [<span data-ttu-id="7ab10-155">人员和 Exchange 中的 EWS 中的联系人</span><span class="sxs-lookup"><span data-stu-id="7ab10-155">People and contacts in EWS in Exchange</span></span>](https://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx#What)
    

