---
title: PlayOnPhone 操作 (EWS)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PlayOnPhone
api_type:
- schema
ms.assetid: 70e6ef33-2046-4eb8-9987-e106009be04b
description: PlayOnPhone 操作发起出站呼叫，并通过电话播放消息。
ms.openlocfilehash: ec77720c69862e210316d61975b0d58c9530a40c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826819"
---
# <a name="playonphone-operation-ews"></a><span data-ttu-id="70a22-103">PlayOnPhone 操作 (EWS)</span><span class="sxs-lookup"><span data-stu-id="70a22-103">PlayOnPhone operation (EWS)</span></span>

<span data-ttu-id="70a22-104">**PlayOnPhone**操作发起出站呼叫，并通过电话播放消息。</span><span class="sxs-lookup"><span data-stu-id="70a22-104">The **PlayOnPhone** operation initiates an outbound call and plays a message over the telephone.</span></span> 
  
## <a name="playonphone-request-example"></a><span data-ttu-id="70a22-105">PlayOnPhone 请求示例</span><span class="sxs-lookup"><span data-stu-id="70a22-105">PlayOnPhone request example</span></span>

### <a name="description"></a><span data-ttu-id="70a22-106">说明</span><span class="sxs-lookup"><span data-stu-id="70a22-106">Description</span></span>

<span data-ttu-id="70a22-107">**PlayOnPhone**请求的下面的示例演示如何以形成一个请求在电话上播放消息。</span><span class="sxs-lookup"><span data-stu-id="70a22-107">The following example of a **PlayOnPhone** request shows how to form a request to play a message on a phone.</span></span> 
  
### <a name="code"></a><span data-ttu-id="70a22-108">代码</span><span class="sxs-lookup"><span data-stu-id="70a22-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xs="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:PlayOnPhone>
      <m:ItemId Id="AkAjzQTbY/i="/>
      <m:DialString>5555551212</m:DialString>
    </m:PlayOnPhone>
  </soap:Body>
</soap:Envelope>
```

## <a name="playonphone-response-example"></a><span data-ttu-id="70a22-109">PlayOnPhone 响应示例</span><span class="sxs-lookup"><span data-stu-id="70a22-109">PlayOnPhone response example</span></span>

### <a name="description"></a><span data-ttu-id="70a22-110">说明</span><span class="sxs-lookup"><span data-stu-id="70a22-110">Description</span></span>

<span data-ttu-id="70a22-111">下面的示例演示对**PlayOnPhone**请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="70a22-111">The following example shows a successful response to the **PlayOnPhone** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="70a22-112">代码</span><span class="sxs-lookup"><span data-stu-id="70a22-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="20" 
                         Version="Exchange2010" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <PlayOnPhoneResponse ResponseClass="Success" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <PhoneCallId Id="ZWMtWYtMY29t"/>
    </PlayOnPhoneResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="70a22-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="70a22-113">See also</span></span>

- [<span data-ttu-id="70a22-114">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="70a22-114">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
- [<span data-ttu-id="70a22-115">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="70a22-115">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

