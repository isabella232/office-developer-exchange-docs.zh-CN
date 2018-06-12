---
title: 端口 (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 4046821a-d6f3-4764-82be-4011221ce7a3
description: 端口元素指定用于连接到存储的端口。
ms.openlocfilehash: f5a2155d97061a87fdf819549ec29898efe4d201
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826842"
---
# <a name="port-pox"></a><span data-ttu-id="38e5b-103">端口 (POX)</span><span class="sxs-lookup"><span data-stu-id="38e5b-103">Port (POX)</span></span>

<span data-ttu-id="38e5b-104">**端口**元素指定用于连接到存储的端口。</span><span class="sxs-lookup"><span data-stu-id="38e5b-104">The **Port** element specifies the port that is used to connect to the store.</span></span> 
  
[<span data-ttu-id="38e5b-105">自动发现 (POX)</span><span class="sxs-lookup"><span data-stu-id="38e5b-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="38e5b-106">响应 (POX)</span><span class="sxs-lookup"><span data-stu-id="38e5b-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="38e5b-107">帐户 (POX)</span><span class="sxs-lookup"><span data-stu-id="38e5b-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="38e5b-108">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="38e5b-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="38e5b-109">端口 (POX)</span><span class="sxs-lookup"><span data-stu-id="38e5b-109">Port (POX)</span></span>](port-pox.md)
  
```xml
<Port/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="38e5b-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="38e5b-110">Attributes and elements</span></span>

<span data-ttu-id="38e5b-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="38e5b-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="38e5b-112">属性</span><span class="sxs-lookup"><span data-stu-id="38e5b-112">Attributes</span></span>

<span data-ttu-id="38e5b-113">无。</span><span class="sxs-lookup"><span data-stu-id="38e5b-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="38e5b-114">子元素</span><span class="sxs-lookup"><span data-stu-id="38e5b-114">Child elements</span></span>

<span data-ttu-id="38e5b-115">无。</span><span class="sxs-lookup"><span data-stu-id="38e5b-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="38e5b-116">父元素</span><span class="sxs-lookup"><span data-stu-id="38e5b-116">Parent elements</span></span>

|<span data-ttu-id="38e5b-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="38e5b-117">**Element**</span></span>|<span data-ttu-id="38e5b-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="38e5b-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="38e5b-119">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="38e5b-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="38e5b-120">包含客户端连接到运行 Microsoft Exchange Server 2007 的安装了客户端访问服务器角色的计算机的规格。</span><span class="sxs-lookup"><span data-stu-id="38e5b-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="38e5b-121">文本值</span><span class="sxs-lookup"><span data-stu-id="38e5b-121">Text value</span></span>

<span data-ttu-id="38e5b-122">文本值表示用于访问 Exchange 服务器的端口。</span><span class="sxs-lookup"><span data-stu-id="38e5b-122">The text value represents the port that is used to access the Exchange server.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="38e5b-123">备注</span><span class="sxs-lookup"><span data-stu-id="38e5b-123">Remarks</span></span>

<span data-ttu-id="38e5b-124">如果[服务器 (POX)](server-pox.md)元素包含一个 URL，则不使用的**端口**值。</span><span class="sxs-lookup"><span data-stu-id="38e5b-124">The **Port** value is not used if the [Server (POX)](server-pox.md) element contains a URL.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="38e5b-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="38e5b-125">See also</span></span>



[<span data-ttu-id="38e5b-126">Exchange POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="38e5b-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

