---
title: ResetPIN 操作 （UM web 服务）
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
description: ResetPIN 操作更改为新的随机值的 PIN （TUI 密码）。
ms.openlocfilehash: e6417b86ce17c0d34fe857cf1209a18972cbef63
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827146"
---
# <a name="resetpin-operation-um-web-service"></a><span data-ttu-id="75390-103">ResetPIN 操作 （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="75390-103">ResetPIN operation (UM web service)</span></span>

<span data-ttu-id="75390-104">ResetPIN 操作更改为新的随机值的 PIN （TUI 密码）。</span><span class="sxs-lookup"><span data-stu-id="75390-104">The ResetPIN operation changes the PIN (TUI password) to a new random value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="75390-105">注解</span><span class="sxs-lookup"><span data-stu-id="75390-105">Remarks</span></span>

<span data-ttu-id="75390-106">ResetPIN 操作创建一个新的 PIN，基于 PIN 策略。</span><span class="sxs-lookup"><span data-stu-id="75390-106">The ResetPIN operation creates a new PIN based on the PIN policies.</span></span> <span data-ttu-id="75390-107">如果操作成功，对邮箱的用户发送电子邮件包含新的 PIN。</span><span class="sxs-lookup"><span data-stu-id="75390-107">If the operation is successful, an e-mail message that contains the new PIN is sent to the mailbox of the user.</span></span> <span data-ttu-id="75390-108">如果操作失败，它将引发异常，其中包含有关失败情况的信息。</span><span class="sxs-lookup"><span data-stu-id="75390-108">If the operation fails, it will throw an exception that contains information about the failure.</span></span>
  
## <a name="resetpin-request-example"></a><span data-ttu-id="75390-109">ResetPIN 请求示例</span><span class="sxs-lookup"><span data-stu-id="75390-109">ResetPIN request example</span></span>

### <a name="description"></a><span data-ttu-id="75390-110">说明</span><span class="sxs-lookup"><span data-stu-id="75390-110">Description</span></span>

<span data-ttu-id="75390-111">ResetPIN 请求的下面的示例演示如何以形成请求重置邮箱的 PIN。</span><span class="sxs-lookup"><span data-stu-id="75390-111">The following example of a ResetPIN request shows how to form a request to reset the PIN for a mailbox.</span></span>
  
### <a name="code"></a><span data-ttu-id="75390-112">代码</span><span class="sxs-lookup"><span data-stu-id="75390-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <ResetPIN xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" />
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-resetpin-response-example"></a><span data-ttu-id="75390-113">成功 ResetPIN 响应示例</span><span class="sxs-lookup"><span data-stu-id="75390-113">Successful ResetPIN response example</span></span>

### <a name="description"></a><span data-ttu-id="75390-114">说明</span><span class="sxs-lookup"><span data-stu-id="75390-114">Description</span></span>

<span data-ttu-id="75390-115">ResetPIN 响应的下面的示例演示 ResetPIN 请求的响应。</span><span class="sxs-lookup"><span data-stu-id="75390-115">The following example of a ResetPIN response shows a response to the ResetPIN request.</span></span>
  
### <a name="code"></a><span data-ttu-id="75390-116">代码</span><span class="sxs-lookup"><span data-stu-id="75390-116">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <ResetPINResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="75390-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="75390-117">See also</span></span>



[<span data-ttu-id="75390-118">ResetPIN （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="75390-118">ResetPIN (UM web service)</span></span>](resetpin-um-web-service.md)
  
[<span data-ttu-id="75390-119">ResetPINResponse （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="75390-119">ResetPINResponse (UM web service)</span></span>](resetpinresponse-um-web-service.md)

