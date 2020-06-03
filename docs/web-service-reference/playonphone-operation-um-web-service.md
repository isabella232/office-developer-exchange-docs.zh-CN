---
title: PlayOnPhone 操作（UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- PlayOnPhone
api_type:
- schema
ms.assetid: 7d55be55-f8b6-4e96-a61e-26fa190217fd
description: PlayOnPhone 操作发出出站呼叫，并通过 DialString 元素指定的电话播放指定的邮件。
ms.openlocfilehash: c5ff82bcd822aa2c659d1782ea4a1349d198bc80
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466232"
---
# <a name="playonphone-operation-um-web-service"></a><span data-ttu-id="088bc-103">PlayOnPhone 操作（UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="088bc-103">PlayOnPhone operation (UM web service)</span></span>

<span data-ttu-id="088bc-104">PlayOnPhone 操作发出出站呼叫，并通过**DialString**元素指定的电话播放指定的邮件。</span><span class="sxs-lookup"><span data-stu-id="088bc-104">The PlayOnPhone operation makes an outbound call and plays a specified message over the telephone that is specified by the **DialString** element.</span></span> 
  
## <a name="playonphone-request-example"></a><span data-ttu-id="088bc-105">PlayOnPhone 请求示例</span><span class="sxs-lookup"><span data-stu-id="088bc-105">PlayOnPhone request example</span></span>

### <a name="description"></a><span data-ttu-id="088bc-106">Description</span><span class="sxs-lookup"><span data-stu-id="088bc-106">Description</span></span>

<span data-ttu-id="088bc-107">以下示例的 PlayOnPhone 请求显示如何形成发出出站呼叫和播放邮件的请求。</span><span class="sxs-lookup"><span data-stu-id="088bc-107">The following example of a PlayOnPhone request shows how to form a request to make an outbound call and play a message.</span></span>
  
### <a name="code"></a><span data-ttu-id="088bc-108">代码</span><span class="sxs-lookup"><span data-stu-id="088bc-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <PlayOnPhone xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <entryId>AAAAAGsd2rbQLVtLobUGbrq/9IUHAEX2ikn/L8JJtI5WHI0FAW8AAAFXHhsAACxVpEl+KVVLl957wp//x6UAGAetcDUAAA==</entryId>
      <DialString>12345</DialString>
    </PlayOnPhone>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-playonphone-response-example"></a><span data-ttu-id="088bc-109">成功的 PlayOnPhone 响应示例</span><span class="sxs-lookup"><span data-stu-id="088bc-109">Successful PlayOnPhone response example</span></span>

### <a name="description"></a><span data-ttu-id="088bc-110">Description</span><span class="sxs-lookup"><span data-stu-id="088bc-110">Description</span></span>

<span data-ttu-id="088bc-111">下面的 PlayOnPhone 响应示例显示对 PlayOnPhone 请求的响应。</span><span class="sxs-lookup"><span data-stu-id="088bc-111">The following example of a PlayOnPhone response shows a response to the PlayOnPhone request.</span></span>
  
### <a name="code"></a><span data-ttu-id="088bc-112">代码</span><span class="sxs-lookup"><span data-stu-id="088bc-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <PlayOnPhoneResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <PlayOnPhoneResponse>NDEzYjEzNmMtZTE2Zi00NTJlLWI3YzctNDhkMTE3MDE3YjlmQGRmLWV1bS0wMS5leGNoYW5nZS5jb3JwLm1pY3Jvc29mdC5jb20=</PlayOnPhoneResponse> 
    </PlayOnPhoneResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="088bc-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="088bc-113">See also</span></span>



[<span data-ttu-id="088bc-114">PlayOnPhone （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="088bc-114">PlayOnPhone (UM web service)</span></span>](playonphone-um-web-service.md)
  
[<span data-ttu-id="088bc-115">PlayOnPhoneResponse （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="088bc-115">PlayOnPhoneResponse (UM web service)</span></span>](playonphoneresponse-um-web-service.md)
  
[<span data-ttu-id="088bc-116">PlayOnPhoneGreeting 操作（UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="088bc-116">PlayOnPhoneGreeting operation (UM web service)</span></span>](playonphonegreeting-operation-um-web-service.md)

