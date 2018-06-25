---
title: UninstallApp 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7707aa6a-381d-43f7-a454-54f6343ed127
description: 查找信息 UninstallApp EWS 操作。
ms.openlocfilehash: 4f44224651993023336eef5540ec29b7f6a6e32e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838320"
---
# <a name="uninstallapp-operation"></a><span data-ttu-id="d0615-103">UninstallApp 操作</span><span class="sxs-lookup"><span data-stu-id="d0615-103">UninstallApp operation</span></span>

<span data-ttu-id="d0615-104">查找有关**UninstallApp** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="d0615-104">Find information about the **UninstallApp** EWS operation.</span></span> 
  
<span data-ttu-id="d0615-105">**UninstallApp**操作卸载 outlook 邮件应用程序。</span><span class="sxs-lookup"><span data-stu-id="d0615-105">The **UninstallApp** operation uninstalls a mail app for Outlook.</span></span> 
  
<span data-ttu-id="d0615-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="d0615-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-uninstallapp-operation"></a><span data-ttu-id="d0615-107">使用 UninstallApp 操作</span><span class="sxs-lookup"><span data-stu-id="d0615-107">Using the UninstallApp operation</span></span>

<span data-ttu-id="d0615-108">**UninstallApp**操作请求中的标识邮件应用程序卸载采用一个参数。</span><span class="sxs-lookup"><span data-stu-id="d0615-108">The **UninstallApp** operation takes one argument in the request that identifies the mail app to uninstall.</span></span> 
  
### <a name="uninstallapp-operation-soap-headers"></a><span data-ttu-id="d0615-109">UninstallApp 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="d0615-109">UninstallApp operation SOAP headers</span></span>

<span data-ttu-id="d0615-110">**UninstallApp**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="d0615-110">The **UninstallApp** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="d0615-111">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="d0615-111">**Header name**</span></span>|<span data-ttu-id="d0615-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="d0615-112">**Element**</span></span>|<span data-ttu-id="d0615-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="d0615-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d0615-114">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="d0615-114">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="d0615-115">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="d0615-115">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="d0615-116">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="d0615-116">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="d0615-117">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="d0615-117">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="d0615-118">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="d0615-118">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="d0615-119">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="d0615-119">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="d0615-120">标识响应该请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="d0615-120">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="d0615-121">适用于响应此标头。</span><span class="sxs-lookup"><span data-stu-id="d0615-121">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="uninstallapp-operation-request-example-uninstall-a-mail-app-in-a-mailbox"></a><span data-ttu-id="d0615-122">UninstallApp 操作请求示例： 卸载邮箱中的邮件应用程序</span><span class="sxs-lookup"><span data-stu-id="d0615-122">UninstallApp operation request example: Uninstall a mail app in a mailbox</span></span>

<span data-ttu-id="d0615-123">下面的示例**UninstallApp**操作的请求显示如何向卸载邮件应用程序使用的应用程序标识符。</span><span class="sxs-lookup"><span data-stu-id="d0615-123">The following example of an **UninstallApp** operation request shows how to a uninstall a mail app by using the app identifier.</span></span> <span data-ttu-id="d0615-124">可以由[GetAppManifests 操作](getappmanifests-operation.md)返回应用程序清单中找到应用程序标识符。</span><span class="sxs-lookup"><span data-stu-id="d0615-124">The app identifier can be found in the app manifest that is returned by the [GetAppManifests operation](getappmanifests-operation.md).</span></span>
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:UninstallApp>
         <m:ID>1C50226D-04B5-4AB2-9FCD-42E236B59E4B</m:ID>
      </m:UninstallApp>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="d0615-125">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="d0615-125">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="d0615-126">UninstallApp</span><span class="sxs-lookup"><span data-stu-id="d0615-126">UninstallApp</span></span>](uninstallapp.md)
    
- [<span data-ttu-id="d0615-127">ID （字符串）</span><span class="sxs-lookup"><span data-stu-id="d0615-127">ID (String)</span></span>](id-string.md)
    
## <a name="successful-uninstallapp-operation-response"></a><span data-ttu-id="d0615-128">成功 UninstallApp 操作响应</span><span class="sxs-lookup"><span data-stu-id="d0615-128">Successful UninstallApp operation response</span></span>

<span data-ttu-id="d0615-129">下面的示例演示对**UninstallApp**操作请求卸载邮件应用程序的成功响应。</span><span class="sxs-lookup"><span data-stu-id="d0615-129">The following example shows a successful response to an **UninstallApp** operation request to uninstall a mail app.</span></span> 
  
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
      <UninstallAppResponse ResponseClass="Success" 
                            xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </UninstallAppResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="d0615-130">响应 SOAP 正文中包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="d0615-130">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="d0615-131">UninstallAppResponse</span><span class="sxs-lookup"><span data-stu-id="d0615-131">UninstallAppResponse</span></span>](uninstallappresponse.md)
    
- [<span data-ttu-id="d0615-132">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d0615-132">ResponseCode</span></span>](responsecode.md)
    
## <a name="uninstallapp-operation-error-response"></a><span data-ttu-id="d0615-133">UninstallApp 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="d0615-133">UninstallApp operation error response</span></span>

<span data-ttu-id="d0615-134">下面的示例演示**UninstallApp**操作请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="d0615-134">The following example shows an error response to an **UninstallApp** operation request.</span></span> <span data-ttu-id="d0615-135">这是卸载已卸载的邮件应用程序请求的响应。</span><span class="sxs-lookup"><span data-stu-id="d0615-135">This is a response to a request to uninstall a mail app that has already been uninstalled.</span></span> 
  
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
      <UninstallAppResponse ResponseClass="Error" 
                            xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Extension ID 1c50226d-04b5-4ab2-9fcd-42e236b59e4b can't be found.</MessageText>
         <ResponseCode>ErrorInternalServerError</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </UninstallAppResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="d0615-136">错误响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="d0615-136">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="d0615-137">UninstallAppResponse</span><span class="sxs-lookup"><span data-stu-id="d0615-137">UninstallAppResponse</span></span>](uninstallappresponse.md)
    
- [<span data-ttu-id="d0615-138">MessageText</span><span class="sxs-lookup"><span data-stu-id="d0615-138">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="d0615-139">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d0615-139">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="d0615-140">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="d0615-140">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="d0615-141">通用到 EWS 且特定于此操作的其他错误代码，请参阅[ResponseCode](responsecode.md)。</span><span class="sxs-lookup"><span data-stu-id="d0615-141">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d0615-142">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d0615-142">See also</span></span>

- [<span data-ttu-id="d0615-143">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="d0615-143">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="d0615-144">InstallApp 操作</span><span class="sxs-lookup"><span data-stu-id="d0615-144">InstallApp operation</span></span>](installapp-operation.md)
    
- [<span data-ttu-id="d0615-145">DisableApp 操作</span><span class="sxs-lookup"><span data-stu-id="d0615-145">DisableApp operation</span></span>](disableapp-operation.md)
    
- [<span data-ttu-id="d0615-146">GetAppManifests</span><span class="sxs-lookup"><span data-stu-id="d0615-146">GetAppManifests</span></span>](getappmanifests.md)
    
- [<span data-ttu-id="d0615-147">GetAppMarketplaceUrl 操作</span><span class="sxs-lookup"><span data-stu-id="d0615-147">GetAppMarketplaceUrl operation</span></span>](getappmarketplaceurl-operation.md)
    

