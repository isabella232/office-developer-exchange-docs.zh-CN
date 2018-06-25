---
title: RedirectAddr (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 0e9fa6b6-7991-4dc1-a59a-48e5f8e041e4
description: RedirectAddr 元素指定应用于后续的自动发现请求的电子邮件地址。
ms.openlocfilehash: fe15054b9962fc2decf52ac3c42536e36358948a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827020"
---
# <a name="redirectaddr-pox"></a><span data-ttu-id="589fd-103">RedirectAddr (POX)</span><span class="sxs-lookup"><span data-stu-id="589fd-103">RedirectAddr (POX)</span></span>

<span data-ttu-id="589fd-104">**RedirectAddr**元素指定应用于后续的自动发现请求的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="589fd-104">The **RedirectAddr** element specifies the e-mail address that should be used for a subsequent Autodiscover request.</span></span> 
  
[<span data-ttu-id="589fd-105">自动发现 (POX)</span><span class="sxs-lookup"><span data-stu-id="589fd-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="589fd-106">响应 (POX)</span><span class="sxs-lookup"><span data-stu-id="589fd-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="589fd-107">帐户 (POX)</span><span class="sxs-lookup"><span data-stu-id="589fd-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="589fd-108">RedirectAddr (POX)</span><span class="sxs-lookup"><span data-stu-id="589fd-108">RedirectAddr (POX)</span></span>](redirectaddr-pox.md)
  
```xml
<RedirectAddr/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="589fd-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="589fd-109">Attributes and elements</span></span>

<span data-ttu-id="589fd-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="589fd-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="589fd-111">属性</span><span class="sxs-lookup"><span data-stu-id="589fd-111">Attributes</span></span>

<span data-ttu-id="589fd-112">无。</span><span class="sxs-lookup"><span data-stu-id="589fd-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="589fd-113">子元素</span><span class="sxs-lookup"><span data-stu-id="589fd-113">Child elements</span></span>

<span data-ttu-id="589fd-114">无。</span><span class="sxs-lookup"><span data-stu-id="589fd-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="589fd-115">父元素</span><span class="sxs-lookup"><span data-stu-id="589fd-115">Parent elements</span></span>

|<span data-ttu-id="589fd-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="589fd-116">**Element**</span></span>|<span data-ttu-id="589fd-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="589fd-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="589fd-118">帐户 (POX)</span><span class="sxs-lookup"><span data-stu-id="589fd-118">Account (POX)</span></span>](account-pox.md) <br/> |<span data-ttu-id="589fd-119">指定用户帐户的设置。</span><span class="sxs-lookup"><span data-stu-id="589fd-119">Specifies account settings for the user.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="589fd-120">文本值</span><span class="sxs-lookup"><span data-stu-id="589fd-120">Text value</span></span>

<span data-ttu-id="589fd-121">文本值代表应用于后续的自动发现请求的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="589fd-121">The text value represents the e-mail address that should be used for a subsequent Autodiscover request.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="589fd-122">注解</span><span class="sxs-lookup"><span data-stu-id="589fd-122">Remarks</span></span>

<span data-ttu-id="589fd-123">如果此元素的自动发现响应中存在，请通过使用**RedirectAddr**元素的文本值中进行另一个请求。</span><span class="sxs-lookup"><span data-stu-id="589fd-123">If this element is present in the Autodiscover response, make another request by using the text value of the **RedirectAddr** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="589fd-124">另请参阅</span><span class="sxs-lookup"><span data-stu-id="589fd-124">See also</span></span>



[<span data-ttu-id="589fd-125">Exchange POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="589fd-125">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

