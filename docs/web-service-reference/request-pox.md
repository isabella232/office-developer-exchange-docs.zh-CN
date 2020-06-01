---
title: 请求（POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: da54eb32-7ce5-4384-9893-255a2243a959
description: Request 元素包含对自动发现服务的请求。
ms.openlocfilehash: bc215d614441ed8f12c0f1490f4abdbb7b574ad0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459544"
---
# <a name="request-pox"></a><span data-ttu-id="b7b52-103">请求（POX）</span><span class="sxs-lookup"><span data-stu-id="b7b52-103">Request (POX)</span></span>

<span data-ttu-id="b7b52-104">**Request**元素包含对自动发现服务的请求。</span><span class="sxs-lookup"><span data-stu-id="b7b52-104">The **Request** element contains the request to the Autodiscover service.</span></span> 
  
- [<span data-ttu-id="b7b52-105">自动发现（POX）</span><span class="sxs-lookup"><span data-stu-id="b7b52-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md) 
- [<span data-ttu-id="b7b52-106">请求（POX）</span><span class="sxs-lookup"><span data-stu-id="b7b52-106">Request (POX)</span></span>](request-pox.md)
  
```xml
<Request>
   <AcceptableResponseSchema/>
   <EMailAddress/>
</Request>
```

```xml
<Request>
   <AcceptableResponseSchema/> 
   <LegacyDN/>
</Request>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="b7b52-107">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b7b52-107">Attributes and elements</span></span>

<span data-ttu-id="b7b52-108">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b7b52-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b7b52-109">Attributes</span><span class="sxs-lookup"><span data-stu-id="b7b52-109">Attributes</span></span>

<span data-ttu-id="b7b52-110">无。</span><span class="sxs-lookup"><span data-stu-id="b7b52-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b7b52-111">子元素</span><span class="sxs-lookup"><span data-stu-id="b7b52-111">Child elements</span></span>

|<span data-ttu-id="b7b52-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="b7b52-112">**Element**</span></span>|<span data-ttu-id="b7b52-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="b7b52-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b7b52-114">AcceptableResponseSchema （POX）</span><span class="sxs-lookup"><span data-stu-id="b7b52-114">AcceptableResponseSchema (POX)</span></span>](acceptableresponseschema-pox.md) <br/> |<span data-ttu-id="b7b52-115">标识自动发现响应的架构。</span><span class="sxs-lookup"><span data-stu-id="b7b52-115">Identifies the schema for an Autodiscover response.</span></span>  <br/> |
|[<span data-ttu-id="b7b52-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="b7b52-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="b7b52-117">标识用户的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="b7b52-117">Identifies the user's e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="b7b52-118">LegacyDN （POX）</span><span class="sxs-lookup"><span data-stu-id="b7b52-118">LegacyDN (POX)</span></span>](legacydn-pox.md) <br/> |<span data-ttu-id="b7b52-119">通过旧版可分辨名称标识用户的邮箱。</span><span class="sxs-lookup"><span data-stu-id="b7b52-119">Identifies a user's mailbox by legacy distinguished name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b7b52-120">父元素</span><span class="sxs-lookup"><span data-stu-id="b7b52-120">Parent elements</span></span>

|<span data-ttu-id="b7b52-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="b7b52-121">**Element**</span></span>|<span data-ttu-id="b7b52-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="b7b52-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b7b52-123">自动发现（POX）</span><span class="sxs-lookup"><span data-stu-id="b7b52-123">AutoDiscover (POX)</span></span>](autodiscover-pox.md) <br/> |<span data-ttu-id="b7b52-124">自动发现请求中的根元素。</span><span class="sxs-lookup"><span data-stu-id="b7b52-124">The root element in an Autodiscover request.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b7b52-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b7b52-125">See also</span></span>

- [<span data-ttu-id="b7b52-126">Exchange 的 POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="b7b52-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

