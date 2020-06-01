---
title: 订阅操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Subscribe
api_type:
- schema
ms.assetid: f17c3d08-c79e-41f1-ba31-6e41e7aafd87
description: 订阅操作用于将客户端应用程序订阅 "推送" 或 "请求" 通知。 请务必注意，请求消息和响应的结构是不同的，具体取决于事件通知的类型。
ms.openlocfilehash: c40e0e434f698c6535ff5d03fd4d45a453959dd6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/01/2020
ms.locfileid: "44467044"
---
# <a name="subscribe-operation"></a><span data-ttu-id="b7ead-104">订阅操作</span><span class="sxs-lookup"><span data-stu-id="b7ead-104">Subscribe operation</span></span>

<span data-ttu-id="b7ead-105">订阅操作用于将客户端应用程序订阅 "推送" 或 "请求" 通知。</span><span class="sxs-lookup"><span data-stu-id="b7ead-105">The Subscribe operation is used to subscribe client applications to either push or pull notifications.</span></span> <span data-ttu-id="b7ead-106">请务必注意，请求消息和响应的结构是不同的，具体取决于事件通知的类型。</span><span class="sxs-lookup"><span data-stu-id="b7ead-106">It is important to be aware that the structure of the request messages and responses is different depending on the type of event notification.</span></span> 
  
## <a name="pull-subscription-subscribe-request-example"></a><span data-ttu-id="b7ead-107">请求订阅订阅请求示例</span><span class="sxs-lookup"><span data-stu-id="b7ead-107">Pull Subscription Subscribe request example</span></span>

### <a name="description"></a><span data-ttu-id="b7ead-108">说明</span><span class="sxs-lookup"><span data-stu-id="b7ead-108">Description</span></span>

<span data-ttu-id="b7ead-109">下面的代码示例演示如何订阅 pull 事件通知订阅。</span><span class="sxs-lookup"><span data-stu-id="b7ead-109">The following code example shows how to subscribe to a pull event notification subscription.</span></span> <span data-ttu-id="b7ead-110">如果新邮件已添加到收件箱中，并且从收件箱中删除了某个项目，订阅将通知客户端应用程序。</span><span class="sxs-lookup"><span data-stu-id="b7ead-110">The subscription informs the client application if new mail is added to the Inbox and if an item is deleted from the Inbox.</span></span> <span data-ttu-id="b7ead-111">如果客户端未在10分钟内请求有关事件的信息，订阅将超时。</span><span class="sxs-lookup"><span data-stu-id="b7ead-111">The subscription will time out if the client does not request information about events within ten minutes.</span></span> <span data-ttu-id="b7ead-112">如果订阅过期，则必须建立新订阅才能继续请求通知。</span><span class="sxs-lookup"><span data-stu-id="b7ead-112">If the subscription expires, a new subscription must be established to continue to request notifications.</span></span>
  
### <a name="code"></a><span data-ttu-id="b7ead-113">代码</span><span class="sxs-lookup"><span data-stu-id="b7ead-113">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <Subscribe xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <PullSubscriptionRequest>
        <t:FolderIds>
          <t:DistinguishedFolderId Id="inbox"/>
        </t:FolderIds>
        <t:EventTypes>
          <t:EventType>NewMailEvent</t:EventType>
          <t:EventType>DeletedEvent</t:EventType>
        </t:EventTypes>
        <t:Timeout>10</t:Timeout>
      </PullSubscriptionRequest>
    </Subscribe>
  </soap:Body>
