---
title: 请求 (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: da54eb32-7ce5-4384-9893-255a2243a959
description: 请求元素包含对自动发现服务的请求。
ms.openlocfilehash: ed6b0a80e83e160287f382a881dc5405bfb47a37
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827124"
---
# <a name="request-pox"></a><span data-ttu-id="5142c-103">请求 (POX)</span><span class="sxs-lookup"><span data-stu-id="5142c-103">Request (POX)</span></span>

<span data-ttu-id="5142c-104">**请求**元素包含对自动发现服务的请求。</span><span class="sxs-lookup"><span data-stu-id="5142c-104">The **Request** element contains the request to the Autodiscover service.</span></span> 
  
[<span data-ttu-id="5142c-105">自动发现 (POX)</span><span class="sxs-lookup"><span data-stu-id="5142c-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="5142c-106">请求 (POX)</span><span class="sxs-lookup"><span data-stu-id="5142c-106">Request (POX)</span></span>](request-pox.md)
  
```xml
<Request>
   <AcceptableResponseSchema/>
   <EMailAddress/>
</Request>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="5142c-107">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5142c-107">Attributes and elements</span></span>

<span data-ttu-id="5142c-108">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5142c-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5142c-109">属性</span><span class="sxs-lookup"><span data-stu-id="5142c-109">Attributes</span></span>

<span data-ttu-id="5142c-110">无。</span><span class="sxs-lookup"><span data-stu-id="5142c-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5142c-111">子元素</span><span class="sxs-lookup"><span data-stu-id="5142c-111">Child elements</span></span>

|<span data-ttu-id="5142c-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="5142c-112">**Element**</span></span>|<span data-ttu-id="5142c-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="5142c-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5142c-114">AcceptableResponseSchema (POX)</span><span class="sxs-lookup"><span data-stu-id="5142c-114">AcceptableResponseSchema (POX)</span></span>](acceptableresponseschema-pox.md) <br/> |<span data-ttu-id="5142c-115">标识为自动发现响应的架构。</span><span class="sxs-lookup"><span data-stu-id="5142c-115">Identifies the schema for an Autodiscover response.</span></span>  <br/> |
|[<span data-ttu-id="5142c-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="5142c-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="5142c-117">标识用户的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="5142c-117">Identifies the user's e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="5142c-118">LegacyDN (POX)</span><span class="sxs-lookup"><span data-stu-id="5142c-118">LegacyDN (POX)</span></span>](legacydn-pox.md) <br/> |<span data-ttu-id="5142c-119">通过旧的可分辨名称标识用户的邮箱。</span><span class="sxs-lookup"><span data-stu-id="5142c-119">Identifies a user's mailbox by legacy distinguished name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5142c-120">父元素</span><span class="sxs-lookup"><span data-stu-id="5142c-120">Parent elements</span></span>

|<span data-ttu-id="5142c-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="5142c-121">**Element**</span></span>|<span data-ttu-id="5142c-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="5142c-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5142c-123">自动发现 (POX)</span><span class="sxs-lookup"><span data-stu-id="5142c-123">AutoDiscover (POX)</span></span>](autodiscover-pox.md) <br/> |<span data-ttu-id="5142c-124">中的自动发现请求的根元素。</span><span class="sxs-lookup"><span data-stu-id="5142c-124">The root element in an Autodiscover request.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5142c-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5142c-125">See also</span></span>



[<span data-ttu-id="5142c-126">Exchange POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="5142c-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

