---
title: InstallApp 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 596eae95-3e78-489a-8bb2-d2dd4a026405
description: 查找有关 InstallApp EWS 操作的信息。
ms.openlocfilehash: ae6aab7f7176aa827bafa9abf1aa67d458d309d2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465686"
---
# <a name="installapp-operation"></a><span data-ttu-id="50144-103">InstallApp 操作</span><span class="sxs-lookup"><span data-stu-id="50144-103">InstallApp operation</span></span>

<span data-ttu-id="50144-104">查找有关**InstallApp** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="50144-104">Find information about the **InstallApp** EWS operation.</span></span> 
  
<span data-ttu-id="50144-105">**InstallApp**操作将为 Outlook 在邮箱中安装邮件应用程序。</span><span class="sxs-lookup"><span data-stu-id="50144-105">The **InstallApp** operation installs a mail app for Outlook in a mailbox.</span></span> 
  
<span data-ttu-id="50144-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="50144-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-installapp-operation"></a><span data-ttu-id="50144-107">使用 InstallApp 操作</span><span class="sxs-lookup"><span data-stu-id="50144-107">Using the InstallApp operation</span></span>

<span data-ttu-id="50144-108">**InstallApp**操作采用一个标识要安装的邮件应用程序的参数。</span><span class="sxs-lookup"><span data-stu-id="50144-108">The **InstallApp** operation takes a single argument that identifies a mail app to install.</span></span> <span data-ttu-id="50144-109">参数包含邮件应用程序的 base64 编码的清单。</span><span class="sxs-lookup"><span data-stu-id="50144-109">The argument contains the base64-encoded manifest for a mail app.</span></span> 
  
### <a name="installapp-operation-soap-headers"></a><span data-ttu-id="50144-110">InstallApp 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="50144-110">InstallApp operation SOAP headers</span></span>

<span data-ttu-id="50144-111">**InstallApp**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="50144-111">The **InstallApp** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="50144-112">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="50144-112">**Header name**</span></span>|<span data-ttu-id="50144-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="50144-113">**Element**</span></span>|<span data-ttu-id="50144-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="50144-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="50144-115">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="50144-115">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="50144-116">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="50144-116">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="50144-117">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="50144-117">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="50144-118">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="50144-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="50144-119">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="50144-119">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="50144-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="50144-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="50144-121">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="50144-121">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="50144-122">此标头适用于响应。</span><span class="sxs-lookup"><span data-stu-id="50144-122">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="installapp-operation-request-example-install-a-mail-app-in-a-mailbox"></a><span data-ttu-id="50144-123">InstallApp 操作请求示例：在邮箱中安装邮件应用程序</span><span class="sxs-lookup"><span data-stu-id="50144-123">InstallApp operation request example: Install a mail app in a mailbox</span></span>

<span data-ttu-id="50144-124">下面的**InstallApp**操作请求示例演示如何为 Outlook 安装邮件应用程序。</span><span class="sxs-lookup"><span data-stu-id="50144-124">The following example of an **InstallApp** operation request shows how to install a mail app for Outlook.</span></span> <span data-ttu-id="50144-125">可以通过使用[getappmanifests 已操作](getappmanifests-operation.md)找到应用程序清单。</span><span class="sxs-lookup"><span data-stu-id="50144-125">The app manifest can be found by using the [GetAppManifests operation](getappmanifests-operation.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="50144-126">Base64 编码的应用程序清单已被随意截断以保留可读性，并且不代表有效的清单。</span><span class="sxs-lookup"><span data-stu-id="50144-126">The base64-encoded app manifest has been arbitrarily truncated to preserve readability and does not represent a valid manifest.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:InstallApp>
         <m:Manifest>TUwiIC8+CiAgPC9SdWxlPgo8L09mZmljZUFwcD4=</m:Manifest>
      </m:InstallApp>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="50144-127">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="50144-127">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="50144-128">InstallApp</span><span class="sxs-lookup"><span data-stu-id="50144-128">InstallApp</span></span>](installapp.md)
    
- [<span data-ttu-id="50144-129">清单</span><span class="sxs-lookup"><span data-stu-id="50144-129">Manifest</span></span>](manifest.md)
    
## <a name="successful-installapp-operation-response"></a><span data-ttu-id="50144-130">成功的 InstallApp 操作响应</span><span class="sxs-lookup"><span data-stu-id="50144-130">Successful InstallApp operation response</span></span>

<span data-ttu-id="50144-131">下面的示例演示对**InstallApp**操作请求的成功响应，以安装邮件应用程序。</span><span class="sxs-lookup"><span data-stu-id="50144-131">The following example shows a successful response to an **InstallApp** operation request to install a mail app.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="14" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <InstallAppResponse ResponseClass="Success" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </InstallAppResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="50144-132">响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="50144-132">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="50144-133">InstallAppResponse</span><span class="sxs-lookup"><span data-stu-id="50144-133">InstallAppResponse</span></span>](installappresponse.md)
    
- [<span data-ttu-id="50144-134">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="50144-134">ResponseCode</span></span>](responsecode.md)
    
## <a name="installapp-operation-error-response"></a><span data-ttu-id="50144-135">InstallApp 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="50144-135">InstallApp operation error response</span></span>

<span data-ttu-id="50144-136">下面的示例演示对**InstallApp**操作请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="50144-136">The following example shows an error response to an **InstallApp** operation request.</span></span> <span data-ttu-id="50144-137">这是对包含无效清单的请求的响应。</span><span class="sxs-lookup"><span data-stu-id="50144-137">This is a response to a request that contains an invalid manifest.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="14" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <InstallAppResponse ResponseClass="Error" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>This app can't be installed. Missing OfficeApp element.</MessageText>
         <ResponseCode>ErrorInternalServerError</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </InstallAppResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="50144-138">错误响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="50144-138">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="50144-139">InstallAppResponse</span><span class="sxs-lookup"><span data-stu-id="50144-139">InstallAppResponse</span></span>](installappresponse.md)
    
- [<span data-ttu-id="50144-140">MessageText</span><span class="sxs-lookup"><span data-stu-id="50144-140">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="50144-141">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="50144-141">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="50144-142">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="50144-142">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="50144-143">另请参阅</span><span class="sxs-lookup"><span data-stu-id="50144-143">See also</span></span>

- [<span data-ttu-id="50144-144">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="50144-144">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="50144-145">DisableApp 操作</span><span class="sxs-lookup"><span data-stu-id="50144-145">DisableApp operation</span></span>](disableapp-operation.md)
    
- [<span data-ttu-id="50144-146">UninstallApp 操作</span><span class="sxs-lookup"><span data-stu-id="50144-146">UninstallApp operation</span></span>](uninstallapp-operation.md)
    
- [<span data-ttu-id="50144-147">Getappmanifests 已</span><span class="sxs-lookup"><span data-stu-id="50144-147">GetAppManifests</span></span>](getappmanifests.md)
    
- [<span data-ttu-id="50144-148">GetAppMarketplaceUrl 操作</span><span class="sxs-lookup"><span data-stu-id="50144-148">GetAppMarketplaceUrl operation</span></span>](getappmarketplaceurl-operation.md)
    

