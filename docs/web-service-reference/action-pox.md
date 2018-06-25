---
title: 操作 (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a3462c6b-453c-462a-830d-f29ee4a2babb
description: Action 元素提供用于确定是否需要返回用户配置信息的另一个自动发现请求的信息。
ms.openlocfilehash: 118bb59f2c929e3c74683dbf3f073da34d67a3e7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754267"
---
# <a name="action-pox"></a><span data-ttu-id="7dcdc-103">操作 (POX)</span><span class="sxs-lookup"><span data-stu-id="7dcdc-103">Action (POX)</span></span>

<span data-ttu-id="7dcdc-104">**Action**元素提供用于确定是否需要返回用户配置信息的另一个自动发现请求的信息。</span><span class="sxs-lookup"><span data-stu-id="7dcdc-104">The **Action** element provides information that is used to determine whether another Autodiscover request is required to return the user configuration information.</span></span> 
  
- [<span data-ttu-id="7dcdc-105">自动发现 (POX)</span><span class="sxs-lookup"><span data-stu-id="7dcdc-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
- [<span data-ttu-id="7dcdc-106">响应 (POX)</span><span class="sxs-lookup"><span data-stu-id="7dcdc-106">Response (POX)</span></span>](response-pox.md)
  
- [<span data-ttu-id="7dcdc-107">帐户 (POX)</span><span class="sxs-lookup"><span data-stu-id="7dcdc-107">Account (POX)</span></span>](account-pox.md)
  
- [<span data-ttu-id="7dcdc-108">操作 (POX)</span><span class="sxs-lookup"><span data-stu-id="7dcdc-108">Action (POX)</span></span>](action-pox.md)
  
```xml
<Action>redirectUrl or redirectAddr or settings</Action>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="7dcdc-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7dcdc-109">Attributes and elements</span></span>

<span data-ttu-id="7dcdc-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7dcdc-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7dcdc-111">属性</span><span class="sxs-lookup"><span data-stu-id="7dcdc-111">Attributes</span></span>

<span data-ttu-id="7dcdc-112">无。</span><span class="sxs-lookup"><span data-stu-id="7dcdc-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7dcdc-113">子元素</span><span class="sxs-lookup"><span data-stu-id="7dcdc-113">Child elements</span></span>

<span data-ttu-id="7dcdc-114">无。</span><span class="sxs-lookup"><span data-stu-id="7dcdc-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7dcdc-115">父元素</span><span class="sxs-lookup"><span data-stu-id="7dcdc-115">Parent elements</span></span>

|<span data-ttu-id="7dcdc-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="7dcdc-116">**Element**</span></span>|<span data-ttu-id="7dcdc-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="7dcdc-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7dcdc-118">帐户 (POX)</span><span class="sxs-lookup"><span data-stu-id="7dcdc-118">Account (POX)</span></span>](account-pox.md) <br/> |<span data-ttu-id="7dcdc-119">指定用户帐户的设置。</span><span class="sxs-lookup"><span data-stu-id="7dcdc-119">Specifies account settings for the user.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7dcdc-120">文本值</span><span class="sxs-lookup"><span data-stu-id="7dcdc-120">Text value</span></span>

<span data-ttu-id="7dcdc-121">文本值表示另一个自动发现请求是否需要检索用户的配置信息。</span><span class="sxs-lookup"><span data-stu-id="7dcdc-121">The text value represents whether another Autodiscover request is necessary to retrieve the user's configuration information.</span></span> <span data-ttu-id="7dcdc-122">下表列出了可能的值。</span><span class="sxs-lookup"><span data-stu-id="7dcdc-122">The following table lists the possible values.</span></span>
  
|<span data-ttu-id="7dcdc-123">**值**</span><span class="sxs-lookup"><span data-stu-id="7dcdc-123">**Value**</span></span>|<span data-ttu-id="7dcdc-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="7dcdc-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7dcdc-125">redirectUrl</span><span class="sxs-lookup"><span data-stu-id="7dcdc-125">redirectUrl</span></span>  <br/> |<span data-ttu-id="7dcdc-126">如果指定此值，则[RedirectUrl (POX)](redirecturl-pox.md)元素将指定在后续的自动发现请求中使用的客户端访问服务器 URL。</span><span class="sxs-lookup"><span data-stu-id="7dcdc-126">If this value is specified, the [RedirectUrl (POX)](redirecturl-pox.md) element will specify the Client Access server URL to be used in the subsequent Autodiscover request.</span></span> <span data-ttu-id="7dcdc-127">客户端应用程序应停止 10 次重定向后重定向。</span><span class="sxs-lookup"><span data-stu-id="7dcdc-127">The client application should stop redirecting after 10 redirects.</span></span>  <br/> |
|<span data-ttu-id="7dcdc-128">redirectAddr</span><span class="sxs-lookup"><span data-stu-id="7dcdc-128">redirectAddr</span></span>  <br/> |<span data-ttu-id="7dcdc-129">如果指定此值，则[RedirectAddr (POX)](redirectaddr-pox.md)元素将指定应用于后续的自动发现请求的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="7dcdc-129">If this value is specified, the [RedirectAddr (POX)](redirectaddr-pox.md) element will specify the e-mail address that should be used for a subsequent Autodiscover request.</span></span>  <br/> |
|<span data-ttu-id="7dcdc-130">settings</span><span class="sxs-lookup"><span data-stu-id="7dcdc-130">settings</span></span>  <br/> |<span data-ttu-id="7dcdc-131">如果指定此值，则自动发现响应中包含用于配置帐户的设置。</span><span class="sxs-lookup"><span data-stu-id="7dcdc-131">If this value is specified, the Autodiscover response contains settings that are used to configure the account.</span></span> <span data-ttu-id="7dcdc-132">将[协议 (POX)](protocol-pox.md)元素中找到的大多数设置。</span><span class="sxs-lookup"><span data-stu-id="7dcdc-132">Most of the settings will be found in the [Protocol (POX)](protocol-pox.md) element.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7dcdc-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7dcdc-133">See also</span></span>

- [<span data-ttu-id="7dcdc-134">Exchange POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="7dcdc-134">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

