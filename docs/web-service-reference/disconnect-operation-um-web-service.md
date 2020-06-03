---
title: 断开连接操作（UM web 服务）
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
description: 断开连接操作将终止由指定的 CallId （UM web 服务）标识的呼叫。
ms.openlocfilehash: a1268f9ea3d879f472e019bf1847fc13d65d1819
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529068"
---
# <a name="disconnect-operation-um-web-service"></a><span data-ttu-id="b7642-103">断开连接操作（UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="b7642-103">Disconnect operation (UM web service)</span></span>

<span data-ttu-id="b7642-104">断开连接操作将终止由指定的[CallId （UM web 服务）](callid-um-web-service.md)标识的呼叫。</span><span class="sxs-lookup"><span data-stu-id="b7642-104">The Disconnect operation terminates the call that is identified by the specified [CallId (UM web service)](callid-um-web-service.md).</span></span>
  
## <a name="disconnect-request-example"></a><span data-ttu-id="b7642-105">断开连接请求示例</span><span class="sxs-lookup"><span data-stu-id="b7642-105">Disconnect request example</span></span>

### <a name="description"></a><span data-ttu-id="b7642-106">Description</span><span class="sxs-lookup"><span data-stu-id="b7642-106">Description</span></span>

<span data-ttu-id="b7642-107">下面的一个断开请求示例演示如何形成一个请求以断开呼叫。</span><span class="sxs-lookup"><span data-stu-id="b7642-107">The following example of a Disconnect request shows how to form a request to disconnect a call.</span></span>
  
### <a name="code"></a><span data-ttu-id="b7642-108">代码</span><span class="sxs-lookup"><span data-stu-id="b7642-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <Disconnect xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <CallId>MDlkZjllZGMtNGUyMy00NzA5LWJkYWYtN2JlMjBjYjBhZTU2QGRmLWV1bS0wMS5leGNoYW5nZS5jb3JwLm1pY3Jvc29mdC5jb20=</CallId>
    </Disconnect>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-disconnect-response-example"></a><span data-ttu-id="b7642-109">成功的断开连接响应示例</span><span class="sxs-lookup"><span data-stu-id="b7642-109">Successful Disconnect response example</span></span>

### <a name="description"></a><span data-ttu-id="b7642-110">Description</span><span class="sxs-lookup"><span data-stu-id="b7642-110">Description</span></span>

<span data-ttu-id="b7642-111">以下示例中的 "断开连接" 响应显示对断开连接请求的响应。</span><span class="sxs-lookup"><span data-stu-id="b7642-111">The following example of a Disconnect response shows a response to the Disconnect request.</span></span>
  
### <a name="code"></a><span data-ttu-id="b7642-112">代码</span><span class="sxs-lookup"><span data-stu-id="b7642-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <DisconnectResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="b7642-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b7642-113">See also</span></span>

- [<span data-ttu-id="b7642-114">断开连接（UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="b7642-114">Disconnect (UM web service)</span></span>](disconnect-um-web-service.md) 
- [<span data-ttu-id="b7642-115">DisconnectResponse （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="b7642-115">DisconnectResponse (UM web service)</span></span>](disconnectresponse-um-web-service.md) 
- [<span data-ttu-id="b7642-116">CallId （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="b7642-116">CallId (UM web service)</span></span>](callid-um-web-service.md)

