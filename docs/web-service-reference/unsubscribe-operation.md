---
title: 取消操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Unsubscribe
api_type:
- schema
ms.assetid: 994a9d2b-1501-4804-90f0-12bd914496ec
description: 取消操作用于结束请求通知订阅。 使用此操作，而不是让订阅超时。 此操作才有效出现通知。
ms.openlocfilehash: 64514a718d473f0fd7d0320bd1ccecddb1940ac8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838357"
---
# <a name="unsubscribe-operation"></a><span data-ttu-id="5b6d5-105">取消操作</span><span class="sxs-lookup"><span data-stu-id="5b6d5-105">Unsubscribe operation</span></span>

<span data-ttu-id="5b6d5-106">取消操作用于结束请求通知订阅。</span><span class="sxs-lookup"><span data-stu-id="5b6d5-106">The Unsubscribe operation is used to end a pull notification subscription.</span></span> <span data-ttu-id="5b6d5-107">使用此操作，而不是让订阅超时。</span><span class="sxs-lookup"><span data-stu-id="5b6d5-107">Use this operation rather than letting a subscription timeout.</span></span> <span data-ttu-id="5b6d5-108">此操作才有效出现通知。</span><span class="sxs-lookup"><span data-stu-id="5b6d5-108">This operation is only valid for pull notifications.</span></span>
  
## <a name="unsubscribe-request-example"></a><span data-ttu-id="5b6d5-109">取消订阅请求示例</span><span class="sxs-lookup"><span data-stu-id="5b6d5-109">Unsubscribe request example</span></span>

### <a name="description"></a><span data-ttu-id="5b6d5-110">说明</span><span class="sxs-lookup"><span data-stu-id="5b6d5-110">Description</span></span>

<span data-ttu-id="5b6d5-111">下面的示例演示发送，以取消订阅通知服务的客户端的 SOAP XML 消息。</span><span class="sxs-lookup"><span data-stu-id="5b6d5-111">The following example shows the SOAP XML message that is sent to unsubscribe a client from the Notification service.</span></span>
  
### <a name="code"></a><span data-ttu-id="5b6d5-112">代码</span><span class="sxs-lookup"><span data-stu-id="5b6d5-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <Unsubscribe xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <SubscriptionId>e6fbf5c1-7e26-4bc6-a5f2-882063d5e34e</SubscriptionId>  
    </Unsubscribe>
  </soap:Body>
</soap:Envelope>
```

### <a name="unsubscribe-request-elements"></a><span data-ttu-id="5b6d5-113">取消订阅请求元素</span><span class="sxs-lookup"><span data-stu-id="5b6d5-113">Unsubscribe request elements</span></span>

<span data-ttu-id="5b6d5-114">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="5b6d5-114">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="5b6d5-115">取消订阅</span><span class="sxs-lookup"><span data-stu-id="5b6d5-115">Unsubscribe</span></span>](unsubscribe.md)
    
- [<span data-ttu-id="5b6d5-116">SubscriptionId (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="5b6d5-116">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md)
    
## <a name="successful-unsubscribe-response-example"></a><span data-ttu-id="5b6d5-117">成功取消订阅响应示例</span><span class="sxs-lookup"><span data-stu-id="5b6d5-117">Successful Unsubscribe response example</span></span>

### <a name="description"></a><span data-ttu-id="5b6d5-118">说明</span><span class="sxs-lookup"><span data-stu-id="5b6d5-118">Description</span></span>

<span data-ttu-id="5b6d5-119">下面的示例演示取消订阅请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="5b6d5-119">The following example shows a successful response to an Unsubscribe request.</span></span>
  
### <a name="code"></a><span data-ttu-id="5b6d5-120">代码</span><span class="sxs-lookup"><span data-stu-id="5b6d5-120">Code</span></span>

```xml
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <UnsubscribeResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:UnsubscribeResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:UnsubscribeResponseMessage>
      </m:ResponseMessages>
    </UnsubscribeResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="unsubscribe-response-elements"></a><span data-ttu-id="5b6d5-121">取消订阅响应元素</span><span class="sxs-lookup"><span data-stu-id="5b6d5-121">Unsubscribe response elements</span></span>

