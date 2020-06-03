---
title: 处理自动发现错误消息
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: e5939ec2-1100-4174-8a88-5a6e09b60b23
description: 了解不同类型的自动发现错误以及如何处理它们。
localization_priority: Priority
ms.openlocfilehash: 0cba7e54cb251a9775e0971826560e277dcd9d2d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455959"
---
# <a name="handling-autodiscover-error-messages"></a><span data-ttu-id="4172d-103">处理自动发现错误消息</span><span class="sxs-lookup"><span data-stu-id="4172d-103">Handling Autodiscover error messages</span></span>

<span data-ttu-id="4172d-104">了解不同类型的自动发现错误以及如何处理它们。</span><span class="sxs-lookup"><span data-stu-id="4172d-104">Learn about the different types of Autodiscover errors and what to do with them.</span></span>
  
<span data-ttu-id="4172d-105">自动发现使您的应用程序能够自动检索配置信息，并且运行良好。</span><span class="sxs-lookup"><span data-stu-id="4172d-105">Autodiscover enables your applications to retrieve configuration information automatically, and it works great.</span></span> <span data-ttu-id="4172d-106">但是，有些事情并不总是根据计划进行。</span><span class="sxs-lookup"><span data-stu-id="4172d-106">However, things don't always go according to plan.</span></span> <span data-ttu-id="4172d-107">我们来看看可能发生的常见错误，以及如何处理这些错误，以最大限度地减少提示用户手动配置客户端的需求。</span><span class="sxs-lookup"><span data-stu-id="4172d-107">Let's look at the common errors that might occur and how you can handle them to minimize the need to prompt your user to manually configure your client.</span></span>
  
## <a name="http-status-errors"></a><span data-ttu-id="4172d-108">HTTP 状态错误</span><span class="sxs-lookup"><span data-stu-id="4172d-108">HTTP status errors</span></span>
<span data-ttu-id="4172d-109"><a name="bk_HttpErrors"> </a></span><span class="sxs-lookup"><span data-stu-id="4172d-109"><a name="bk_HttpErrors"> </a></span></span>

<span data-ttu-id="4172d-110">发送自动发现请求时，您可能会遇到的第一种错误类型是 HTTP 状态。</span><span class="sxs-lookup"><span data-stu-id="4172d-110">The first type of error you might encounter when sending Autodiscover requests is the HTTP status.</span></span> <span data-ttu-id="4172d-111">如果响应中的 HTTP 状态是200（OK）之外的任何内容，响应有效负载将不包含您要查找的自动发现响应。</span><span class="sxs-lookup"><span data-stu-id="4172d-111">If the HTTP status in your response is anything other than 200 (OK), the response payload doesn't contain the Autodiscover response you were looking for.</span></span> <span data-ttu-id="4172d-112">为简单起见，我们可以将非200状态代码分组为三个类别。</span><span class="sxs-lookup"><span data-stu-id="4172d-112">For simplicity, we can group non-200 status codes into three categories.</span></span>
  
<span data-ttu-id="4172d-113">**表1。HTTP 状态代码**</span><span class="sxs-lookup"><span data-stu-id="4172d-113">**Table 1. HTTP status codes**</span></span>

