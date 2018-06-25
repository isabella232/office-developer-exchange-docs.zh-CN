---
title: SetOofStatus 操作 （UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- SetOofStatus
api_type:
- schema
ms.assetid: 97c271e9-506e-43eb-89cd-46803fc47ee5
description: SetOofStatus 操作设置一个值，该值指示是否应为发出请求的用户播放外出 (OOF) 问候语。
ms.openlocfilehash: 2bb1deeec8ddb5be56979bfb2fae3396672298a3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827445"
---
# <a name="setoofstatus-operation-um-web-service"></a><span data-ttu-id="70aae-103">SetOofStatus 操作 （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="70aae-103">SetOofStatus operation (UM web service)</span></span>

<span data-ttu-id="70aae-104">SetOofStatus 操作设置一个值，该值指示是否应为发出请求的用户播放外出 (OOF) 问候语。</span><span class="sxs-lookup"><span data-stu-id="70aae-104">The SetOofStatus operation sets a value that indicates whether the Out of Office (OOF) greeting should be played for the user who makes the request.</span></span>
  
## <a name="setoofstatus-request-example"></a><span data-ttu-id="70aae-105">SetOofStatus 请求示例</span><span class="sxs-lookup"><span data-stu-id="70aae-105">SetOofStatus request example</span></span>

### <a name="description"></a><span data-ttu-id="70aae-106">说明</span><span class="sxs-lookup"><span data-stu-id="70aae-106">Description</span></span>

<span data-ttu-id="70aae-107">SetOofStatus 请求的下面的示例演示如何以形成启用邮箱的外出问候语的请求。</span><span class="sxs-lookup"><span data-stu-id="70aae-107">The following example of a SetOofStatus request shows how to form a request to enable the Out of Office greeting for a mailbox.</span></span>
  
### <a name="code"></a><span data-ttu-id="70aae-108">代码</span><span class="sxs-lookup"><span data-stu-id="70aae-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetOofStatus xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
        <status>true</status>
    </SetOofStatus>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-setoofstatus-response-example"></a><span data-ttu-id="70aae-109">成功 SetOofStatus 响应示例</span><span class="sxs-lookup"><span data-stu-id="70aae-109">Successful SetOofStatus response example</span></span>

### <a name="description"></a><span data-ttu-id="70aae-110">说明</span><span class="sxs-lookup"><span data-stu-id="70aae-110">Description</span></span>

<span data-ttu-id="70aae-111">SetOofStatus 响应的下面的示例演示 SetOofStatus 请求的响应。</span><span class="sxs-lookup"><span data-stu-id="70aae-111">The following example of a SetOofStatus response shows a response to the SetOofStatus request.</span></span>
  
### <a name="code"></a><span data-ttu-id="70aae-112">代码</span><span class="sxs-lookup"><span data-stu-id="70aae-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetOofStatusResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="70aae-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="70aae-113">See also</span></span>



[<span data-ttu-id="70aae-114">SetOofStatus （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="70aae-114">SetOofStatus (UM web service)</span></span>](setoofstatus-um-web-service.md)
  
[<span data-ttu-id="70aae-115">SetOofStatusResponse （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="70aae-115">SetOofStatusResponse (UM web service)</span></span>](setoofstatusresponse-um-web-service.md)
  
[<span data-ttu-id="70aae-116">状态 （UM web 服务-SetOofStatus）</span><span class="sxs-lookup"><span data-stu-id="70aae-116">Status (UM web service - SetOofStatus)</span></span>](status-um-web-servicesetoofstatus.md)

