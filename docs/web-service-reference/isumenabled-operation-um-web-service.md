---
title: IsUMEnabled 操作 （UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- IsUMEnabled
api_type:
- schema
ms.assetid: fbe6cd95-f7a5-42b9-8a9d-b6159a269d55
description: IsUMEnabled 操作确定是否将邮箱启用了统一消息。
ms.openlocfilehash: 9d94a359d6b11e41762d21aa2fe5501bd9f7b577
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826107"
---
# <a name="isumenabled-operation-um-web-service"></a><span data-ttu-id="f675e-103">IsUMEnabled 操作 （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="f675e-103">IsUMEnabled operation (UM web service)</span></span>

<span data-ttu-id="f675e-104">IsUMEnabled 操作确定是否将邮箱启用了统一消息。</span><span class="sxs-lookup"><span data-stu-id="f675e-104">The IsUMEnabled operation determines whether a mailbox is enabled for Unified Messaging.</span></span>
  
## <a name="isumenabled-request-example"></a><span data-ttu-id="f675e-105">IsUMEnabled 请求示例</span><span class="sxs-lookup"><span data-stu-id="f675e-105">IsUMEnabled request example</span></span>

### <a name="description"></a><span data-ttu-id="f675e-106">说明</span><span class="sxs-lookup"><span data-stu-id="f675e-106">Description</span></span>

<span data-ttu-id="f675e-107">IsUMEnabled 请求的下面的示例演示如何表单以确定是否将邮箱启用统一消息的请求。</span><span class="sxs-lookup"><span data-stu-id="f675e-107">The following example of an IsUMEnabled request shows how to form a request to determine whether a mailbox is enabled for Unified Messaging.</span></span>
  
### <a name="code"></a><span data-ttu-id="f675e-108">代码</span><span class="sxs-lookup"><span data-stu-id="f675e-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <IsUMEnabled xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" />
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-isumenabled-response-example"></a><span data-ttu-id="f675e-109">成功 IsUMEnabled 响应示例</span><span class="sxs-lookup"><span data-stu-id="f675e-109">Successful IsUMEnabled response example</span></span>

### <a name="description"></a><span data-ttu-id="f675e-110">说明</span><span class="sxs-lookup"><span data-stu-id="f675e-110">Description</span></span>

<span data-ttu-id="f675e-111">下面的示例演示对 IsUMEnabled 请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="f675e-111">The following example shows a successful response to an IsUMEnabled request.</span></span>
  
### <a name="code"></a><span data-ttu-id="f675e-112">代码</span><span class="sxs-lookup"><span data-stu-id="f675e-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <IsUMEnabledResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <IsUMEnabledResponse>true</IsUMEnabledResponse> 
    </IsUMEnabledResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="f675e-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f675e-113">See also</span></span>



[<span data-ttu-id="f675e-114">IsUMEnabled （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="f675e-114">IsUMEnabled (UM web service)</span></span>](isumenabled-um-web-service.md)
  
[<span data-ttu-id="f675e-115">IsUMEnabledResponse （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="f675e-115">IsUMEnabledResponse (UM web service)</span></span>](isumenabledresponse-um-web-service.md)


[<span data-ttu-id="f675e-116">Exchange 的统一的消息 web 服务 XML 元素</span><span class="sxs-lookup"><span data-stu-id="f675e-116">Unified Messaging web service XML elements for Exchange</span></span>](unified-messaging-web-service-xml-elements-for-exchange.md)