|<span data-ttu-id="4172d-114">**状态代码**</span><span class="sxs-lookup"><span data-stu-id="4172d-114">**Status code**</span></span>|<span data-ttu-id="4172d-115">**错误类型**</span><span class="sxs-lookup"><span data-stu-id="4172d-115">**Type of error**</span></span>|<span data-ttu-id="4172d-116">**处理 .。。**</span><span class="sxs-lookup"><span data-stu-id="4172d-116">**To handle…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4172d-117">301或302</span><span class="sxs-lookup"><span data-stu-id="4172d-117">301 or 302</span></span>  <br/> |<span data-ttu-id="4172d-118">重定向错误</span><span class="sxs-lookup"><span data-stu-id="4172d-118">Redirect error</span></span>  <br/> |<span data-ttu-id="4172d-119">将您的请求重新发送到包含在 "Location" HTTP 响应头中的 URI。</span><span class="sxs-lookup"><span data-stu-id="4172d-119">Resend your request to the URI contained in the "Location" HTTP response header.</span></span> <span data-ttu-id="4172d-120">有关详细信息，请参阅[处理重定向错误](#bk_HandlingRedirects)。</span><span class="sxs-lookup"><span data-stu-id="4172d-120">For details, see [Handling redirect errors](#bk_HandlingRedirects).</span></span>  <br/> |
|<span data-ttu-id="4172d-121">401</span><span class="sxs-lookup"><span data-stu-id="4172d-121">401</span></span>  <br/> |<span data-ttu-id="4172d-122">未经授权的错误</span><span class="sxs-lookup"><span data-stu-id="4172d-122">Unauthorized error</span></span>  <br/> |<span data-ttu-id="4172d-123">由于[自动发现过程](autodiscover-for-exchange.md)涉及尝试多个可能的 url，因此您可以在一个 URL 上获取此程序，使下一个 url 接受您的凭据。</span><span class="sxs-lookup"><span data-stu-id="4172d-123">Because the [Autodiscover process](autodiscover-for-exchange.md) involves trying multiple potential URLs, you could get this on one URL only to have the next one accept your credentials.</span></span> <span data-ttu-id="4172d-124">出于此原因，您不应考虑使用一个401错误来指示凭据无效。</span><span class="sxs-lookup"><span data-stu-id="4172d-124">For this reason, you shouldn't consider a single 401 error to indicate that the credentials are invalid.</span></span> <span data-ttu-id="4172d-125">但是，如果收到来自多个 Url 的401错误，您可能希望提示用户重新输入密码（如果可能）。</span><span class="sxs-lookup"><span data-stu-id="4172d-125">However, if you receive 401 errors from multiple URLs, you might want to prompt the user to reenter their password (if possible).</span></span>  <br/> |
|<span data-ttu-id="4172d-126">任何其他非200状态</span><span class="sxs-lookup"><span data-stu-id="4172d-126">Any other non-200 status</span></span>  <br/> |<span data-ttu-id="4172d-127">无效的自动发现终结点错误</span><span class="sxs-lookup"><span data-stu-id="4172d-127">Invalid Autodiscover endpoint error</span></span>  <br/> |<span data-ttu-id="4172d-128">请考虑返回任何其他非200状态代码为无效的 URL，并继续尝试列表中的下一个 URL。</span><span class="sxs-lookup"><span data-stu-id="4172d-128">Consider the URL that returns any other non-200 status code to be invalid, and continue trying the next URL in your list.</span></span>  <br/> |
   
## <a name="autodiscover-errors"></a><span data-ttu-id="4172d-129">自动发现错误</span><span class="sxs-lookup"><span data-stu-id="4172d-129">Autodiscover errors</span></span>
<span data-ttu-id="4172d-130"><a name="bk_AutodiscoverErrors"> </a></span><span class="sxs-lookup"><span data-stu-id="4172d-130"><a name="bk_AutodiscoverErrors"> </a></span></span>

<span data-ttu-id="4172d-131">即使在发送自动发现请求之后收到200（OK）状态代码，这并不意味着服务器发送了您所需的信息。</span><span class="sxs-lookup"><span data-stu-id="4172d-131">Even if you get a 200 (OK) status code after sending an Autodiscover request, that doesn't mean that the server sent the information you need.</span></span> <span data-ttu-id="4172d-132">200状态仅表示您有一个自动发现响应，并且该响应可能在有效负载中包含一个错误。</span><span class="sxs-lookup"><span data-stu-id="4172d-132">The 200 status only means that you have an Autodiscover response, and that response might contain an error within the payload.</span></span> <span data-ttu-id="4172d-133">错误消息的位置因格式是 SOAP 还是 POX 而异。</span><span class="sxs-lookup"><span data-stu-id="4172d-133">The location of the error information differs depending on whether the format is SOAP or POX.</span></span>
  
