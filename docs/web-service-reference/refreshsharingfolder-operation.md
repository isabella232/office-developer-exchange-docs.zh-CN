---
title: RefreshSharingFolder 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RefreshSharingFolder
api_type:
- schema
ms.assetid: 1b047e34-40f0-459f-ac9e-e9f8e7349479
description: RefreshSharingFolder 操作刷新使用中的共享文件夹的最新数据指定的本地文件夹。
ms.openlocfilehash: 0037de28f0720b97cd51c58a6ee7e3c06e84d642
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827041"
---
# <a name="refreshsharingfolder-operation"></a><span data-ttu-id="bdbd2-103">RefreshSharingFolder 操作</span><span class="sxs-lookup"><span data-stu-id="bdbd2-103">RefreshSharingFolder operation</span></span>

<span data-ttu-id="bdbd2-104">**RefreshSharingFolder**操作刷新使用中的共享文件夹的最新数据指定的本地文件夹。</span><span class="sxs-lookup"><span data-stu-id="bdbd2-104">The **RefreshSharingFolder** operation refreshes the specified local folder with the latest data from the folder that is being shared.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="bdbd2-105">SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="bdbd2-105">SOAP Headers</span></span>

<span data-ttu-id="bdbd2-106">**RefreshSharingFolder**操作可以使用列出并在下表中所述的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="bdbd2-106">The **RefreshSharingFolder** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="bdbd2-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="bdbd2-107">**Header**</span></span>|<span data-ttu-id="bdbd2-108">**元素**</span><span class="sxs-lookup"><span data-stu-id="bdbd2-108">**Element**</span></span>|<span data-ttu-id="bdbd2-109">**说明**</span><span class="sxs-lookup"><span data-stu-id="bdbd2-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bdbd2-110">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="bdbd2-110">RequestVersion</span></span>  <br/> |[<span data-ttu-id="bdbd2-111">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="bdbd2-111">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="bdbd2-112">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="bdbd2-112">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="bdbd2-113">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="bdbd2-113">ServerVersion</span></span>  <br/> |[<span data-ttu-id="bdbd2-114">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="bdbd2-114">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="bdbd2-115">标识响应该请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="bdbd2-115">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="refreshsharingfolder-request-example"></a><span data-ttu-id="bdbd2-116">RefreshSharingFolder 请求示例</span><span class="sxs-lookup"><span data-stu-id="bdbd2-116">RefreshSharingFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="bdbd2-117">说明</span><span class="sxs-lookup"><span data-stu-id="bdbd2-117">Description</span></span>

<span data-ttu-id="bdbd2-118">下面的示例演示如何以形成刷新指定的本地文件夹中的共享文件夹的最新数据的请求。</span><span class="sxs-lookup"><span data-stu-id="bdbd2-118">The following example shows how to form a request to refresh the specified local folder with the latest data from the folder that is being shared.</span></span> <span data-ttu-id="bdbd2-119">[SharingFolderId](sharingfolderid.md)元素指定要刷新的本地文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="bdbd2-119">The [SharingFolderId](sharingfolderid.md) element specifies the identifier of the local folder to be refreshed.</span></span> 
  
### <a name="code"></a><span data-ttu-id="bdbd2-120">代码</span><span class="sxs-lookup"><span data-stu-id="bdbd2-120">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010"/>
  </soap:Header>
  <soap:Body>
    <RefreshSharingFolder xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:SharingFolderId Id="AAMkAD=" ChangeKey="AwAAA=" />
    </RefreshSharingFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="bdbd2-121">请求元素</span><span class="sxs-lookup"><span data-stu-id="bdbd2-121">Request elements</span></span>

<span data-ttu-id="bdbd2-122">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="bdbd2-122">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="bdbd2-123">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="bdbd2-123">RequestServerVersion</span></span>](requestserverversion.md)
    
- [<span data-ttu-id="bdbd2-124">RefreshSharingFolder</span><span class="sxs-lookup"><span data-stu-id="bdbd2-124">RefreshSharingFolder</span></span>](refreshsharingfolder.md)
    
- [<span data-ttu-id="bdbd2-125">SharingFolderId</span><span class="sxs-lookup"><span data-stu-id="bdbd2-125">SharingFolderId</span></span>](sharingfolderid.md)
    
## <a name="successful-refreshsharingfolder-response"></a><span data-ttu-id="bdbd2-126">成功的 RefreshSharingFolder 响应</span><span class="sxs-lookup"><span data-stu-id="bdbd2-126">Successful RefreshSharingFolder Response</span></span>

### <a name="description"></a><span data-ttu-id="bdbd2-127">说明</span><span class="sxs-lookup"><span data-stu-id="bdbd2-127">Description</span></span>

