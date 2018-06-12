---
title: GetCallInfo 操作 （UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- GetCallInfo
api_type:
- schema
ms.assetid: 6bccd418-caf7-4eb9-8a6f-410e56a635c3
description: GetCallInfo 操作返回由 CallId （UM web 服务） 指定的出站呼叫的状态。
ms.openlocfilehash: 36f9cba3690520ebb457a4cb2bfbcde3fea4b8dc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754475"
---
# <a name="getcallinfo-operation-um-web-service"></a><span data-ttu-id="6bd2b-103">GetCallInfo 操作 （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="6bd2b-103">GetCallInfo operation (UM web service)</span></span>

<span data-ttu-id="6bd2b-104">GetCallInfo 操作返回由[CallId （UM web 服务）](callid-um-web-service.md)指定的出站呼叫的状态。</span><span class="sxs-lookup"><span data-stu-id="6bd2b-104">The GetCallInfo operation returns the status of the outbound call that is specified by [CallId (UM web service)](callid-um-web-service.md).</span></span>
  
## <a name="getcallinfo-request-example"></a><span data-ttu-id="6bd2b-105">GetCallInfo 请求示例</span><span class="sxs-lookup"><span data-stu-id="6bd2b-105">GetCallInfo request example</span></span>

### <a name="description"></a><span data-ttu-id="6bd2b-106">说明</span><span class="sxs-lookup"><span data-stu-id="6bd2b-106">Description</span></span>

<span data-ttu-id="6bd2b-107">GetCallInfo 请求的下面的示例演示如何以形成一个请求以获取有关指定的出站呼叫的信息。</span><span class="sxs-lookup"><span data-stu-id="6bd2b-107">The following example of a GetCallInfo request shows how to form a request to get information about a specified outbound call.</span></span>
  
### <a name="code"></a><span data-ttu-id="6bd2b-108">代码</span><span class="sxs-lookup"><span data-stu-id="6bd2b-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetCallInfo xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <CallId>MDlkZjllZGMtNGUyMy00NzA5LWJkYWYtN2JlMjBjYjBhZTU2QGRmLWV1bS0wMS5leGNoYW5nZS5jb3JwLm1pY3Jvc29mdC5jb20=</CallId>
    </GetCallInfo>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-getcallinfo-response-example"></a><span data-ttu-id="6bd2b-109">成功 GetCallInfo 响应示例</span><span class="sxs-lookup"><span data-stu-id="6bd2b-109">Successful GetCallInfo response example</span></span>

### <a name="description"></a><span data-ttu-id="6bd2b-110">说明</span><span class="sxs-lookup"><span data-stu-id="6bd2b-110">Description</span></span>

<span data-ttu-id="6bd2b-111">GetCallInfo 响应的下面的示例演示 GetCallInfo 请求的响应。</span><span class="sxs-lookup"><span data-stu-id="6bd2b-111">The following example of a GetCallInfo response shows a response to a GetCallInfo request.</span></span>
  
### <a name="code"></a><span data-ttu-id="6bd2b-112">代码</span><span class="sxs-lookup"><span data-stu-id="6bd2b-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <GetCallInfoResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <GetCallInfoResponse>
        <CallState>Connected</CallState> 
        <EventCause>None</EventCause> 
      </GetCallInfoResponse>
    </GetCallInfoResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="6bd2b-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6bd2b-113">See also</span></span>



[<span data-ttu-id="6bd2b-114">GetCallInfo （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="6bd2b-114">GetCallInfo (UM web service)</span></span>](getcallinfo-um-web-service.md)
  
[<span data-ttu-id="6bd2b-115">GetCallInfoResponse （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="6bd2b-115">GetCallInfoResponse (UM web service)</span></span>](getcallinforesponse-um-web-service.md)
  
[<span data-ttu-id="6bd2b-116">CallId （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="6bd2b-116">CallId (UM web service)</span></span>](callid-um-web-service.md)
  
[<span data-ttu-id="6bd2b-117">CallState （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="6bd2b-117">CallState (UM web service)</span></span>](callstate-um-web-service.md)
  
[<span data-ttu-id="6bd2b-118">EventCause （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="6bd2b-118">EventCause (UM web service)</span></span>](eventcause-um-web-service.md)
