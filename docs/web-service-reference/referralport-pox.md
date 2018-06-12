---
title: ReferralPort (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: cd693f1e-fed4-4eb9-8297-178906f47050
description: ReferralPort 元素指定用于获取目录引用的端口。
ms.openlocfilehash: 5045c0c5a9f15d5a31ac2e884b942e00dfb1f520
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827037"
---
# <a name="referralport-pox"></a><span data-ttu-id="42457-103">ReferralPort (POX)</span><span class="sxs-lookup"><span data-stu-id="42457-103">ReferralPort (POX)</span></span>

<span data-ttu-id="42457-104">**ReferralPort**元素指定用于获取目录引用的端口。</span><span class="sxs-lookup"><span data-stu-id="42457-104">The **ReferralPort** element specifies the port that is used to get a referral to a directory.</span></span> 
  
[<span data-ttu-id="42457-105">自动发现 (POX)</span><span class="sxs-lookup"><span data-stu-id="42457-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="42457-106">响应 (POX)</span><span class="sxs-lookup"><span data-stu-id="42457-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="42457-107">帐户 (POX)</span><span class="sxs-lookup"><span data-stu-id="42457-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="42457-108">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="42457-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="42457-109">ReferralPort (POX)</span><span class="sxs-lookup"><span data-stu-id="42457-109">ReferralPort (POX)</span></span>](referralport-pox.md)
  
```xml
<ReferralPort/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="42457-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="42457-110">Attributes and elements</span></span>

<span data-ttu-id="42457-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="42457-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="42457-112">属性</span><span class="sxs-lookup"><span data-stu-id="42457-112">Attributes</span></span>

<span data-ttu-id="42457-113">无。</span><span class="sxs-lookup"><span data-stu-id="42457-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="42457-114">子元素</span><span class="sxs-lookup"><span data-stu-id="42457-114">Child elements</span></span>

<span data-ttu-id="42457-115">无。</span><span class="sxs-lookup"><span data-stu-id="42457-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="42457-116">父元素</span><span class="sxs-lookup"><span data-stu-id="42457-116">Parent elements</span></span>

|<span data-ttu-id="42457-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="42457-117">**Element**</span></span>|<span data-ttu-id="42457-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="42457-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="42457-119">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="42457-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="42457-120">包含客户端连接到运行 Microsoft Exchange Server 2007 的安装了客户端访问服务器角色的计算机的规格。</span><span class="sxs-lookup"><span data-stu-id="42457-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="42457-121">文本值</span><span class="sxs-lookup"><span data-stu-id="42457-121">Text value</span></span>

<span data-ttu-id="42457-122">文本值表示用于访问 Exchange 服务器的端口。</span><span class="sxs-lookup"><span data-stu-id="42457-122">The text value represents the port that is used to access the Exchange server.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="42457-123">备注</span><span class="sxs-lookup"><span data-stu-id="42457-123">Remarks</span></span>

<span data-ttu-id="42457-124">[类型 (POX)](type-pox.md)元素等于 EXCH 或 EXPR 时才使用**ReferralPort**元素。</span><span class="sxs-lookup"><span data-stu-id="42457-124">The **ReferralPort** element is only used when the [Type (POX)](type-pox.md) element equals EXCH or EXPR.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="42457-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="42457-125">See also</span></span>



[<span data-ttu-id="42457-126">Exchange POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="42457-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

