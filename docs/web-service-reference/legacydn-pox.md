---
title: LegacyDN (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 9fb9529f-52c5-4907-a84b-935b78de16c3
description: LegacyDN 元素标识用户的邮箱的旧的可分辨名称。
ms.openlocfilehash: f7ec1dea29a7d3ad6d470ef7812390d179fe1d2a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826243"
---
# <a name="legacydn-pox"></a><span data-ttu-id="41671-103">LegacyDN (POX)</span><span class="sxs-lookup"><span data-stu-id="41671-103">LegacyDN (POX)</span></span>

<span data-ttu-id="41671-104">**LegacyDN**元素标识用户的邮箱的旧的可分辨名称。</span><span class="sxs-lookup"><span data-stu-id="41671-104">The **LegacyDN** element identifies a user's mailbox by legacy distinguished name.</span></span> 
  
```xml
<LegacyDN/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="41671-105">属性和元素</span><span class="sxs-lookup"><span data-stu-id="41671-105">Attributes and elements</span></span>

<span data-ttu-id="41671-106">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="41671-106">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="41671-107">属性</span><span class="sxs-lookup"><span data-stu-id="41671-107">Attributes</span></span>

<span data-ttu-id="41671-108">无。</span><span class="sxs-lookup"><span data-stu-id="41671-108">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="41671-109">子元素</span><span class="sxs-lookup"><span data-stu-id="41671-109">Child elements</span></span>

<span data-ttu-id="41671-110">无。</span><span class="sxs-lookup"><span data-stu-id="41671-110">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="41671-111">父元素</span><span class="sxs-lookup"><span data-stu-id="41671-111">Parent elements</span></span>

|<span data-ttu-id="41671-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="41671-112">**Element**</span></span>|<span data-ttu-id="41671-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="41671-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="41671-114">请求 (POX)</span><span class="sxs-lookup"><span data-stu-id="41671-114">Request (POX)</span></span>](request-pox.md) <br/> |<span data-ttu-id="41671-115">包含对自动发现服务的请求。</span><span class="sxs-lookup"><span data-stu-id="41671-115">Contains the request to the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="41671-116">用户 (POX)</span><span class="sxs-lookup"><span data-stu-id="41671-116">User (POX)</span></span>](user-pox.md) <br/> |<span data-ttu-id="41671-117">提供特定于用户的信息。</span><span class="sxs-lookup"><span data-stu-id="41671-117">Provides user-specific information.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="41671-118">文本值</span><span class="sxs-lookup"><span data-stu-id="41671-118">Text value</span></span>

<span data-ttu-id="41671-119">文本值表示用户的旧的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="41671-119">The text value represents a user's legacy e-mail address.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="41671-120">注解</span><span class="sxs-lookup"><span data-stu-id="41671-120">Remarks</span></span>

<span data-ttu-id="41671-121">[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md)元素是自动发现请求的其他元素。</span><span class="sxs-lookup"><span data-stu-id="41671-121">The [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) element is an alternative element for an Autodiscover request.</span></span> <span data-ttu-id="41671-122">运行 Microsoft Exchange Server 2007 的计算机上存在的邮箱时使用它。</span><span class="sxs-lookup"><span data-stu-id="41671-122">It is used when a mailbox exists on a computer that is running Microsoft Exchange Server 2007.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="41671-123">另请参阅</span><span class="sxs-lookup"><span data-stu-id="41671-123">See also</span></span>

- [<span data-ttu-id="41671-124">Exchange POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="41671-124">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

