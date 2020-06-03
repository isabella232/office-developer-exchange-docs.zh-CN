---
title: EcpUrl-aggr （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e7879e3-9b8f-4f23-8291-bacec0e479c0
description: EcpUrl-aggr 元素指定可与 EcpUrl （POX）元素的值组合在一起的部分 URL，以生成可用于访问启用邮件的用户的电子邮件聚合设置的 URL。
ms.openlocfilehash: 26e855900154fb965eae9ba90a373b88e85c2ad3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457282"
---
# <a name="ecpurl-aggr-pox"></a><span data-ttu-id="e2b73-103">EcpUrl-aggr （POX）</span><span class="sxs-lookup"><span data-stu-id="e2b73-103">EcpUrl-aggr (POX)</span></span>

<span data-ttu-id="e2b73-104">**EcpUrl-aggr**元素指定可与[EcpUrl （POX）](ecpurl-pox.md)元素的值组合在一起的部分 url，以生成可用于访问启用邮件的用户的电子邮件聚合设置的 url。</span><span class="sxs-lookup"><span data-stu-id="e2b73-104">The **EcpUrl-aggr** element specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access email aggregation settings for a mail-enabled user.</span></span> 
  
[<span data-ttu-id="e2b73-105">自动发现（POX）</span><span class="sxs-lookup"><span data-stu-id="e2b73-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="e2b73-106">响应（POX）</span><span class="sxs-lookup"><span data-stu-id="e2b73-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="e2b73-107">帐户（POX）</span><span class="sxs-lookup"><span data-stu-id="e2b73-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="e2b73-108">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="e2b73-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="e2b73-109">EcpUrl-aggr （POX）</span><span class="sxs-lookup"><span data-stu-id="e2b73-109">EcpUrl-aggr (POX)</span></span>](ecpurl-aggr-pox.md)
  
```XML
<EcpUrl-aggr/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="e2b73-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e2b73-110">Attributes and elements</span></span>

<span data-ttu-id="e2b73-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e2b73-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e2b73-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="e2b73-112">Attributes</span></span>

<span data-ttu-id="e2b73-113">无。</span><span class="sxs-lookup"><span data-stu-id="e2b73-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e2b73-114">子元素</span><span class="sxs-lookup"><span data-stu-id="e2b73-114">Child elements</span></span>

<span data-ttu-id="e2b73-115">无。</span><span class="sxs-lookup"><span data-stu-id="e2b73-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e2b73-116">父元素</span><span class="sxs-lookup"><span data-stu-id="e2b73-116">Parent elements</span></span>

|<span data-ttu-id="e2b73-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="e2b73-117">**Element**</span></span>|<span data-ttu-id="e2b73-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="e2b73-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e2b73-119">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="e2b73-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="e2b73-120">包含将客户端连接到运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的规范。</span><span class="sxs-lookup"><span data-stu-id="e2b73-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e2b73-121">文本值</span><span class="sxs-lookup"><span data-stu-id="e2b73-121">Text value</span></span>

<span data-ttu-id="e2b73-122">Text 值表示一个可与[EcpUrl （POX）](ecpurl-pox.md)元素的值结合使用的部分 url，以生成可用于访问用户的电子邮件聚合设置的 URL。</span><span class="sxs-lookup"><span data-stu-id="e2b73-122">The text value represents a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access email aggregation settings for the user.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e2b73-123">备注</span><span class="sxs-lookup"><span data-stu-id="e2b73-123">Remarks</span></span>

<span data-ttu-id="e2b73-124">**EcpUrl-aggr**元素是**Protocol**元素的可选子元素。</span><span class="sxs-lookup"><span data-stu-id="e2b73-124">The **EcpUrl-aggr** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e2b73-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e2b73-125">See also</span></span>



[<span data-ttu-id="e2b73-126">Exchange 的 POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="e2b73-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

