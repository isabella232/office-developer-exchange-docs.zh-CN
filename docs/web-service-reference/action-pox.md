---
title: Action （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a3462c6b-453c-462a-830d-f29ee4a2babb
description: Action 元素提供用于确定是否需要其他自动发现请求来返回用户配置信息的信息。
ms.openlocfilehash: f6d542b908948d09020b850b60ca1bdb025dd342
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529691"
---
# <a name="action-pox"></a><span data-ttu-id="2bba3-103">Action （POX）</span><span class="sxs-lookup"><span data-stu-id="2bba3-103">Action (POX)</span></span>

<span data-ttu-id="2bba3-104">**Action**元素提供用于确定是否需要其他自动发现请求来返回用户配置信息的信息。</span><span class="sxs-lookup"><span data-stu-id="2bba3-104">The **Action** element provides information that is used to determine whether another Autodiscover request is required to return the user configuration information.</span></span> 
  
- [<span data-ttu-id="2bba3-105">自动发现（POX）</span><span class="sxs-lookup"><span data-stu-id="2bba3-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
- [<span data-ttu-id="2bba3-106">响应（POX）</span><span class="sxs-lookup"><span data-stu-id="2bba3-106">Response (POX)</span></span>](response-pox.md)
  
- [<span data-ttu-id="2bba3-107">帐户（POX）</span><span class="sxs-lookup"><span data-stu-id="2bba3-107">Account (POX)</span></span>](account-pox.md)
  
- [<span data-ttu-id="2bba3-108">Action （POX）</span><span class="sxs-lookup"><span data-stu-id="2bba3-108">Action (POX)</span></span>](action-pox.md)
  
```xml
<Action>redirectUrl or redirectAddr or settings</Action>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="2bba3-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2bba3-109">Attributes and elements</span></span>

<span data-ttu-id="2bba3-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2bba3-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2bba3-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="2bba3-111">Attributes</span></span>

<span data-ttu-id="2bba3-112">无。</span><span class="sxs-lookup"><span data-stu-id="2bba3-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2bba3-113">子元素</span><span class="sxs-lookup"><span data-stu-id="2bba3-113">Child elements</span></span>

<span data-ttu-id="2bba3-114">无。</span><span class="sxs-lookup"><span data-stu-id="2bba3-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2bba3-115">父元素</span><span class="sxs-lookup"><span data-stu-id="2bba3-115">Parent elements</span></span>

|<span data-ttu-id="2bba3-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="2bba3-116">**Element**</span></span>|<span data-ttu-id="2bba3-117">**描述**</span><span class="sxs-lookup"><span data-stu-id="2bba3-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2bba3-118">帐户（POX）</span><span class="sxs-lookup"><span data-stu-id="2bba3-118">Account (POX)</span></span>](account-pox.md) <br/> |<span data-ttu-id="2bba3-119">指定用户的帐户设置。</span><span class="sxs-lookup"><span data-stu-id="2bba3-119">Specifies account settings for the user.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2bba3-120">文本值</span><span class="sxs-lookup"><span data-stu-id="2bba3-120">Text value</span></span>

<span data-ttu-id="2bba3-121">Text 值表示检索用户的配置信息是否需要其他自动发现请求。</span><span class="sxs-lookup"><span data-stu-id="2bba3-121">The text value represents whether another Autodiscover request is necessary to retrieve the user's configuration information.</span></span> <span data-ttu-id="2bba3-122">下表列出了可能的值。</span><span class="sxs-lookup"><span data-stu-id="2bba3-122">The following table lists the possible values.</span></span>
  
|<span data-ttu-id="2bba3-123">**值**</span><span class="sxs-lookup"><span data-stu-id="2bba3-123">**Value**</span></span>|<span data-ttu-id="2bba3-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="2bba3-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2bba3-125">redirectUrl</span><span class="sxs-lookup"><span data-stu-id="2bba3-125">redirectUrl</span></span>  <br/> |<span data-ttu-id="2bba3-126">如果指定此值， [RedirectUrl （POX）](redirecturl-pox.md)元素将指定要在后续自动发现请求中使用的客户端访问服务器 URL。</span><span class="sxs-lookup"><span data-stu-id="2bba3-126">If this value is specified, the [RedirectUrl (POX)](redirecturl-pox.md) element will specify the Client Access server URL to be used in the subsequent Autodiscover request.</span></span> <span data-ttu-id="2bba3-127">客户端应用程序应在10次重定向后停止重定向。</span><span class="sxs-lookup"><span data-stu-id="2bba3-127">The client application should stop redirecting after 10 redirects.</span></span>  <br/> |
|<span data-ttu-id="2bba3-128">redirectAddr</span><span class="sxs-lookup"><span data-stu-id="2bba3-128">redirectAddr</span></span>  <br/> |<span data-ttu-id="2bba3-129">如果指定此值， [RedirectAddr （POX）](redirectaddr-pox.md)元素将指定应用于后续自动发现请求的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="2bba3-129">If this value is specified, the [RedirectAddr (POX)](redirectaddr-pox.md) element will specify the e-mail address that should be used for a subsequent Autodiscover request.</span></span>  <br/> |
|<span data-ttu-id="2bba3-130">settings</span><span class="sxs-lookup"><span data-stu-id="2bba3-130">settings</span></span>  <br/> |<span data-ttu-id="2bba3-131">如果指定此值，自动发现响应将包含用于配置帐户的设置。</span><span class="sxs-lookup"><span data-stu-id="2bba3-131">If this value is specified, the Autodiscover response contains settings that are used to configure the account.</span></span> <span data-ttu-id="2bba3-132">大部分设置都将在[Protocol （POX）](protocol-pox.md)元素中找到。</span><span class="sxs-lookup"><span data-stu-id="2bba3-132">Most of the settings will be found in the [Protocol (POX)](protocol-pox.md) element.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2bba3-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2bba3-133">See also</span></span>

- [<span data-ttu-id="2bba3-134">Exchange 的 POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="2bba3-134">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

