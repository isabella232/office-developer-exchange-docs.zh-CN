---
title: ResetPIN 操作（UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- ResetPIN
api_type:
- schema
ms.assetid: c0f14a15-3389-4311-8bac-f87930c5f5d4
description: ResetPIN 操作将 PIN （TUI 密码）更改为新的随机值。
ms.openlocfilehash: 8de64ce7a47e9c426f8eb9298e1ca00508fb616c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465490"
---
# <a name="resetpin-operation-um-web-service"></a><span data-ttu-id="80d83-103">ResetPIN 操作（UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="80d83-103">ResetPIN operation (UM web service)</span></span>

<span data-ttu-id="80d83-104">ResetPIN 操作将 PIN （TUI 密码）更改为新的随机值。</span><span class="sxs-lookup"><span data-stu-id="80d83-104">The ResetPIN operation changes the PIN (TUI password) to a new random value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="80d83-105">备注</span><span class="sxs-lookup"><span data-stu-id="80d83-105">Remarks</span></span>

<span data-ttu-id="80d83-106">ResetPIN 操作根据 PIN 策略创建新 PIN。</span><span class="sxs-lookup"><span data-stu-id="80d83-106">The ResetPIN operation creates a new PIN based on the PIN policies.</span></span> <span data-ttu-id="80d83-107">如果操作成功，则会将包含新 PIN 的电子邮件发送到用户的邮箱。</span><span class="sxs-lookup"><span data-stu-id="80d83-107">If the operation is successful, an e-mail message that contains the new PIN is sent to the mailbox of the user.</span></span> <span data-ttu-id="80d83-108">如果操作失败，它将引发一个异常，其中包含有关失败的信息。</span><span class="sxs-lookup"><span data-stu-id="80d83-108">If the operation fails, it will throw an exception that contains information about the failure.</span></span>
  
## <a name="resetpin-request-example"></a><span data-ttu-id="80d83-109">ResetPIN 请求示例</span><span class="sxs-lookup"><span data-stu-id="80d83-109">ResetPIN request example</span></span>

### <a name="description"></a><span data-ttu-id="80d83-110">Description</span><span class="sxs-lookup"><span data-stu-id="80d83-110">Description</span></span>

<span data-ttu-id="80d83-111">以下示例的 ResetPIN 请求显示如何形成一个重置邮箱的 PIN 的请求。</span><span class="sxs-lookup"><span data-stu-id="80d83-111">The following example of a ResetPIN request shows how to form a request to reset the PIN for a mailbox.</span></span>
  
### <a name="code"></a><span data-ttu-id="80d83-112">代码</span><span class="sxs-lookup"><span data-stu-id="80d83-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <ResetPIN xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" />
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-resetpin-response-example"></a><span data-ttu-id="80d83-113">成功的 ResetPIN 响应示例</span><span class="sxs-lookup"><span data-stu-id="80d83-113">Successful ResetPIN response example</span></span>

### <a name="description"></a><span data-ttu-id="80d83-114">Description</span><span class="sxs-lookup"><span data-stu-id="80d83-114">Description</span></span>

<span data-ttu-id="80d83-115">下面的 ResetPIN 响应示例显示对 ResetPIN 请求的响应。</span><span class="sxs-lookup"><span data-stu-id="80d83-115">The following example of a ResetPIN response shows a response to the ResetPIN request.</span></span>
  
### <a name="code"></a><span data-ttu-id="80d83-116">代码</span><span class="sxs-lookup"><span data-stu-id="80d83-116">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <ResetPINResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="80d83-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="80d83-117">See also</span></span>



[<span data-ttu-id="80d83-118">ResetPIN （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="80d83-118">ResetPIN (UM web service)</span></span>](resetpin-um-web-service.md)
  
[<span data-ttu-id="80d83-119">ResetPINResponse （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="80d83-119">ResetPINResponse (UM web service)</span></span>](resetpinresponse-um-web-service.md)

