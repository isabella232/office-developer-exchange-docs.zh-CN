---
title: DisableApp 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 211731a3-2470-49af-bda3-1ddfc15a8e46
description: 查找信息 DisableApp EWS 操作。
ms.openlocfilehash: be9e124d7464012ffa797a69192893d85804a004
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753882"
---
# <a name="disableapp-operation"></a><span data-ttu-id="8978f-103">DisableApp 操作</span><span class="sxs-lookup"><span data-stu-id="8978f-103">DisableApp operation</span></span>

<span data-ttu-id="8978f-104">查找有关**DisableApp** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="8978f-104">Find information about the **DisableApp** EWS operation.</span></span> 
  
<span data-ttu-id="8978f-105">**DisableApp**操作禁用 Outlook 邮件应用程序。</span><span class="sxs-lookup"><span data-stu-id="8978f-105">The **DisableApp** operation disables a mail app for Outlook.</span></span> 
  
<span data-ttu-id="8978f-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="8978f-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-disableapp-operation"></a><span data-ttu-id="8978f-107">使用 DisableApp 操作</span><span class="sxs-lookup"><span data-stu-id="8978f-107">Using the DisableApp operation</span></span>

<span data-ttu-id="8978f-108">**DisableApp**操作采用两个参数中标识邮件应用程序禁用请求和禁用原因的原因。</span><span class="sxs-lookup"><span data-stu-id="8978f-108">The **DisableApp** operation takes two arguments in the request that identify the mail app to disable and the reason why it was disabled.</span></span> 
  
### <a name="disableapp-operation-soap-headers"></a><span data-ttu-id="8978f-109">DisableApp 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="8978f-109">DisableApp operation SOAP headers</span></span>

<span data-ttu-id="8978f-110">**DisableApp**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="8978f-110">The **DisableApp** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="8978f-111">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="8978f-111">**Header name**</span></span>|<span data-ttu-id="8978f-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="8978f-112">**Element**</span></span>|<span data-ttu-id="8978f-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="8978f-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8978f-114">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="8978f-114">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="8978f-115">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="8978f-115">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="8978f-116">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="8978f-116">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="8978f-117">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="8978f-117">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="8978f-118">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="8978f-118">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="8978f-119">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="8978f-119">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="8978f-120">标识响应该请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="8978f-120">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="8978f-121">适用于响应此标头。</span><span class="sxs-lookup"><span data-stu-id="8978f-121">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="disableapp-operation-request-example-disable-a-mail-app-installed-in-a-mailbox"></a><span data-ttu-id="8978f-122">DisableApp 操作请求示例： 禁用邮箱中安装邮件应用程序</span><span class="sxs-lookup"><span data-stu-id="8978f-122">DisableApp operation request example: Disable a mail app installed in a mailbox</span></span>

<span data-ttu-id="8978f-123">下面的示例**DisableApp**操作的请求显示如何禁用邮件应用程序。</span><span class="sxs-lookup"><span data-stu-id="8978f-123">The following example of a **DisableApp** operation request shows how to a disable a mail app.</span></span> <span data-ttu-id="8978f-124">[GetAppManifests 操作](getappmanifests-operation.md)响应中返回的应用程序清单中，可以找到应用程序标识符。</span><span class="sxs-lookup"><span data-stu-id="8978f-124">The app identifier can be found in the app manifest that is returned in a [GetAppManifests operation](getappmanifests-operation.md) response.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
      <t:MailboxCulture>en-US</t:MailboxCulture>
      <t:TimeZoneContext>
         <t:TimeZoneDefinition Id="GMT Standard Time"/>
      </t:TimeZoneContext>
   </soap:Header>
   <soap:Body >
      <m:DisableApp>
         <m:ID>1C50226D-04B5-4AB2-9FCD-42E236B59E4B</m:ID>
         <m:DisableReason>NoReason</m:DisableReason>
      </m:DisableApp>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="8978f-125">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="8978f-125">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="8978f-126">DisableApp</span><span class="sxs-lookup"><span data-stu-id="8978f-126">DisableApp</span></span>](disableapp.md)
    
