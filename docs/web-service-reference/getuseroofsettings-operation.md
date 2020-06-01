---
title: GetUserOofSettings 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetUserOofSettings
api_type:
- schema
ms.assetid: 153e4440-495b-4972-9811-2fbea740142a
description: GetUserOofSettings 操作将获取邮箱用户的外出（OOF）设置和邮件。
ms.openlocfilehash: 622faa622b0ea231a6331ff62631885d4252c1f5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457695"
---
# <a name="getuseroofsettings-operation"></a><span data-ttu-id="9ef1a-103">GetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="9ef1a-103">GetUserOofSettings operation</span></span>

<span data-ttu-id="9ef1a-104">**GetUserOofSettings**操作将获取邮箱用户的外出（OOF）设置和邮件。</span><span class="sxs-lookup"><span data-stu-id="9ef1a-104">The **GetUserOofSettings** operation gets a mailbox user's Out of Office (OOF) settings and messages.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="9ef1a-105">SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="9ef1a-105">SOAP Headers</span></span>

<span data-ttu-id="9ef1a-106">**GetUserOofSettings**操作可以使用下表中列出和描述的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="9ef1a-106">The **GetUserOofSettings** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="9ef1a-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="9ef1a-107">**Header**</span></span>|<span data-ttu-id="9ef1a-108">**元素**</span><span class="sxs-lookup"><span data-stu-id="9ef1a-108">**Element**</span></span>|<span data-ttu-id="9ef1a-109">**说明**</span><span class="sxs-lookup"><span data-stu-id="9ef1a-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9ef1a-110">模拟</span><span class="sxs-lookup"><span data-stu-id="9ef1a-110">Impersonation</span></span>  <br/> |[<span data-ttu-id="9ef1a-111">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="9ef1a-111">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="9ef1a-112">标识客户端应用程序模拟的用户。</span><span class="sxs-lookup"><span data-stu-id="9ef1a-112">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="9ef1a-113">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="9ef1a-113">ServerVersion</span></span>  <br/> |[<span data-ttu-id="9ef1a-114">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="9ef1a-114">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="9ef1a-115">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="9ef1a-115">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="using-the-getuseroofsettings-operation"></a><span data-ttu-id="9ef1a-116">使用 GetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="9ef1a-116">Using the GetUserOofSettings Operation</span></span>

<span data-ttu-id="9ef1a-117">**GetUserOofSettings**操作提供对用户的 OOF 设置的访问权限。</span><span class="sxs-lookup"><span data-stu-id="9ef1a-117">The **GetUserOofSettings** operation provides access to a user's OOF settings.</span></span> <span data-ttu-id="9ef1a-118">用户由用户的电子邮件地址标识。</span><span class="sxs-lookup"><span data-stu-id="9ef1a-118">A user is identified by the user's email address.</span></span> <span data-ttu-id="9ef1a-119">如果 OOF 邮件为 null 且启用了 OOF 功能，则不会发送 OOF 邮件。</span><span class="sxs-lookup"><span data-stu-id="9ef1a-119">If the OOF message is null and OOF is enabled, no OOF message is sent.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="9ef1a-120">如果 OOF 邮件是由 MicrosoftOfficeOutlook 设置的，则此操作将返回 HTML 格式的 OOF 邮件。</span><span class="sxs-lookup"><span data-stu-id="9ef1a-120">If the OOF messages are set by MicrosoftOfficeOutlook, this operation will return the OOF messages in HTML format.</span></span> 
  
## <a name="getuseroofsettings-request-example"></a><span data-ttu-id="9ef1a-121">GetUserOofSettings 请求示例</span><span class="sxs-lookup"><span data-stu-id="9ef1a-121">GetUserOofSettings request example</span></span>

### <a name="description"></a><span data-ttu-id="9ef1a-122">说明</span><span class="sxs-lookup"><span data-stu-id="9ef1a-122">Description</span></span>

<span data-ttu-id="9ef1a-123">下面的示例演示一个**GetUserOofSettings**请求，该请求获取单个用户的 OOF 信息。</span><span class="sxs-lookup"><span data-stu-id="9ef1a-123">The following example shows a **GetUserOofSettings** request that gets a single user's OOF information.</span></span> 
  
### <a name="code"></a><span data-ttu-id="9ef1a-124">代码</span><span class="sxs-lookup"><span data-stu-id="9ef1a-124">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetUserOofSettingsRequest xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <Mailbox xmlns ="https://schemas.microsoft.com/exchange/services/2006/types">
        <Address>User1@example.com</Address>
      </Mailbox>
    </GetUserOofSettingsRequest>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="9ef1a-125">Request 元素</span><span class="sxs-lookup"><span data-stu-id="9ef1a-125">Request elements</span></span>

<span data-ttu-id="9ef1a-126">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="9ef1a-126">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="9ef1a-127">GetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="9ef1a-127">GetUserOofSettingsRequest</span></span>](getuseroofsettingsrequest.md)
    
- [<span data-ttu-id="9ef1a-128">邮箱（可用性）</span><span class="sxs-lookup"><span data-stu-id="9ef1a-128">Mailbox (Availability)</span></span>](mailbox-availability.md)
    
- [<span data-ttu-id="9ef1a-129">Address （string）</span><span class="sxs-lookup"><span data-stu-id="9ef1a-129">Address (string)</span></span>](address-string.md)
    
## <a name="successful-getuseroofsettings-response-example"></a><span data-ttu-id="9ef1a-130">成功的 GetUserOofSettings 响应示例</span><span class="sxs-lookup"><span data-stu-id="9ef1a-130">Successful GetUserOofSettings response example</span></span>

