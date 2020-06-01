---
title: DomainName （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 2b4af2b2-58b5-4f28-9cb3-c07a11377747
description: DomainName 元素指定用户的域。
ms.openlocfilehash: ff38d6a876e396317dedece0a81a9f9f0db0f587
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458423"
---
# <a name="domainname-pox"></a><span data-ttu-id="d34df-103">DomainName （POX）</span><span class="sxs-lookup"><span data-stu-id="d34df-103">DomainName (POX)</span></span>

<span data-ttu-id="d34df-104">**DomainName**元素指定用户的域。</span><span class="sxs-lookup"><span data-stu-id="d34df-104">The **DomainName** element specifies the user's domain.</span></span> 
  
- [<span data-ttu-id="d34df-105">自动发现（POX）</span><span class="sxs-lookup"><span data-stu-id="d34df-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)  
- [<span data-ttu-id="d34df-106">响应（POX）</span><span class="sxs-lookup"><span data-stu-id="d34df-106">Response (POX)</span></span>](response-pox.md)  
- [<span data-ttu-id="d34df-107">帐户（POX）</span><span class="sxs-lookup"><span data-stu-id="d34df-107">Account (POX)</span></span>](account-pox.md) 
- [<span data-ttu-id="d34df-108">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="d34df-108">Protocol (POX)</span></span>](protocol-pox.md) 
- [<span data-ttu-id="d34df-109">DomainName （POX）</span><span class="sxs-lookup"><span data-stu-id="d34df-109">DomainName (POX)</span></span>](domainname-pox.md)
  
```xml
<DomainName/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="d34df-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d34df-110">Attributes and elements</span></span>

<span data-ttu-id="d34df-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d34df-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d34df-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="d34df-112">Attributes</span></span>

<span data-ttu-id="d34df-113">无。</span><span class="sxs-lookup"><span data-stu-id="d34df-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d34df-114">子元素</span><span class="sxs-lookup"><span data-stu-id="d34df-114">Child elements</span></span>

<span data-ttu-id="d34df-115">无。</span><span class="sxs-lookup"><span data-stu-id="d34df-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d34df-116">父元素</span><span class="sxs-lookup"><span data-stu-id="d34df-116">Parent elements</span></span>

|<span data-ttu-id="d34df-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="d34df-117">**Element**</span></span>|<span data-ttu-id="d34df-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="d34df-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d34df-119">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="d34df-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="d34df-120">包含用于将客户端连接到运行 Microsoft Exchange Server 2007 且安装了客户端访问服务器角色的计算机的规范。</span><span class="sxs-lookup"><span data-stu-id="d34df-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d34df-121">文本值</span><span class="sxs-lookup"><span data-stu-id="d34df-121">Text value</span></span>

<span data-ttu-id="d34df-122">该文本值指定用户的域。</span><span class="sxs-lookup"><span data-stu-id="d34df-122">The text value specifies the user's domain.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d34df-123">备注</span><span class="sxs-lookup"><span data-stu-id="d34df-123">Remarks</span></span>

<span data-ttu-id="d34df-124">如果未指定任何值，则默认身份验证是将电子邮件地址用作用户主体名称（UPN）格式。</span><span class="sxs-lookup"><span data-stu-id="d34df-124">If no value is specified, the default authentication is to use the e-mail address as a user principal name (UPN) format.</span></span> <span data-ttu-id="d34df-125">例如： \<Username\> @ \<Domain\> 。</span><span class="sxs-lookup"><span data-stu-id="d34df-125">For example: \<Username\>@\<Domain\>.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d34df-126">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d34df-126">See also</span></span>

- [<span data-ttu-id="d34df-127">Exchange 的 POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="d34df-127">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

