---
title: RedirectUrl （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: c54f310f-8c99-4c37-8e73-ac87722b6229
description: RedirectUrl 元素包含运行 Microsoft Exchange Server 2007 且安装了应用于获取自动发现设置的客户端访问服务器角色的计算机的 URL。
ms.openlocfilehash: 5400b1e7a4bb7ebebc58b6a0f1fc9bf37f5a2e22
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468087"
---
# <a name="redirecturl-pox"></a><span data-ttu-id="730bd-103">RedirectUrl （POX）</span><span class="sxs-lookup"><span data-stu-id="730bd-103">RedirectUrl (POX)</span></span>

<span data-ttu-id="730bd-104">**RedirectUrl**元素包含运行 Microsoft Exchange server 2007 且安装了应用于获取自动发现设置的客户端访问服务器角色的计算机的 URL。</span><span class="sxs-lookup"><span data-stu-id="730bd-104">The **RedirectUrl** element contains the URL of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed that should be used to obtain Autodiscover settings.</span></span> 
  
[<span data-ttu-id="730bd-105">自动发现（POX）</span><span class="sxs-lookup"><span data-stu-id="730bd-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="730bd-106">响应（POX）</span><span class="sxs-lookup"><span data-stu-id="730bd-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="730bd-107">帐户（POX）</span><span class="sxs-lookup"><span data-stu-id="730bd-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="730bd-108">RedirectUrl （POX）</span><span class="sxs-lookup"><span data-stu-id="730bd-108">RedirectUrl (POX)</span></span>](redirecturl-pox.md)
  
```xml
<RedirectUrl/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="730bd-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="730bd-109">Attributes and elements</span></span>

<span data-ttu-id="730bd-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="730bd-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="730bd-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="730bd-111">Attributes</span></span>

<span data-ttu-id="730bd-112">无。</span><span class="sxs-lookup"><span data-stu-id="730bd-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="730bd-113">子元素</span><span class="sxs-lookup"><span data-stu-id="730bd-113">Child elements</span></span>

<span data-ttu-id="730bd-114">无。</span><span class="sxs-lookup"><span data-stu-id="730bd-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="730bd-115">父元素</span><span class="sxs-lookup"><span data-stu-id="730bd-115">Parent elements</span></span>

|<span data-ttu-id="730bd-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="730bd-116">**Element**</span></span>|<span data-ttu-id="730bd-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="730bd-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="730bd-118">帐户（POX）</span><span class="sxs-lookup"><span data-stu-id="730bd-118">Account (POX)</span></span>](account-pox.md) <br/> |<span data-ttu-id="730bd-119">指定用户的帐户设置。</span><span class="sxs-lookup"><span data-stu-id="730bd-119">Specifies account settings for the user.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="730bd-120">文本值</span><span class="sxs-lookup"><span data-stu-id="730bd-120">Text value</span></span>

<span data-ttu-id="730bd-121">Text 值表示应用于获取自动发现设置的客户端访问服务器的 URL。</span><span class="sxs-lookup"><span data-stu-id="730bd-121">The text value represents the URL of the Client Access server that should be used to obtain Autodiscover settings.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="730bd-122">备注</span><span class="sxs-lookup"><span data-stu-id="730bd-122">Remarks</span></span>

<span data-ttu-id="730bd-123">客户端应用程序应在10次重定向后停止重定向。</span><span class="sxs-lookup"><span data-stu-id="730bd-123">The client application should stop redirecting after 10 redirects.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="730bd-124">另请参阅</span><span class="sxs-lookup"><span data-stu-id="730bd-124">See also</span></span>



[<span data-ttu-id="730bd-125">Exchange 的 POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="730bd-125">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

