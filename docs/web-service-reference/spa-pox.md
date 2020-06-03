---
title: SPA （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: fba018d5-0c65-4e1b-9767-d1ce8b356278
description: SPA 元素指示是否需要安全密码身份验证（SPA）。
ms.openlocfilehash: cf57b3a6046b1b9b030b7cae81381189eee92c1c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467639"
---
# <a name="spa-pox"></a><span data-ttu-id="d9154-103">SPA （POX）</span><span class="sxs-lookup"><span data-stu-id="d9154-103">SPA (POX)</span></span>

<span data-ttu-id="d9154-104">**SPA**元素指示是否需要安全密码身份验证（SPA）。</span><span class="sxs-lookup"><span data-stu-id="d9154-104">The **SPA** element indicates whether Secure Password Authentication (SPA) is required.</span></span> 
  
[<span data-ttu-id="d9154-105">自动发现（POX）</span><span class="sxs-lookup"><span data-stu-id="d9154-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="d9154-106">响应（POX）</span><span class="sxs-lookup"><span data-stu-id="d9154-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="d9154-107">帐户（POX）</span><span class="sxs-lookup"><span data-stu-id="d9154-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="d9154-108">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="d9154-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="d9154-109">SPA （POX）</span><span class="sxs-lookup"><span data-stu-id="d9154-109">SPA (POX)</span></span>](spa-pox.md)
  
```xml
<SPA/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="d9154-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d9154-110">Attributes and elements</span></span>

<span data-ttu-id="d9154-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d9154-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d9154-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="d9154-112">Attributes</span></span>

<span data-ttu-id="d9154-113">无。</span><span class="sxs-lookup"><span data-stu-id="d9154-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d9154-114">子元素</span><span class="sxs-lookup"><span data-stu-id="d9154-114">Child elements</span></span>

<span data-ttu-id="d9154-115">无。</span><span class="sxs-lookup"><span data-stu-id="d9154-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d9154-116">父元素</span><span class="sxs-lookup"><span data-stu-id="d9154-116">Parent elements</span></span>

|<span data-ttu-id="d9154-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="d9154-117">**Element**</span></span>|<span data-ttu-id="d9154-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="d9154-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d9154-119">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="d9154-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="d9154-120">包含用于将客户端连接到运行 Microsoft Exchange Server 2007 且安装了客户端访问服务器角色的计算机的规范。</span><span class="sxs-lookup"><span data-stu-id="d9154-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d9154-121">文本值</span><span class="sxs-lookup"><span data-stu-id="d9154-121">Text value</span></span>

<span data-ttu-id="d9154-122">该文本值指示是否需要 SPA。</span><span class="sxs-lookup"><span data-stu-id="d9154-122">The text value indicates whether SPA is required.</span></span> <span data-ttu-id="d9154-123">如果文本值为 **"开**"，则需要 SPA。</span><span class="sxs-lookup"><span data-stu-id="d9154-123">If the text value is **on**, SPA is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d9154-124">备注</span><span class="sxs-lookup"><span data-stu-id="d9154-124">Remarks</span></span>

<span data-ttu-id="d9154-125">如果此元素不存在，则默认值设置为 **"开**"。</span><span class="sxs-lookup"><span data-stu-id="d9154-125">If this element is not present, the default value is set to **on**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d9154-126">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d9154-126">See also</span></span>



[<span data-ttu-id="d9154-127">Exchange 的 POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="d9154-127">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