### <a name="description"></a><span data-ttu-id="9ef1a-131">说明</span><span class="sxs-lookup"><span data-stu-id="9ef1a-131">Description</span></span>

<span data-ttu-id="9ef1a-132">以下示例显示了带有 OOF 邮件的已禁用 OOF 状态。</span><span class="sxs-lookup"><span data-stu-id="9ef1a-132">The following example shows a disabled OOF state with the OOF messages.</span></span>
  
### <a name="code"></a><span data-ttu-id="9ef1a-133">代码</span><span class="sxs-lookup"><span data-stu-id="9ef1a-133">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetUserOofSettingsResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseMessage ResponseClass="Success">
        <ResponseCode>NoError</ResponseCode>
      </ResponseMessage>
      <OofSettings xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
        <OofState>Disabled</OofState>
        <ExternalAudience>All</ExternalAudience>
        <Duration>
          <StartTime>2006-11-03T23:00:00</StartTime>
          <EndTime>2006-11-04T23:00:00</EndTime>
        </Duration>
        <InternalReply>
          <Message>I am out of office. This is my internal reply.</Message>
        </InternalReply>
        <ExternalReply>
          <Message>I am out of office. This is my external reply.</Message>
        </ExternalReply>
      </OofSettings>
      <AllowExternalOof>All</AllowExternalOof>
    </GetUserOofSettingsResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-getuseroofsettings-response-elements"></a><span data-ttu-id="9ef1a-134">成功的 GetUserOofSettings 响应元素</span><span class="sxs-lookup"><span data-stu-id="9ef1a-134">Successful GetUserOofSettings response elements</span></span>

<span data-ttu-id="9ef1a-135">响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="9ef1a-135">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="9ef1a-136">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="9ef1a-136">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="9ef1a-137">GetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="9ef1a-137">GetUserOofSettingsResponse</span></span>](getuseroofsettingsresponse.md)
    
- [<span data-ttu-id="9ef1a-138">ResponseMessage</span><span class="sxs-lookup"><span data-stu-id="9ef1a-138">ResponseMessage</span></span>](responsemessage.md)
    
- [<span data-ttu-id="9ef1a-139">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="9ef1a-139">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="9ef1a-140">OofSettings</span><span class="sxs-lookup"><span data-stu-id="9ef1a-140">OofSettings</span></span>](oofsettings.md)
    
- [<span data-ttu-id="9ef1a-141">OofState</span><span class="sxs-lookup"><span data-stu-id="9ef1a-141">OofState</span></span>](oofstate.md)
    
- [<span data-ttu-id="9ef1a-142">ExternalAudience</span><span class="sxs-lookup"><span data-stu-id="9ef1a-142">ExternalAudience</span></span>](externalaudience.md)
    
- [<span data-ttu-id="9ef1a-143">持续时间（UserOofSettings）</span><span class="sxs-lookup"><span data-stu-id="9ef1a-143">Duration (UserOofSettings)</span></span>](duration-useroofsettings.md)
    
- [<span data-ttu-id="9ef1a-144">StartTime</span><span class="sxs-lookup"><span data-stu-id="9ef1a-144">StartTime</span></span>](starttime.md)
    
- [<span data-ttu-id="9ef1a-145">EndTime</span><span class="sxs-lookup"><span data-stu-id="9ef1a-145">EndTime</span></span>](endtime.md)
    
- [<span data-ttu-id="9ef1a-146">InternalReply</span><span class="sxs-lookup"><span data-stu-id="9ef1a-146">InternalReply</span></span>](internalreply.md)
    
- [<span data-ttu-id="9ef1a-147">ExternalReply</span><span class="sxs-lookup"><span data-stu-id="9ef1a-147">ExternalReply</span></span>](externalreply.md)
    
- [<span data-ttu-id="9ef1a-148">邮件</span><span class="sxs-lookup"><span data-stu-id="9ef1a-148">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="9ef1a-149">AllowExternalOof</span><span class="sxs-lookup"><span data-stu-id="9ef1a-149">AllowExternalOof</span></span>](allowexternaloof.md)
    
## <a name="getuseroofsettings-error-response-example"></a><span data-ttu-id="9ef1a-150">GetUserOofSettings 错误响应示例</span><span class="sxs-lookup"><span data-stu-id="9ef1a-150">GetUserOofSettings Error response example</span></span>

### <a name="description"></a><span data-ttu-id="9ef1a-151">说明</span><span class="sxs-lookup"><span data-stu-id="9ef1a-151">Description</span></span>

<span data-ttu-id="9ef1a-152">下面的示例演示尝试访问另一个用户的 OOF 信息时导致的错误响应。</span><span class="sxs-lookup"><span data-stu-id="9ef1a-152">The following example shows an error response caused by an attempt to access another user's OOF information.</span></span>
  
### <a name="code"></a><span data-ttu-id="9ef1a-153">代码</span><span class="sxs-lookup"><span data-stu-id="9ef1a-153">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <soap:Fault>
      <faultcode>soap:Client</faultcode>
      <faultstring>Microsoft.Exchange.Data.Storage.AccessDeniedException: User is not mailbox owner. User = S-1-5-21-3642464542-282065186-3871681729-1155, MailboxGuid = S-1-5-21-3642464542-282065186-3871681729-1156 ---> User is not mailbox owner. </faultstring>
      <faultactor>https://CAS01.example.com/EWS/Exchange.asmx</faultactor>
      <detail>
        <ErrorCode xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">-2146233088</ErrorCode>
      </detail>
    </soap:Fault>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="9ef1a-154">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9ef1a-154">See also</span></span>



- [<span data-ttu-id="9ef1a-155">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="9ef1a-155">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

