---
title: ArchiveItem 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1af216b3-13ea-498e-b4fc-23513755d731
description: 查找信息 ArchiveItem EWS 操作。
ms.openlocfilehash: 954943acefef8da61e92de5f8857ca023ca4fc9f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753259"
---
# <a name="archiveitem-operation"></a><span data-ttu-id="9cb31-103">ArchiveItem 操作</span><span class="sxs-lookup"><span data-stu-id="9cb31-103">ArchiveItem operation</span></span>

<span data-ttu-id="9cb31-104">查找有关**ArchiveItem** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="9cb31-104">Find information about the **ArchiveItem** EWS operation.</span></span> 
  
<span data-ttu-id="9cb31-105">**ArchiveItem**操作将项目移动到邮箱用户的存档邮箱。</span><span class="sxs-lookup"><span data-stu-id="9cb31-105">The **ArchiveItem** operation moves an item into the mailbox user's archive mailbox.</span></span> 
  
<span data-ttu-id="9cb31-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="9cb31-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-archiveitem-operation"></a><span data-ttu-id="9cb31-107">使用 ArchiveItem 操作</span><span class="sxs-lookup"><span data-stu-id="9cb31-107">Using the ArchiveItem operation</span></span>

<span data-ttu-id="9cb31-108">**ArchiveItem**操作所需的请求中标识为这些项目移动到存档邮箱和目标文件夹的项目的两个参数。</span><span class="sxs-lookup"><span data-stu-id="9cb31-108">The **ArchiveItem** operation takes two arguments in the request that identify the items to move to the archive mailbox and the destination folder for those items.</span></span> <span data-ttu-id="9cb31-109">必须按顺序执行此操作，以启用存档邮箱。</span><span class="sxs-lookup"><span data-stu-id="9cb31-109">An archive mailbox must be enabled in order for this operation to work.</span></span> <span data-ttu-id="9cb31-110">有关如何启用存档邮箱的信息，请参阅[管理就地存档](http://technet.microsoft.com/en-us/library/jj651146.aspx)。</span><span class="sxs-lookup"><span data-stu-id="9cb31-110">For information about how to enable an archive mailbox, see [Manage In-Place Archives](http://technet.microsoft.com/en-us/library/jj651146.aspx).</span></span>
  
### <a name="archiveitem-operation-soap-headers"></a><span data-ttu-id="9cb31-111">ArchiveItem 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="9cb31-111">ArchiveItem operation SOAP headers</span></span>

<span data-ttu-id="9cb31-112">**ArchiveItem**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="9cb31-112">The **ArchiveItem** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="9cb31-113">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="9cb31-113">**Header name**</span></span>|<span data-ttu-id="9cb31-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="9cb31-114">**Element**</span></span>|<span data-ttu-id="9cb31-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="9cb31-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9cb31-116">**模拟**</span><span class="sxs-lookup"><span data-stu-id="9cb31-116">**Impersonation**</span></span> <br/> |[<span data-ttu-id="9cb31-117">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="9cb31-117">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="9cb31-118">标识模拟客户端应用程序的用户。</span><span class="sxs-lookup"><span data-stu-id="9cb31-118">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="9cb31-119">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="9cb31-119">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="9cb31-120">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="9cb31-120">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="9cb31-121">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="9cb31-121">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="9cb31-122">标识的企业文化，，如 RFC 3066，**标识的语言标记**，以用于访问邮箱中所定义。</span><span class="sxs-lookup"><span data-stu-id="9cb31-122">Identifies the culture, as defined in RFC 3066, **Tags for the Identification of Languages**, to be used to access the mailbox.</span></span> <span data-ttu-id="9cb31-123">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="9cb31-123">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="9cb31-124">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="9cb31-124">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="9cb31-125">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="9cb31-125">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="9cb31-126">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="9cb31-126">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="9cb31-127">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="9cb31-127">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="9cb31-128">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="9cb31-128">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="9cb31-129">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="9cb31-129">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="9cb31-130">标识响应该请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="9cb31-130">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="9cb31-131">适用于响应此标头。</span><span class="sxs-lookup"><span data-stu-id="9cb31-131">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="archiveitem-operation-request-example-move-an-item-to-the-archive-inbox-folder"></a><span data-ttu-id="9cb31-132">ArchiveItem 操作请求示例： 将项目移动到存档收件箱文件夹</span><span class="sxs-lookup"><span data-stu-id="9cb31-132">ArchiveItem operation request example: Move an item to the archive inbox folder</span></span>

<span data-ttu-id="9cb31-133">**ArchiveItem**操作请求的下面的示例演示如何将项目移动到存档收件箱文件夹。</span><span class="sxs-lookup"><span data-stu-id="9cb31-133">The following example of an **ArchiveItem** operation request shows how to move an item to the archive Inbox folder.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9cb31-134">所有项目标识符，本文中的更改项具有已截短要保留可读性。</span><span class="sxs-lookup"><span data-stu-id="9cb31-134">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013"/>
   </soap:Header>
   <soap:Body>
      <m:ArchiveItem>
         <m:ArchiveSourceFolderId>
            <t:DistinguishedFolderId Id="inbox"/>
         </m:ArchiveSourceFolderId>
         <m:ItemIds>
            <t:ItemId Id="AQMkG5BBwrQAAAxoAAAA=" ChangeKey="CQAAAHCtAAAAAAB7"/>
         </m:ItemIds>
      </m:ArchiveItem>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="9cb31-135">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="9cb31-135">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="9cb31-136">ArchiveItem</span><span class="sxs-lookup"><span data-stu-id="9cb31-136">ArchiveItem</span></span>](archiveitem.md)    
- [<span data-ttu-id="9cb31-137">ArchiveSourceFolderId</span><span class="sxs-lookup"><span data-stu-id="9cb31-137">ArchiveSourceFolderId</span></span>](archivesourcefolderid.md)    
- [<span data-ttu-id="9cb31-138">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="9cb31-138">DistinguishedFolderId</span></span>](distinguishedfolderid.md)    
- [<span data-ttu-id="9cb31-139">ItemIds</span><span class="sxs-lookup"><span data-stu-id="9cb31-139">ItemIds</span></span>](itemids.md)   
- [<span data-ttu-id="9cb31-140">ItemId</span><span class="sxs-lookup"><span data-stu-id="9cb31-140">ItemId</span></span>](itemid.md)
    
## <a name="successful-archiveitem-operation-response"></a><span data-ttu-id="9cb31-141">成功 ArchiveItem 操作响应</span><span class="sxs-lookup"><span data-stu-id="9cb31-141">Successful ArchiveItem operation response</span></span>

<span data-ttu-id="9cb31-142">下面的示例演示对**ArchiveItem**操作请求将项目移动到存档邮箱的成功响应。</span><span class="sxs-lookup"><span data-stu-id="9cb31-142">The following example shows a successful response to an **ArchiveItem** operation request to move an item to an archive mailbox.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="526" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:ArchiveItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                             xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:ArchiveItemResponseMessage ResponseClass="Success">
               <m:ResponseCode>NoError</m:ResponseCode>
               <m:Items/>
            </m:ArchiveItemResponseMessage>
         </m:ResponseMessages>
      </m:ArchiveItemResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="9cb31-143">响应 SOAP 正文中包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="9cb31-143">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="9cb31-144">ArchiveItemResponse</span><span class="sxs-lookup"><span data-stu-id="9cb31-144">ArchiveItemResponse</span></span>](archiveitemresponse.md)    
