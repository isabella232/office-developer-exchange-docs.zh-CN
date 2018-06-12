---
title: SPA (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: fba018d5-0c65-4e1b-9767-d1ce8b356278
description: SPA 元素指示是否需要安全密码身份验证 (SPA)。
ms.openlocfilehash: 1fb0f3bb40e64be89eae7dfc208d51387f532191
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827533"
---
# <a name="spa-pox"></a><span data-ttu-id="090fe-103">SPA (POX)</span><span class="sxs-lookup"><span data-stu-id="090fe-103">SPA (POX)</span></span>

<span data-ttu-id="090fe-104">**SPA**元素指示是否需要安全密码身份验证 (SPA)。</span><span class="sxs-lookup"><span data-stu-id="090fe-104">The **SPA** element indicates whether Secure Password Authentication (SPA) is required.</span></span> 
  
[<span data-ttu-id="090fe-105">自动发现 (POX)</span><span class="sxs-lookup"><span data-stu-id="090fe-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="090fe-106">响应 (POX)</span><span class="sxs-lookup"><span data-stu-id="090fe-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="090fe-107">帐户 (POX)</span><span class="sxs-lookup"><span data-stu-id="090fe-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="090fe-108">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="090fe-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="090fe-109">SPA (POX)</span><span class="sxs-lookup"><span data-stu-id="090fe-109">SPA (POX)</span></span>](spa-pox.md)
  
```xml
<SPA/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="090fe-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="090fe-110">Attributes and elements</span></span>

<span data-ttu-id="090fe-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="090fe-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="090fe-112">属性</span><span class="sxs-lookup"><span data-stu-id="090fe-112">Attributes</span></span>

<span data-ttu-id="090fe-113">无。</span><span class="sxs-lookup"><span data-stu-id="090fe-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="090fe-114">子元素</span><span class="sxs-lookup"><span data-stu-id="090fe-114">Child elements</span></span>

<span data-ttu-id="090fe-115">无。</span><span class="sxs-lookup"><span data-stu-id="090fe-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="090fe-116">父元素</span><span class="sxs-lookup"><span data-stu-id="090fe-116">Parent elements</span></span>

|<span data-ttu-id="090fe-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="090fe-117">**Element**</span></span>|<span data-ttu-id="090fe-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="090fe-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="090fe-119">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="090fe-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="090fe-120">包含客户端连接到运行 Microsoft Exchange Server 2007 的安装了客户端访问服务器角色的计算机的规格。</span><span class="sxs-lookup"><span data-stu-id="090fe-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="090fe-121">文本值</span><span class="sxs-lookup"><span data-stu-id="090fe-121">Text value</span></span>

<span data-ttu-id="090fe-122">文本值指示是否需要 SPA。</span><span class="sxs-lookup"><span data-stu-id="090fe-122">The text value indicates whether SPA is required.</span></span> <span data-ttu-id="090fe-123">**上**的文本值时，SPA 是必需的。</span><span class="sxs-lookup"><span data-stu-id="090fe-123">If the text value is **on**, SPA is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="090fe-124">备注</span><span class="sxs-lookup"><span data-stu-id="090fe-124">Remarks</span></span>

<span data-ttu-id="090fe-125">如果此元素不存在，默认值设置为**上**。</span><span class="sxs-lookup"><span data-stu-id="090fe-125">If this element is not present, the default value is set to **on**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="090fe-126">另请参阅</span><span class="sxs-lookup"><span data-stu-id="090fe-126">See also</span></span>



[<span data-ttu-id="090fe-127">Exchange POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="090fe-127">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)
