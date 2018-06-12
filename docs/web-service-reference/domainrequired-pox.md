---
title: DomainRequired (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 1f26b691-7331-4c7f-a92b-dfcc66c26963
description: DomainRequired 元素指示域是否需要身份验证。
ms.openlocfilehash: f314b9d27d1b4ee472d249ec49af1a785ff9ac25
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753972"
---
# <a name="domainrequired-pox"></a><span data-ttu-id="d96b1-103">DomainRequired (POX)</span><span class="sxs-lookup"><span data-stu-id="d96b1-103">DomainRequired (POX)</span></span>

<span data-ttu-id="d96b1-104">**DomainRequired**元素指示域是否需要身份验证。</span><span class="sxs-lookup"><span data-stu-id="d96b1-104">The **DomainRequired** element indicates whether the domain is required for authentication.</span></span> 
  
- [<span data-ttu-id="d96b1-105">自动发现 (POX)</span><span class="sxs-lookup"><span data-stu-id="d96b1-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)  
- [<span data-ttu-id="d96b1-106">响应 (POX)</span><span class="sxs-lookup"><span data-stu-id="d96b1-106">Response (POX)</span></span>](response-pox.md) 
- [<span data-ttu-id="d96b1-107">帐户 (POX)</span><span class="sxs-lookup"><span data-stu-id="d96b1-107">Account (POX)</span></span>](account-pox.md)  
- [<span data-ttu-id="d96b1-108">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="d96b1-108">Protocol (POX)</span></span>](protocol-pox.md)  
- [<span data-ttu-id="d96b1-109">DomainRequired (POX)</span><span class="sxs-lookup"><span data-stu-id="d96b1-109">DomainRequired (POX)</span></span>](domainrequired-pox.md)
  
```xml
<DomainRequired>on or off</DomainRequired>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="d96b1-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d96b1-110">Attributes and elements</span></span>

<span data-ttu-id="d96b1-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d96b1-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d96b1-112">属性</span><span class="sxs-lookup"><span data-stu-id="d96b1-112">Attributes</span></span>

<span data-ttu-id="d96b1-113">无。</span><span class="sxs-lookup"><span data-stu-id="d96b1-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d96b1-114">子元素</span><span class="sxs-lookup"><span data-stu-id="d96b1-114">Child elements</span></span>

<span data-ttu-id="d96b1-115">无。</span><span class="sxs-lookup"><span data-stu-id="d96b1-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d96b1-116">父元素</span><span class="sxs-lookup"><span data-stu-id="d96b1-116">Parent elements</span></span>

|<span data-ttu-id="d96b1-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="d96b1-117">**Element**</span></span>|<span data-ttu-id="d96b1-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="d96b1-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d96b1-119">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="d96b1-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="d96b1-120">包含客户端连接到运行 Microsoft Exchange Server 2007 的安装了客户端访问服务器角色的计算机的规格。</span><span class="sxs-lookup"><span data-stu-id="d96b1-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d96b1-121">文本值</span><span class="sxs-lookup"><span data-stu-id="d96b1-121">Text value</span></span>

<span data-ttu-id="d96b1-122">文本值指示是否需要身份验证的域。</span><span class="sxs-lookup"><span data-stu-id="d96b1-122">The text value indicates whether the domain is required for authentication.</span></span> <span data-ttu-id="d96b1-123">可能的值为**在**打开和**关闭**。</span><span class="sxs-lookup"><span data-stu-id="d96b1-123">The possible values are **on** and **off**.</span></span> <span data-ttu-id="d96b1-124">如果值为**上**，后续请求必须包含用户的帐户的域。</span><span class="sxs-lookup"><span data-stu-id="d96b1-124">If the value is **on**, the subsequent request must contain the domain of the user's account.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d96b1-125">备注</span><span class="sxs-lookup"><span data-stu-id="d96b1-125">Remarks</span></span>

<span data-ttu-id="d96b1-126">如果在[使用 LoginName (POX)](loginname-pox.md)元素中，不指定域或未指定**LoginName**元素，用户必须输入的域之前身份验证将失败。</span><span class="sxs-lookup"><span data-stu-id="d96b1-126">If the domain is not specified in the [LoginName (POX)](loginname-pox.md) element, or the **LoginName** element was not specified, the user must enter the domain before authentication will succeed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d96b1-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d96b1-127">See also</span></span>

- [<span data-ttu-id="d96b1-128">Exchange POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="d96b1-128">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