### <a name="soap-autodiscover-errors"></a><span data-ttu-id="4172d-134">SOAP 自动发现错误</span><span class="sxs-lookup"><span data-stu-id="4172d-134">SOAP Autodiscover errors</span></span>

<span data-ttu-id="4172d-135">对于 SOAP 自动发现，响应可以包含一个或多个[ErrorCode （SOAP）](https://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx)元素，位于不同的位置。</span><span class="sxs-lookup"><span data-stu-id="4172d-135">For SOAP Autodiscover, the response can contain one or more [ErrorCode (SOAP)](https://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx) elements, in different places.</span></span> <span data-ttu-id="4172d-136">通常情况下，您可以将一个作为[响应（soap）](https://msdn.microsoft.com/library/4c2bcdeb-95ce-4ffa-bd83-118af53b534f%28Office.15%29.aspx)元素的子元素，另一个作为响应中的每个[UserResponse （soap）](https://msdn.microsoft.com/library/5007b1ba-bfcc-40d7-b1cb-e32fbaf54ffd%28Office.15%29.aspx)元素的子元素。</span><span class="sxs-lookup"><span data-stu-id="4172d-136">Typically you can expect one as a child element of the [Response (SOAP)](https://msdn.microsoft.com/library/4c2bcdeb-95ce-4ffa-bd83-118af53b534f%28Office.15%29.aspx) element, and one as a child of each [UserResponse (SOAP)](https://msdn.microsoft.com/library/5007b1ba-bfcc-40d7-b1cb-e32fbaf54ffd%28Office.15%29.aspx) element in the response.</span></span> <span data-ttu-id="4172d-137">您可能还会遇到一个[UserSettingError （SOAP）](https://msdn.microsoft.com/library/abb175c5-4f38-4dcc-81e3-b511686862eb%28Office.15%29.aspx)元素的子元素（如果有的话）。</span><span class="sxs-lookup"><span data-stu-id="4172d-137">You might also encounter one as a child of a [UserSettingError (SOAP)](https://msdn.microsoft.com/library/abb175c5-4f38-4dcc-81e3-b511686862eb%28Office.15%29.aspx) element, if one is present.</span></span> <span data-ttu-id="4172d-138">错误的上下文取决于**ErrorCode**元素所在的位置，如下所示：</span><span class="sxs-lookup"><span data-stu-id="4172d-138">The context of the error depends on where the **ErrorCode** element is located, as follows:</span></span> 
  
- <span data-ttu-id="4172d-139">作为**Response**元素的子元素， **ErrorCode**元素表示应用于整个请求的错误。</span><span class="sxs-lookup"><span data-stu-id="4172d-139">As a child element of the **Response** element, the **ErrorCode** element represents an error that applies to the entire request.</span></span> 
    
- <span data-ttu-id="4172d-140">作为**UserResponse**元素的子元素，它表示仅适用于该特定用户的错误。</span><span class="sxs-lookup"><span data-stu-id="4172d-140">As a child of the **UserResponse** element, it represents an error that applies just to that specific user.</span></span> 
    
- <span data-ttu-id="4172d-141">作为**UserSettingError**元素的子元素，它表示应用于所请求的特定设置的错误。</span><span class="sxs-lookup"><span data-stu-id="4172d-141">As a child of a **UserSettingError** element, it represents an error that applies to a specific setting that was requested.</span></span> 
    
<span data-ttu-id="4172d-142">我们来看看响应的一个示例。</span><span class="sxs-lookup"><span data-stu-id="4172d-142">Let's take a look at an example of a response.</span></span> <span data-ttu-id="4172d-143">在此示例中， **Response**元素下的**ErrorCode**元素的值为 "NoError"，表示整体成功。</span><span class="sxs-lookup"><span data-stu-id="4172d-143">In this example, the **ErrorCode** element under the **Response** element has a value of "NoError", which indicates overall success.</span></span> <span data-ttu-id="4172d-144">但是， **UserResponse**元素下的**ErrorCode**元素的值为 "RedirectAddress"，表示该特定用户发生了错误。</span><span class="sxs-lookup"><span data-stu-id="4172d-144">However, the **ErrorCode** element under the **UserResponse** element has a value of "RedirectAddress", which indicates that an error occurred for that particular user.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/" 
    xmlns:a="http://www.w3.org/2005/08/addressing">
  <s:Header>
    <a:Action s:mustUnderstand="1">https://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettingsResponse</a:Action>
    <h:ServerVersionInfo xmlns:h="https://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
      <h:MajorVersion>14</h:MajorVersion>
      <h:MinorVersion>3</h:MinorVersion>
      <h:MajorBuildNumber>136</h:MajorBuildNumber>
      <h:MinorBuildNumber>1</h:MinorBuildNumber>
      <h:Version>Exchange2010_SP2</h:Version>
    </h:ServerVersionInfo>
  </s:Header>
  <s:Body>
    <GetUserSettingsResponseMessage xmlns="https://schemas.microsoft.com/exchange/2010/Autodiscover">
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

<span data-ttu-id="4172d-145">[ErrorCode （SOAP）](https://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx)文章包含可能的错误的完整列表。</span><span class="sxs-lookup"><span data-stu-id="4172d-145">The [ErrorCode (SOAP)](https://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx) article contains a full list of possible errors.</span></span> <span data-ttu-id="4172d-146">大多数情况下，它们都表示出现不可恢复的错误，但少数是特别的处理保证。</span><span class="sxs-lookup"><span data-stu-id="4172d-146">Most of these indicate an unrecoverable error, but a few warrant special handling.</span></span> 
  
<span data-ttu-id="4172d-147">**表2。SOAP Autodisover ErrorCode 值**</span><span class="sxs-lookup"><span data-stu-id="4172d-147">**Table 2. SOAP Autodisover ErrorCode values**</span></span>

|<span data-ttu-id="4172d-148">**ErrorCode 值**</span><span class="sxs-lookup"><span data-stu-id="4172d-148">**ErrorCode value**</span></span>|<span data-ttu-id="4172d-149">**处理 .。。**</span><span class="sxs-lookup"><span data-stu-id="4172d-149">**To handle…**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4172d-150">RedirectAddress</span><span class="sxs-lookup"><span data-stu-id="4172d-150">RedirectAddress</span></span>  <br/> |<span data-ttu-id="4172d-151">使用[新的电子邮件地址重启](#bk_RestartAutodiscover) [RedirectTarget （SOAP）](https://msdn.microsoft.com/library/f8162724-cf9a-4543-a1ad-5846c8b10bfa%28Office.15%29.aspx)元素中的电子邮件地址的自动发现。</span><span class="sxs-lookup"><span data-stu-id="4172d-151">[Restarting Autodiscover with a new email address](#bk_RestartAutodiscover) with the email address in the [RedirectTarget (SOAP)](https://msdn.microsoft.com/library/f8162724-cf9a-4543-a1ad-5846c8b10bfa%28Office.15%29.aspx) element.</span></span>  <br/> |
|<span data-ttu-id="4172d-152">RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="4172d-152">RedirectUrl</span></span>  <br/> |<span data-ttu-id="4172d-153">将[您的请求重新发送到](#bk_ResendRequest) **RedirectTarget**元素中的 url 的新 url。</span><span class="sxs-lookup"><span data-stu-id="4172d-153">[Resending your request to a new URL](#bk_ResendRequest) to the URL in the **RedirectTarget** element.</span></span>  <br/> |
|<span data-ttu-id="4172d-154">ServerBusy</span><span class="sxs-lookup"><span data-stu-id="4172d-154">ServerBusy</span></span>  <br/> |<span data-ttu-id="4172d-155">请在短暂延迟后重试此 URL。</span><span class="sxs-lookup"><span data-stu-id="4172d-155">Retry this URL after a small delay.</span></span> <span data-ttu-id="4172d-156">您可以等待一段设定的时间，或者只是将此 URL 移到 Url 列表的末尾，以尝试。</span><span class="sxs-lookup"><span data-stu-id="4172d-156">You might wait a set amount of time or simply move this URL to the end of your list of URLs to try.</span></span> <span data-ttu-id="4172d-157">如果从某个 URL 多次收到此错误，则应将该 URL 视为无效。</span><span class="sxs-lookup"><span data-stu-id="4172d-157">If you receive this error multiple times from a URL, you should consider the URL to be invalid.</span></span>  <br/> |
   
### <a name="pox-autodiscover-errors"></a><span data-ttu-id="4172d-158">POX 自动发现错误</span><span class="sxs-lookup"><span data-stu-id="4172d-158">POX Autodiscover errors</span></span>

<span data-ttu-id="4172d-159">POX 自动发现服务以略有不同的方式报告错误。</span><span class="sxs-lookup"><span data-stu-id="4172d-159">The POX Autodiscover service reports errors a little differently.</span></span> <span data-ttu-id="4172d-160">不可恢复的错误包含在[Error （POX）](https://msdn.microsoft.com/library/91c63b62-ab68-4c32-a2f7-5a87c188335b%28Office.15%29.aspx)元素中。</span><span class="sxs-lookup"><span data-stu-id="4172d-160">Non-recoverable errors are contained in the [Error (POX)](https://msdn.microsoft.com/library/91c63b62-ab68-4c32-a2f7-5a87c188335b%28Office.15%29.aspx) element.</span></span> <span data-ttu-id="4172d-161">[ErrorCode （POX）](https://msdn.microsoft.com/library/064d73e4-45b7-4797-828e-9df590830db8%28Office.15%29.aspx)文章包含可能的错误代码的完整列表。</span><span class="sxs-lookup"><span data-stu-id="4172d-161">The [ErrorCode (POX)](https://msdn.microsoft.com/library/064d73e4-45b7-4797-828e-9df590830db8%28Office.15%29.aspx) article contains a full list of possible error codes.</span></span> 
  
<span data-ttu-id="4172d-162">重定向错误包含在[Action （POX）](https://msdn.microsoft.com/library/a3462c6b-453c-462a-830d-f29ee4a2babb%28Office.15%29.aspx)元素中。</span><span class="sxs-lookup"><span data-stu-id="4172d-162">Redirect errors are contained in the [Action (POX)](https://msdn.microsoft.com/library/a3462c6b-453c-462a-830d-f29ee4a2babb%28Office.15%29.aspx) element.</span></span> <span data-ttu-id="4172d-163">除 "设置" 之外的**Action**元素的任何值都表示重定向错误。</span><span class="sxs-lookup"><span data-stu-id="4172d-163">Any value of the **Action** element other than "settings" indicates a redirect error.</span></span> 
  
<span data-ttu-id="4172d-164">**表3。POX Autodisover ErrorCode 值**</span><span class="sxs-lookup"><span data-stu-id="4172d-164">**Table 3. POX Autodisover ErrorCode values**</span></span>

|<span data-ttu-id="4172d-165">**操作值**</span><span class="sxs-lookup"><span data-stu-id="4172d-165">**Action value**</span></span>|<span data-ttu-id="4172d-166">**处理 .。。**</span><span class="sxs-lookup"><span data-stu-id="4172d-166">**To handle…**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4172d-167">redirectAddr</span><span class="sxs-lookup"><span data-stu-id="4172d-167">redirectAddr</span></span>  <br/> |<span data-ttu-id="4172d-168">使用[新电子邮件地址重启](#bk_RestartAutodiscover) [RedirectAddr （POX）](https://msdn.microsoft.com/library/0e9fa6b6-7991-4dc1-a59a-48e5f8e041e4%28Office.15%29.aspx)元素中的电子邮件地址的自动发现。</span><span class="sxs-lookup"><span data-stu-id="4172d-168">[Restarting Autodiscover with a new email address](#bk_RestartAutodiscover) with the email address in the [RedirectAddr (POX)](https://msdn.microsoft.com/library/0e9fa6b6-7991-4dc1-a59a-48e5f8e041e4%28Office.15%29.aspx) element.</span></span>  <br/> |
|<span data-ttu-id="4172d-169">redirectUrl</span><span class="sxs-lookup"><span data-stu-id="4172d-169">redirectUrl</span></span>  <br/> |<span data-ttu-id="4172d-170">将[您的请求重新发送到](#bk_ResendRequest) [RedirectUrl （POX）](https://msdn.microsoft.com/library/c54f310f-8c99-4c37-8e73-ac87722b6229%28Office.15%29.aspx)元素中的 url 的新 url。</span><span class="sxs-lookup"><span data-stu-id="4172d-170">[Resending your request to a new URL](#bk_ResendRequest) to the URL in the [RedirectUrl (POX)](https://msdn.microsoft.com/library/c54f310f-8c99-4c37-8e73-ac87722b6229%28Office.15%29.aspx) element.</span></span>  <br/> |
   
<span data-ttu-id="4172d-171">在此示例中， **Action**元素的值为 "redirectAddr"，表示应使用**redirectAddr**元素中包含的新电子邮件地址发送新的请求。</span><span class="sxs-lookup"><span data-stu-id="4172d-171">In this example, the **Action** element has a value of "redirectAddr", which indicates that a new request should be sent with the new email address contained in the **RedirectAddr** element.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="https://schemas.microsoft.com/exchange/autodiscover/responseschema/2006">
  <Response xmlns="https://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a">
    <Account>
      <Action>redirectAddr</Action>
      <RedirectAddr>elvin@mail.contoso.com</RedirectAddr>
    </Account>
  </Response>
</Autodiscover>
```

## <a name="handling-redirect-errors"></a><span data-ttu-id="4172d-172">处理重定向错误</span><span class="sxs-lookup"><span data-stu-id="4172d-172">Handling redirect errors</span></span>
<span data-ttu-id="4172d-173"><a name="bk_HandlingRedirects"> </a></span><span class="sxs-lookup"><span data-stu-id="4172d-173"><a name="bk_HandlingRedirects"> </a></span></span>

<span data-ttu-id="4172d-174">您可以通过两种方式处理重定向错误方案：</span><span class="sxs-lookup"><span data-stu-id="4172d-174">You can handle redirect error scenarios in two ways:</span></span>
  
- <span data-ttu-id="4172d-175">通过使用新的电子邮件地址重新启动自动发现。</span><span class="sxs-lookup"><span data-stu-id="4172d-175">By restarting Autodiscover with a new email address.</span></span>
    
- <span data-ttu-id="4172d-176">通过将您的请求重新发送到新的 URL。</span><span class="sxs-lookup"><span data-stu-id="4172d-176">By resending your request to a new URL.</span></span>
    
<span data-ttu-id="4172d-177">这两种方案在继续之前都需要进行一些验证。</span><span class="sxs-lookup"><span data-stu-id="4172d-177">Both scenarios require some validation before proceeding.</span></span>
  
### <a name="restarting-autodiscover-with-a-new-email-address"></a><span data-ttu-id="4172d-178">使用新的电子邮件地址重新启动自动发现</span><span class="sxs-lookup"><span data-stu-id="4172d-178">Restarting Autodiscover with a new email address</span></span>
<span data-ttu-id="4172d-179"><a name="bk_RestartAutodiscover"> </a></span><span class="sxs-lookup"><span data-stu-id="4172d-179"><a name="bk_RestartAutodiscover"> </a></span></span>

<span data-ttu-id="4172d-180">当您在自动发现重定向响应中获取新的电子邮件地址时，请首先验证重定向错误响应中提供的新电子邮件地址是否与您在导致错误的请求中发送的地址不相同。</span><span class="sxs-lookup"><span data-stu-id="4172d-180">When you get a new email address in an Autodiscover redirect response, first verify that the new email address that was provided in the redirect error response is not the same address that you sent in the request that resulted in the error.</span></span> <span data-ttu-id="4172d-181">如果是，则不应重新启动自动发现，而应考虑生成响应的 URL 是否无效。</span><span class="sxs-lookup"><span data-stu-id="4172d-181">If it is, you should not restart Autodiscover and instead consider the URL that generated the response to be invalid.</span></span>
  
<span data-ttu-id="4172d-182">如果新的电子邮件地址不同，请丢弃现有的潜在自动发现终结点 Url 列表，并根据新的电子邮件地址生成新的列表。</span><span class="sxs-lookup"><span data-stu-id="4172d-182">If the new email address is different, discard your existing list of potential Autodiscover endpoint URLs and generate a new list based on the new email address.</span></span>
  
### <a name="resending-your-request-to-a-new-url"></a><span data-ttu-id="4172d-183">将请求重新发送到新 URL</span><span class="sxs-lookup"><span data-stu-id="4172d-183">Resending your request to a new URL</span></span>
<span data-ttu-id="4172d-184"><a name="bk_ResendRequest"> </a></span><span class="sxs-lookup"><span data-stu-id="4172d-184"><a name="bk_ResendRequest"> </a></span></span>

<span data-ttu-id="4172d-185">当您在自动发现重定向响应中获取新 URL 时，应首先验证 URL，如下所示：</span><span class="sxs-lookup"><span data-stu-id="4172d-185">When you get a new URL in an Autodiscover redirect response, you should first validate the URL as follows:</span></span>
  
- <span data-ttu-id="4172d-186">验证 URL 是否为 HTTPS URL。</span><span class="sxs-lookup"><span data-stu-id="4172d-186">Verify that the URL is an HTTPS URL.</span></span>
    
- <span data-ttu-id="4172d-187">验证您以前没有收到与当前电子邮件地址在此 URL 中的错误。</span><span class="sxs-lookup"><span data-stu-id="4172d-187">Verify that you have not received an error from this URL with the current email address before.</span></span>
    
- <span data-ttu-id="4172d-188">如果适用于你的应用程序，请通知用户重定向，并获取其对重定向的访问权限。</span><span class="sxs-lookup"><span data-stu-id="4172d-188">If applicable to your application, inform the user of the redirection and get their permission to follow the redirect.</span></span>
    
- <span data-ttu-id="4172d-189">向 URL 发送请求，并[验证服务器出示的 SSL 证书是否有效](how-to-validate-a-server-certificate-for-the-ews-managed-api.md)。</span><span class="sxs-lookup"><span data-stu-id="4172d-189">Send a request to the URL and [verify that the SSL certificate presented by the server is valid](how-to-validate-a-server-certificate-for-the-ews-managed-api.md).</span></span>
    
<span data-ttu-id="4172d-190">如果 URL 通过验证，请将请求重新发送到此新 URL。</span><span class="sxs-lookup"><span data-stu-id="4172d-190">If the URL passes validation, resend the request to this new URL.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4172d-191">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4172d-191">See also</span></span>


- [<span data-ttu-id="4172d-192">Exchange 自动发现</span><span class="sxs-lookup"><span data-stu-id="4172d-192">Autodiscover for Exchange</span></span>](autodiscover-for-exchange.md)
    
- [<span data-ttu-id="4172d-193">通过使用 Exchange 中的 SCP 查找来找到自动发现终结点</span><span class="sxs-lookup"><span data-stu-id="4172d-193">Find Autodiscover endpoints by using SCP lookup in Exchange</span></span>](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md)
    
- [<span data-ttu-id="4172d-194">ErrorCode （SOAP）</span><span class="sxs-lookup"><span data-stu-id="4172d-194">ErrorCode (SOAP)</span></span>](https://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx)
    
- [<span data-ttu-id="4172d-195">ErrorCode （POX）</span><span class="sxs-lookup"><span data-stu-id="4172d-195">ErrorCode (POX)</span></span>](https://msdn.microsoft.com/library/064d73e4-45b7-4797-828e-9df590830db8%28Office.15%29.aspx)
    

