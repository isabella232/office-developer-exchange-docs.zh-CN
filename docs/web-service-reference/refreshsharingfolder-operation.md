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
description: RefreshSharingFolder 操作将使用所共享的文件夹中的最新数据刷新指定的本地文件夹。
ms.openlocfilehash: dd7136ae82353841db09497d23eabe450c1c8b13
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456736"
---
# <a name="refreshsharingfolder-operation"></a><span data-ttu-id="3de94-103">RefreshSharingFolder 操作</span><span class="sxs-lookup"><span data-stu-id="3de94-103">RefreshSharingFolder operation</span></span>

<span data-ttu-id="3de94-104">**RefreshSharingFolder**操作将使用所共享的文件夹中的最新数据刷新指定的本地文件夹。</span><span class="sxs-lookup"><span data-stu-id="3de94-104">The **RefreshSharingFolder** operation refreshes the specified local folder with the latest data from the folder that is being shared.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="3de94-105">SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="3de94-105">SOAP Headers</span></span>

<span data-ttu-id="3de94-106">**RefreshSharingFolder**操作可以使用下表中列出和描述的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="3de94-106">The **RefreshSharingFolder** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="3de94-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="3de94-107">**Header**</span></span>|<span data-ttu-id="3de94-108">**元素**</span><span class="sxs-lookup"><span data-stu-id="3de94-108">**Element**</span></span>|<span data-ttu-id="3de94-109">**说明**</span><span class="sxs-lookup"><span data-stu-id="3de94-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3de94-110">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="3de94-110">RequestVersion</span></span>  <br/> |[<span data-ttu-id="3de94-111">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="3de94-111">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="3de94-112">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="3de94-112">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="3de94-113">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="3de94-113">ServerVersion</span></span>  <br/> |[<span data-ttu-id="3de94-114">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="3de94-114">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="3de94-115">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="3de94-115">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="refreshsharingfolder-request-example"></a><span data-ttu-id="3de94-116">RefreshSharingFolder 请求示例</span><span class="sxs-lookup"><span data-stu-id="3de94-116">RefreshSharingFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="3de94-117">Description</span><span class="sxs-lookup"><span data-stu-id="3de94-117">Description</span></span>

<span data-ttu-id="3de94-118">下面的示例演示如何使用要共享的文件夹中的最新数据来组成刷新指定本地文件夹的请求。</span><span class="sxs-lookup"><span data-stu-id="3de94-118">The following example shows how to form a request to refresh the specified local folder with the latest data from the folder that is being shared.</span></span> <span data-ttu-id="3de94-119">[SharingFolderId](sharingfolderid.md)元素指定要刷新的本地文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="3de94-119">The [SharingFolderId](sharingfolderid.md) element specifies the identifier of the local folder to be refreshed.</span></span> 
  
### <a name="code"></a><span data-ttu-id="3de94-120">代码</span><span class="sxs-lookup"><span data-stu-id="3de94-120">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010"/>
  </soap:Header>
  <soap:Body>
    <RefreshSharingFolder xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:SharingFolderId Id="AAMkAD=" ChangeKey="AwAAA=" />
    </RefreshSharingFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="3de94-121">Request 元素</span><span class="sxs-lookup"><span data-stu-id="3de94-121">Request elements</span></span>

<span data-ttu-id="3de94-122">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="3de94-122">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="3de94-123">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="3de94-123">RequestServerVersion</span></span>](requestserverversion.md)
    
- [<span data-ttu-id="3de94-124">RefreshSharingFolder</span><span class="sxs-lookup"><span data-stu-id="3de94-124">RefreshSharingFolder</span></span>](refreshsharingfolder.md)
    
- [<span data-ttu-id="3de94-125">SharingFolderId</span><span class="sxs-lookup"><span data-stu-id="3de94-125">SharingFolderId</span></span>](sharingfolderid.md)
    
## <a name="successful-refreshsharingfolder-response"></a><span data-ttu-id="3de94-126">成功的 RefreshSharingFolder 响应</span><span class="sxs-lookup"><span data-stu-id="3de94-126">Successful RefreshSharingFolder Response</span></span>

### <a name="description"></a><span data-ttu-id="3de94-127">Description</span><span class="sxs-lookup"><span data-stu-id="3de94-127">Description</span></span>

