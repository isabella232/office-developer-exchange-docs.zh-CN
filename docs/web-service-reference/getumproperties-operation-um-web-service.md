---
title: GetUMProperties 操作 （UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- GetUMProperties
api_type:
- schema
ms.assetid: 301fb9a3-67df-44c4-8ffe-0600237fc344
description: GetUMProperties 操作获取发出请求的用户的邮箱的所有统一消息的属性。
ms.openlocfilehash: 8878099bbd907fe0648f7d64dde3cd9600c2c45f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825678"
---
# <a name="getumproperties-operation-um-web-service"></a><span data-ttu-id="69828-103">GetUMProperties 操作 （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="69828-103">GetUMProperties operation (UM web service)</span></span>

<span data-ttu-id="69828-104">GetUMProperties 操作获取发出请求的用户的邮箱的所有统一消息的属性。</span><span class="sxs-lookup"><span data-stu-id="69828-104">The GetUMProperties operation gets all the Unified Messaging properties for the mailbox of the user who is making the request.</span></span>
  
## <a name="getumproperties-request-example"></a><span data-ttu-id="69828-105">GetUMProperties 请求示例</span><span class="sxs-lookup"><span data-stu-id="69828-105">GetUMProperties request example</span></span>

### <a name="description"></a><span data-ttu-id="69828-106">说明</span><span class="sxs-lookup"><span data-stu-id="69828-106">Description</span></span>

<span data-ttu-id="69828-107">GetUMProperties 请求的下面的示例演示如何以形成一个请求以获取统一消息的邮箱属性。</span><span class="sxs-lookup"><span data-stu-id="69828-107">The following example of a GetUMProperties request shows how to form a request to get the Unified Messaging properties of a mailbox.</span></span>
  
### <a name="code"></a><span data-ttu-id="69828-108">代码</span><span class="sxs-lookup"><span data-stu-id="69828-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetUMProperties xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" />
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-getumproperties-response-example"></a><span data-ttu-id="69828-109">成功 GetUMProperties 响应示例</span><span class="sxs-lookup"><span data-stu-id="69828-109">Successful GetUMProperties response example</span></span>

### <a name="description"></a><span data-ttu-id="69828-110">说明</span><span class="sxs-lookup"><span data-stu-id="69828-110">Description</span></span>

<span data-ttu-id="69828-111">GetUMProperties 响应的下面的示例演示 GetUMProperties 请求的响应。</span><span class="sxs-lookup"><span data-stu-id="69828-111">The following example of a GetUMProperties response shows a response to the GetUMProperties request.</span></span>
  
### <a name="code"></a><span data-ttu-id="69828-112">代码</span><span class="sxs-lookup"><span data-stu-id="69828-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <GetUMPropertiesResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <GetUMPropertiesResponse>
        <OofStatus>false</OofStatus> 
        <MissedCallNotificationEnabled>true</MissedCallNotificationEnabled> 
        <PlayOnPhoneDialString>12345</PlayOnPhoneDialString> 
        <TelephoneAccessNumbers>54321</TelephoneAccessNumbers> 
        <TelephoneAccessFolderEmail>AAAAAGsd2rbQLVtLobUGbrq/9IUBAEX2ikn/L8JJtI5WHI0FAW8AAAFXHhsAAA==</TelephoneAccessFolderEmail> 
      </GetUMPropertiesResponse>
    </GetUMPropertiesResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="69828-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="69828-113">See also</span></span>



[<span data-ttu-id="69828-114">GetUMProperties （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="69828-114">GetUMProperties (UM web service)</span></span>](getumproperties-um-web-service.md)
  
[<span data-ttu-id="69828-115">GetUMPropertiesResponse （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="69828-115">GetUMPropertiesResponse (UM web service)</span></span>](getumpropertiesresponse-um-web-service.md)
