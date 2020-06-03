---
title: RedirectAddr （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 0e9fa6b6-7991-4dc1-a59a-48e5f8e041e4
description: RedirectAddr 元素指定应用于后续自动发现请求的电子邮件地址。
ms.openlocfilehash: 6bff28001851f421b4c7429770185401f2f0a743
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529873"
---
# <a name="redirectaddr-pox"></a><span data-ttu-id="8d6f7-103">RedirectAddr （POX）</span><span class="sxs-lookup"><span data-stu-id="8d6f7-103">RedirectAddr (POX)</span></span>

<span data-ttu-id="8d6f7-104">**RedirectAddr**元素指定应用于后续自动发现请求的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="8d6f7-104">The **RedirectAddr** element specifies the e-mail address that should be used for a subsequent Autodiscover request.</span></span> 
  
[<span data-ttu-id="8d6f7-105">自动发现（POX）</span><span class="sxs-lookup"><span data-stu-id="8d6f7-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="8d6f7-106">响应（POX）</span><span class="sxs-lookup"><span data-stu-id="8d6f7-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="8d6f7-107">帐户（POX）</span><span class="sxs-lookup"><span data-stu-id="8d6f7-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="8d6f7-108">RedirectAddr （POX）</span><span class="sxs-lookup"><span data-stu-id="8d6f7-108">RedirectAddr (POX)</span></span>](redirectaddr-pox.md)
  
```xml
<RedirectAddr/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="8d6f7-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8d6f7-109">Attributes and elements</span></span>

<span data-ttu-id="8d6f7-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8d6f7-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8d6f7-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="8d6f7-111">Attributes</span></span>

<span data-ttu-id="8d6f7-112">无。</span><span class="sxs-lookup"><span data-stu-id="8d6f7-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8d6f7-113">子元素</span><span class="sxs-lookup"><span data-stu-id="8d6f7-113">Child elements</span></span>

<span data-ttu-id="8d6f7-114">无。</span><span class="sxs-lookup"><span data-stu-id="8d6f7-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8d6f7-115">父元素</span><span class="sxs-lookup"><span data-stu-id="8d6f7-115">Parent elements</span></span>

|<span data-ttu-id="8d6f7-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="8d6f7-116">**Element**</span></span>|<span data-ttu-id="8d6f7-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="8d6f7-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8d6f7-118">帐户（POX）</span><span class="sxs-lookup"><span data-stu-id="8d6f7-118">Account (POX)</span></span>](account-pox.md) <br/> |<span data-ttu-id="8d6f7-119">指定用户的帐户设置。</span><span class="sxs-lookup"><span data-stu-id="8d6f7-119">Specifies account settings for the user.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8d6f7-120">文本值</span><span class="sxs-lookup"><span data-stu-id="8d6f7-120">Text value</span></span>

<span data-ttu-id="8d6f7-121">该文本值表示应用于后续自动发现请求的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="8d6f7-121">The text value represents the e-mail address that should be used for a subsequent Autodiscover request.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8d6f7-122">备注</span><span class="sxs-lookup"><span data-stu-id="8d6f7-122">Remarks</span></span>

<span data-ttu-id="8d6f7-123">如果此元素存在于自动发现响应中，请使用**RedirectAddr**元素的文本值进行另一个请求。</span><span class="sxs-lookup"><span data-stu-id="8d6f7-123">If this element is present in the Autodiscover response, make another request by using the text value of the **RedirectAddr** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8d6f7-124">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8d6f7-124">See also</span></span>



[<span data-ttu-id="8d6f7-125">Exchange 的 POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="8d6f7-125">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

