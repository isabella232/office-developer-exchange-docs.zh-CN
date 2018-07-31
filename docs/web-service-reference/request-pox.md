---
title: Request (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: da54eb32-7ce5-4384-9893-255a2243a959
description: 请求元素包含对自动发现服务的请求。
ms.openlocfilehash: 3f5d5258a92840fe79c4936370323b78aa4715b3
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354426"
---
# <a name="request-pox"></a><span data-ttu-id="fc6b1-103">Request (POX)</span><span class="sxs-lookup"><span data-stu-id="fc6b1-103">Request (POX)</span></span>

<span data-ttu-id="fc6b1-104">**请求**元素包含对自动发现服务的请求。</span><span class="sxs-lookup"><span data-stu-id="fc6b1-104">The **Request** element contains the request to the Autodiscover service.</span></span> 
  
- [<span data-ttu-id="fc6b1-105">AutoDiscover (POX)</span><span class="sxs-lookup"><span data-stu-id="fc6b1-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md) 
- [<span data-ttu-id="fc6b1-106">Request (POX)</span><span class="sxs-lookup"><span data-stu-id="fc6b1-106">Request (POX)</span></span>](request-pox.md)
  
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

## <a name="attributes-and-elements"></a><span data-ttu-id="fc6b1-107">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fc6b1-107">Attributes and elements</span></span>

<span data-ttu-id="fc6b1-108">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fc6b1-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fc6b1-109">Attributes</span><span class="sxs-lookup"><span data-stu-id="fc6b1-109">Attributes</span></span>

<span data-ttu-id="fc6b1-110">无。</span><span class="sxs-lookup"><span data-stu-id="fc6b1-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fc6b1-111">子元素</span><span class="sxs-lookup"><span data-stu-id="fc6b1-111">Child elements</span></span>

|<span data-ttu-id="fc6b1-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="fc6b1-112">**Element**</span></span>|<span data-ttu-id="fc6b1-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="fc6b1-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fc6b1-114">AcceptableResponseSchema (POX)</span><span class="sxs-lookup"><span data-stu-id="fc6b1-114">AcceptableResponseSchema (POX)</span></span>](acceptableresponseschema-pox.md) <br/> |<span data-ttu-id="fc6b1-115">标识为自动发现响应的架构。</span><span class="sxs-lookup"><span data-stu-id="fc6b1-115">Identifies the schema for an Autodiscover response.</span></span>  <br/> |
|[<span data-ttu-id="fc6b1-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="fc6b1-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="fc6b1-117">标识用户的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="fc6b1-117">Identifies the user's e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="fc6b1-118">LegacyDN (POX)</span><span class="sxs-lookup"><span data-stu-id="fc6b1-118">LegacyDN (POX)</span></span>](legacydn-pox.md) <br/> |<span data-ttu-id="fc6b1-119">通过旧的可分辨名称标识用户的邮箱。</span><span class="sxs-lookup"><span data-stu-id="fc6b1-119">Identifies a user's mailbox by legacy distinguished name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fc6b1-120">父元素</span><span class="sxs-lookup"><span data-stu-id="fc6b1-120">Parent elements</span></span>

|<span data-ttu-id="fc6b1-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="fc6b1-121">**Element**</span></span>|<span data-ttu-id="fc6b1-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="fc6b1-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fc6b1-123">AutoDiscover (POX)</span><span class="sxs-lookup"><span data-stu-id="fc6b1-123">AutoDiscover (POX)</span></span>](autodiscover-pox.md) <br/> |<span data-ttu-id="fc6b1-124">中的自动发现请求的根元素。</span><span class="sxs-lookup"><span data-stu-id="fc6b1-124">The root element in an Autodiscover request.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fc6b1-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fc6b1-125">See also</span></span>

- [<span data-ttu-id="fc6b1-126">Exchange POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="fc6b1-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

