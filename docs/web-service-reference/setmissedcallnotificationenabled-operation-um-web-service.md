---
title: SetMissedCallNotificationEnabled 操作（UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- SetMissedCallNotificationEnabled
api_type:
- schema
ms.assetid: 6693b5db-ac6b-43bc-af83-a9c94fc425bf
description: SetMissedCallNotificationEnabled 操作启用或禁用未接来电通知。
ms.openlocfilehash: ca4942942a81bc187e8e18a5e6f003f8587f79d1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467394"
---
# <a name="setmissedcallnotificationenabled-operation-um-web-service"></a><span data-ttu-id="f05c2-103">SetMissedCallNotificationEnabled 操作（UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="f05c2-103">SetMissedCallNotificationEnabled operation (UM web service)</span></span>

<span data-ttu-id="f05c2-104">SetMissedCallNotificationEnabled 操作启用或禁用未接来电通知。</span><span class="sxs-lookup"><span data-stu-id="f05c2-104">The SetMissedCallNotificationEnabled operation enables or disables missed call notifications.</span></span>
  
## <a name="setmissedcallnotificationenabled-request-example"></a><span data-ttu-id="f05c2-105">SetMissedCallNotificationEnabled 请求示例</span><span class="sxs-lookup"><span data-stu-id="f05c2-105">SetMissedCallNotificationEnabled request example</span></span>

### <a name="description"></a><span data-ttu-id="f05c2-106">Description</span><span class="sxs-lookup"><span data-stu-id="f05c2-106">Description</span></span>

<span data-ttu-id="f05c2-107">以下示例的 SetMissedCallNotificationEnabled 请求显示如何构成启用未接来电通知的请求。</span><span class="sxs-lookup"><span data-stu-id="f05c2-107">The following example of a SetMissedCallNotificationEnabled request shows how to form a request to enable missed call notifications.</span></span>
  
### <a name="code"></a><span data-ttu-id="f05c2-108">代码</span><span class="sxs-lookup"><span data-stu-id="f05c2-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetMissedCallNotificationEnabled xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
        <status>true</status>
    </SetMissedCallNotificationEnabled>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-setmissedcallnotificationenabled-response-example"></a><span data-ttu-id="f05c2-109">成功的 SetMissedCallNotificationEnabled 响应示例</span><span class="sxs-lookup"><span data-stu-id="f05c2-109">Successful SetMissedCallNotificationEnabled response example</span></span>

### <a name="description"></a><span data-ttu-id="f05c2-110">Description</span><span class="sxs-lookup"><span data-stu-id="f05c2-110">Description</span></span>

<span data-ttu-id="f05c2-111">下面的 PlayOnPhoneGreeting 响应示例显示对 SetMissedCallNotificationEnabled 请求的响应。</span><span class="sxs-lookup"><span data-stu-id="f05c2-111">The following example of a PlayOnPhoneGreeting response shows a response to the SetMissedCallNotificationEnabled request.</span></span>
  
### <a name="code"></a><span data-ttu-id="f05c2-112">代码</span><span class="sxs-lookup"><span data-stu-id="f05c2-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetMissedCallNotificationEnabledResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="f05c2-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f05c2-113">See also</span></span>



[<span data-ttu-id="f05c2-114">SetMissedCallNotificationEnabled （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="f05c2-114">SetMissedCallNotificationEnabled (UM web service)</span></span>](setmissedcallnotificationenabled-um-web-service.md)
  
[<span data-ttu-id="f05c2-115">SetMissedCallNotificationEnabledResponse （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="f05c2-115">SetMissedCallNotificationEnabledResponse (UM web service)</span></span>](setmissedcallnotificationenabledresponse-um-web-service.md)
  
[<span data-ttu-id="f05c2-116">Status （UM web 服务-SetMissedCallNotificationEnabled）</span><span class="sxs-lookup"><span data-stu-id="f05c2-116">Status (UM web service - SetMissedCallNotificationEnabled)</span></span>](status-um-web-servicesetmissedcallnotificationenabled.md)