- [<span data-ttu-id="8978f-127">ID （字符串）</span><span class="sxs-lookup"><span data-stu-id="8978f-127">ID (String)</span></span>](id-string.md)
    
- [<span data-ttu-id="8978f-128">DisableReason</span><span class="sxs-lookup"><span data-stu-id="8978f-128">DisableReason</span></span>](disablereason.md)
    
## <a name="successful-disableapp-operation-response"></a><span data-ttu-id="8978f-129">成功 DisableApp 操作响应</span><span class="sxs-lookup"><span data-stu-id="8978f-129">Successful DisableApp operation response</span></span>

<span data-ttu-id="8978f-130">下面的示例演示对**DisableApp**操作请求禁用邮件应用程序的成功响应。</span><span class="sxs-lookup"><span data-stu-id="8978f-130">The following example shows a successful response to a **DisableApp** operation request to disable a mail app.</span></span> 
  
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
      <DisableAppResponse ResponseClass="Success" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </DisableAppResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="8978f-131">响应 SOAP 正文中包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="8978f-131">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="8978f-132">DisableAppResponse</span><span class="sxs-lookup"><span data-stu-id="8978f-132">DisableAppResponse</span></span>](disableappresponse.md)
    
- [<span data-ttu-id="8978f-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="8978f-133">ResponseCode</span></span>](responsecode.md)
    
## <a name="disableapp-operation-error-response"></a><span data-ttu-id="8978f-134">DisableApp 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="8978f-134">DisableApp operation error response</span></span>

<span data-ttu-id="8978f-135">下面的示例演示对**DisableApp**操作请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="8978f-135">The following example shows an error response to a **DisableApp** operation request.</span></span> <span data-ttu-id="8978f-136">这是禁用的邮箱中未安装的邮件应用程序请求的响应。</span><span class="sxs-lookup"><span data-stu-id="8978f-136">This is a response to a request to disable a mail app that is not installed in a mailbox.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="556" MinorBuildNumber="14" Version="Exchange2013" xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" xmlns="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <DisableAppResponse ResponseClass="Error" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Extension ID 1C50226D-04B5-4AB2-9FCD-42E236B59E4A can't be found.</MessageText>
         <ResponseCode>ErrorExtensionNotFound</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </DisableAppResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="8978f-137">错误响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="8978f-137">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="8978f-138">DisableAppResponse</span><span class="sxs-lookup"><span data-stu-id="8978f-138">DisableAppResponse</span></span>](disableappresponse.md)
    
- [<span data-ttu-id="8978f-139">MessageText</span><span class="sxs-lookup"><span data-stu-id="8978f-139">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="8978f-140">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="8978f-140">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="8978f-141">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="8978f-141">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="8978f-142">通用到 EWS 且特定于此操作的其他错误代码，请参阅[ResponseCode](responsecode.md)。</span><span class="sxs-lookup"><span data-stu-id="8978f-142">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8978f-143">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8978f-143">See also</span></span>

- [<span data-ttu-id="8978f-144">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="8978f-144">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)   
- [<span data-ttu-id="8978f-145">InstallApp 操作</span><span class="sxs-lookup"><span data-stu-id="8978f-145">InstallApp operation</span></span>](installapp-operation.md)   
- [<span data-ttu-id="8978f-146">UninstallApp 操作</span><span class="sxs-lookup"><span data-stu-id="8978f-146">UninstallApp operation</span></span>](uninstallapp-operation.md)   
- [<span data-ttu-id="8978f-147">GetAppManifests</span><span class="sxs-lookup"><span data-stu-id="8978f-147">GetAppManifests</span></span>](getappmanifests.md)   
- [<span data-ttu-id="8978f-148">GetAppMarketplaceUrl 操作</span><span class="sxs-lookup"><span data-stu-id="8978f-148">GetAppMarketplaceUrl operation</span></span>](getappmarketplaceurl-operation.md)   
- [<span data-ttu-id="8978f-149">Outlook 外接程序</span><span class="sxs-lookup"><span data-stu-id="8978f-149">Outlook add-ins</span></span>](http://msdn.microsoft.com/library/71e64bc9-e347-4f5d-8948-0a47b5dd93e6%28Office.15%29.aspx)
    

