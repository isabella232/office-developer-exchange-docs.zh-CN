---
title: RedirectUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: c54f310f-8c99-4c37-8e73-ac87722b6229
description: RedirectUrl 元素包含的计算机的运行 Microsoft Exchange Server 2007 的客户端访问服务器安装了角色，用于获取自动发现设置的 URL。
ms.openlocfilehash: 3b634f1a3a3d44b6aae1a826a005149200641dcb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827027"
---
# <a name="redirecturl-pox"></a><span data-ttu-id="f47eb-103">RedirectUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="f47eb-103">RedirectUrl (POX)</span></span>

<span data-ttu-id="f47eb-104">**RedirectUrl**元素包含的计算机的运行 Microsoft Exchange Server 2007 的客户端访问服务器安装了角色，用于获取自动发现设置的 URL。</span><span class="sxs-lookup"><span data-stu-id="f47eb-104">The **RedirectUrl** element contains the URL of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed that should be used to obtain Autodiscover settings.</span></span> 
  
[<span data-ttu-id="f47eb-105">自动发现 (POX)</span><span class="sxs-lookup"><span data-stu-id="f47eb-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="f47eb-106">响应 (POX)</span><span class="sxs-lookup"><span data-stu-id="f47eb-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="f47eb-107">帐户 (POX)</span><span class="sxs-lookup"><span data-stu-id="f47eb-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="f47eb-108">RedirectUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="f47eb-108">RedirectUrl (POX)</span></span>](redirecturl-pox.md)
  
```xml
<RedirectUrl/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="f47eb-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f47eb-109">Attributes and elements</span></span>

<span data-ttu-id="f47eb-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f47eb-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f47eb-111">属性</span><span class="sxs-lookup"><span data-stu-id="f47eb-111">Attributes</span></span>

<span data-ttu-id="f47eb-112">无。</span><span class="sxs-lookup"><span data-stu-id="f47eb-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f47eb-113">子元素</span><span class="sxs-lookup"><span data-stu-id="f47eb-113">Child elements</span></span>

<span data-ttu-id="f47eb-114">无。</span><span class="sxs-lookup"><span data-stu-id="f47eb-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f47eb-115">父元素</span><span class="sxs-lookup"><span data-stu-id="f47eb-115">Parent elements</span></span>

|<span data-ttu-id="f47eb-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="f47eb-116">**Element**</span></span>|<span data-ttu-id="f47eb-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="f47eb-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f47eb-118">帐户 (POX)</span><span class="sxs-lookup"><span data-stu-id="f47eb-118">Account (POX)</span></span>](account-pox.md) <br/> |<span data-ttu-id="f47eb-119">指定用户帐户的设置。</span><span class="sxs-lookup"><span data-stu-id="f47eb-119">Specifies account settings for the user.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f47eb-120">文本值</span><span class="sxs-lookup"><span data-stu-id="f47eb-120">Text value</span></span>

<span data-ttu-id="f47eb-121">文本值表示用于获取自动发现设置客户端访问服务器的 URL。</span><span class="sxs-lookup"><span data-stu-id="f47eb-121">The text value represents the URL of the Client Access server that should be used to obtain Autodiscover settings.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f47eb-122">注解</span><span class="sxs-lookup"><span data-stu-id="f47eb-122">Remarks</span></span>

<span data-ttu-id="f47eb-123">客户端应用程序应停止 10 次重定向后重定向。</span><span class="sxs-lookup"><span data-stu-id="f47eb-123">The client application should stop redirecting after 10 redirects.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f47eb-124">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f47eb-124">See also</span></span>



[<span data-ttu-id="f47eb-125">Exchange POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="f47eb-125">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

