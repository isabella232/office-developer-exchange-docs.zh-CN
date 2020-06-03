---
title: LegacyDN （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 9fb9529f-52c5-4907-a84b-935b78de16c3
description: LegacyDN 元素通过旧版可分辨名称标识用户的邮箱。
ms.openlocfilehash: b9af4278a5421dc932573396c3563a64a78de41e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526380"
---
# <a name="legacydn-pox"></a><span data-ttu-id="7751c-103">LegacyDN （POX）</span><span class="sxs-lookup"><span data-stu-id="7751c-103">LegacyDN (POX)</span></span>

<span data-ttu-id="7751c-104">**LegacyDN**元素通过旧版可分辨名称标识用户的邮箱。</span><span class="sxs-lookup"><span data-stu-id="7751c-104">The **LegacyDN** element identifies a user's mailbox by legacy distinguished name.</span></span> 
  
```xml
<LegacyDN/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="7751c-105">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7751c-105">Attributes and elements</span></span>

<span data-ttu-id="7751c-106">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7751c-106">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7751c-107">Attributes</span><span class="sxs-lookup"><span data-stu-id="7751c-107">Attributes</span></span>

<span data-ttu-id="7751c-108">无。</span><span class="sxs-lookup"><span data-stu-id="7751c-108">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7751c-109">子元素</span><span class="sxs-lookup"><span data-stu-id="7751c-109">Child elements</span></span>

<span data-ttu-id="7751c-110">无。</span><span class="sxs-lookup"><span data-stu-id="7751c-110">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7751c-111">父元素</span><span class="sxs-lookup"><span data-stu-id="7751c-111">Parent elements</span></span>

|<span data-ttu-id="7751c-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="7751c-112">**Element**</span></span>|<span data-ttu-id="7751c-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="7751c-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7751c-114">请求（POX）</span><span class="sxs-lookup"><span data-stu-id="7751c-114">Request (POX)</span></span>](request-pox.md) <br/> |<span data-ttu-id="7751c-115">包含对自动发现服务的请求。</span><span class="sxs-lookup"><span data-stu-id="7751c-115">Contains the request to the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="7751c-116">User （POX）</span><span class="sxs-lookup"><span data-stu-id="7751c-116">User (POX)</span></span>](user-pox.md) <br/> |<span data-ttu-id="7751c-117">提供用户特定的信息。</span><span class="sxs-lookup"><span data-stu-id="7751c-117">Provides user-specific information.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7751c-118">文本值</span><span class="sxs-lookup"><span data-stu-id="7751c-118">Text value</span></span>

<span data-ttu-id="7751c-119">该文本值表示用户的旧电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="7751c-119">The text value represents a user's legacy e-mail address.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7751c-120">备注</span><span class="sxs-lookup"><span data-stu-id="7751c-120">Remarks</span></span>

<span data-ttu-id="7751c-121">[EmailAddress （NonEmptyStringType）](emailaddress-nonemptystringtype.md)元素是自动发现请求的替代元素。</span><span class="sxs-lookup"><span data-stu-id="7751c-121">The [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) element is an alternative element for an Autodiscover request.</span></span> <span data-ttu-id="7751c-122">当运行 Microsoft Exchange Server 2007 的计算机上存在邮箱时，将使用此方法。</span><span class="sxs-lookup"><span data-stu-id="7751c-122">It is used when a mailbox exists on a computer that is running Microsoft Exchange Server 2007.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7751c-123">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7751c-123">See also</span></span>

- [<span data-ttu-id="7751c-124">Exchange 的 POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="7751c-124">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

