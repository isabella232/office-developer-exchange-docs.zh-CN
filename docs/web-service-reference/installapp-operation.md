---
title: InstallApp 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 596eae95-3e78-489a-8bb2-d2dd4a026405
description: 查找信息 InstallApp EWS 操作。
ms.openlocfilehash: ccc5d2dde949070bae905ff1ebb182c892f07fcb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825951"
---
# <a name="installapp-operation"></a><span data-ttu-id="5f0b6-103">InstallApp 操作</span><span class="sxs-lookup"><span data-stu-id="5f0b6-103">InstallApp operation</span></span>

<span data-ttu-id="5f0b6-104">查找有关**InstallApp** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="5f0b6-104">Find information about the **InstallApp** EWS operation.</span></span> 
  
<span data-ttu-id="5f0b6-105">**InstallApp**操作的邮箱中的 Outlook 安装邮件应用程序。</span><span class="sxs-lookup"><span data-stu-id="5f0b6-105">The **InstallApp** operation installs a mail app for Outlook in a mailbox.</span></span> 
  
<span data-ttu-id="5f0b6-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="5f0b6-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-installapp-operation"></a><span data-ttu-id="5f0b6-107">使用 InstallApp 操作</span><span class="sxs-lookup"><span data-stu-id="5f0b6-107">Using the InstallApp operation</span></span>

<span data-ttu-id="5f0b6-108">**InstallApp**操作所需的单个参数，标识用于安装的邮件应用程序。</span><span class="sxs-lookup"><span data-stu-id="5f0b6-108">The **InstallApp** operation takes a single argument that identifies a mail app to install.</span></span> <span data-ttu-id="5f0b6-109">参数包含 base64 编码的邮件应用程序清单。</span><span class="sxs-lookup"><span data-stu-id="5f0b6-109">The argument contains the base64-encoded manifest for a mail app.</span></span> 
  
### <a name="installapp-operation-soap-headers"></a><span data-ttu-id="5f0b6-110">InstallApp 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="5f0b6-110">InstallApp operation SOAP headers</span></span>

<span data-ttu-id="5f0b6-111">**InstallApp**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="5f0b6-111">The **InstallApp** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="5f0b6-112">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="5f0b6-112">**Header name**</span></span>|<span data-ttu-id="5f0b6-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="5f0b6-113">**Element**</span></span>|<span data-ttu-id="5f0b6-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="5f0b6-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5f0b6-115">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="5f0b6-115">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="5f0b6-116">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="5f0b6-116">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="5f0b6-117">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="5f0b6-117">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="5f0b6-118">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="5f0b6-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="5f0b6-119">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="5f0b6-119">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="5f0b6-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="5f0b6-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="5f0b6-121">标识响应该请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="5f0b6-121">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="5f0b6-122">适用于响应此标头。</span><span class="sxs-lookup"><span data-stu-id="5f0b6-122">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="installapp-operation-request-example-install-a-mail-app-in-a-mailbox"></a><span data-ttu-id="5f0b6-123">InstallApp 操作请求示例： 在邮箱中安装邮件应用程序</span><span class="sxs-lookup"><span data-stu-id="5f0b6-123">InstallApp operation request example: Install a mail app in a mailbox</span></span>

<span data-ttu-id="5f0b6-124">**InstallApp**操作请求的下面的示例演示如何安装 Outlook 邮件应用程序。</span><span class="sxs-lookup"><span data-stu-id="5f0b6-124">The following example of an **InstallApp** operation request shows how to install a mail app for Outlook.</span></span> <span data-ttu-id="5f0b6-125">可以通过使用[GetAppManifests 操作](getappmanifests-operation.md)找到应用程序清单。</span><span class="sxs-lookup"><span data-stu-id="5f0b6-125">The app manifest can be found by using the [GetAppManifests operation](getappmanifests-operation.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="5f0b6-126">Base64 编码的应用程序清单已被任意截断以保留可读性和不代表一个有效的清单。</span><span class="sxs-lookup"><span data-stu-id="5f0b6-126">The base64-encoded app manifest has been arbitrarily truncated to preserve readability and does not represent a valid manifest.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="5f0b6-127">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="5f0b6-127">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="5f0b6-128">InstallApp</span><span class="sxs-lookup"><span data-stu-id="5f0b6-128">InstallApp</span></span>](installapp.md)
    
- [<span data-ttu-id="5f0b6-129">Manifest</span><span class="sxs-lookup"><span data-stu-id="5f0b6-129">Manifest</span></span>](manifest.md)
    
## <a name="successful-installapp-operation-response"></a><span data-ttu-id="5f0b6-130">成功 InstallApp 操作响应</span><span class="sxs-lookup"><span data-stu-id="5f0b6-130">Successful InstallApp operation response</span></span>

<span data-ttu-id="5f0b6-131">下面的示例演示安装邮件应用程序的**InstallApp**操作请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="5f0b6-131">The following example shows a successful response to an **InstallApp** operation request to install a mail app.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="14" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <InstallAppResponse ResponseClass="Success" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </InstallAppResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="5f0b6-132">响应 SOAP 正文中包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="5f0b6-132">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="5f0b6-133">InstallAppResponse</span><span class="sxs-lookup"><span data-stu-id="5f0b6-133">InstallAppResponse</span></span>](installappresponse.md)
    
- [<span data-ttu-id="5f0b6-134">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="5f0b6-134">ResponseCode</span></span>](responsecode.md)
    
## <a name="installapp-operation-error-response"></a><span data-ttu-id="5f0b6-135">InstallApp 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="5f0b6-135">InstallApp operation error response</span></span>

<span data-ttu-id="5f0b6-136">下面的示例演示**InstallApp**操作请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="5f0b6-136">The following example shows an error response to an **InstallApp** operation request.</span></span> <span data-ttu-id="5f0b6-137">这是包含清单无效请求的响应。</span><span class="sxs-lookup"><span data-stu-id="5f0b6-137">This is a response to a request that contains an invalid manifest.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="14" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <InstallAppResponse ResponseClass="Error" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>This app can't be installed. Missing OfficeApp element.</MessageText>
         <ResponseCode>ErrorInternalServerError</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </InstallAppResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="5f0b6-138">错误响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="5f0b6-138">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="5f0b6-139">InstallAppResponse</span><span class="sxs-lookup"><span data-stu-id="5f0b6-139">InstallAppResponse</span></span>](installappresponse.md)
    
- [<span data-ttu-id="5f0b6-140">MessageText</span><span class="sxs-lookup"><span data-stu-id="5f0b6-140">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="5f0b6-141">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="5f0b6-141">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="5f0b6-142">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="5f0b6-142">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="5f0b6-143">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5f0b6-143">See also</span></span>

- [<span data-ttu-id="5f0b6-144">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="5f0b6-144">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="5f0b6-145">DisableApp 操作</span><span class="sxs-lookup"><span data-stu-id="5f0b6-145">DisableApp operation</span></span>](disableapp-operation.md)
    
- [<span data-ttu-id="5f0b6-146">UninstallApp 操作</span><span class="sxs-lookup"><span data-stu-id="5f0b6-146">UninstallApp operation</span></span>](uninstallapp-operation.md)
    
- [<span data-ttu-id="5f0b6-147">GetAppManifests</span><span class="sxs-lookup"><span data-stu-id="5f0b6-147">GetAppManifests</span></span>](getappmanifests.md)
    
- [<span data-ttu-id="5f0b6-148">GetAppMarketplaceUrl 操作</span><span class="sxs-lookup"><span data-stu-id="5f0b6-148">GetAppMarketplaceUrl operation</span></span>](getappmarketplaceurl-operation.md)
    

