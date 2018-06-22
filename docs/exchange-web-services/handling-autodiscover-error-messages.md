---
title: 处理自动发现的错误消息
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: e5939ec2-1100-4174-8a88-5a6e09b60b23
description: 了解不同类型的自动发现错误和如何处理它们。
ms.openlocfilehash: fcafc799f4d35e92159d2913845474ecf7bc5657
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19752724"
---
# <a name="handling-autodiscover-error-messages"></a><span data-ttu-id="490cc-103">处理自动发现的错误消息</span><span class="sxs-lookup"><span data-stu-id="490cc-103">Handling Autodiscover error messages</span></span>

<span data-ttu-id="490cc-104">了解不同类型的自动发现错误和如何处理它们。</span><span class="sxs-lookup"><span data-stu-id="490cc-104">Learn about the different types of Autodiscover errors and what to do with them.</span></span>
  
<span data-ttu-id="490cc-105">自动发现，您的应用程序可以自动检索配置信息和它棒。</span><span class="sxs-lookup"><span data-stu-id="490cc-105">Autodiscover enables your applications to retrieve configuration information automatically, and it works great.</span></span> <span data-ttu-id="490cc-106">但是，操作并不总是会根据计划。</span><span class="sxs-lookup"><span data-stu-id="490cc-106">However, things don't always go according to plan.</span></span> <span data-ttu-id="490cc-107">让我们看一下，可能出现的常见错误和如何处理这些大程度地减少需要提示用户手动配置您的客户端。</span><span class="sxs-lookup"><span data-stu-id="490cc-107">Let's look at the common errors that might occur and how you can handle them to minimize the need to prompt your user to manually configure your client.</span></span>
  
## <a name="http-status-errors"></a><span data-ttu-id="490cc-108">HTTP 状态错误</span><span class="sxs-lookup"><span data-stu-id="490cc-108">HTTP status errors</span></span>
<span data-ttu-id="490cc-109"><a name="bk_HttpErrors"> </a></span><span class="sxs-lookup"><span data-stu-id="490cc-109"></span></span>

<span data-ttu-id="490cc-110">发送自动发现请求时可能会遇到的第一种是错误的 HTTP 状态。</span><span class="sxs-lookup"><span data-stu-id="490cc-110">The first type of error you might encounter when sending Autodiscover requests is the HTTP status.</span></span> <span data-ttu-id="490cc-111">如果您的响应中的 HTTP 状态 200 (OK) 之外的任何内容，则响应负载不包含您要寻找的自动发现响应。</span><span class="sxs-lookup"><span data-stu-id="490cc-111">If the HTTP status in your response is anything other than 200 (OK), the response payload doesn't contain the Autodiscover response you were looking for.</span></span> <span data-ttu-id="490cc-112">为了简单起见，我们可以分为三个类别分组非 200 状态代码。</span><span class="sxs-lookup"><span data-stu-id="490cc-112">For simplicity, we can group non-200 status codes into three categories.</span></span>
  
<span data-ttu-id="490cc-113">**表 1。HTTP 状态代码**</span><span class="sxs-lookup"><span data-stu-id="490cc-113">**Table 1. HTTP status codes**</span></span>

