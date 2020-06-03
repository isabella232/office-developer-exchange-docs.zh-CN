---
title: EcpUrl-photo （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4a37bbfb-c763-4a3c-93ea-14c2e7355dbc
description: EcpUrl 元素指定一个部分 URL，该 URL 可以与 EcpUrl （POX）元素的值相结合，以生成可用于查看或更改启用邮件的用户的当前照片的 URL。
ms.openlocfilehash: 2be930e8d9e4c2bbdb26eff49a429569fc0a1d5d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461280"
---
# <a name="ecpurl-photo-pox"></a><span data-ttu-id="cb47c-103">EcpUrl-photo （POX）</span><span class="sxs-lookup"><span data-stu-id="cb47c-103">EcpUrl-photo (POX)</span></span>

<span data-ttu-id="cb47c-104">**EcpUrl**元素指定一个部分 url，该 url 可以与[EcpUrl （POX）](ecpurl-pox.md)元素的值相结合，以生成可用于查看或更改启用邮件的用户的当前照片的 URL。</span><span class="sxs-lookup"><span data-stu-id="cb47c-104">The **EcpUrl-photo** element specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to view or change a mail-enabled user's current photo.</span></span> 
  
[<span data-ttu-id="cb47c-105">自动发现（POX）</span><span class="sxs-lookup"><span data-stu-id="cb47c-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="cb47c-106">响应（POX）</span><span class="sxs-lookup"><span data-stu-id="cb47c-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="cb47c-107">帐户（POX）</span><span class="sxs-lookup"><span data-stu-id="cb47c-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="cb47c-108">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="cb47c-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="cb47c-109">EcpUrl-photo （POX）</span><span class="sxs-lookup"><span data-stu-id="cb47c-109">EcpUrl-photo (POX)</span></span>](ecpurl-photo-pox.md)
  
```XML
<EcpUrl-photo/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="cb47c-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="cb47c-110">Attributes and elements</span></span>

<span data-ttu-id="cb47c-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="cb47c-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cb47c-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="cb47c-112">Attributes</span></span>

<span data-ttu-id="cb47c-113">无。</span><span class="sxs-lookup"><span data-stu-id="cb47c-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cb47c-114">子元素</span><span class="sxs-lookup"><span data-stu-id="cb47c-114">Child elements</span></span>

<span data-ttu-id="cb47c-115">无。</span><span class="sxs-lookup"><span data-stu-id="cb47c-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cb47c-116">父元素</span><span class="sxs-lookup"><span data-stu-id="cb47c-116">Parent elements</span></span>

|<span data-ttu-id="cb47c-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="cb47c-117">**Element**</span></span>|<span data-ttu-id="cb47c-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="cb47c-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cb47c-119">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="cb47c-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="cb47c-120">包含将客户端连接到运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的规范。</span><span class="sxs-lookup"><span data-stu-id="cb47c-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cb47c-121">文本值</span><span class="sxs-lookup"><span data-stu-id="cb47c-121">Text value</span></span>

<span data-ttu-id="cb47c-122">Text 值表示一个可与[EcpUrl （POX）](ecpurl-pox.md)元素的值结合使用的部分 url，以生成可用于查看或更改用户的当前照片的 URL。</span><span class="sxs-lookup"><span data-stu-id="cb47c-122">The text value represents a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to view or change the user's current photo.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="cb47c-123">备注</span><span class="sxs-lookup"><span data-stu-id="cb47c-123">Remarks</span></span>

<span data-ttu-id="cb47c-124">**EcpUrl**元素是**Protocol**元素的可选子元素。</span><span class="sxs-lookup"><span data-stu-id="cb47c-124">The **EcpUrl-photo** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cb47c-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cb47c-125">See also</span></span>



[<span data-ttu-id="cb47c-126">Exchange 的 POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="cb47c-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