</soap:Envelope>
```

### <a name="pull-subscription-subscribe-request-elements"></a><span data-ttu-id="b7ead-114">请求订阅订阅请求元素</span><span class="sxs-lookup"><span data-stu-id="b7ead-114">Pull Subscription Subscribe Request Elements</span></span>

<span data-ttu-id="b7ead-115">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="b7ead-115">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="b7ead-116">订阅</span><span class="sxs-lookup"><span data-stu-id="b7ead-116">Subscribe</span></span>](subscribe.md)
    
- [<span data-ttu-id="b7ead-117">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="b7ead-117">PullSubscriptionRequest</span></span>](pullsubscriptionrequest.md)
    
- [<span data-ttu-id="b7ead-118">FolderIds</span><span class="sxs-lookup"><span data-stu-id="b7ead-118">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="b7ead-119">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="b7ead-119">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="b7ead-120">EventTypes</span><span class="sxs-lookup"><span data-stu-id="b7ead-120">EventTypes</span></span>](eventtypes.md)
    
- [<span data-ttu-id="b7ead-121">EventType</span><span class="sxs-lookup"><span data-stu-id="b7ead-121">EventType</span></span>](eventtype.md)
    
- [<span data-ttu-id="b7ead-122">Timeout</span><span class="sxs-lookup"><span data-stu-id="b7ead-122">Timeout</span></span>](timeout.md)
    
<span data-ttu-id="b7ead-123">若要查找订阅操作的请求邮件的其他选项，请浏览架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="b7ead-123">To find other options for the request message of the Subscribe operation, explore the schema hierarchy.</span></span> <span data-ttu-id="b7ead-124">从[PullSubscriptionRequest](pullsubscriptionrequest.md)元素开始。</span><span class="sxs-lookup"><span data-stu-id="b7ead-124">Start at the [PullSubscriptionRequest](pullsubscriptionrequest.md) element.</span></span> 
  
## <a name="successful-pull-subscription-subscribe-response-example"></a><span data-ttu-id="b7ead-125">成功的请求订阅订阅响应示例</span><span class="sxs-lookup"><span data-stu-id="b7ead-125">Successful Pull Subscription Subscribe response example</span></span>

### <a name="description"></a><span data-ttu-id="b7ead-126">说明</span><span class="sxs-lookup"><span data-stu-id="b7ead-126">Description</span></span>

<span data-ttu-id="b7ead-127">下面的示例展示了一个成功的请求订阅响应。</span><span class="sxs-lookup"><span data-stu-id="b7ead-127">The following example shows a successful pull subscription response.</span></span> <span data-ttu-id="b7ead-128">响应包含订阅标识符和用于获取与订阅关联的事件数组的水印。</span><span class="sxs-lookup"><span data-stu-id="b7ead-128">The response contains the subscription identifier and watermark that is used to get the array of events that are associated with a subscription.</span></span> <span data-ttu-id="b7ead-129">订阅标识符还用于从订阅中取消订阅客户端。</span><span class="sxs-lookup"><span data-stu-id="b7ead-129">The subscription identifier is also used to unsubscribe a client from a subscription.</span></span>
  
### <a name="code"></a><span data-ttu-id="b7ead-130">代码</span><span class="sxs-lookup"><span data-stu-id="b7ead-130">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SubscribeResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:SubscribeResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:SubscriptionId>39ea5d0f-f062-455e-a1e9-89c0304390f4</m:SubscriptionId>
          <m:Watermark>AAAAAHgGAAAAAAAAAQ==</m:Watermark>
        </m:SubscribeResponseMessage>
      </m:ResponseMessages>
    </SubscribeResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="pull-subscription-subscribe-response-elements"></a><span data-ttu-id="b7ead-131">请求订阅订阅响应元素</span><span class="sxs-lookup"><span data-stu-id="b7ead-131">Pull Subscription Subscribe response elements</span></span>

<span data-ttu-id="b7ead-132">响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="b7ead-132">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="b7ead-133">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="b7ead-133">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="b7ead-134">SubscribeResponse</span><span class="sxs-lookup"><span data-stu-id="b7ead-134">SubscribeResponse</span></span>](subscriberesponse.md)
    
- [<span data-ttu-id="b7ead-135">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="b7ead-135">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="b7ead-136">SubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="b7ead-136">SubscribeResponseMessage</span></span>](subscriberesponsemessage.md)
    
- [<span data-ttu-id="b7ead-137">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="b7ead-137">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="b7ead-138">SubscriptionId （GetEvents）</span><span class="sxs-lookup"><span data-stu-id="b7ead-138">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md)
    
- [<span data-ttu-id="b7ead-139">Watermark</span><span class="sxs-lookup"><span data-stu-id="b7ead-139">Watermark</span></span>](watermark.md)
    
## <a name="pull-subscription-subscribe-error-response-example"></a><span data-ttu-id="b7ead-140">请求订阅订阅错误响应示例</span><span class="sxs-lookup"><span data-stu-id="b7ead-140">Pull Subscription Subscribe Error response example</span></span>

### <a name="description"></a><span data-ttu-id="b7ead-141">说明</span><span class="sxs-lookup"><span data-stu-id="b7ead-141">Description</span></span>

<span data-ttu-id="b7ead-142">下面的示例演示对订阅请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="b7ead-142">The following example shows an error response to a Subscribe request.</span></span> <span data-ttu-id="b7ead-143">此错误是由于尝试使用代理访问来订阅通知而引起的。</span><span class="sxs-lookup"><span data-stu-id="b7ead-143">The error is caused by an attempt to subscribe to notifications by using delegate access.</span></span>
  
### <a name="code"></a><span data-ttu-id="b7ead-144">代码</span><span class="sxs-lookup"><span data-stu-id="b7ead-144">Code</span></span>

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
    <SubscribeResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:SubscribeResponseMessage ResponseClass="Error">
          <m:MessageText>Subscriptions are not supported for delegate user access.</m:MessageText>
          <m:ResponseCode>ErrorSubscriptionDelegateAccessNotSupported</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:SubscribeResponseMessage>
      </m:ResponseMessages>
    </SubscribeResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="pull-subscription-error-response-elements"></a><span data-ttu-id="b7ead-145">请求订阅错误响应元素</span><span class="sxs-lookup"><span data-stu-id="b7ead-145">Pull Subscription Error response elements</span></span>

<span data-ttu-id="b7ead-146">错误响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="b7ead-146">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="b7ead-147">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="b7ead-147">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="b7ead-148">SubscribeResponse</span><span class="sxs-lookup"><span data-stu-id="b7ead-148">SubscribeResponse</span></span>](subscriberesponse.md)
    
- [<span data-ttu-id="b7ead-149">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="b7ead-149">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="b7ead-150">SubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="b7ead-150">SubscribeResponseMessage</span></span>](subscriberesponsemessage.md)
    
- [<span data-ttu-id="b7ead-151">MessageText</span><span class="sxs-lookup"><span data-stu-id="b7ead-151">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="b7ead-152">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="b7ead-152">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="b7ead-153">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="b7ead-153">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="push-subscription-request-example"></a><span data-ttu-id="b7ead-154">推送订阅请求示例</span><span class="sxs-lookup"><span data-stu-id="b7ead-154">Push Subscription request example</span></span>

### <a name="description"></a><span data-ttu-id="b7ead-155">说明</span><span class="sxs-lookup"><span data-stu-id="b7ead-155">Description</span></span>

<span data-ttu-id="b7ead-156">下面的代码示例演示如何订阅推送事件通知订阅。</span><span class="sxs-lookup"><span data-stu-id="b7ead-156">The following code example shows how to subscribe to a push event notification subscription.</span></span> <span data-ttu-id="b7ead-157">请求标识要监视的文件夹、要监视的事件类型、状态通知的频率以及侦听推送通知的客户端 Web 服务的 URL。</span><span class="sxs-lookup"><span data-stu-id="b7ead-157">The request identifies the folders to monitor, the types of events to monitor, the frequency of status notifications, and the URL of the client Web service that listens for the push notifications.</span></span>
  
### <a name="code"></a><span data-ttu-id="b7ead-158">代码</span><span class="sxs-lookup"><span data-stu-id="b7ead-158">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <Subscribe xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <PushSubscriptionRequest xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
        <FolderIds xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <DistinguishedFolderId Id="inbox" />
        </FolderIds>
        <EventTypes xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <EventType>NewMailEvent</EventType>
          <EventType>CopiedEvent</EventType>
          <EventType>CreatedEvent</EventType>
          <EventType>DeletedEvent</EventType>
          <EventType>ModifiedEvent</EventType>
          <EventType>MovedEvent</EventType>
        </EventTypes>
        <StatusFrequency xmlns="https://schemas.microsoft.com/exchange/services/2006/types">1</StatusFrequency>
        <URL xmlns="https://schemas.microsoft.com/exchange/services/2006/types">http://clientWebService/Service.asmx</URL>
      </PushSubscriptionRequest>
    </Subscribe>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="b7ead-159">备注</span><span class="sxs-lookup"><span data-stu-id="b7ead-159">Comments</span></span>

<span data-ttu-id="b7ead-160">在发送推送通知订阅请求之前，必须设置客户端 Web 服务;否则，将不会向有效终结点发送第一个通知，并且推送通知将失败。</span><span class="sxs-lookup"><span data-stu-id="b7ead-160">The client Web service must be set up before the push notification subscribe request is sent; otherwise, the first notification will not be sent to a valid endpoint and the push notification will fail.</span></span> <span data-ttu-id="b7ead-161">有关详细信息，请参阅[推送通知示例应用程序](https://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="b7ead-161">For more information, see [Push Notification Sample Application](https://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx).</span></span>
  
<span data-ttu-id="b7ead-162">当您重新订阅时，将创建一个新的[SubscriptionId （GetEvents）](subscriptionid-getevents.md) 。</span><span class="sxs-lookup"><span data-stu-id="b7ead-162">A new [SubscriptionId (GetEvents)](subscriptionid-getevents.md) is created when you resubscribe.</span></span> <span data-ttu-id="b7ead-163">使用之前订阅的水印在上一个订阅结束的位置使用重新订阅。</span><span class="sxs-lookup"><span data-stu-id="b7ead-163">Use the watermark of a previous subscription to resubscribe at the point where the previous subscription ended.</span></span> 
  
### <a name="push-subscription-request-elements"></a><span data-ttu-id="b7ead-164">推送订阅请求元素</span><span class="sxs-lookup"><span data-stu-id="b7ead-164">Push Subscription Request Elements</span></span>

<span data-ttu-id="b7ead-165">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="b7ead-165">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="b7ead-166">订阅</span><span class="sxs-lookup"><span data-stu-id="b7ead-166">Subscribe</span></span>](subscribe.md)
    
- [<span data-ttu-id="b7ead-167">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="b7ead-167">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md)
    
- [<span data-ttu-id="b7ead-168">FolderIds</span><span class="sxs-lookup"><span data-stu-id="b7ead-168">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="b7ead-169">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="b7ead-169">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="b7ead-170">EventTypes</span><span class="sxs-lookup"><span data-stu-id="b7ead-170">EventTypes</span></span>](eventtypes.md)
    
- [<span data-ttu-id="b7ead-171">EventType</span><span class="sxs-lookup"><span data-stu-id="b7ead-171">EventType</span></span>](eventtype.md)
    
- [<span data-ttu-id="b7ead-172">StatusFrequency</span><span class="sxs-lookup"><span data-stu-id="b7ead-172">StatusFrequency</span></span>](statusfrequency.md)
    
- [<span data-ttu-id="b7ead-173">Url</span><span class="sxs-lookup"><span data-stu-id="b7ead-173">Url </span></span>](url-ex15websvcsotherref.md)
    
## <a name="successful-push-subscription-response-example"></a><span data-ttu-id="b7ead-174">成功的推送订阅响应示例</span><span class="sxs-lookup"><span data-stu-id="b7ead-174">Successful Push Subscription response example</span></span>

### <a name="description"></a><span data-ttu-id="b7ead-175">说明</span><span class="sxs-lookup"><span data-stu-id="b7ead-175">Description</span></span>

<span data-ttu-id="b7ead-176">下面的示例展示了一个成功的推送订阅响应。</span><span class="sxs-lookup"><span data-stu-id="b7ead-176">The following example shows a successful push subscription response.</span></span> 
  
### <a name="code"></a><span data-ttu-id="b7ead-177">代码</span><span class="sxs-lookup"><span data-stu-id="b7ead-177">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SubscribeResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseMessages>
        <SubscribeResponseMessage ResponseClass="Success">
          <ResponseCode>NoError</ResponseCode>
          <SubscriptionId>83826921-afdf-48be-b469-628cc02b5f49</SubscriptionId>
          <Watermark>AQAAAOpvG0LURVdOhQkPOWZLPcI8EgAAAAAAAAE=</Watermark>
        </SubscribeResponseMessage>
      </ResponseMessages>
    </SubscribeResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="push-subscription-response-elements"></a><span data-ttu-id="b7ead-178">推送订阅响应元素</span><span class="sxs-lookup"><span data-stu-id="b7ead-178">Push Subscription response elements</span></span>

<span data-ttu-id="b7ead-179">响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="b7ead-179">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="b7ead-180">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="b7ead-180">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="b7ead-181">SubscribeResponse</span><span class="sxs-lookup"><span data-stu-id="b7ead-181">SubscribeResponse</span></span>](subscriberesponse.md)
    
- [<span data-ttu-id="b7ead-182">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="b7ead-182">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="b7ead-183">SubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="b7ead-183">SubscribeResponseMessage</span></span>](subscriberesponsemessage.md)
    
- [<span data-ttu-id="b7ead-184">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="b7ead-184">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="b7ead-185">SubscriptionId （GetEvents）</span><span class="sxs-lookup"><span data-stu-id="b7ead-185">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md)
    
- [<span data-ttu-id="b7ead-186">Watermark</span><span class="sxs-lookup"><span data-stu-id="b7ead-186">Watermark</span></span>](watermark.md)
    
## <a name="see-also"></a><span data-ttu-id="b7ead-187">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b7ead-187">See also</span></span>



[<span data-ttu-id="b7ead-188">取消订阅操作</span><span class="sxs-lookup"><span data-stu-id="b7ead-188">Unsubscribe operation</span></span>](unsubscribe-operation.md)
  
[<span data-ttu-id="b7ead-189">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="b7ead-189">GetEvents operation</span></span>](getevents-operation.md)


[<span data-ttu-id="b7ead-190">使用请求订阅</span><span class="sxs-lookup"><span data-stu-id="b7ead-190">Using Pull Subscriptions</span></span>](https://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx)
  
[<span data-ttu-id="b7ead-191">推送通知示例应用程序</span><span class="sxs-lookup"><span data-stu-id="b7ead-191">Push Notification Sample Application</span></span>](https://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx)

