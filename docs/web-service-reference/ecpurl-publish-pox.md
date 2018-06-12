---
title: EcpUrl 发布 (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a51189db-f6e5-428d-833d-65a209204a5b
description: EcpUrl 发布元素指定可以结合使用 EcpUrl (POX) 元素的值生成一个 URL，可用于访问日历发布已启用邮件的用户设置的部分 URL。
ms.openlocfilehash: 82f55be3ce529f6e57db5ffe18bbdea609b13595
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754011"
---
# <a name="ecpurl-publish-pox"></a><span data-ttu-id="6a461-103">EcpUrl 发布 (POX)</span><span class="sxs-lookup"><span data-stu-id="6a461-103">EcpUrl-publish (POX)</span></span>

<span data-ttu-id="6a461-104">**EcpUrl 发布**元素指定可以结合使用[EcpUrl (POX)](ecpurl-pox.md)元素的值生成一个 URL，可用于访问日历发布已启用邮件的用户设置的部分 URL。</span><span class="sxs-lookup"><span data-stu-id="6a461-104">The **EcpUrl-publish** element specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access calendar publishing settings for a mail-enabled user.</span></span> 
  
[<span data-ttu-id="6a461-105">自动发现 (POX)</span><span class="sxs-lookup"><span data-stu-id="6a461-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="6a461-106">响应 (POX)</span><span class="sxs-lookup"><span data-stu-id="6a461-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="6a461-107">帐户 (POX)</span><span class="sxs-lookup"><span data-stu-id="6a461-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="6a461-108">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="6a461-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="6a461-109">EcpUrl 发布 (POX)</span><span class="sxs-lookup"><span data-stu-id="6a461-109">EcpUrl-publish (POX)</span></span>](ecpurl-publish-pox.md)
  
```XML
<EcpUrl-publish/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="6a461-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6a461-110">Attributes and elements</span></span>

<span data-ttu-id="6a461-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6a461-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6a461-112">属性</span><span class="sxs-lookup"><span data-stu-id="6a461-112">Attributes</span></span>

<span data-ttu-id="6a461-113">无。</span><span class="sxs-lookup"><span data-stu-id="6a461-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6a461-114">子元素</span><span class="sxs-lookup"><span data-stu-id="6a461-114">Child elements</span></span>

<span data-ttu-id="6a461-115">无。</span><span class="sxs-lookup"><span data-stu-id="6a461-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6a461-116">父元素</span><span class="sxs-lookup"><span data-stu-id="6a461-116">Parent elements</span></span>

|<span data-ttu-id="6a461-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="6a461-117">**Element**</span></span>|<span data-ttu-id="6a461-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="6a461-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6a461-119">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="6a461-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="6a461-120">包含客户端连接到运行 Microsoft Exchange Server 已安装了客户端访问服务器角色的计算机的规格。</span><span class="sxs-lookup"><span data-stu-id="6a461-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6a461-121">文本值</span><span class="sxs-lookup"><span data-stu-id="6a461-121">Text value</span></span>

<span data-ttu-id="6a461-122">文本值表示可以结合使用[EcpUrl (POX)](ecpurl-pox.md)元素的值生成一个 URL，可用于访问用户的日历发布设置的部分 URL。</span><span class="sxs-lookup"><span data-stu-id="6a461-122">The text value represents a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access calendar publishing settings for the user.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6a461-123">备注</span><span class="sxs-lookup"><span data-stu-id="6a461-123">Remarks</span></span>

<span data-ttu-id="6a461-124">**EcpUrl 发布**元素是**协议**元素的可选子元素。</span><span class="sxs-lookup"><span data-stu-id="6a461-124">The **EcpUrl-publish** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6a461-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6a461-125">See also</span></span>



[<span data-ttu-id="6a461-126">Exchange POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="6a461-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

