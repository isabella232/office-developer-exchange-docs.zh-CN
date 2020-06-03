---
title: MarkAllItemsAsRead 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ea5b1cb6-6998-46fb-a99c-a6d3da77591f
description: 查找有关 MarkAllItemsAsRead EWS 操作的信息。
ms.openlocfilehash: aeeacea1cd5eed723f93027dd1ef75b34605fdfd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530528"
---
# <a name="markallitemsasread-operation"></a><span data-ttu-id="30920-103">MarkAllItemsAsRead 操作</span><span class="sxs-lookup"><span data-stu-id="30920-103">MarkAllItemsAsRead operation</span></span>

<span data-ttu-id="30920-104">查找有关**MarkAllItemsAsRead** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="30920-104">Find information about the **MarkAllItemsAsRead** EWS operation.</span></span> 
  
<span data-ttu-id="30920-105">**MarkAllItemsAsRead**操作设置一个或多个文件夹中所有项目的[IsRead](isread.md)属性，以指示所有项目都已读或未读。</span><span class="sxs-lookup"><span data-stu-id="30920-105">The **MarkAllItemsAsRead** operation sets the [IsRead](isread.md) property on all items, in one or more folders, to indicate that all items are either read or unread.</span></span> 
  
<span data-ttu-id="30920-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="30920-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-markallitemsasread-operation"></a><span data-ttu-id="30920-107">使用 MarkAllItemsAsRead 操作</span><span class="sxs-lookup"><span data-stu-id="30920-107">Using the MarkAllItemsAsRead operation</span></span>

<span data-ttu-id="30920-108">**MarkAllItemsAsRead**操作可以设置文件夹中的所有项目的[IsRead](isread.md)属性，这些项目由 EXCHANGE Web 服务（EWS）文件夹标识符或默认 Exchange 文件夹名称标识。</span><span class="sxs-lookup"><span data-stu-id="30920-108">The **MarkAllItemsAsRead** operation can set the [IsRead](isread.md) property on all items in folders identified by either the Exchange Web Services (EWS) folder identifier or the default Exchange folder name.</span></span> <span data-ttu-id="30920-109">**MarkAllItemsAsRead**操作还可以禁止发送标记为 "已读" 的项目的已读回执。</span><span class="sxs-lookup"><span data-stu-id="30920-109">The **MarkAllItemsAsRead** operation can also suppress the sending of read receipts for items marked as read.</span></span> 
  
### <a name="markallitemsasread-operation-soap-headers"></a><span data-ttu-id="30920-110">MarkAllItemsAsRead 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="30920-110">MarkAllItemsAsRead operation SOAP headers</span></span>

<span data-ttu-id="30920-111">**MarkAllItemsAsRead**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="30920-111">The **MarkAllItemsAsRead** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="30920-112">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="30920-112">**Header name**</span></span>|<span data-ttu-id="30920-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="30920-113">**Element**</span></span>|<span data-ttu-id="30920-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="30920-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="30920-115">**模拟**</span><span class="sxs-lookup"><span data-stu-id="30920-115">**Impersonation**</span></span> <br/> |[<span data-ttu-id="30920-116">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="30920-116">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="30920-117">标识客户端应用程序模拟的用户。</span><span class="sxs-lookup"><span data-stu-id="30920-117">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="30920-118">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="30920-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="30920-119">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="30920-119">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="30920-120">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="30920-120">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="30920-121">确定用于访问邮箱的区域性（如 RFC 3066 中定义的用于标识语言的标记）。</span><span class="sxs-lookup"><span data-stu-id="30920-121">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="30920-122">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="30920-122">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="30920-123">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="30920-123">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="30920-124">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="30920-124">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="30920-125">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="30920-125">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="30920-126">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="30920-126">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="30920-127">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="30920-127">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="30920-128">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="30920-128">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="30920-129">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="30920-129">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="30920-130">此标头适用于响应。</span><span class="sxs-lookup"><span data-stu-id="30920-130">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="markallitemsasread-operation-request-example-mark-all-items-in-a-folder-as-read"></a><span data-ttu-id="30920-131">MarkAllItemsAsRead 操作请求示例：将文件夹中的所有项目标记为已读</span><span class="sxs-lookup"><span data-stu-id="30920-131">MarkAllItemsAsRead operation request example: Mark all items in a folder as read</span></span>

