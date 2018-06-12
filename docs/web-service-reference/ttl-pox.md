---
title: TTL (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 178eefa1-995c-4bea-930b-e51293961191
description: TTL 元素指定的时间生存，以小时，在此期间设置一直保持有效。
ms.openlocfilehash: 5fecf3103553a82ed2aeeecfc1e4e1b9fe38583c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838293"
---
# <a name="ttl-pox"></a><span data-ttu-id="11566-103">TTL (POX)</span><span class="sxs-lookup"><span data-stu-id="11566-103">TTL (POX)</span></span>

<span data-ttu-id="11566-104">**TTL**元素指定的时间生存，以小时，在此期间设置一直保持有效。</span><span class="sxs-lookup"><span data-stu-id="11566-104">The **TTL** element specifies the Time to Live, in hours, during which the settings remain valid.</span></span> 
  
[<span data-ttu-id="11566-105">自动发现 (POX)</span><span class="sxs-lookup"><span data-stu-id="11566-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="11566-106">响应 (POX)</span><span class="sxs-lookup"><span data-stu-id="11566-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="11566-107">帐户 (POX)</span><span class="sxs-lookup"><span data-stu-id="11566-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="11566-108">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="11566-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="11566-109">TTL (POX)</span><span class="sxs-lookup"><span data-stu-id="11566-109">TTL (POX)</span></span>](ttl-pox.md)
  
```xml
<TTL/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="11566-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="11566-110">Attributes and elements</span></span>

<span data-ttu-id="11566-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="11566-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="11566-112">属性</span><span class="sxs-lookup"><span data-stu-id="11566-112">Attributes</span></span>

<span data-ttu-id="11566-113">无。</span><span class="sxs-lookup"><span data-stu-id="11566-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="11566-114">子元素</span><span class="sxs-lookup"><span data-stu-id="11566-114">Child elements</span></span>

<span data-ttu-id="11566-115">无。</span><span class="sxs-lookup"><span data-stu-id="11566-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="11566-116">父元素</span><span class="sxs-lookup"><span data-stu-id="11566-116">Parent elements</span></span>

|<span data-ttu-id="11566-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="11566-117">**Element**</span></span>|<span data-ttu-id="11566-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="11566-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="11566-119">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="11566-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="11566-120">包含客户端连接到在其安装客户端访问服务器角色的 Exchange Server 2007 计算机的规格。</span><span class="sxs-lookup"><span data-stu-id="11566-120">Contains the specifications for connecting a client to the Exchange Server 2007 computer on which the Client Access server role is installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="11566-121">文本值</span><span class="sxs-lookup"><span data-stu-id="11566-121">Text value</span></span>

<span data-ttu-id="11566-122">文本值表示生存时间中的设置期间保持有效的时间。</span><span class="sxs-lookup"><span data-stu-id="11566-122">The text value represents the Time to Live, in hours, during which the settings remain valid.</span></span> <span data-ttu-id="11566-123">值为零表示该重新发现功能，则不需要。</span><span class="sxs-lookup"><span data-stu-id="11566-123">A value of zero indicates that rediscovery is not required.</span></span> <span data-ttu-id="11566-124">如果未不指定任何值，此元素的默认值为 1 小时。</span><span class="sxs-lookup"><span data-stu-id="11566-124">If no value is specified, the default value for this element is 1 hour.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="11566-125">备注</span><span class="sxs-lookup"><span data-stu-id="11566-125">Remarks</span></span>

<span data-ttu-id="11566-126">**TTL**元素表示的时间过后，应使用自动发现请求重新发现设置。</span><span class="sxs-lookup"><span data-stu-id="11566-126">After the time that is represented by the **TTL** element has elapsed, the settings should be rediscovered by using an Autodiscover request.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="11566-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="11566-127">See also</span></span>



[<span data-ttu-id="11566-128">Exchange POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="11566-128">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

