---
title: NetworkRequirements (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 1555fd2e-05b6-4b94-907b-dae9174049d9
description: NetworkRequirements 元素包含用于确定客户端计算机是否满足 Internet 服务提供程序 (ISP) 的要求连接到服务器的网络上的条件。
ms.openlocfilehash: f3abcff04cd4121b8dcc7ceff7658ad389e6d0b0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826529"
---
# <a name="networkrequirements-pox"></a><span data-ttu-id="5e392-103">NetworkRequirements (POX)</span><span class="sxs-lookup"><span data-stu-id="5e392-103">NetworkRequirements (POX)</span></span>

<span data-ttu-id="5e392-104">**NetworkRequirements**元素包含用于确定客户端计算机是否满足 Internet 服务提供程序 (ISP) 的要求连接到服务器的网络上的条件。</span><span class="sxs-lookup"><span data-stu-id="5e392-104">The **NetworkRequirements** element contains the criteria that are used to determine whether the client computer is on a network that meets the requirements of the Internet service provider (ISP) to connect to the server.</span></span> 
  
[<span data-ttu-id="5e392-105">自动发现 (POX)</span><span class="sxs-lookup"><span data-stu-id="5e392-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="5e392-106">响应 (POX)</span><span class="sxs-lookup"><span data-stu-id="5e392-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="5e392-107">帐户 (POX)</span><span class="sxs-lookup"><span data-stu-id="5e392-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="5e392-108">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="5e392-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="5e392-109">NetworkRequirements (POX)</span><span class="sxs-lookup"><span data-stu-id="5e392-109">NetworkRequirements (POX)</span></span>](networkrequirements-pox.md)
  
```xml
<NetworkRequirements>
   <IPv4Start/>
   <IPv4End/>
   <IPv6Start/>
   <IPv6End/>
</NetworkRequirements>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="5e392-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5e392-110">Attributes and elements</span></span>

<span data-ttu-id="5e392-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5e392-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5e392-112">属性</span><span class="sxs-lookup"><span data-stu-id="5e392-112">Attributes</span></span>

<span data-ttu-id="5e392-113">无。</span><span class="sxs-lookup"><span data-stu-id="5e392-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5e392-114">子元素</span><span class="sxs-lookup"><span data-stu-id="5e392-114">Child elements</span></span>

|<span data-ttu-id="5e392-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="5e392-115">**Element**</span></span>|<span data-ttu-id="5e392-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="5e392-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5e392-117">IPv4Start (POX)</span><span class="sxs-lookup"><span data-stu-id="5e392-117">IPv4Start (POX)</span></span>](ipv4start-pox.md) <br/> |<span data-ttu-id="5e392-118">标识的范围内的 IP 版本 4 (IPv4) 开始用于标识网络上的计算机的地址。</span><span class="sxs-lookup"><span data-stu-id="5e392-118">Identifies the start of a range of IP version 4 (IPv4) addresses that are used to identify a computer on a network.</span></span>  <br/> |
|[<span data-ttu-id="5e392-119">IPv4End (POX)</span><span class="sxs-lookup"><span data-stu-id="5e392-119">IPv4End (POX)</span></span>](ipv4end-pox.md) <br/> |<span data-ttu-id="5e392-120">标识的末尾的范围内的 IP 版本 4 (IPv4) 用于标识网络上的计算机的地址。</span><span class="sxs-lookup"><span data-stu-id="5e392-120">Identifies the end of a range of IP version 4 (IPv4) addresses that are used to identify a computer on the network.</span></span>  <br/> |
|[<span data-ttu-id="5e392-121">IPv6Start (POX)</span><span class="sxs-lookup"><span data-stu-id="5e392-121">IPv6Start (POX)</span></span>](ipv6start-pox.md) <br/> |<span data-ttu-id="5e392-122">标识的范围内的 IP 版本 6 (IPv6) 开始用于标识网络上的计算机的地址。</span><span class="sxs-lookup"><span data-stu-id="5e392-122">Identifies the start of a range of IP version 6 (IPv6) addresses that are used to identify a computer on a network.</span></span>  <br/> |
|[<span data-ttu-id="5e392-123">IPv6End (POX)</span><span class="sxs-lookup"><span data-stu-id="5e392-123">IPv6End (POX)</span></span>](ipv6end-pox.md) <br/> |<span data-ttu-id="5e392-124">标识的末尾的范围内的 IP 版本 6 (IPv6) 用于标识网络上的计算机的地址。</span><span class="sxs-lookup"><span data-stu-id="5e392-124">Identifies the end of a range of IP version 6 (IPv6) addresses that are used to identify a computer on a network.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5e392-125">父元素</span><span class="sxs-lookup"><span data-stu-id="5e392-125">Parent elements</span></span>

|<span data-ttu-id="5e392-126">**元素**</span><span class="sxs-lookup"><span data-stu-id="5e392-126">**Element**</span></span>|<span data-ttu-id="5e392-127">**说明**</span><span class="sxs-lookup"><span data-stu-id="5e392-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5e392-128">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="5e392-128">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="5e392-129">包含客户端连接到运行 Microsoft Exchange Server 2007 的安装了客户端访问服务器角色的计算机的规格。</span><span class="sxs-lookup"><span data-stu-id="5e392-129">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5e392-130">注解</span><span class="sxs-lookup"><span data-stu-id="5e392-130">Remarks</span></span>

<span data-ttu-id="5e392-131">如果电子邮件客户端不匹配的网络要求，它应尝试其他协议类型。</span><span class="sxs-lookup"><span data-stu-id="5e392-131">If the e-mail client does not match the network requirements, it should try other protocol types.</span></span> <span data-ttu-id="5e392-132">Isp 可以提供一组具有[协议 (POX)](protocol-pox.md)标记不需要身份验证但所需的 ISP 网络上的服务器。</span><span class="sxs-lookup"><span data-stu-id="5e392-132">ISPs may provide one set of servers with [Protocol (POX)](protocol-pox.md) tags that do not require authentication but are required to be on the ISP network.</span></span> <span data-ttu-id="5e392-133">Isp 可以列出服务器要求身份验证，但不是需要位于特定的网络上的另一的组。</span><span class="sxs-lookup"><span data-stu-id="5e392-133">ISPs may list another set of servers that require authentication but are not required to be on a specific network.</span></span> 
  
<span data-ttu-id="5e392-134">**NetworkRequirements**元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="5e392-134">The **NetworkRequirements** element is optional.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5e392-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5e392-135">See also</span></span>



[<span data-ttu-id="5e392-136">Exchange POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="5e392-136">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

