---
title: Getappmanifests 已操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 21a4987c-c24d-4a6e-ace4-e81edcda6303
description: 查找有关 Getappmanifests 已 EWS 操作的信息。
ms.openlocfilehash: 4d4c1d32f14cf144335ddfdf8c9cd4c88a4421d0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463004"
---
# <a name="getappmanifests-operation"></a><span data-ttu-id="e22c1-103">Getappmanifests 已操作</span><span class="sxs-lookup"><span data-stu-id="e22c1-103">GetAppManifests operation</span></span>

<span data-ttu-id="e22c1-104">查找有关**getappmanifests 已**EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="e22c1-104">Find information about the **GetAppManifests** EWS operation.</span></span> 
  
<span data-ttu-id="e22c1-105">**Getappmanifests 已**操作检索应用程序清单。</span><span class="sxs-lookup"><span data-stu-id="e22c1-105">The **GetAppManifests** operation retrieves app manifests.</span></span> 
  
<span data-ttu-id="e22c1-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="e22c1-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getappmanifests-operation"></a><span data-ttu-id="e22c1-107">使用 Getappmanifests 已操作</span><span class="sxs-lookup"><span data-stu-id="e22c1-107">Using the GetAppManifests operation</span></span>

<span data-ttu-id="e22c1-108">**Getappmanifests 已**操作不采用任何参数来请求邮箱的应用程序清单。</span><span class="sxs-lookup"><span data-stu-id="e22c1-108">The **GetAppManifests** operation does not take any arguments to request the app manifests for a mailbox.</span></span> <span data-ttu-id="e22c1-109">响应将包含在邮箱中安装的每个应用程序的 base64 编码的 XML 清单文件。</span><span class="sxs-lookup"><span data-stu-id="e22c1-109">The response will contain base64-encoded XML manifest files for each app that is installed in a mailbox.</span></span> 
  
### <a name="getappmanifests-operation-soap-headers"></a><span data-ttu-id="e22c1-110">Getappmanifests 已操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="e22c1-110">GetAppManifests operation SOAP headers</span></span>

<span data-ttu-id="e22c1-111">**Getappmanifests 已**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="e22c1-111">The **GetAppManifests** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="e22c1-112">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="e22c1-112">**Header name**</span></span>|<span data-ttu-id="e22c1-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="e22c1-113">**Element**</span></span>|<span data-ttu-id="e22c1-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="e22c1-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e22c1-115">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="e22c1-115">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="e22c1-116">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="e22c1-116">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="e22c1-117">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="e22c1-117">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="e22c1-118">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="e22c1-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="e22c1-119">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="e22c1-119">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="e22c1-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="e22c1-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="e22c1-121">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="e22c1-121">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="e22c1-122">此标头适用于响应。</span><span class="sxs-lookup"><span data-stu-id="e22c1-122">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getappmanifests-operation-request-example-get-the-app-manifests-for-a-mailbox"></a><span data-ttu-id="e22c1-123">Getappmanifests 已操作请求示例：获取邮箱的应用程序清单</span><span class="sxs-lookup"><span data-stu-id="e22c1-123">GetAppManifests operation request example: Get the app manifests for a mailbox</span></span>

<span data-ttu-id="e22c1-124">下面的**getappmanifests 已**操作请求示例演示如何获取邮箱的应用程序清单。</span><span class="sxs-lookup"><span data-stu-id="e22c1-124">The following example of a **GetAppManifests** operation request shows how to get the app manifests for a mailbox.</span></span> <span data-ttu-id="e22c1-125">[ApiVersionSupported](apiversionsupported.md)元素和[SchemaVersionSupported](schemaversionsupported.md)元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="e22c1-125">The [ApiVersionSupported](apiversionsupported.md) element and the [SchemaVersionSupported](schemaversionsupported.md) element are optional.</span></span> 
  
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
      <m:GetAppManifests>
        <m:ApiVersionSupported>1.1</m:ApiVersionSupported>
        <m:SchemaVersionSupported>1.1</m:SchemaVersionSupported>
      </m:GetAppManifests>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="e22c1-126">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="e22c1-126">The request SOAP body contains the following element:</span></span>
  
- [<span data-ttu-id="e22c1-127">Getappmanifests 已</span><span class="sxs-lookup"><span data-stu-id="e22c1-127">GetAppManifests</span></span>](getappmanifests.md)
    
- [<span data-ttu-id="e22c1-128">ApiVersionSupported</span><span class="sxs-lookup"><span data-stu-id="e22c1-128">ApiVersionSupported</span></span>](apiversionsupported.md)
    
- [<span data-ttu-id="e22c1-129">SchemaVersionSupported</span><span class="sxs-lookup"><span data-stu-id="e22c1-129">SchemaVersionSupported</span></span>](schemaversionsupported.md)
    