<span data-ttu-id="bdbd2-128">下面的示例演示对**RefreshSharingFolder**请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="bdbd2-128">The following example shows a successful response to a **RefreshSharingFolder** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="bdbd2-129">代码</span><span class="sxs-lookup"><span data-stu-id="bdbd2-129">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="11" 
                         Version="Exchange2010" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <RefreshSharingFolderResponseMessage ResponseClass="Success"
                                xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                                xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseCode>NoError</m:ResponseCode>
    </RefreshSharingFolderResponseMessage>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a><span data-ttu-id="bdbd2-130">成功响应元素</span><span class="sxs-lookup"><span data-stu-id="bdbd2-130">Successful response elements</span></span>

<span data-ttu-id="bdbd2-131">在响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="bdbd2-131">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="bdbd2-132">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="bdbd2-132">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="bdbd2-133">RefreshSharingFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="bdbd2-133">RefreshSharingFolderResponseMessage</span></span>](refreshsharingfolderresponsemessage.md)
    
- [<span data-ttu-id="bdbd2-134">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="bdbd2-134">ResponseCode</span></span>](responsecode.md)
    
## <a name="refreshsharingfolder-error-response"></a><span data-ttu-id="bdbd2-135">RefreshSharingFolder 错误响应</span><span class="sxs-lookup"><span data-stu-id="bdbd2-135">RefreshSharingFolder error response</span></span>

### <a name="description"></a><span data-ttu-id="bdbd2-136">说明</span><span class="sxs-lookup"><span data-stu-id="bdbd2-136">Description</span></span>

<span data-ttu-id="bdbd2-137">下面的示例演示对**RefreshSharingFolder**请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="bdbd2-137">The following example shows an error response to a **RefreshSharingFolder** request.</span></span> <span data-ttu-id="bdbd2-138">本示例中， **RefreshSharingFolder**请求失败，因为找不到订阅对应于指定的本地文件夹。</span><span class="sxs-lookup"><span data-stu-id="bdbd2-138">In this example, the **RefreshSharingFolder** request failed because a subscription that corresponds to the specified local folder was not found.</span></span> 
  
### <a name="code"></a><span data-ttu-id="bdbd2-139">代码</span><span class="sxs-lookup"><span data-stu-id="bdbd2-139">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="11" 
                         Version="Exchange2010" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <RefreshSharingFolderResponseMessage ResponseClass="Error"
                                xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                                xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:MessageText>Failed to synchronize the sharing folder.</m:MessageText>
      <m:ResponseCode>ErrorSharingSynchronizationFailed</m:ResponseCode>
      <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
      <m:MessageXml>
        <t:Value Name="ErrorDetails">Microsoft.Exchange.InfoWorker.Common.Sharing.SubscriptionNotFoundException: The subscription wasn't found.;</t:Value>
      </m:MessageXml>
    </RefreshSharingFolderResponseMessage>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="bdbd2-140">错误响应元素</span><span class="sxs-lookup"><span data-stu-id="bdbd2-140">Error response elements</span></span>

<span data-ttu-id="bdbd2-141">错误响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="bdbd2-141">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="bdbd2-142">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="bdbd2-142">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="bdbd2-143">RefreshSharingFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="bdbd2-143">RefreshSharingFolderResponseMessage</span></span>](refreshsharingfolderresponsemessage.md)
    
- [<span data-ttu-id="bdbd2-144">MessageText</span><span class="sxs-lookup"><span data-stu-id="bdbd2-144">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="bdbd2-145">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="bdbd2-145">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="bdbd2-146">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="bdbd2-146">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="bdbd2-147">MessageXml</span><span class="sxs-lookup"><span data-stu-id="bdbd2-147">MessageXml</span></span>](messagexml.md)
    
## <a name="see-also"></a><span data-ttu-id="bdbd2-148">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bdbd2-148">See also</span></span>



[<span data-ttu-id="bdbd2-149">RefreshSharingFolder</span><span class="sxs-lookup"><span data-stu-id="bdbd2-149">RefreshSharingFolder</span></span>](refreshsharingfolder.md)
  
[<span data-ttu-id="bdbd2-150">RefreshSharingFolderType</span><span class="sxs-lookup"><span data-stu-id="bdbd2-150">RefreshSharingFolderType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.RefreshSharingFolderType.aspx)
  
[<span data-ttu-id="bdbd2-151">RefreshSharingFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="bdbd2-151">RefreshSharingFolderResponseMessage</span></span>](refreshsharingfolderresponsemessage.md)
  
[<span data-ttu-id="bdbd2-152">RefreshSharingFolderResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="bdbd2-152">RefreshSharingFolderResponseMessageType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.RefreshSharingFolderResponseMessageType.aspx)


[<span data-ttu-id="bdbd2-153">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="bdbd2-153">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
  
- [<span data-ttu-id="bdbd2-154">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="bdbd2-154">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