|<span data-ttu-id="490cc-114">**状态代码**</span><span class="sxs-lookup"><span data-stu-id="490cc-114">**Status code**</span></span>|<span data-ttu-id="490cc-115">**错误的类型**</span><span class="sxs-lookup"><span data-stu-id="490cc-115">**Type of error**</span></span>|<span data-ttu-id="490cc-116">**处理...**</span><span class="sxs-lookup"><span data-stu-id="490cc-116">**To handle…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="490cc-117">301 或 302</span><span class="sxs-lookup"><span data-stu-id="490cc-117">301 or 302</span></span>  <br/> |<span data-ttu-id="490cc-118">重定向错误</span><span class="sxs-lookup"><span data-stu-id="490cc-118">Redirect error</span></span>  <br/> |<span data-ttu-id="490cc-119">重新您的请求发送到"位置"HTTP 响应标头中包含的 URI。</span><span class="sxs-lookup"><span data-stu-id="490cc-119">Resend your request to the URI contained in the "Location" HTTP response header.</span></span> <span data-ttu-id="490cc-120">有关详细信息，请参阅[处理重定向错误](#bk_HandlingRedirects)。</span><span class="sxs-lookup"><span data-stu-id="490cc-120">For details, see [Handling redirect errors](#bk_HandlingRedirects).</span></span>  <br/> |
|<span data-ttu-id="490cc-121">401</span><span class="sxs-lookup"><span data-stu-id="490cc-121">401</span></span>  <br/> |<span data-ttu-id="490cc-122">未经授权的错误</span><span class="sxs-lookup"><span data-stu-id="490cc-122">Unauthorized error</span></span>  <br/> |<span data-ttu-id="490cc-123">[自动发现过程](autodiscover-for-exchange.md)涉及尝试多个潜在的 Url，因为您无法获取此个 URL 仅具有下一个接受您的凭据。</span><span class="sxs-lookup"><span data-stu-id="490cc-123">Because the [Autodiscover process](autodiscover-for-exchange.md) involves trying multiple potential URLs, you could get this on one URL only to have the next one accept your credentials.</span></span> <span data-ttu-id="490cc-124">因此，您不应考虑单个 401 错误以指示的凭据是无效。</span><span class="sxs-lookup"><span data-stu-id="490cc-124">For this reason, you shouldn't consider a single 401 error to indicate that the credentials are invalid.</span></span> <span data-ttu-id="490cc-125">但是，如果您收到 401 错误来自多个 Url，您可能希望提示用户重新输入自己的密码 （如果可能）。</span><span class="sxs-lookup"><span data-stu-id="490cc-125">However, if you receive 401 errors from multiple URLs, you might want to prompt the user to reenter their password (if possible).</span></span>  <br/> |
|<span data-ttu-id="490cc-126">任何其他非 200 状态</span><span class="sxs-lookup"><span data-stu-id="490cc-126">Any other non-200 status</span></span>  <br/> |<span data-ttu-id="490cc-127">无效的自动发现终结点错误</span><span class="sxs-lookup"><span data-stu-id="490cc-127">Invalid Autodiscover endpoint error</span></span>  <br/> |<span data-ttu-id="490cc-128">请考虑返回任何其他非 200 状态代码无效，URL 并继续尝试在列表中的下一个 URL。</span><span class="sxs-lookup"><span data-stu-id="490cc-128">Consider the URL that returns any other non-200 status code to be invalid, and continue trying the next URL in your list.</span></span>  <br/> |
   
## <a name="autodiscover-errors"></a><span data-ttu-id="490cc-129">自动发现错误</span><span class="sxs-lookup"><span data-stu-id="490cc-129">Autodiscover errors</span></span>
<span data-ttu-id="490cc-130"><a name="bk_AutodiscoverErrors"> </a></span><span class="sxs-lookup"><span data-stu-id="490cc-130"></span></span>

<span data-ttu-id="490cc-131">即使您获得 200 (OK) 状态代码后发送的自动发现请求时，不意味着服务器发送所需的信息。</span><span class="sxs-lookup"><span data-stu-id="490cc-131">Even if you get a 200 (OK) status code after sending an Autodiscover request, that doesn't mean that the server sent the information you need.</span></span> <span data-ttu-id="490cc-132">200 状态仅意味着您具有自动发现响应，且该响应可能包含内负载错误。</span><span class="sxs-lookup"><span data-stu-id="490cc-132">The 200 status only means that you have an Autodiscover response, and that response might contain an error within the payload.</span></span> <span data-ttu-id="490cc-133">根据格式是否为 SOAP 或 POX 不同错误信息的位置。</span><span class="sxs-lookup"><span data-stu-id="490cc-133">The location of the error information differs depending on whether the format is SOAP or POX.</span></span>
  
### <a name="soap-autodiscover-errors"></a><span data-ttu-id="490cc-134">SOAP 自动发现错误</span><span class="sxs-lookup"><span data-stu-id="490cc-134">SOAP Autodiscover errors</span></span>

<span data-ttu-id="490cc-135">对于 SOAP 自动发现响应可包含一个或多个[错误代码 (SOAP)](http://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx)元素，在不同的位置。</span><span class="sxs-lookup"><span data-stu-id="490cc-135">For SOAP Autodiscover, the response can contain one or more [ErrorCode (SOAP)](http://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx) elements, in different places.</span></span> <span data-ttu-id="490cc-136">通常您可以在响应中预期一个作为[响应 (SOAP)](http://msdn.microsoft.com/library/4c2bcdeb-95ce-4ffa-bd83-118af53b534f%28Office.15%29.aspx)元素的子元素，另一个作为每个[用户回音 (SOAP)](http://msdn.microsoft.com/library/5007b1ba-bfcc-40d7-b1cb-e32fbaf54ffd%28Office.15%29.aspx)元素的子元素。</span><span class="sxs-lookup"><span data-stu-id="490cc-136">Typically you can expect one as a child element of the [Response (SOAP)](http://msdn.microsoft.com/library/4c2bcdeb-95ce-4ffa-bd83-118af53b534f%28Office.15%29.aspx) element, and one as a child of each [UserResponse (SOAP)](http://msdn.microsoft.com/library/5007b1ba-bfcc-40d7-b1cb-e32fbaf54ffd%28Office.15%29.aspx) element in the response.</span></span> <span data-ttu-id="490cc-137">此外可能会遇到一个作为子元素的[UserSettingError (SOAP)](http://msdn.microsoft.com/library/abb175c5-4f38-4dcc-81e3-b511686862eb%28Office.15%29.aspx)元素，如果存在此参数。</span><span class="sxs-lookup"><span data-stu-id="490cc-137">You might also encounter one as a child of a [UserSettingError (SOAP)](http://msdn.microsoft.com/library/abb175c5-4f38-4dcc-81e3-b511686862eb%28Office.15%29.aspx) element, if one is present.</span></span> <span data-ttu-id="490cc-138">错误的上下文取决于**ErrorCode**元素的位置，，如下所示：</span><span class="sxs-lookup"><span data-stu-id="490cc-138">The context of the error depends on where the **ErrorCode** element is located, as follows:</span></span> 
  
- <span data-ttu-id="490cc-139">作为**响应**元素的子元素， **ErrorCode**元素均表示一条错误，适用于整个请求。</span><span class="sxs-lookup"><span data-stu-id="490cc-139">As a child element of the **Response** element, the **ErrorCode** element represents an error that applies to the entire request.</span></span> 
    
- <span data-ttu-id="490cc-140">作为**用户回音**元素的子元素，它代表适用于特定用户的只是一个错误。</span><span class="sxs-lookup"><span data-stu-id="490cc-140">As a child of the **UserResponse** element, it represents an error that applies just to that specific user.</span></span> 
    
- <span data-ttu-id="490cc-141">作为**UserSettingError**元素的子元素，它表示一条错误，适用于所请求的特定设置。</span><span class="sxs-lookup"><span data-stu-id="490cc-141">As a child of a **UserSettingError** element, it represents an error that applies to a specific setting that was requested.</span></span> 
    
<span data-ttu-id="490cc-142">让我们看看的响应的示例。</span><span class="sxs-lookup"><span data-stu-id="490cc-142">Let's take a look at an example of a response.</span></span> <span data-ttu-id="490cc-143">本示例中，**响应**元素下的**ErrorCode**元素的值为"NoError"，指示总体成功。</span><span class="sxs-lookup"><span data-stu-id="490cc-143">In this example, the **ErrorCode** element under the **Response** element has a value of "NoError", which indicates overall success.</span></span> <span data-ttu-id="490cc-144">但是，**用户回音**元素下的**ErrorCode**元素的值为"RedirectAddress"，指示该特定用户的发生了错误。</span><span class="sxs-lookup"><span data-stu-id="490cc-144">However, the **ErrorCode** element under the **UserResponse** element has a value of "RedirectAddress", which indicates that an error occurred for that particular user.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/" 
    xmlns:a="http://www.w3.org/2005/08/addressing">
  <s:Header>
    <a:Action s:mustUnderstand="1">http://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettingsResponse</a:Action>
    <h:ServerVersionInfo xmlns:h="http://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
      <h:MajorVersion>14</h:MajorVersion>
      <h:MinorVersion>3</h:MinorVersion>
      <h:MajorBuildNumber>136</h:MajorBuildNumber>
      <h:MinorBuildNumber>1</h:MinorBuildNumber>
      <h:Version>Exchange2010_SP2</h:Version>
    </h:ServerVersionInfo>
  </s:Header>
  <s:Body>
    <GetUserSettingsResponseMessage xmlns="http://schemas.microsoft.com/exchange/2010/Autodiscover">
      <Response xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
        <ErrorCode>NoError</ErrorCode>
        <ErrorMessage />
        <UserResponses>
          <UserResponse>
            <ErrorCode>RedirectAddress</ErrorCode>
            <ErrorMessage>Redirection address.</ErrorMessage>
            <RedirectTarget>elvin@mail.contoso.com</RedirectTarget>
            <UserSettingErrors />
            <UserSettings />
          </UserResponse>
        </UserResponses>
      </Response>
    </GetUserSettingsResponseMessage>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="490cc-145">[ErrorCode (SOAP)](http://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx)本文包含可能出现的错误的完整列表。</span><span class="sxs-lookup"><span data-stu-id="490cc-145">The [ErrorCode (SOAP)](http://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx) article contains a full list of possible errors.</span></span> <span data-ttu-id="490cc-146">大部分这些指示不可恢复的错误，但一些保证特殊处理。</span><span class="sxs-lookup"><span data-stu-id="490cc-146">Most of these indicate an unrecoverable error, but a few warrant special handling.</span></span> 
  
<span data-ttu-id="490cc-147">**表 2。SOAP Autodisover ErrorCode 值**</span><span class="sxs-lookup"><span data-stu-id="490cc-147">**Table 2. SOAP Autodisover ErrorCode values**</span></span>

|<span data-ttu-id="490cc-148">**ErrorCode 值**</span><span class="sxs-lookup"><span data-stu-id="490cc-148">**ErrorCode value**</span></span>|<span data-ttu-id="490cc-149">**处理...**</span><span class="sxs-lookup"><span data-stu-id="490cc-149">**To handle…**</span></span>|
|:-----|:-----|
|<span data-ttu-id="490cc-150">RedirectAddress</span><span class="sxs-lookup"><span data-stu-id="490cc-150">RedirectAddress</span></span>  <br/> |<span data-ttu-id="490cc-151">与[RedirectTarget (SOAP)](http://msdn.microsoft.com/library/f8162724-cf9a-4543-a1ad-5846c8b10bfa%28Office.15%29.aspx)元素中的电子邮件地址，[重新启动与新的电子邮件地址的自动发现](#bk_RestartAutodiscover)。</span><span class="sxs-lookup"><span data-stu-id="490cc-151">[Restarting Autodiscover with a new email address](#bk_RestartAutodiscover) with the email address in the [RedirectTarget (SOAP)](http://msdn.microsoft.com/library/f8162724-cf9a-4543-a1ad-5846c8b10bfa%28Office.15%29.aspx) element.</span></span>  <br/> |
|<span data-ttu-id="490cc-152">RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="490cc-152">RedirectUrl</span></span>  <br/> |<span data-ttu-id="490cc-153">**RedirectTarget**元素中的 url 的[重新发送您的请求指向新 URL](#bk_ResendRequest) 。</span><span class="sxs-lookup"><span data-stu-id="490cc-153">[Resending your request to a new URL](#bk_ResendRequest) to the URL in the **RedirectTarget** element.</span></span>  <br/> |
|<span data-ttu-id="490cc-154">ServerBusy</span><span class="sxs-lookup"><span data-stu-id="490cc-154">ServerBusy</span></span>  <br/> |<span data-ttu-id="490cc-155">在小型延迟后重试此 URL。</span><span class="sxs-lookup"><span data-stu-id="490cc-155">Retry this URL after a small delay.</span></span> <span data-ttu-id="490cc-156">您可能等待的时间设置，或只是将此 URL 移动到的尝试的 Url 列表末尾。</span><span class="sxs-lookup"><span data-stu-id="490cc-156">You might wait a set amount of time or simply move this URL to the end of your list of URLs to try.</span></span> <span data-ttu-id="490cc-157">如果从 URL 多次收到此错误，则应考虑的 URL 无效。</span><span class="sxs-lookup"><span data-stu-id="490cc-157">If you receive this error multiple times from a URL, you should consider the URL to be invalid.</span></span>  <br/> |
   
### <a name="pox-autodiscover-errors"></a><span data-ttu-id="490cc-158">POX 自动发现错误</span><span class="sxs-lookup"><span data-stu-id="490cc-158">POX Autodiscover errors</span></span>

<span data-ttu-id="490cc-159">POX 自动发现服务略有不同报告的错误。</span><span class="sxs-lookup"><span data-stu-id="490cc-159">The POX Autodiscover service reports errors a little differently.</span></span> <span data-ttu-id="490cc-160">[错误 (POX)](http://msdn.microsoft.com/library/91c63b62-ab68-4c32-a2f7-5a87c188335b%28Office.15%29.aspx)元素中包含非恢复错误。</span><span class="sxs-lookup"><span data-stu-id="490cc-160">Non-recoverable errors are contained in the [Error (POX)](http://msdn.microsoft.com/library/91c63b62-ab68-4c32-a2f7-5a87c188335b%28Office.15%29.aspx) element.</span></span> <span data-ttu-id="490cc-161">[ErrorCode (POX)](http://msdn.microsoft.com/library/064d73e4-45b7-4797-828e-9df590830db8%28Office.15%29.aspx)本文包含可能错误代码的完整列表。</span><span class="sxs-lookup"><span data-stu-id="490cc-161">The [ErrorCode (POX)](http://msdn.microsoft.com/library/064d73e4-45b7-4797-828e-9df590830db8%28Office.15%29.aspx) article contains a full list of possible error codes.</span></span> 
  
<span data-ttu-id="490cc-162">[操作 (POX)](http://msdn.microsoft.com/library/a3462c6b-453c-462a-830d-f29ee4a2babb%28Office.15%29.aspx)元素中包含重定向错误。</span><span class="sxs-lookup"><span data-stu-id="490cc-162">Redirect errors are contained in the [Action (POX)](http://msdn.microsoft.com/library/a3462c6b-453c-462a-830d-f29ee4a2babb%28Office.15%29.aspx) element.</span></span> <span data-ttu-id="490cc-163">**Action**元素"设置"之外的任何值指示重定向错误。</span><span class="sxs-lookup"><span data-stu-id="490cc-163">Any value of the **Action** element other than "settings" indicates a redirect error.</span></span> 
  
<span data-ttu-id="490cc-164">**表 3。POX Autodisover ErrorCode 值**</span><span class="sxs-lookup"><span data-stu-id="490cc-164">**Table 3. POX Autodisover ErrorCode values**</span></span>

|<span data-ttu-id="490cc-165">**Action 值**</span><span class="sxs-lookup"><span data-stu-id="490cc-165">**Action value**</span></span>|<span data-ttu-id="490cc-166">**处理...**</span><span class="sxs-lookup"><span data-stu-id="490cc-166">**To handle…**</span></span>|
|:-----|:-----|
|<span data-ttu-id="490cc-167">redirectAddr</span><span class="sxs-lookup"><span data-stu-id="490cc-167">redirectAddr</span></span>  <br/> |<span data-ttu-id="490cc-168">与[RedirectAddr (POX)](http://msdn.microsoft.com/library/0e9fa6b6-7991-4dc1-a59a-48e5f8e041e4%28Office.15%29.aspx)元素中的电子邮件地址，[重新启动与新的电子邮件地址的自动发现](#bk_RestartAutodiscover)。</span><span class="sxs-lookup"><span data-stu-id="490cc-168">[Restarting Autodiscover with a new email address](#bk_RestartAutodiscover) with the email address in the [RedirectAddr (POX)](http://msdn.microsoft.com/library/0e9fa6b6-7991-4dc1-a59a-48e5f8e041e4%28Office.15%29.aspx) element.</span></span>  <br/> |
|<span data-ttu-id="490cc-169">redirectUrl</span><span class="sxs-lookup"><span data-stu-id="490cc-169">redirectUrl</span></span>  <br/> |<span data-ttu-id="490cc-170">[RedirectUrl (POX)](http://msdn.microsoft.com/library/c54f310f-8c99-4c37-8e73-ac87722b6229%28Office.15%29.aspx)元素中的 url 的[重新发送您的请求指向新 URL](#bk_ResendRequest) 。</span><span class="sxs-lookup"><span data-stu-id="490cc-170">[Resending your request to a new URL](#bk_ResendRequest) to the URL in the [RedirectUrl (POX)](http://msdn.microsoft.com/library/c54f310f-8c99-4c37-8e73-ac87722b6229%28Office.15%29.aspx) element.</span></span>  <br/> |
   
<span data-ttu-id="490cc-171">本示例中，为**Action**元素的值为"redirectAddr"，指示应将新的请求发送**RedirectAddr**元素中包含的新电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="490cc-171">In this example, the **Action** element has a value of "redirectAddr", which indicates that a new request should be sent with the new email address contained in the **RedirectAddr** element.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="http://schemas.microsoft.com/exchange/autodiscover/responseschema/2006">
  <Response xmlns="http://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a">
    <Account>
      <Action>redirectAddr</Action>
      <RedirectAddr>elvin@mail.contoso.com</RedirectAddr>
    </Account>
  </Response>
</Autodiscover>
```

## <a name="handling-redirect-errors"></a><span data-ttu-id="490cc-172">处理重定向错误</span><span class="sxs-lookup"><span data-stu-id="490cc-172">Handling redirect errors</span></span>
<span data-ttu-id="490cc-173"><a name="bk_HandlingRedirects"> </a></span><span class="sxs-lookup"><span data-stu-id="490cc-173"></span></span>

<span data-ttu-id="490cc-174">您可以处理以下两种方式重定向错误方案：</span><span class="sxs-lookup"><span data-stu-id="490cc-174">You can handle redirect error scenarios in two ways:</span></span>
  
- <span data-ttu-id="490cc-175">通过使用新的电子邮件地址，重新启动自动发现。</span><span class="sxs-lookup"><span data-stu-id="490cc-175">By restarting Autodiscover with a new email address.</span></span>
    
- <span data-ttu-id="490cc-176">通过重新您的请求发送到新 URL。</span><span class="sxs-lookup"><span data-stu-id="490cc-176">By resending your request to a new URL.</span></span>
    
<span data-ttu-id="490cc-177">这两种方案需要一些然后再继续验证。</span><span class="sxs-lookup"><span data-stu-id="490cc-177">Both scenarios require some validation before proceeding.</span></span>
  
### <a name="restarting-autodiscover-with-a-new-email-address"></a><span data-ttu-id="490cc-178">使用新的电子邮件地址重新启动自动发现</span><span class="sxs-lookup"><span data-stu-id="490cc-178">Restarting Autodiscover with a new email address</span></span>
<span data-ttu-id="490cc-179"><a name="bk_RestartAutodiscover"> </a></span><span class="sxs-lookup"><span data-stu-id="490cc-179"></span></span>

<span data-ttu-id="490cc-180">当您获取中自动发现新的电子邮件地址重定向响应，首先验证重定向错误响应中提供的新电子邮件地址不是导致此错误的请求中发送相同的地址。</span><span class="sxs-lookup"><span data-stu-id="490cc-180">When you get a new email address in an Autodiscover redirect response, first verify that the new email address that was provided in the redirect error response is not the same address that you sent in the request that resulted in the error.</span></span> <span data-ttu-id="490cc-181">如果是，您不应重新启动自动发现和改为考虑生成响应无效的 URL。</span><span class="sxs-lookup"><span data-stu-id="490cc-181">If it is, you should not restart Autodiscover and instead consider the URL that generated the response to be invalid.</span></span>
  
<span data-ttu-id="490cc-182">如果不同的新电子邮件地址，放弃的潜在的自动发现终结点 Url 现有列表，并生成新的电子邮件地址所基于的新列表。</span><span class="sxs-lookup"><span data-stu-id="490cc-182">If the new email address is different, discard your existing list of potential Autodiscover endpoint URLs and generate a new list based on the new email address.</span></span>
  
### <a name="resending-your-request-to-a-new-url"></a><span data-ttu-id="490cc-183">重新您的请求发送到新 URL</span><span class="sxs-lookup"><span data-stu-id="490cc-183">Resending your request to a new URL</span></span>
<span data-ttu-id="490cc-184"><a name="bk_ResendRequest"> </a></span><span class="sxs-lookup"><span data-stu-id="490cc-184"></span></span>

<span data-ttu-id="490cc-185">自动发现重定向响应中收到新 URL，您首先应，如下所示验证 URL:</span><span class="sxs-lookup"><span data-stu-id="490cc-185">When you get a new URL in an Autodiscover redirect response, you should first validate the URL as follows:</span></span>
  
- <span data-ttu-id="490cc-186">验证 URL 是 HTTPS URL。</span><span class="sxs-lookup"><span data-stu-id="490cc-186">Verify that the URL is an HTTPS URL.</span></span>
    
- <span data-ttu-id="490cc-187">确认您未从之前的当前电子邮件地址与此 URL 中收到了错误。</span><span class="sxs-lookup"><span data-stu-id="490cc-187">Verify that you have not received an error from this URL with the current email address before.</span></span>
    
- <span data-ttu-id="490cc-188">如果适用于您的应用程序，告知用户重定向并获取其权限遵循重定向。</span><span class="sxs-lookup"><span data-stu-id="490cc-188">If applicable to your application, inform the user of the redirection and get their permission to follow the redirect.</span></span>
    
- <span data-ttu-id="490cc-189">将请求发送到 URL 和[验证服务器提供的 SSL 证书有效](how-to-validate-a-server-certificate-for-the-ews-managed-api.md)。</span><span class="sxs-lookup"><span data-stu-id="490cc-189">Send a request to the URL and [verify that the SSL certificate presented by the server is valid](how-to-validate-a-server-certificate-for-the-ews-managed-api.md).</span></span>
    
<span data-ttu-id="490cc-190">如果 URL 通过验证，则重新请求发送到此新的 URL。</span><span class="sxs-lookup"><span data-stu-id="490cc-190">If the URL passes validation, resend the request to this new URL.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="490cc-191">另请参阅</span><span class="sxs-lookup"><span data-stu-id="490cc-191">See also</span></span>


- [<span data-ttu-id="490cc-192">Exchange 自动发现</span><span class="sxs-lookup"><span data-stu-id="490cc-192">Autodiscover for Exchange</span></span>](autodiscover-for-exchange.md)
    
- [<span data-ttu-id="490cc-193">在 Exchange 使用 SCP 查找来查找自动发现终结点</span><span class="sxs-lookup"><span data-stu-id="490cc-193">Find Autodiscover endpoints by using SCP lookup in Exchange</span></span>](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md)
    
- [<span data-ttu-id="490cc-194">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="490cc-194">ErrorCode (SOAP)</span></span>](http://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx)
    
- [<span data-ttu-id="490cc-195">ErrorCode (POX)</span><span class="sxs-lookup"><span data-stu-id="490cc-195">ErrorCode (POX)</span></span>](http://msdn.microsoft.com/library/064d73e4-45b7-4797-828e-9df590830db8%28Office.15%29.aspx)
    

