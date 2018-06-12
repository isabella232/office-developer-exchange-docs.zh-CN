---
title: MarkAllItemsAsRead 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ea5b1cb6-6998-46fb-a99c-a6d3da77591f
description: 查找信息 MarkAllItemsAsRead EWS 操作。
ms.openlocfilehash: 995a6219f0a3b41bddb0d65c875d981322e1ce78
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826354"
---
# <a name="markallitemsasread-operation"></a><span data-ttu-id="d82d7-103">MarkAllItemsAsRead 操作</span><span class="sxs-lookup"><span data-stu-id="d82d7-103">MarkAllItemsAsRead operation</span></span>

<span data-ttu-id="d82d7-104">查找有关**MarkAllItemsAsRead** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="d82d7-104">Find information about the **MarkAllItemsAsRead** EWS operation.</span></span> 
  
<span data-ttu-id="d82d7-105">**MarkAllItemsAsRead**操作将[IsRead](isread.md)属性设置中一个或多个文件夹，以指示所有项目都都读或未读的所有项。</span><span class="sxs-lookup"><span data-stu-id="d82d7-105">The **MarkAllItemsAsRead** operation sets the [IsRead](isread.md) property on all items, in one or more folders, to indicate that all items are either read or unread.</span></span> 
  
<span data-ttu-id="d82d7-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="d82d7-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-markallitemsasread-operation"></a><span data-ttu-id="d82d7-107">使用 MarkAllItemsAsRead 操作</span><span class="sxs-lookup"><span data-stu-id="d82d7-107">Using the MarkAllItemsAsRead operation</span></span>

<span data-ttu-id="d82d7-108">**MarkAllItemsAsRead**操作可以通过 Exchange Web Services (EWS) 文件夹标识符或默认 Exchange 文件夹名称标识的文件夹中的所有项设置[IsRead](isread.md)属性。</span><span class="sxs-lookup"><span data-stu-id="d82d7-108">The **MarkAllItemsAsRead** operation can set the [IsRead](isread.md) property on all items in folders identified by either the Exchange Web Services (EWS) folder identifier or the default Exchange folder name.</span></span> <span data-ttu-id="d82d7-109">**MarkAllItemsAsRead**操作还可以隐藏的项目标记为已读发送已读回执。</span><span class="sxs-lookup"><span data-stu-id="d82d7-109">The **MarkAllItemsAsRead** operation can also suppress the sending of read receipts for items marked as read.</span></span> 
  
### <a name="markallitemsasread-operation-soap-headers"></a><span data-ttu-id="d82d7-110">MarkAllItemsAsRead 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="d82d7-110">MarkAllItemsAsRead operation SOAP headers</span></span>

