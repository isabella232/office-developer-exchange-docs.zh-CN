---
title: SetPlayOnPhoneDialString 操作（UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- SetPlayOnPhoneDialString
api_type:
- schema
ms.assetid: a68479f2-d900-4dd8-a5ce-dbea8247e841
description: SetPlayOnPhoneDialString 操作将拨号字符串设置为 PlayOnPhone 操作（UM web 服务）和 PlayOnPhoneGreeting 操作（UM web 服务）的默认值。
ms.openlocfilehash: 7df806eedc2d6d037394f31ec4ccbfe28aaf3372
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458640"
---
# <a name="setplayonphonedialstring-operation-um-web-service"></a><span data-ttu-id="cb17a-103">SetPlayOnPhoneDialString 操作（UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="cb17a-103">SetPlayOnPhoneDialString operation (UM web service)</span></span>

<span data-ttu-id="cb17a-104">SetPlayOnPhoneDialString 操作将拨号字符串设置为[PlayOnPhone 操作（um web 服务）](playonphone-operation-um-web-service.md)和[PLAYONPHONEGREETING 操作（um web 服务）](playonphonegreeting-operation-um-web-service.md)的默认值。</span><span class="sxs-lookup"><span data-stu-id="cb17a-104">The SetPlayOnPhoneDialString operation sets the dial string to use as the default for the [PlayOnPhone operation (UM web service)](playonphone-operation-um-web-service.md) and the [PlayOnPhoneGreeting operation (UM web service)](playonphonegreeting-operation-um-web-service.md).</span></span>
  
## <a name="setplayonphonedialstring-request-example"></a><span data-ttu-id="cb17a-105">SetPlayOnPhoneDialString 请求示例</span><span class="sxs-lookup"><span data-stu-id="cb17a-105">SetPlayOnPhoneDialString request example</span></span>

### <a name="description"></a><span data-ttu-id="cb17a-106">Description</span><span class="sxs-lookup"><span data-stu-id="cb17a-106">Description</span></span>

<span data-ttu-id="cb17a-107">以下示例的 SetPlayOnPhoneDialString 请求显示如何形成请求以设置邮箱的默认拨号字符串。</span><span class="sxs-lookup"><span data-stu-id="cb17a-107">The following example of a SetPlayOnPhoneDialString request shows how to form a request to set the default dial string for a mailbox.</span></span>
  
### <a name="code"></a><span data-ttu-id="cb17a-108">代码</span><span class="sxs-lookup"><span data-stu-id="cb17a-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetPlayOnPhoneDialString xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
        <dialString>12345</dialString>
    </SetPlayOnPhoneDialString>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-setplayonphonedialstring-response-example"></a><span data-ttu-id="cb17a-109">成功的 SetPlayOnPhoneDialString 响应示例</span><span class="sxs-lookup"><span data-stu-id="cb17a-109">Successful SetPlayOnPhoneDialString response example</span></span>

### <a name="description"></a><span data-ttu-id="cb17a-110">Description</span><span class="sxs-lookup"><span data-stu-id="cb17a-110">Description</span></span>

<span data-ttu-id="cb17a-111">下面的 SetPlayOnePhoneDialString 响应示例显示对 SetPlayOnPhoneDialString 请求的响应。</span><span class="sxs-lookup"><span data-stu-id="cb17a-111">The following example of a SetPlayOnePhoneDialString response shows a response to the SetPlayOnPhoneDialString request.</span></span>
  
### <a name="code"></a><span data-ttu-id="cb17a-112">代码</span><span class="sxs-lookup"><span data-stu-id="cb17a-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetPlayOnPhoneDialStringResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="cb17a-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cb17a-113">See also</span></span>



[<span data-ttu-id="cb17a-114">SetPlayOnPhoneDialString （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="cb17a-114">SetPlayOnPhoneDialString (UM web service)</span></span>](setplayonphonedialstring-um-web-service.md)
  
[<span data-ttu-id="cb17a-115">SetPlayOnPhoneDialStringResponse （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="cb17a-115">SetPlayOnPhoneDialStringResponse (UM web service)</span></span>](setplayonphonedialstringresponse-um-web-service.md)
  
[<span data-ttu-id="cb17a-116">dialString （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="cb17a-116">dialString (UM web service)</span></span>](dialstring-um-web-service.md)

