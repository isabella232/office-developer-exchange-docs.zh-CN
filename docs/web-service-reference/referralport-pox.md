---
title: ReferralPort （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: cd693f1e-fed4-4eb9-8297-178906f47050
description: ReferralPort 元素指定用于获取目录引用的端口。
ms.openlocfilehash: 6b3968d7b2f252439d2dfbc647bd8337668cf818
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456792"
---
# <a name="referralport-pox"></a><span data-ttu-id="bc921-103">ReferralPort （POX）</span><span class="sxs-lookup"><span data-stu-id="bc921-103">ReferralPort (POX)</span></span>

<span data-ttu-id="bc921-104">**ReferralPort**元素指定用于获取目录引用的端口。</span><span class="sxs-lookup"><span data-stu-id="bc921-104">The **ReferralPort** element specifies the port that is used to get a referral to a directory.</span></span> 
  
[<span data-ttu-id="bc921-105">自动发现（POX）</span><span class="sxs-lookup"><span data-stu-id="bc921-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="bc921-106">响应（POX）</span><span class="sxs-lookup"><span data-stu-id="bc921-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="bc921-107">帐户（POX）</span><span class="sxs-lookup"><span data-stu-id="bc921-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="bc921-108">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="bc921-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="bc921-109">ReferralPort （POX）</span><span class="sxs-lookup"><span data-stu-id="bc921-109">ReferralPort (POX)</span></span>](referralport-pox.md)
  
```xml
<ReferralPort/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="bc921-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="bc921-110">Attributes and elements</span></span>

<span data-ttu-id="bc921-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="bc921-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bc921-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="bc921-112">Attributes</span></span>

<span data-ttu-id="bc921-113">无。</span><span class="sxs-lookup"><span data-stu-id="bc921-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bc921-114">子元素</span><span class="sxs-lookup"><span data-stu-id="bc921-114">Child elements</span></span>

<span data-ttu-id="bc921-115">无。</span><span class="sxs-lookup"><span data-stu-id="bc921-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="bc921-116">父元素</span><span class="sxs-lookup"><span data-stu-id="bc921-116">Parent elements</span></span>

|<span data-ttu-id="bc921-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="bc921-117">**Element**</span></span>|<span data-ttu-id="bc921-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="bc921-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bc921-119">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="bc921-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="bc921-120">包含用于将客户端连接到运行 Microsoft Exchange Server 2007 且安装了客户端访问服务器角色的计算机的规范。</span><span class="sxs-lookup"><span data-stu-id="bc921-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="bc921-121">文本值</span><span class="sxs-lookup"><span data-stu-id="bc921-121">Text value</span></span>

<span data-ttu-id="bc921-122">该文本值表示用于访问 Exchange 服务器的端口。</span><span class="sxs-lookup"><span data-stu-id="bc921-122">The text value represents the port that is used to access the Exchange server.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bc921-123">备注</span><span class="sxs-lookup"><span data-stu-id="bc921-123">Remarks</span></span>

<span data-ttu-id="bc921-124">仅当[Type （POX）](type-pox.md)元素等于 EXCH 或 EXPR 时，才使用**ReferralPort**元素。</span><span class="sxs-lookup"><span data-stu-id="bc921-124">The **ReferralPort** element is only used when the [Type (POX)](type-pox.md) element equals EXCH or EXPR.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bc921-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bc921-125">See also</span></span>



[<span data-ttu-id="bc921-126">Exchange 的 POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="bc921-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

