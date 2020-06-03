---
title: NetworkRequirements （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 1555fd2e-05b6-4b94-907b-dae9174049d9
description: NetworkRequirements 元素包含用于确定客户端计算机是否在满足 Internet 服务提供商（ISP）的要求以连接到服务器的网络上的条件。
ms.openlocfilehash: d588f7eb12a445fba9c997c4b9db0a6842105b4e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462722"
---
# <a name="networkrequirements-pox"></a><span data-ttu-id="5b9d3-103">NetworkRequirements （POX）</span><span class="sxs-lookup"><span data-stu-id="5b9d3-103">NetworkRequirements (POX)</span></span>

<span data-ttu-id="5b9d3-104">**NetworkRequirements**元素包含用于确定客户端计算机是否在满足 Internet 服务提供商（ISP）的要求以连接到服务器的网络上的条件。</span><span class="sxs-lookup"><span data-stu-id="5b9d3-104">The **NetworkRequirements** element contains the criteria that are used to determine whether the client computer is on a network that meets the requirements of the Internet service provider (ISP) to connect to the server.</span></span> 
  
[<span data-ttu-id="5b9d3-105">自动发现（POX）</span><span class="sxs-lookup"><span data-stu-id="5b9d3-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="5b9d3-106">响应（POX）</span><span class="sxs-lookup"><span data-stu-id="5b9d3-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="5b9d3-107">帐户（POX）</span><span class="sxs-lookup"><span data-stu-id="5b9d3-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="5b9d3-108">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="5b9d3-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="5b9d3-109">NetworkRequirements （POX）</span><span class="sxs-lookup"><span data-stu-id="5b9d3-109">NetworkRequirements (POX)</span></span>](networkrequirements-pox.md)
  
```xml
<NetworkRequirements>
   <IPv4Start/>
   <IPv4End/>
   <IPv6Start/>
   <IPv6End/>
</NetworkRequirements>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="5b9d3-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5b9d3-110">Attributes and elements</span></span>

<span data-ttu-id="5b9d3-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5b9d3-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5b9d3-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="5b9d3-112">Attributes</span></span>

<span data-ttu-id="5b9d3-113">无。</span><span class="sxs-lookup"><span data-stu-id="5b9d3-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5b9d3-114">子元素</span><span class="sxs-lookup"><span data-stu-id="5b9d3-114">Child elements</span></span>

|<span data-ttu-id="5b9d3-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="5b9d3-115">**Element**</span></span>|<span data-ttu-id="5b9d3-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="5b9d3-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5b9d3-117">IPv4Start （POX）</span><span class="sxs-lookup"><span data-stu-id="5b9d3-117">IPv4Start (POX)</span></span>](ipv4start-pox.md) <br/> |<span data-ttu-id="5b9d3-118">标识用于标识网络上的计算机的 IP 版本4（IPv4）地址范围的起始地址。</span><span class="sxs-lookup"><span data-stu-id="5b9d3-118">Identifies the start of a range of IP version 4 (IPv4) addresses that are used to identify a computer on a network.</span></span>  <br/> |
|[<span data-ttu-id="5b9d3-119">IPv4End （POX）</span><span class="sxs-lookup"><span data-stu-id="5b9d3-119">IPv4End (POX)</span></span>](ipv4end-pox.md) <br/> |<span data-ttu-id="5b9d3-120">标识用于标识网络上的计算机的 IP 版本4（IPv4）地址范围的结束地址。</span><span class="sxs-lookup"><span data-stu-id="5b9d3-120">Identifies the end of a range of IP version 4 (IPv4) addresses that are used to identify a computer on the network.</span></span>  <br/> |
|[<span data-ttu-id="5b9d3-121">IPv6Start （POX）</span><span class="sxs-lookup"><span data-stu-id="5b9d3-121">IPv6Start (POX)</span></span>](ipv6start-pox.md) <br/> |<span data-ttu-id="5b9d3-122">标识用于标识网络上的计算机的 IP 版本6（IPv6）地址范围的起始地址。</span><span class="sxs-lookup"><span data-stu-id="5b9d3-122">Identifies the start of a range of IP version 6 (IPv6) addresses that are used to identify a computer on a network.</span></span>  <br/> |
|[<span data-ttu-id="5b9d3-123">IPv6End （POX）</span><span class="sxs-lookup"><span data-stu-id="5b9d3-123">IPv6End (POX)</span></span>](ipv6end-pox.md) <br/> |<span data-ttu-id="5b9d3-124">标识用于标识网络上的计算机的 IP 版本6（IPv6）地址范围的结束。</span><span class="sxs-lookup"><span data-stu-id="5b9d3-124">Identifies the end of a range of IP version 6 (IPv6) addresses that are used to identify a computer on a network.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5b9d3-125">父元素</span><span class="sxs-lookup"><span data-stu-id="5b9d3-125">Parent elements</span></span>

|<span data-ttu-id="5b9d3-126">**元素**</span><span class="sxs-lookup"><span data-stu-id="5b9d3-126">**Element**</span></span>|<span data-ttu-id="5b9d3-127">**说明**</span><span class="sxs-lookup"><span data-stu-id="5b9d3-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5b9d3-128">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="5b9d3-128">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="5b9d3-129">包含用于将客户端连接到运行 Microsoft Exchange Server 2007 且安装了客户端访问服务器角色的计算机的规范。</span><span class="sxs-lookup"><span data-stu-id="5b9d3-129">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5b9d3-130">备注</span><span class="sxs-lookup"><span data-stu-id="5b9d3-130">Remarks</span></span>

<span data-ttu-id="5b9d3-131">如果电子邮件客户端不符合网络要求，它应尝试其他协议类型。</span><span class="sxs-lookup"><span data-stu-id="5b9d3-131">If the e-mail client does not match the network requirements, it should try other protocol types.</span></span> <span data-ttu-id="5b9d3-132">Isp 可以为一组具有[协议（POX）](protocol-pox.md)标记的服务器提供不需要进行身份验证，但必须在 ISP 网络中进行身份验证的服务器。</span><span class="sxs-lookup"><span data-stu-id="5b9d3-132">ISPs may provide one set of servers with [Protocol (POX)](protocol-pox.md) tags that do not require authentication but are required to be on the ISP network.</span></span> <span data-ttu-id="5b9d3-133">Isp 可能列出了需要进行身份验证但不需要在特定网络上的另一组服务器。</span><span class="sxs-lookup"><span data-stu-id="5b9d3-133">ISPs may list another set of servers that require authentication but are not required to be on a specific network.</span></span> 
  
<span data-ttu-id="5b9d3-134">**NetworkRequirements**元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="5b9d3-134">The **NetworkRequirements** element is optional.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5b9d3-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5b9d3-135">See also</span></span>



[<span data-ttu-id="5b9d3-136">Exchange 的 POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="5b9d3-136">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

