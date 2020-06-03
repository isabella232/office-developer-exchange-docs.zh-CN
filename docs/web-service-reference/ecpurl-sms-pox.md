---
title: EcpUrl-sms （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5e5e589-ee16-42a8-9cd4-ae3909fc869b
description: EcpUrl 元素指定一个部分 URL，该 URL 可以与 EcpUrl （POX）元素的值相结合，以生成可用于为启用邮件的用户访问短信服务（SMS）设置的 URL。
ms.openlocfilehash: 24f475e7f2d54fa565cc90796a983c0bd842e4da
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458682"
---
# <a name="ecpurl-sms-pox"></a><span data-ttu-id="d2831-103">EcpUrl-sms （POX）</span><span class="sxs-lookup"><span data-stu-id="d2831-103">EcpUrl-sms (POX)</span></span>

<span data-ttu-id="d2831-104">**EcpUrl**元素指定一个部分 url，该 url 可以与[EcpUrl （POX）](ecpurl-pox.md)元素的值相结合，以生成可用于为启用邮件的用户访问短信服务（SMS）设置的 url。</span><span class="sxs-lookup"><span data-stu-id="d2831-104">The **EcpUrl-sms** element specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access Short Message Service (SMS) settings for a mail-enabled user.</span></span> 
  
[<span data-ttu-id="d2831-105">自动发现（POX）</span><span class="sxs-lookup"><span data-stu-id="d2831-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="d2831-106">响应（POX）</span><span class="sxs-lookup"><span data-stu-id="d2831-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="d2831-107">帐户（POX）</span><span class="sxs-lookup"><span data-stu-id="d2831-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="d2831-108">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="d2831-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="d2831-109">EcpUrl-sms （POX）</span><span class="sxs-lookup"><span data-stu-id="d2831-109">EcpUrl-sms (POX)</span></span>](ecpurl-sms-pox.md)
  
```XML
<EcpUrl-sms/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="d2831-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d2831-110">Attributes and elements</span></span>

<span data-ttu-id="d2831-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d2831-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d2831-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="d2831-112">Attributes</span></span>

<span data-ttu-id="d2831-113">无。</span><span class="sxs-lookup"><span data-stu-id="d2831-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d2831-114">子元素</span><span class="sxs-lookup"><span data-stu-id="d2831-114">Child elements</span></span>

<span data-ttu-id="d2831-115">无。</span><span class="sxs-lookup"><span data-stu-id="d2831-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d2831-116">父元素</span><span class="sxs-lookup"><span data-stu-id="d2831-116">Parent elements</span></span>

|<span data-ttu-id="d2831-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="d2831-117">**Element**</span></span>|<span data-ttu-id="d2831-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="d2831-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d2831-119">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="d2831-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="d2831-120">包含将客户端连接到运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的规范。</span><span class="sxs-lookup"><span data-stu-id="d2831-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d2831-121">文本值</span><span class="sxs-lookup"><span data-stu-id="d2831-121">Text value</span></span>

<span data-ttu-id="d2831-122">Text 值表示一个可与[EcpUrl （POX）](ecpurl-pox.md)元素的值结合使用的部分 url，以生成可用于访问用户的 SMS 设置的 URL。</span><span class="sxs-lookup"><span data-stu-id="d2831-122">The text value represents a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access SMS settings for the user.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d2831-123">备注</span><span class="sxs-lookup"><span data-stu-id="d2831-123">Remarks</span></span>

<span data-ttu-id="d2831-124">**EcpUrl**元素是**Protocol**元素的可选子元素。</span><span class="sxs-lookup"><span data-stu-id="d2831-124">The **EcpUrl-sms** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d2831-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d2831-125">See also</span></span>



[<span data-ttu-id="d2831-126">Exchange 的 POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="d2831-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