<span data-ttu-id="5b6d5-122">在响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="5b6d5-122">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="5b6d5-123">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="5b6d5-123">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="5b6d5-124">取消订阅</span><span class="sxs-lookup"><span data-stu-id="5b6d5-124">Unsubscribe</span></span>](unsubscribe.md)
    
- [<span data-ttu-id="5b6d5-125">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="5b6d5-125">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="5b6d5-126">UnsubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="5b6d5-126">UnsubscribeResponseMessage</span></span>](unsubscriberesponsemessage.md)
    
- [<span data-ttu-id="5b6d5-127">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="5b6d5-127">ResponseCode</span></span>](responsecode.md)
    
## <a name="unsubscribe-error-response-example"></a><span data-ttu-id="5b6d5-128">取消订阅错误响应示例</span><span class="sxs-lookup"><span data-stu-id="5b6d5-128">Unsubscribe Error response example</span></span>

### <a name="description"></a><span data-ttu-id="5b6d5-129">说明</span><span class="sxs-lookup"><span data-stu-id="5b6d5-129">Description</span></span>

<span data-ttu-id="5b6d5-130">下面的示例取消订阅错误响应发生响应尝试使用找不到订阅标识符取消订阅 Exchange 存储中。</span><span class="sxs-lookup"><span data-stu-id="5b6d5-130">The following example of an Unsubscribe error response occurs in response to an attempt to unsubscribe by using a subscription identifier that cannot be located in the Exchange store.</span></span>
  
### <a name="code"></a><span data-ttu-id="5b6d5-131">代码</span><span class="sxs-lookup"><span data-stu-id="5b6d5-131">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <UnsubscribeResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:UnsubscribeResponseMessage ResponseClass="Error">
          <m:MessageText>The specified subscription was not found.</m:MessageText>
          <m:ResponseCode>ErrorSubscriptionNotFound</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:UnsubscribeResponseMessage>
      </m:ResponseMessages>
    </UnsubscribeResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="unsubscribe-error-response-elements"></a><span data-ttu-id="5b6d5-132">取消订阅错误响应元素</span><span class="sxs-lookup"><span data-stu-id="5b6d5-132">Unsubscribe Error response elements</span></span>

<span data-ttu-id="5b6d5-133">错误响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="5b6d5-133">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="5b6d5-134">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="5b6d5-134">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="5b6d5-135">UnsubscribeResponse</span><span class="sxs-lookup"><span data-stu-id="5b6d5-135">UnsubscribeResponse</span></span>](unsubscriberesponse.md)
    
- [<span data-ttu-id="5b6d5-136">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="5b6d5-136">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="5b6d5-137">UnsubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="5b6d5-137">UnsubscribeResponseMessage</span></span>](unsubscriberesponsemessage.md)
    
- [<span data-ttu-id="5b6d5-138">MessageText</span><span class="sxs-lookup"><span data-stu-id="5b6d5-138">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="5b6d5-139">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="5b6d5-139">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="5b6d5-140">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="5b6d5-140">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="5b6d5-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5b6d5-141">See also</span></span>

- [<span data-ttu-id="5b6d5-142">订阅操作</span><span class="sxs-lookup"><span data-stu-id="5b6d5-142">Subscribe operation</span></span>](subscribe-operation.md)
- [<span data-ttu-id="5b6d5-143">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="5b6d5-143">GetEvents operation</span></span>](getevents-operation.md)
- [<span data-ttu-id="5b6d5-144">使用请求订阅</span><span class="sxs-lookup"><span data-stu-id="5b6d5-144">Using Pull Subscriptions</span></span>](http://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx)

