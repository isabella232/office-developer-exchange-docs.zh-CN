---
title: SetUserOofSettings 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SetUserOofSettings
api_type:
- schema
ms.assetid: 36277ef0-18ee-4b35-9e6e-8c321d8f5433
description: SetUserOofSettings Web 方法设置邮箱用户的外出（OOF）设置和邮件。
ms.openlocfilehash: 88b5475dd2f0fe6d334bad51a0fe8d0beb767634
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463151"
---
# <a name="setuseroofsettings-operation"></a><span data-ttu-id="178b5-103">SetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="178b5-103">SetUserOofSettings operation</span></span>

<span data-ttu-id="178b5-104">**SetUserOofSettings** Web 方法设置邮箱用户的外出（OOF）设置和邮件。</span><span class="sxs-lookup"><span data-stu-id="178b5-104">The **SetUserOofSettings** Web method sets a mailbox user's Out of Office (OOF) settings and message.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="178b5-105">SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="178b5-105">SOAP Headers</span></span>

<span data-ttu-id="178b5-106">**SetUserOofSettings**操作可以使用下表中列出和描述的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="178b5-106">The **SetUserOofSettings** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="178b5-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="178b5-107">**Header**</span></span>|<span data-ttu-id="178b5-108">**元素**</span><span class="sxs-lookup"><span data-stu-id="178b5-108">**Element**</span></span>|<span data-ttu-id="178b5-109">**说明**</span><span class="sxs-lookup"><span data-stu-id="178b5-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="178b5-110">模拟</span><span class="sxs-lookup"><span data-stu-id="178b5-110">Impersonation</span></span>  <br/> |[<span data-ttu-id="178b5-111">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="178b5-111">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="178b5-112">标识客户端应用程序模拟的用户。</span><span class="sxs-lookup"><span data-stu-id="178b5-112">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="178b5-113">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="178b5-113">ServerVersion</span></span>  <br/> |[<span data-ttu-id="178b5-114">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="178b5-114">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="178b5-115">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="178b5-115">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="setuseroofsettings-request-example"></a><span data-ttu-id="178b5-116">SetUserOofSettings 请求示例</span><span class="sxs-lookup"><span data-stu-id="178b5-116">SetUserOofSettings request example</span></span>

### <a name="description"></a><span data-ttu-id="178b5-117">说明</span><span class="sxs-lookup"><span data-stu-id="178b5-117">Description</span></span>

<span data-ttu-id="178b5-118">以下示例的**SetUserOofSettings**请求将 OOF 设置设置为10天。</span><span class="sxs-lookup"><span data-stu-id="178b5-118">The following example of a **SetUserOofSettings** request sets an OOF setting for 10 days.</span></span> 
  
### <a name="code"></a><span data-ttu-id="178b5-119">代码</span><span class="sxs-lookup"><span data-stu-id="178b5-119">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetUserOofSettingsRequest xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <Mailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
        <Name>User1</Name>
        <Address>user1@example.com</Address>
        <RoutingType>SMTP</RoutingType>
      </Mailbox>
      <UserOofSettings xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
        <OofState>Enabled</OofState>
        <ExternalAudience>All</ExternalAudience>
        <Duration>
          <StartTime>2006-10-05T00:00:00</StartTime>
          <EndTime>2006-10-25T00:00:00</EndTime>
        </Duration>
        <InternalReply>
          <Message>I am out of office.  This is my internal reply.</Message>
        </InternalReply>
        <ExternalReply>
          <Message>I am out of office. This is my external reply.</Message>
        </ExternalReply>
      </UserOofSettings>
    </SetUserOofSettingsRequest>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="178b5-120">Request 元素</span><span class="sxs-lookup"><span data-stu-id="178b5-120">Request elements</span></span>

<span data-ttu-id="178b5-121">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="178b5-121">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="178b5-122">SetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="178b5-122">SetUserOofSettingsRequest</span></span>](setuseroofsettingsrequest.md)
    
- [<span data-ttu-id="178b5-123">邮箱（可用性）</span><span class="sxs-lookup"><span data-stu-id="178b5-123">Mailbox (Availability)</span></span>](mailbox-availability.md)
    
- [<span data-ttu-id="178b5-124">名称（EmailAddress）</span><span class="sxs-lookup"><span data-stu-id="178b5-124">Name (EmailAddress)</span></span>](name-emailaddress.md)
    
- [<span data-ttu-id="178b5-125">Address （string）</span><span class="sxs-lookup"><span data-stu-id="178b5-125">Address (string)</span></span>](address-string.md)
    
- [<span data-ttu-id="178b5-126">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="178b5-126">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md)
    
- [<span data-ttu-id="178b5-127">UserOofSettings</span><span class="sxs-lookup"><span data-stu-id="178b5-127">UserOofSettings</span></span>](useroofsettings.md)
    
- [<span data-ttu-id="178b5-128">OofState</span><span class="sxs-lookup"><span data-stu-id="178b5-128">OofState</span></span>](oofstate.md)
    
- [<span data-ttu-id="178b5-129">ExternalAudience</span><span class="sxs-lookup"><span data-stu-id="178b5-129">ExternalAudience</span></span>](externalaudience.md)
    
- [<span data-ttu-id="178b5-130">持续时间（UserOofSettings）</span><span class="sxs-lookup"><span data-stu-id="178b5-130">Duration (UserOofSettings)</span></span>](duration-useroofsettings.md)
    
- [<span data-ttu-id="178b5-131">StartTime</span><span class="sxs-lookup"><span data-stu-id="178b5-131">StartTime</span></span>](starttime.md)
    
- [<span data-ttu-id="178b5-132">EndTime</span><span class="sxs-lookup"><span data-stu-id="178b5-132">EndTime</span></span>](endtime.md)
    
- [<span data-ttu-id="178b5-133">InternalReply</span><span class="sxs-lookup"><span data-stu-id="178b5-133">InternalReply</span></span>](internalreply.md)
    
- [<span data-ttu-id="178b5-134">邮件（可用性）</span><span class="sxs-lookup"><span data-stu-id="178b5-134">Message (Availability)</span></span>](message-availability.md)
    
- [<span data-ttu-id="178b5-135">ExternalReply</span><span class="sxs-lookup"><span data-stu-id="178b5-135">ExternalReply</span></span>](externalreply.md)
    
## <a name="successful-setuseroofsettings-response-example"></a><span data-ttu-id="178b5-136">成功的 SetUserOofSettings 响应示例</span><span class="sxs-lookup"><span data-stu-id="178b5-136">Successful SetUserOofSettings response example</span></span>

### <a name="description"></a><span data-ttu-id="178b5-137">说明</span><span class="sxs-lookup"><span data-stu-id="178b5-137">Description</span></span>

<span data-ttu-id="178b5-138">下面的示例演示对**SetUserOofSettings**请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="178b5-138">The following example shows a successful response to the **SetUserOofSettings** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="178b5-139">代码</span><span class="sxs-lookup"><span data-stu-id="178b5-139">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" /> 
  </soap:Header>
  <soap:Body>
    <SetUserOofSettingsResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseMessage ResponseClass="Success">
        <ResponseCode>NoError</ResponseCode> 
      </ResponseMessage>
    </SetUserOofSettingsResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a><span data-ttu-id="178b5-140">成功的响应元素</span><span class="sxs-lookup"><span data-stu-id="178b5-140">Successful response elements</span></span>

<span data-ttu-id="178b5-141">响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="178b5-141">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="178b5-142">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="178b5-142">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="178b5-143">SetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="178b5-143">SetUserOofSettingsResponse</span></span>](setuseroofsettingsresponse.md)
    
- [<span data-ttu-id="178b5-144">ResponseMessage</span><span class="sxs-lookup"><span data-stu-id="178b5-144">ResponseMessage</span></span>](responsemessage.md)
    
- [<span data-ttu-id="178b5-145">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="178b5-145">ResponseCode</span></span>](responsecode.md)
    
## <a name="see-also"></a><span data-ttu-id="178b5-146">另请参阅</span><span class="sxs-lookup"><span data-stu-id="178b5-146">See also</span></span>



- [<span data-ttu-id="178b5-147">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="178b5-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

