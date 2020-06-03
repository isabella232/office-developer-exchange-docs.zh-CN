---
title: GetAppMarketplaceUrl 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2c016fc3-0e13-4624-9a5b-d3e84577a860
description: 查找有关 GetAppMarketplaceUrl EWS 操作的信息。
ms.openlocfilehash: 6797af44c3aaa6653c440b3d53a282d8c90a4381
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459523"
---
# <a name="getappmarketplaceurl-operation"></a><span data-ttu-id="eda61-103">GetAppMarketplaceUrl 操作</span><span class="sxs-lookup"><span data-stu-id="eda61-103">GetAppMarketplaceUrl operation</span></span>

<span data-ttu-id="eda61-104">查找有关**GetAppMarketplaceUrl** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="eda61-104">Find information about the **GetAppMarketplaceUrl** EWS operation.</span></span> 
  
<span data-ttu-id="eda61-105">**GetAppMarketplaceUrl**操作检索应用程序市场的 URL，客户端可以访问该 URL 以获取要安装在邮箱中的应用程序。</span><span class="sxs-lookup"><span data-stu-id="eda61-105">The **GetAppMarketplaceUrl** operation retrieves the URL for the app marketplace that a client can visit to acquire apps to install in a mailbox.</span></span> 
  
<span data-ttu-id="eda61-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="eda61-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getappmarketplaceurl-operation"></a><span data-ttu-id="eda61-107">使用 GetAppMarketplaceUrl 操作</span><span class="sxs-lookup"><span data-stu-id="eda61-107">Using the GetAppMarketplaceUrl operation</span></span>

<span data-ttu-id="eda61-108">**GetAppMarketplaceUrl**操作不采用任何参数来请求客户端可以从中安装应用程序的 MARKETPLACE 的 URL。</span><span class="sxs-lookup"><span data-stu-id="eda61-108">The **GetAppMarketplaceUrl** operation does not take any arguments to request the URL for the marketplace from which a client can install apps.</span></span> <span data-ttu-id="eda61-109">响应将包含指向应用市场的 URL。</span><span class="sxs-lookup"><span data-stu-id="eda61-109">The response will contain a URL to the app marketplace.</span></span> 
  
### <a name="getappmarketplaceurl-operation-soap-headers"></a><span data-ttu-id="eda61-110">GetAppMarketplaceUrl 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="eda61-110">GetAppMarketplaceUrl operation SOAP headers</span></span>

<span data-ttu-id="eda61-111">**GetAppMarketplaceUrl**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="eda61-111">The **GetAppMarketplaceUrl** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="eda61-112">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="eda61-112">**Header name**</span></span>|<span data-ttu-id="eda61-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="eda61-113">**Element**</span></span>|<span data-ttu-id="eda61-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="eda61-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="eda61-115">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="eda61-115">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="eda61-116">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="eda61-116">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="eda61-117">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="eda61-117">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="eda61-118">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="eda61-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="eda61-119">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="eda61-119">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="eda61-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="eda61-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="eda61-121">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="eda61-121">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="eda61-122">此标头适用于响应。</span><span class="sxs-lookup"><span data-stu-id="eda61-122">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getappmarketplaceurl-operation-request-example-get-the-app-marketplace-url-for-a-mailbox"></a><span data-ttu-id="eda61-123">GetAppMarketplaceUrl 操作请求示例：获取邮箱的应用程序市场 URL</span><span class="sxs-lookup"><span data-stu-id="eda61-123">GetAppMarketplaceUrl operation request example: Get the app marketplace URL for a mailbox</span></span>

<span data-ttu-id="eda61-124">以下示例的**GetAppMarketplaceUrl**操作请求显示如何获取邮箱的应用程序市场 URL。</span><span class="sxs-lookup"><span data-stu-id="eda61-124">The following example of a **GetAppMarketplaceUrl** operation request shows how to get the app marketplace URL for a mailbox.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013_SP1" />
      <t:MailboxCulture>en-US</t:MailboxCulture>
      <t:TimeZoneContext>
         <t:TimeZoneDefinition Id="GMT Standard Time"/>
      </t:TimeZoneContext>
   </soap:Header>
   <soap:Body >
      <m:GetAppMarketplaceUrl>
        <m:ApiVersionSupported>1.0</m:ApiVersionSupported>
        <m:SchemaVersionSupported>1.0</m:SchemaVersionSupported>
      </m:GetAppMarketplaceUrl>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="eda61-125">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="eda61-125">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="eda61-126">GetAppMarketplaceUrl</span><span class="sxs-lookup"><span data-stu-id="eda61-126">GetAppMarketplaceUrl</span></span>](getappmarketplaceurl.md)
    
- [<span data-ttu-id="eda61-127">ApiVersionSupported</span><span class="sxs-lookup"><span data-stu-id="eda61-127">ApiVersionSupported</span></span>](apiversionsupported.md)
    
