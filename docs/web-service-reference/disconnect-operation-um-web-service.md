---
title: 断开连接操作 （UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- Disconnect
api_type:
- schema
ms.assetid: a987000b-d6e6-49d7-944c-e9c278d0236f
description: 断开连接操作终止呼叫是由指定 CallId （UM web 服务）。
ms.openlocfilehash: 1e04e65fa1951a6aa46e2c8b6dd5fe524c84a8fc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753902"
---
# <a name="disconnect-operation-um-web-service"></a><span data-ttu-id="598df-103">断开连接操作 （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="598df-103">Disconnect operation (UM web service)</span></span>

<span data-ttu-id="598df-104">断开连接操作终止呼叫是由指定[CallId （UM web 服务）](callid-um-web-service.md)。</span><span class="sxs-lookup"><span data-stu-id="598df-104">The Disconnect operation terminates the call that is identified by the specified [CallId (UM web service)](callid-um-web-service.md).</span></span>
  
## <a name="disconnect-request-example"></a><span data-ttu-id="598df-105">断开连接请求示例</span><span class="sxs-lookup"><span data-stu-id="598df-105">Disconnect request example</span></span>

### <a name="description"></a><span data-ttu-id="598df-106">说明</span><span class="sxs-lookup"><span data-stu-id="598df-106">Description</span></span>

<span data-ttu-id="598df-107">断开连接请求的下面的示例演示如何以形成一个要断开呼叫的请求。</span><span class="sxs-lookup"><span data-stu-id="598df-107">The following example of a Disconnect request shows how to form a request to disconnect a call.</span></span>
  
### <a name="code"></a><span data-ttu-id="598df-108">代码</span><span class="sxs-lookup"><span data-stu-id="598df-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <Disconnect xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <CallId>MDlkZjllZGMtNGUyMy00NzA5LWJkYWYtN2JlMjBjYjBhZTU2QGRmLWV1bS0wMS5leGNoYW5nZS5jb3JwLm1pY3Jvc29mdC5jb20=</CallId>
    </Disconnect>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-disconnect-response-example"></a><span data-ttu-id="598df-109">成功断开响应示例</span><span class="sxs-lookup"><span data-stu-id="598df-109">Successful Disconnect response example</span></span>

### <a name="description"></a><span data-ttu-id="598df-110">说明</span><span class="sxs-lookup"><span data-stu-id="598df-110">Description</span></span>

<span data-ttu-id="598df-111">断开连接的响应的下面的示例演示对断开连接的请求的响应。</span><span class="sxs-lookup"><span data-stu-id="598df-111">The following example of a Disconnect response shows a response to the Disconnect request.</span></span>
  
### <a name="code"></a><span data-ttu-id="598df-112">代码</span><span class="sxs-lookup"><span data-stu-id="598df-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <DisconnectResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="598df-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="598df-113">See also</span></span>

- [<span data-ttu-id="598df-114">断开连接 （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="598df-114">Disconnect (UM web service)</span></span>](disconnect-um-web-service.md) 
- [<span data-ttu-id="598df-115">DisconnectResponse （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="598df-115">DisconnectResponse (UM web service)</span></span>](disconnectresponse-um-web-service.md) 
- [<span data-ttu-id="598df-116">CallId （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="598df-116">CallId (UM web service)</span></span>](callid-um-web-service.md)