<span data-ttu-id="3de94-128">下面的示例演示对**RefreshSharingFolder**请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="3de94-128">The following example shows a successful response to a **RefreshSharingFolder** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="3de94-129">代码</span><span class="sxs-lookup"><span data-stu-id="3de94-129">Code</span></span>

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
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <RefreshSharingFolderResponseMessage ResponseClass="Success"
                                xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                                xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseCode>NoError</m:ResponseCode>
    </RefreshSharingFolderResponseMessage>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a><span data-ttu-id="3de94-130">成功的响应元素</span><span class="sxs-lookup"><span data-stu-id="3de94-130">Successful response elements</span></span>

<span data-ttu-id="3de94-131">响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="3de94-131">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="3de94-132">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="3de94-132">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="3de94-133">RefreshSharingFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="3de94-133">RefreshSharingFolderResponseMessage</span></span>](refreshsharingfolderresponsemessage.md)
    
- [<span data-ttu-id="3de94-134">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="3de94-134">ResponseCode</span></span>](responsecode.md)
    
## <a name="refreshsharingfolder-error-response"></a><span data-ttu-id="3de94-135">RefreshSharingFolder 错误响应</span><span class="sxs-lookup"><span data-stu-id="3de94-135">RefreshSharingFolder error response</span></span>

### <a name="description"></a><span data-ttu-id="3de94-136">Description</span><span class="sxs-lookup"><span data-stu-id="3de94-136">Description</span></span>

<span data-ttu-id="3de94-137">下面的示例演示对**RefreshSharingFolder**请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="3de94-137">The following example shows an error response to a **RefreshSharingFolder** request.</span></span> <span data-ttu-id="3de94-138">在此示例中， **RefreshSharingFolder**请求失败，因为找不到与指定的本地文件夹相对应的订阅。</span><span class="sxs-lookup"><span data-stu-id="3de94-138">In this example, the **RefreshSharingFolder** request failed because a subscription that corresponds to the specified local folder was not found.</span></span> 
  
### <a name="code"></a><span data-ttu-id="3de94-139">代码</span><span class="sxs-lookup"><span data-stu-id="3de94-139">Code</span></span>

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
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <RefreshSharingFolderResponseMessage ResponseClass="Error"
                                xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                                xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a><span data-ttu-id="3de94-140">错误响应元素</span><span class="sxs-lookup"><span data-stu-id="3de94-140">Error response elements</span></span>

<span data-ttu-id="3de94-141">错误响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="3de94-141">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="3de94-142">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="3de94-142">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="3de94-143">RefreshSharingFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="3de94-143">RefreshSharingFolderResponseMessage</span></span>](refreshsharingfolderresponsemessage.md)
    
- [<span data-ttu-id="3de94-144">MessageText</span><span class="sxs-lookup"><span data-stu-id="3de94-144">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="3de94-145">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="3de94-145">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="3de94-146">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="3de94-146">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="3de94-147">MessageXml</span><span class="sxs-lookup"><span data-stu-id="3de94-147">MessageXml</span></span>](messagexml.md)
    
## <a name="see-also"></a><span data-ttu-id="3de94-148">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3de94-148">See also</span></span>



[<span data-ttu-id="3de94-149">RefreshSharingFolder</span><span class="sxs-lookup"><span data-stu-id="3de94-149">RefreshSharingFolder</span></span>](refreshsharingfolder.md)
  
[<span data-ttu-id="3de94-150">RefreshSharingFolderType</span><span class="sxs-lookup"><span data-stu-id="3de94-150">RefreshSharingFolderType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.RefreshSharingFolderType.aspx)
  
[<span data-ttu-id="3de94-151">RefreshSharingFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="3de94-151">RefreshSharingFolderResponseMessage</span></span>](refreshsharingfolderresponsemessage.md)
  
[<span data-ttu-id="3de94-152">RefreshSharingFolderResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="3de94-152">RefreshSharingFolderResponseMessageType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.RefreshSharingFolderResponseMessageType.aspx)


[<span data-ttu-id="3de94-153">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="3de94-153">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
  
- [<span data-ttu-id="3de94-154">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="3de94-154">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