- [<span data-ttu-id="eda61-128">SchemaVersionSupported</span><span class="sxs-lookup"><span data-stu-id="eda61-128">SchemaVersionSupported</span></span>](schemaversionsupported.md)
    
## <a name="successful-getappmarketplaceurl-operation-response"></a><span data-ttu-id="eda61-129">成功的 GetAppMarketplaceUrl 操作响应</span><span class="sxs-lookup"><span data-stu-id="eda61-129">Successful GetAppMarketplaceUrl operation response</span></span>

<span data-ttu-id="eda61-130">下面的示例演示对**GetAppMarketplaceUrl**操作请求的成功响应，以获取邮箱的应用程序市场 URL。</span><span class="sxs-lookup"><span data-stu-id="eda61-130">The following example shows a successful response to a **GetAppMarketplaceUrl** operation request to get the app marketplace URL for a mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="eda61-131">应用程序市场 URL 已更改，以保留可读性。</span><span class="sxs-lookup"><span data-stu-id="eda61-131">The app marketplace URL has been altered to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="918" 
                           MinorBuildNumber="7" 
                           Version="V2_10" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetAppMarketplaceUrlResponse ResponseClass="Success" 
                                    xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <AppMarketplaceUrl>http://marketplace.contoso.com</AppMarketplaceUrl>
      </GetAppMarketplaceUrlResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="eda61-132">响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="eda61-132">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="eda61-133">GetAppMarketplaceUrlResponse</span><span class="sxs-lookup"><span data-stu-id="eda61-133">GetAppMarketplaceUrlResponse</span></span>](getappmarketplaceurlresponse.md)
    
- [<span data-ttu-id="eda61-134">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="eda61-134">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="eda61-135">AppMarketplaceUrl</span><span class="sxs-lookup"><span data-stu-id="eda61-135">AppMarketplaceUrl</span></span>](appmarketplaceurl.md)
    
## <a name="getappmarketplaceurl-operation-error-response"></a><span data-ttu-id="eda61-136">GetAppMarketPlaceUrl 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="eda61-136">GetAppMarketPlaceUrl operation error response</span></span>

<span data-ttu-id="eda61-137">为此操作返回的错误是与不正确的服务配置相关的，也可能是一般性的 EWS 错误。</span><span class="sxs-lookup"><span data-stu-id="eda61-137">Errors returned for this operation are either related to an incorrect service configuration or are generic EWS errors.</span></span> <span data-ttu-id="eda61-138">有关对 EWS 通用的错误代码以及特定于此操作的错误代码，请参阅[ResponseCode](responsecode.md)。</span><span class="sxs-lookup"><span data-stu-id="eda61-138">For error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span> 
  
<span data-ttu-id="eda61-139">下面的示例演示在未配置外部 Exchange 控制面板（ECP）时返回的错误响应。</span><span class="sxs-lookup"><span data-stu-id="eda61-139">The following example shows an error response that is returned when external Exchange Control Panel (ECP) is not configured.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="918" 
                           MinorBuildNumber="7" 
                           Version="V2_10" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetAppMarketplaceUrlResponse ResponseClass="Error" 
                                    xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Cannot get external ECP URL. This might happen if external ECP URL isn't configured.</MessageText>
         <ResponseCode>ErrorCannotGetExternalEcpUrl</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </GetAppMarketplaceUrlResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="eda61-140">错误响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="eda61-140">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="eda61-141">GetAppMarketplaceUrlResponse</span><span class="sxs-lookup"><span data-stu-id="eda61-141">GetAppMarketplaceUrlResponse</span></span>](getappmarketplaceurlresponse.md)
    
- [<span data-ttu-id="eda61-142">MessageText</span><span class="sxs-lookup"><span data-stu-id="eda61-142">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="eda61-143">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="eda61-143">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="eda61-144">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="eda61-144">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="eda61-145">另请参阅</span><span class="sxs-lookup"><span data-stu-id="eda61-145">See also</span></span>

- [<span data-ttu-id="eda61-146">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="eda61-146">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="eda61-147">DisableApp 操作</span><span class="sxs-lookup"><span data-stu-id="eda61-147">DisableApp operation</span></span>](disableapp-operation.md)
    
- [<span data-ttu-id="eda61-148">InstallApp 操作</span><span class="sxs-lookup"><span data-stu-id="eda61-148">InstallApp operation</span></span>](installapp-operation.md)
    
- [<span data-ttu-id="eda61-149">UninstallApp 操作</span><span class="sxs-lookup"><span data-stu-id="eda61-149">UninstallApp operation</span></span>](uninstallapp-operation.md)
    
- [<span data-ttu-id="eda61-150">Getappmanifests 已操作</span><span class="sxs-lookup"><span data-stu-id="eda61-150">GetAppManifests operation</span></span>](getappmanifests-operation.md)
    