## <a name="successful-getappmanifests-operation-response"></a><span data-ttu-id="e22c1-130">成功的 Getappmanifests 已操作响应</span><span class="sxs-lookup"><span data-stu-id="e22c1-130">Successful GetAppManifests operation response</span></span>

<span data-ttu-id="e22c1-131">下面的示例演示对**getappmanifests 已**操作请求的成功响应，以获取邮箱的应用程序清单。</span><span class="sxs-lookup"><span data-stu-id="e22c1-131">The following example shows a successful response to a **GetAppManifests** operation request to get the app manifests for a mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e22c1-132">已随意截断所有 base64 应用清单以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="e22c1-132">All base64 app manifests have been arbitrarily truncated to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="918" 
                           MinorBuildNumber="07" 
                           Version="V2_10" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetAppManifestsResponse ResponseClass="Success" 
                               xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <m:Apps xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
          <t:App xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
            <t:Manifest>WNlQXBwPg==</t:Manifest>
          </t:App>
         </m:Apps>
      </GetAppManifestsResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="e22c1-133">响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="e22c1-133">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="e22c1-134">GetAppManifestsResponse</span><span class="sxs-lookup"><span data-stu-id="e22c1-134">GetAppManifestsResponse</span></span>](getappmanifestsresponse.md)
    
- [<span data-ttu-id="e22c1-135">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e22c1-135">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="e22c1-136">应用</span><span class="sxs-lookup"><span data-stu-id="e22c1-136">Apps</span></span>](apps.md)
    
- [<span data-ttu-id="e22c1-137">App</span><span class="sxs-lookup"><span data-stu-id="e22c1-137">App</span></span>](app.md)
    
- [<span data-ttu-id="e22c1-138">清单</span><span class="sxs-lookup"><span data-stu-id="e22c1-138">Manifest</span></span>](manifest.md)
    
<span data-ttu-id="e22c1-139">响应 SOAP 正文还可以包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="e22c1-139">The response SOAP body can also contain the following element:</span></span>
  
- [<span data-ttu-id="e22c1-140">清单</span><span class="sxs-lookup"><span data-stu-id="e22c1-140">Manifests</span></span>](manifests.md)
    
## <a name="getappmanifests-operation-error-response"></a><span data-ttu-id="e22c1-141">Getappmanifests 已操作错误响应</span><span class="sxs-lookup"><span data-stu-id="e22c1-141">GetAppManifests operation error response</span></span>

<span data-ttu-id="e22c1-142">为此操作返回的错误与输入参数的无效格式或为常规的 EWS 错误相关。</span><span class="sxs-lookup"><span data-stu-id="e22c1-142">Errors returned for this operation are related to an invalid format of the input parameters or are generic EWS errors.</span></span> <span data-ttu-id="e22c1-143">有关对 EWS 通用的错误代码以及特定于此操作的错误代码，请参阅[ResponseCode](responsecode.md)。</span><span class="sxs-lookup"><span data-stu-id="e22c1-143">For error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
```
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <ServerVersionInfo MajorVersion="15"
                       MinorVersion="0"
                       MajorBuildNumber="918"
                       MinorBuildNumber="07"
                       Version="V2_10"
                       xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetAppManifestsResponse ResponseClass="Error"
                             xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <MessageText>The apiVersionSupported parameter is invalid. 
                   It should be in the form of major version, minor 
                   version, separated by '.', for example '2.34'.</MessageText>
      <ResponseCode>ErrorInvalidRequest</ResponseCode>
      <DescriptiveLinkKey>0</DescriptiveLinkKey>
    </GetAppManifestsResponse>
  </s:Body>
</s:Envelope>

```

## <a name="see-also"></a><span data-ttu-id="e22c1-144">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e22c1-144">See also</span></span>

- [<span data-ttu-id="e22c1-145">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="e22c1-145">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="e22c1-146">DisableApp 操作</span><span class="sxs-lookup"><span data-stu-id="e22c1-146">DisableApp operation</span></span>](disableapp-operation.md)
    
- [<span data-ttu-id="e22c1-147">InstallApp 操作</span><span class="sxs-lookup"><span data-stu-id="e22c1-147">InstallApp operation</span></span>](installapp-operation.md)
    
- [<span data-ttu-id="e22c1-148">UninstallApp 操作</span><span class="sxs-lookup"><span data-stu-id="e22c1-148">UninstallApp operation</span></span>](uninstallapp-operation.md)
    
- [<span data-ttu-id="e22c1-149">GetAppMarketplaceUrl 操作</span><span class="sxs-lookup"><span data-stu-id="e22c1-149">GetAppMarketplaceUrl operation</span></span>](getappmarketplaceurl-operation.md)
    

