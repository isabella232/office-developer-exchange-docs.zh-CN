---
title: EcpUrl-um （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 455c77c6-c03f-49a7-a8ca-aa0023b6e73b
description: EcpUrl 元素指定一个部分 URL，该 URL 可以与 EcpUrl （POX）元素的值结合使用，以生成一个 URL，该 url 可用于访问启用邮件的用户的语音邮件设置。
ms.openlocfilehash: 0fa3d42113d7d9accd6bba3d3b065477baf4d484
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463487"
---
# <a name="ecpurl-um-pox"></a><span data-ttu-id="7a39f-103">EcpUrl-um （POX）</span><span class="sxs-lookup"><span data-stu-id="7a39f-103">EcpUrl-um (POX)</span></span>

<span data-ttu-id="7a39f-104">**EcpUrl**元素指定一个部分 url，该 url 可以与[EcpUrl （POX）](ecpurl-pox.md)元素的值结合使用，以生成一个 url，该 url 可用于访问启用邮件的用户的语音邮件设置。</span><span class="sxs-lookup"><span data-stu-id="7a39f-104">The **EcpUrl-um** element specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access voice mail settings for a mail-enabled user.</span></span> 
  
[<span data-ttu-id="7a39f-105">自动发现（POX）</span><span class="sxs-lookup"><span data-stu-id="7a39f-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="7a39f-106">响应（POX）</span><span class="sxs-lookup"><span data-stu-id="7a39f-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="7a39f-107">帐户（POX）</span><span class="sxs-lookup"><span data-stu-id="7a39f-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="7a39f-108">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="7a39f-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="7a39f-109">EcpUrl-um （POX）</span><span class="sxs-lookup"><span data-stu-id="7a39f-109">EcpUrl-um (POX)</span></span>](ecpurl-um-pox.md)
  
```XML
<EcpUrl-um/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="7a39f-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7a39f-110">Attributes and elements</span></span>

<span data-ttu-id="7a39f-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7a39f-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7a39f-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="7a39f-112">Attributes</span></span>

<span data-ttu-id="7a39f-113">无。</span><span class="sxs-lookup"><span data-stu-id="7a39f-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7a39f-114">子元素</span><span class="sxs-lookup"><span data-stu-id="7a39f-114">Child elements</span></span>

<span data-ttu-id="7a39f-115">无。</span><span class="sxs-lookup"><span data-stu-id="7a39f-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7a39f-116">父元素</span><span class="sxs-lookup"><span data-stu-id="7a39f-116">Parent elements</span></span>

|<span data-ttu-id="7a39f-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="7a39f-117">**Element**</span></span>|<span data-ttu-id="7a39f-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="7a39f-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7a39f-119">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="7a39f-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="7a39f-120">包含将客户端连接到运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的规范。</span><span class="sxs-lookup"><span data-stu-id="7a39f-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7a39f-121">文本值</span><span class="sxs-lookup"><span data-stu-id="7a39f-121">Text value</span></span>

<span data-ttu-id="7a39f-122">Text 值表示一个可与[EcpUrl （POX）](ecpurl-pox.md)元素的值结合使用的部分 url，以生成可用于访问用户的语音邮件设置的 URL。</span><span class="sxs-lookup"><span data-stu-id="7a39f-122">The text value represents a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access voice mail settings for the user.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7a39f-123">备注</span><span class="sxs-lookup"><span data-stu-id="7a39f-123">Remarks</span></span>

<span data-ttu-id="7a39f-124">**EcpUrl**元素是**Protocol**元素的可选子元素。</span><span class="sxs-lookup"><span data-stu-id="7a39f-124">The **EcpUrl-um** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7a39f-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7a39f-125">See also</span></span>



[<span data-ttu-id="7a39f-126">Exchange 的 POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="7a39f-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