- [<span data-ttu-id="9cb31-145">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="9cb31-145">ResponseMessages</span></span>](responsemessages.md)   
- [<span data-ttu-id="9cb31-146">ArchiveItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="9cb31-146">ArchiveItemResponseMessage</span></span>](archiveitemresponsemessage.md)    
- [<span data-ttu-id="9cb31-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="9cb31-147">ResponseCode</span></span>](responsecode.md)    
- [<span data-ttu-id="9cb31-148">Items</span><span class="sxs-lookup"><span data-stu-id="9cb31-148">Items</span></span>](items.md)
    
## <a name="archiveitem-operation-error-response"></a><span data-ttu-id="9cb31-149">ArchiveItem 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="9cb31-149">ArchiveItem operation error response</span></span>

<span data-ttu-id="9cb31-150">下面的示例演示**ArchiveItem**操作请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="9cb31-150">The following example shows an error response to an **ArchiveItem** operation request.</span></span> <span data-ttu-id="9cb31-151">这是对存档项目时没有为用户启用存档邮箱的有效请求的响应。</span><span class="sxs-lookup"><span data-stu-id="9cb31-151">This is a response to a valid request to archive an item when an archive mailbox is not enabled for a user.</span></span> 
  
```xml
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
      <m:ArchiveItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                             xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:ArchiveItemResponseMessage ResponseClass="Error">
               <m:MessageText>Archive mailbox is not enabled for this user.</m:MessageText>
               <m:ResponseCode>ErrorInvalidOperation</m:ResponseCode>
               <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
               <m:Items/>
            </m:ArchiveItemResponseMessage>
         </m:ResponseMessages>
      </m:ArchiveItemResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="9cb31-152">错误响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="9cb31-152">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="9cb31-153">ArchiveItemResponse</span><span class="sxs-lookup"><span data-stu-id="9cb31-153">ArchiveItemResponse</span></span>](archiveitemresponse.md)    
- [<span data-ttu-id="9cb31-154">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="9cb31-154">ResponseMessages</span></span>](responsemessages.md)    
- [<span data-ttu-id="9cb31-155">ArchiveItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="9cb31-155">ArchiveItemResponseMessage</span></span>](archiveitemresponsemessage.md)    
- [<span data-ttu-id="9cb31-156">MessageText</span><span class="sxs-lookup"><span data-stu-id="9cb31-156">MessageText</span></span>](messagetext.md)    
- [<span data-ttu-id="9cb31-157">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="9cb31-157">ResponseCode</span></span>](responsecode.md)    
- [<span data-ttu-id="9cb31-158">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="9cb31-158">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)    
- [<span data-ttu-id="9cb31-159">Items</span><span class="sxs-lookup"><span data-stu-id="9cb31-159">Items</span></span>](items.md)
    
<span data-ttu-id="9cb31-160">通用到 EWS 且特定于此操作的其他错误代码，请参阅[ResponseCode](responsecode.md)。</span><span class="sxs-lookup"><span data-stu-id="9cb31-160">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9cb31-161">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9cb31-161">See also</span></span>

- [<span data-ttu-id="9cb31-162">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="9cb31-162">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md) 
- [<span data-ttu-id="9cb31-163">在 Exchange 中 EWS 存档</span><span class="sxs-lookup"><span data-stu-id="9cb31-163">Archiving in EWS in Exchange</span></span>](http://msdn.microsoft.com/library/78ae179b-ae4f-4f64-911a-e0c70e0fa314%28Office.15%29.aspx)
    