<span data-ttu-id="d82d7-111">**MarkAllItemsAsRead**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="d82d7-111">The **MarkAllItemsAsRead** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="d82d7-112">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="d82d7-112">**Header name**</span></span>|<span data-ttu-id="d82d7-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="d82d7-113">**Element**</span></span>|<span data-ttu-id="d82d7-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="d82d7-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d82d7-115">**模拟**</span><span class="sxs-lookup"><span data-stu-id="d82d7-115">**Impersonation**</span></span> <br/> |[<span data-ttu-id="d82d7-116">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="d82d7-116">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="d82d7-117">标识模拟客户端应用程序的用户。</span><span class="sxs-lookup"><span data-stu-id="d82d7-117">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="d82d7-118">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="d82d7-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="d82d7-119">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="d82d7-119">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="d82d7-120">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="d82d7-120">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="d82d7-121">定义 RFC 3066 中，"标记的标识的语言"，以用于访问邮箱标识与的区域性。</span><span class="sxs-lookup"><span data-stu-id="d82d7-121">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="d82d7-122">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="d82d7-122">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="d82d7-123">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="d82d7-123">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="d82d7-124">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="d82d7-124">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="d82d7-125">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="d82d7-125">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="d82d7-126">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="d82d7-126">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="d82d7-127">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="d82d7-127">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="d82d7-128">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="d82d7-128">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="d82d7-129">标识响应该请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="d82d7-129">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="d82d7-130">适用于响应此标头。</span><span class="sxs-lookup"><span data-stu-id="d82d7-130">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="markallitemsasread-operation-request-example-mark-all-items-in-a-folder-as-read"></a><span data-ttu-id="d82d7-131">MarkAllItemsAsRead 操作请求示例： 标记为已读文件夹中的所有项目</span><span class="sxs-lookup"><span data-stu-id="d82d7-131">MarkAllItemsAsRead operation request example: Mark all items in a folder as read</span></span>

<span data-ttu-id="d82d7-132">**MarkAllItemsAsRead**操作请求的下面的示例演示如何将[IsRead](isread.md)属性，也称为读取标志，设置为**true**文件夹中的所有项目。</span><span class="sxs-lookup"><span data-stu-id="d82d7-132">The following example of a **MarkAllItemsAsRead** operation request shows how to set the [IsRead](isread.md) property, which is also called the read flag, to **true** on all items in a folder.</span></span> <span data-ttu-id="d82d7-133">此示例还演示的 read 不以任何读的回执请求的响应发送回执。</span><span class="sxs-lookup"><span data-stu-id="d82d7-133">This example also shows that read receipts are not sent in response to any read receipt requests.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d82d7-134">所有项目标识符，本文中的更改项具有已截短要保留可读性。</span><span class="sxs-lookup"><span data-stu-id="d82d7-134">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> <span data-ttu-id="d82d7-135">更改键不需要此操作。</span><span class="sxs-lookup"><span data-stu-id="d82d7-135">Change keys are not required for this operation.</span></span> 
  
```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
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

<span data-ttu-id="d82d7-136">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="d82d7-136">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="d82d7-137">MarkAllItemsAsRead</span><span class="sxs-lookup"><span data-stu-id="d82d7-137">MarkAllItemsAsRead</span></span>](markallitemsasread.md)
    
- [<span data-ttu-id="d82d7-138">ReadFlag</span><span class="sxs-lookup"><span data-stu-id="d82d7-138">ReadFlag</span></span>](readflag.md)
    
- [<span data-ttu-id="d82d7-139">SuppressReadReceipts</span><span class="sxs-lookup"><span data-stu-id="d82d7-139">SuppressReadReceipts</span></span>](suppressreadreceipts.md)
    
- [<span data-ttu-id="d82d7-140">FolderIds</span><span class="sxs-lookup"><span data-stu-id="d82d7-140">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="d82d7-141">文件夹 Id</span><span class="sxs-lookup"><span data-stu-id="d82d7-141">FolderId</span></span>](folderid.md)
    
## <a name="successful-markallitemsasread-operation-response"></a><span data-ttu-id="d82d7-142">成功 MarkAllItemsAsRead 操作响应</span><span class="sxs-lookup"><span data-stu-id="d82d7-142">Successful MarkAllItemsAsRead operation response</span></span>

<span data-ttu-id="d82d7-143">下面的示例演示对**MarkAllItemsAsRead**操作请求标记为已读文件夹中的所有项目的成功响应。</span><span class="sxs-lookup"><span data-stu-id="d82d7-143">The following example shows a successful response to a **MarkAllItemsAsRead** operation request to mark all items in a folder as read.</span></span> 
  
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
      <m:MarkAllItemsAsReadResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:MarkAllItemsAsReadResponseMessage ResponseClass="Success">
               <m:ResponseCode>NoError</m:ResponseCode>
            </m:MarkAllItemsAsReadResponseMessage>
         </m:ResponseMessages>
      </m:MarkAllItemsAsReadResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="d82d7-144">响应 SOAP 正文中包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="d82d7-144">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="d82d7-145">MarkAllItemsAsReadResponse</span><span class="sxs-lookup"><span data-stu-id="d82d7-145">MarkAllItemsAsReadResponse</span></span>](markallitemsasreadresponse.md)
    
- [<span data-ttu-id="d82d7-146">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d82d7-146">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="d82d7-147">MarkAllItemsAsReadResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d82d7-147">MarkAllItemsAsReadResponseMessage</span></span>](markallitemsasreadresponsemessage.md)
    
- [<span data-ttu-id="d82d7-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d82d7-148">ResponseCode</span></span>](responsecode.md)
    
## <a name="markallitemsasread-operation-request-example-mark-all-items-in-a-folder-as-unread"></a><span data-ttu-id="d82d7-149">MarkAllItemsAsRead 操作请求示例： 标记为未读文件夹中的所有项目</span><span class="sxs-lookup"><span data-stu-id="d82d7-149">MarkAllItemsAsRead operation request example: Mark all items in a folder as unread</span></span>

<span data-ttu-id="d82d7-150">**MarkAllItemsAsRead**操作请求的下面的示例演示如何在文件夹中的所有项目将[IsRead](isread.md)属性设置为**false** 。</span><span class="sxs-lookup"><span data-stu-id="d82d7-150">The following example of a **MarkAllItemsAsRead** operation request shows how to set the [IsRead](isread.md) property to **false** on all items in a folder.</span></span> <span data-ttu-id="d82d7-151">此示例还演示的 read 不以任何读的回执请求的响应发送回执。</span><span class="sxs-lookup"><span data-stu-id="d82d7-151">This example also shows that read receipts are not sent in response to any read receipt requests.</span></span> 
  
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

<span data-ttu-id="d82d7-152">请求标记为未读的所有项目的响应相同的请求将所有项目都标记为已读成功响应。</span><span class="sxs-lookup"><span data-stu-id="d82d7-152">A successful response to a request to mark all items as read is the same as the response to a request to mark all items as unread.</span></span>
  
<span data-ttu-id="d82d7-153">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="d82d7-153">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="d82d7-154">MarkAllItemsAsRead</span><span class="sxs-lookup"><span data-stu-id="d82d7-154">MarkAllItemsAsRead</span></span>](markallitemsasread.md)
    
- [<span data-ttu-id="d82d7-155">ReadFlag</span><span class="sxs-lookup"><span data-stu-id="d82d7-155">ReadFlag</span></span>](readflag.md)
    
- [<span data-ttu-id="d82d7-156">SuppressReadReceipts</span><span class="sxs-lookup"><span data-stu-id="d82d7-156">SuppressReadReceipts</span></span>](suppressreadreceipts.md)
    
- [<span data-ttu-id="d82d7-157">FolderIds</span><span class="sxs-lookup"><span data-stu-id="d82d7-157">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="d82d7-158">文件夹 Id</span><span class="sxs-lookup"><span data-stu-id="d82d7-158">FolderId</span></span>](folderid.md)
    
## <a name="markallitemsasread-operation-error-response"></a><span data-ttu-id="d82d7-159">MarkAllItemsAsRead 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="d82d7-159">MarkAllItemsAsRead operation error response</span></span>

<span data-ttu-id="d82d7-160">下面的示例演示**MarkAllItemsAsRead**操作请求文件夹中的所有项目标记为已读或未读，该文件夹不存在的邮箱中时出现错误响应。</span><span class="sxs-lookup"><span data-stu-id="d82d7-160">The following example shows an error response to a **MarkAllItemsAsRead** operation request to mark all items in a folder as read or unread when the folder does not exist in the mailbox.</span></span> 
  
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
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:MarkAllItemsAsReadResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="d82d7-161">错误响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="d82d7-161">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="d82d7-162">MarkAllItemsAsReadResponse</span><span class="sxs-lookup"><span data-stu-id="d82d7-162">MarkAllItemsAsReadResponse</span></span>](markallitemsasreadresponse.md)
    
- [<span data-ttu-id="d82d7-163">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d82d7-163">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="d82d7-164">MarkAllItemsAsReadResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d82d7-164">MarkAllItemsAsReadResponseMessage</span></span>](markallitemsasreadresponsemessage.md)
    
- [<span data-ttu-id="d82d7-165">MessageText</span><span class="sxs-lookup"><span data-stu-id="d82d7-165">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="d82d7-166">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d82d7-166">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="d82d7-167">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="d82d7-167">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="d82d7-168">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d82d7-168">See also</span></span>

- [<span data-ttu-id="d82d7-169">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="d82d7-169">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="d82d7-170">FindFolder Operation</span><span class="sxs-lookup"><span data-stu-id="d82d7-170">FindFolder operation</span></span>](findfolder-operation.md)
    

