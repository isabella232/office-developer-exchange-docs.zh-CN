---
title: EcpUrl-ret （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5f090fd2-b0c4-4ca0-a959-1433d73a2069
description: EcpUrl 元素指定一个部分 URL，该 URL 可以与 EcpUrl （POX）元素的值相结合，以生成可用于访问启用邮件的用户的保留标记设置的 URL。
ms.openlocfilehash: 1f6878dc58bb01fca6a56fdd645efd3363a3d442
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458689"
---
# <a name="ecpurl-ret-pox"></a><span data-ttu-id="c6ded-103">EcpUrl-ret （POX）</span><span class="sxs-lookup"><span data-stu-id="c6ded-103">EcpUrl-ret (POX)</span></span>

<span data-ttu-id="c6ded-104">**EcpUrl**元素指定一个部分 url，该 url 可以与[EcpUrl （POX）](ecpurl-pox.md)元素的值相结合，以生成可用于访问启用邮件的用户的保留标记设置的 url。</span><span class="sxs-lookup"><span data-stu-id="c6ded-104">The **EcpUrl-ret** element specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access retention tag settings for a mail-enabled user.</span></span> 
  
[<span data-ttu-id="c6ded-105">自动发现（POX）</span><span class="sxs-lookup"><span data-stu-id="c6ded-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="c6ded-106">响应（POX）</span><span class="sxs-lookup"><span data-stu-id="c6ded-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="c6ded-107">帐户（POX）</span><span class="sxs-lookup"><span data-stu-id="c6ded-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="c6ded-108">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="c6ded-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="c6ded-109">EcpUrl-ret （POX）</span><span class="sxs-lookup"><span data-stu-id="c6ded-109">EcpUrl-ret (POX)</span></span>](ecpurl-ret-pox.md)
  
```XML
<EcpUrl-ret/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="c6ded-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c6ded-110">Attributes and elements</span></span>

<span data-ttu-id="c6ded-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c6ded-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c6ded-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="c6ded-112">Attributes</span></span>

<span data-ttu-id="c6ded-113">无。</span><span class="sxs-lookup"><span data-stu-id="c6ded-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c6ded-114">子元素</span><span class="sxs-lookup"><span data-stu-id="c6ded-114">Child elements</span></span>

<span data-ttu-id="c6ded-115">无。</span><span class="sxs-lookup"><span data-stu-id="c6ded-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c6ded-116">父元素</span><span class="sxs-lookup"><span data-stu-id="c6ded-116">Parent elements</span></span>

|<span data-ttu-id="c6ded-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="c6ded-117">**Element**</span></span>|<span data-ttu-id="c6ded-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="c6ded-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c6ded-119">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="c6ded-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="c6ded-120">包含将客户端连接到运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的规范。</span><span class="sxs-lookup"><span data-stu-id="c6ded-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c6ded-121">文本值</span><span class="sxs-lookup"><span data-stu-id="c6ded-121">Text value</span></span>

<span data-ttu-id="c6ded-122">Text 值表示一个可与[EcpUrl （POX）](ecpurl-pox.md)元素的值结合使用的部分 url，以生成可用于访问用户的保留标记设置的 URL。</span><span class="sxs-lookup"><span data-stu-id="c6ded-122">The text value represents a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access retention tag settings for the user.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c6ded-123">备注</span><span class="sxs-lookup"><span data-stu-id="c6ded-123">Remarks</span></span>

<span data-ttu-id="c6ded-124">**EcpUrl-ret**元素是**Protocol**元素的可选子元素。</span><span class="sxs-lookup"><span data-stu-id="c6ded-124">The **EcpUrl-ret** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c6ded-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c6ded-125">See also</span></span>



[<span data-ttu-id="c6ded-126">Exchange 的 POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="c6ded-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