<span data-ttu-id="30920-132">以下示例的**MarkAllItemsAsRead**操作请求显示如何将文件夹中所有项目的[IsRead](isread.md)属性（也称为 "读取" 标志）设置为**true** 。</span><span class="sxs-lookup"><span data-stu-id="30920-132">The following example of a **MarkAllItemsAsRead** operation request shows how to set the [IsRead](isread.md) property, which is also called the read flag, to **true** on all items in a folder.</span></span> <span data-ttu-id="30920-133">此示例还显示了在响应任何已读回执请求时不会发送 "已读" 回执。</span><span class="sxs-lookup"><span data-stu-id="30920-133">This example also shows that read receipts are not sent in response to any read receipt requests.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="30920-134">本文中的所有项目标识符和更改密钥都已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="30920-134">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> <span data-ttu-id="30920-135">此操作不需要更改键。</span><span class="sxs-lookup"><span data-stu-id="30920-135">Change keys are not required for this operation.</span></span> 
  
```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body>
      <m:MarkAllItemsAsRead>
         <m:ReadFlag>true</m:ReadFlag>
         <m:SuppressReadReceipts>true</m:SuppressReadReceipts>
         <m:FolderIds>
            <t:FolderId Id="AAMkADEzOTExYZRAAA=" 
                        ChangeKey="AQAAAAA3vA==" />
         </m:FolderIds>
      </m:MarkAllItemsAsRead>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="30920-136">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="30920-136">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="30920-137">MarkAllItemsAsRead</span><span class="sxs-lookup"><span data-stu-id="30920-137">MarkAllItemsAsRead</span></span>](markallitemsasread.md)
    
- [<span data-ttu-id="30920-138">ReadFlag</span><span class="sxs-lookup"><span data-stu-id="30920-138">ReadFlag</span></span>](readflag.md)
    
- [<span data-ttu-id="30920-139">SuppressReadReceipts</span><span class="sxs-lookup"><span data-stu-id="30920-139">SuppressReadReceipts</span></span>](suppressreadreceipts.md)
    
- [<span data-ttu-id="30920-140">FolderIds</span><span class="sxs-lookup"><span data-stu-id="30920-140">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="30920-141">FolderId</span><span class="sxs-lookup"><span data-stu-id="30920-141">FolderId</span></span>](folderid.md)
    
## <a name="successful-markallitemsasread-operation-response"></a><span data-ttu-id="30920-142">成功的 MarkAllItemsAsRead 操作响应</span><span class="sxs-lookup"><span data-stu-id="30920-142">Successful MarkAllItemsAsRead operation response</span></span>

<span data-ttu-id="30920-143">下面的示例演示对**MarkAllItemsAsRead**操作请求的成功响应，以将文件夹中的所有项目标记为已读。</span><span class="sxs-lookup"><span data-stu-id="30920-143">The following example shows a successful response to a **MarkAllItemsAsRead** operation request to mark all items in a folder as read.</span></span> 
  
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
      <m:MarkAllItemsAsReadResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:MarkAllItemsAsReadResponseMessage ResponseClass="Success">
               <m:ResponseCode>NoError</m:ResponseCode>
            </m:MarkAllItemsAsReadResponseMessage>
         </m:ResponseMessages>
      </m:MarkAllItemsAsReadResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="30920-144">响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="30920-144">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="30920-145">MarkAllItemsAsReadResponse</span><span class="sxs-lookup"><span data-stu-id="30920-145">MarkAllItemsAsReadResponse</span></span>](markallitemsasreadresponse.md)
    
- [<span data-ttu-id="30920-146">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="30920-146">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="30920-147">MarkAllItemsAsReadResponseMessage</span><span class="sxs-lookup"><span data-stu-id="30920-147">MarkAllItemsAsReadResponseMessage</span></span>](markallitemsasreadresponsemessage.md)
    
- [<span data-ttu-id="30920-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="30920-148">ResponseCode</span></span>](responsecode.md)
    
## <a name="markallitemsasread-operation-request-example-mark-all-items-in-a-folder-as-unread"></a><span data-ttu-id="30920-149">MarkAllItemsAsRead 操作请求示例：将文件夹中的所有项目标记为未读</span><span class="sxs-lookup"><span data-stu-id="30920-149">MarkAllItemsAsRead operation request example: Mark all items in a folder as unread</span></span>

<span data-ttu-id="30920-150">下面的**MarkAllItemsAsRead**操作请求示例演示如何在文件夹中的所有项目上将[IsRead](isread.md)属性设置为**false** 。</span><span class="sxs-lookup"><span data-stu-id="30920-150">The following example of a **MarkAllItemsAsRead** operation request shows how to set the [IsRead](isread.md) property to **false** on all items in a folder.</span></span> <span data-ttu-id="30920-151">此示例还显示了在响应任何已读回执请求时不会发送 "已读" 回执。</span><span class="sxs-lookup"><span data-stu-id="30920-151">This example also shows that read receipts are not sent in response to any read receipt requests.</span></span> 
  
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
      <m:MarkAllItemsAsRead>
         <m:ReadFlag>false</m:ReadFlag>
         <m:SuppressReadReceipts>true</m:SuppressReadReceipts>
         <m:FolderIds>
            <t:FolderId Id="AAMkADEzOTExYZRAAA=" 
                        ChangeKey="AQAAAAA3vA==" />
         </m:FolderIds>
      </m:MarkAllItemsAsRead>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="30920-152">对将所有项目标记为已读的请求的成功响应与对将所有项目标记为未读的请求的响应相同。</span><span class="sxs-lookup"><span data-stu-id="30920-152">A successful response to a request to mark all items as read is the same as the response to a request to mark all items as unread.</span></span>
  
<span data-ttu-id="30920-153">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="30920-153">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="30920-154">MarkAllItemsAsRead</span><span class="sxs-lookup"><span data-stu-id="30920-154">MarkAllItemsAsRead</span></span>](markallitemsasread.md)
    
- [<span data-ttu-id="30920-155">ReadFlag</span><span class="sxs-lookup"><span data-stu-id="30920-155">ReadFlag</span></span>](readflag.md)
    
- [<span data-ttu-id="30920-156">SuppressReadReceipts</span><span class="sxs-lookup"><span data-stu-id="30920-156">SuppressReadReceipts</span></span>](suppressreadreceipts.md)
    
- [<span data-ttu-id="30920-157">FolderIds</span><span class="sxs-lookup"><span data-stu-id="30920-157">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="30920-158">FolderId</span><span class="sxs-lookup"><span data-stu-id="30920-158">FolderId</span></span>](folderid.md)
    
## <a name="markallitemsasread-operation-error-response"></a><span data-ttu-id="30920-159">MarkAllItemsAsRead 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="30920-159">MarkAllItemsAsRead operation error response</span></span>

<span data-ttu-id="30920-160">下面的示例演示对**MarkAllItemsAsRead**操作请求的错误响应，以便将文件夹中的所有项目标记为已读或未读（当该文件夹在邮箱中不存在时）。</span><span class="sxs-lookup"><span data-stu-id="30920-160">The following example shows an error response to a **MarkAllItemsAsRead** operation request to mark all items in a folder as read or unread when the folder does not exist in the mailbox.</span></span> 
  
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
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:MarkAllItemsAsReadResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:MarkAllItemsAsReadResponseMessage ResponseClass="Error">
               <m:MessageText>The specified object was not found in the store.</m:MessageText>
               <m:ResponseCode>ErrorItemNotFound</m:ResponseCode>
               <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
            </m:MarkAllItemsAsReadResponseMessage>
         </m:ResponseMessages>
      </m:MarkAllItemsAsReadResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="30920-161">错误响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="30920-161">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="30920-162">MarkAllItemsAsReadResponse</span><span class="sxs-lookup"><span data-stu-id="30920-162">MarkAllItemsAsReadResponse</span></span>](markallitemsasreadresponse.md)
    
- [<span data-ttu-id="30920-163">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="30920-163">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="30920-164">MarkAllItemsAsReadResponseMessage</span><span class="sxs-lookup"><span data-stu-id="30920-164">MarkAllItemsAsReadResponseMessage</span></span>](markallitemsasreadresponsemessage.md)
    
- [<span data-ttu-id="30920-165">MessageText</span><span class="sxs-lookup"><span data-stu-id="30920-165">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="30920-166">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="30920-166">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="30920-167">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="30920-167">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="30920-168">另请参阅</span><span class="sxs-lookup"><span data-stu-id="30920-168">See also</span></span>

- [<span data-ttu-id="30920-169">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="30920-169">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="30920-170">FindFolder Operation</span><span class="sxs-lookup"><span data-stu-id="30920-170">FindFolder operation</span></span>](findfolder-operation.md)
    

