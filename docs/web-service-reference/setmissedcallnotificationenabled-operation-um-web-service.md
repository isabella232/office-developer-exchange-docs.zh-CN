---
title: SetMissedCallNotificationEnabled 操作 （UM web 服务）
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
description: SetMissedCallNotificationEnabled 操作启用或禁用错过的呼叫通知。
ms.openlocfilehash: be9479d6ed2c5238ed19c3d22e028fca62b8deed
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827434"
---
# <a name="setmissedcallnotificationenabled-operation-um-web-service"></a><span data-ttu-id="d0d2b-103">SetMissedCallNotificationEnabled 操作 （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="d0d2b-103">SetMissedCallNotificationEnabled operation (UM web service)</span></span>

<span data-ttu-id="d0d2b-104">SetMissedCallNotificationEnabled 操作启用或禁用错过的呼叫通知。</span><span class="sxs-lookup"><span data-stu-id="d0d2b-104">The SetMissedCallNotificationEnabled operation enables or disables missed call notifications.</span></span>
  
## <a name="setmissedcallnotificationenabled-request-example"></a><span data-ttu-id="d0d2b-105">SetMissedCallNotificationEnabled 请求示例</span><span class="sxs-lookup"><span data-stu-id="d0d2b-105">SetMissedCallNotificationEnabled request example</span></span>

### <a name="description"></a><span data-ttu-id="d0d2b-106">说明</span><span class="sxs-lookup"><span data-stu-id="d0d2b-106">Description</span></span>

<span data-ttu-id="d0d2b-107">SetMissedCallNotificationEnabled 请求的下面的示例演示如何以形成启用未接来电通知的请求。</span><span class="sxs-lookup"><span data-stu-id="d0d2b-107">The following example of a SetMissedCallNotificationEnabled request shows how to form a request to enable missed call notifications.</span></span>
  
### <a name="code"></a><span data-ttu-id="d0d2b-108">代码</span><span class="sxs-lookup"><span data-stu-id="d0d2b-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetMissedCallNotificationEnabled xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
        <status>true</status>
    </SetMissedCallNotificationEnabled>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-setmissedcallnotificationenabled-response-example"></a><span data-ttu-id="d0d2b-109">成功 SetMissedCallNotificationEnabled 响应示例</span><span class="sxs-lookup"><span data-stu-id="d0d2b-109">Successful SetMissedCallNotificationEnabled response example</span></span>

### <a name="description"></a><span data-ttu-id="d0d2b-110">说明</span><span class="sxs-lookup"><span data-stu-id="d0d2b-110">Description</span></span>

<span data-ttu-id="d0d2b-111">PlayOnPhoneGreeting 响应的下面的示例演示 SetMissedCallNotificationEnabled 请求的响应。</span><span class="sxs-lookup"><span data-stu-id="d0d2b-111">The following example of a PlayOnPhoneGreeting response shows a response to the SetMissedCallNotificationEnabled request.</span></span>
  
### <a name="code"></a><span data-ttu-id="d0d2b-112">代码</span><span class="sxs-lookup"><span data-stu-id="d0d2b-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetMissedCallNotificationEnabledResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="d0d2b-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d0d2b-113">See also</span></span>



[<span data-ttu-id="d0d2b-114">SetMissedCallNotificationEnabled （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="d0d2b-114">SetMissedCallNotificationEnabled (UM web service)</span></span>](setmissedcallnotificationenabled-um-web-service.md)
  
[<span data-ttu-id="d0d2b-115">SetMissedCallNotificationEnabledResponse （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="d0d2b-115">SetMissedCallNotificationEnabledResponse (UM web service)</span></span>](setmissedcallnotificationenabledresponse-um-web-service.md)
  
[<span data-ttu-id="d0d2b-116">状态 （UM web 服务-SetMissedCallNotificationEnabled）</span><span class="sxs-lookup"><span data-stu-id="d0d2b-116">Status (UM web service - SetMissedCallNotificationEnabled)</span></span>](status-um-web-servicesetmissedcallnotificationenabled.md)

