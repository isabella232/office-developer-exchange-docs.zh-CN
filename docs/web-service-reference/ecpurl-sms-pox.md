---
title: EcpUrl sms (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5e5e589-ee16-42a8-9cd4-ae3909fc869b
description: EcpUrl sms 元素指定可以结合使用 EcpUrl (POX) 元素的值生成一个 URL，可用于访问已启用邮件的用户的短信服务 (SMS) 设置的部分 URL。
ms.openlocfilehash: 38471db7b7e046e43425b132b1716033c1c96afd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754010"
---
# <a name="ecpurl-sms-pox"></a><span data-ttu-id="34bbd-103">EcpUrl sms (POX)</span><span class="sxs-lookup"><span data-stu-id="34bbd-103">EcpUrl-sms (POX)</span></span>

<span data-ttu-id="34bbd-104">**EcpUrl sms**元素指定可以结合使用[EcpUrl (POX)](ecpurl-pox.md)元素的值生成一个 URL，可用于访问已启用邮件的用户的短信服务 (SMS) 设置的部分 URL。</span><span class="sxs-lookup"><span data-stu-id="34bbd-104">The **EcpUrl-sms** element specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access Short Message Service (SMS) settings for a mail-enabled user.</span></span> 
  
[<span data-ttu-id="34bbd-105">自动发现 (POX)</span><span class="sxs-lookup"><span data-stu-id="34bbd-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="34bbd-106">响应 (POX)</span><span class="sxs-lookup"><span data-stu-id="34bbd-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="34bbd-107">帐户 (POX)</span><span class="sxs-lookup"><span data-stu-id="34bbd-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="34bbd-108">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="34bbd-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="34bbd-109">EcpUrl sms (POX)</span><span class="sxs-lookup"><span data-stu-id="34bbd-109">EcpUrl-sms (POX)</span></span>](ecpurl-sms-pox.md)
  
```XML
<EcpUrl-sms/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="34bbd-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="34bbd-110">Attributes and elements</span></span>

<span data-ttu-id="34bbd-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="34bbd-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="34bbd-112">属性</span><span class="sxs-lookup"><span data-stu-id="34bbd-112">Attributes</span></span>

<span data-ttu-id="34bbd-113">无。</span><span class="sxs-lookup"><span data-stu-id="34bbd-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="34bbd-114">子元素</span><span class="sxs-lookup"><span data-stu-id="34bbd-114">Child elements</span></span>

<span data-ttu-id="34bbd-115">无。</span><span class="sxs-lookup"><span data-stu-id="34bbd-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="34bbd-116">父元素</span><span class="sxs-lookup"><span data-stu-id="34bbd-116">Parent elements</span></span>

|<span data-ttu-id="34bbd-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="34bbd-117">**Element**</span></span>|<span data-ttu-id="34bbd-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="34bbd-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="34bbd-119">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="34bbd-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="34bbd-120">包含客户端连接到运行 Microsoft Exchange Server 已安装了客户端访问服务器角色的计算机的规格。</span><span class="sxs-lookup"><span data-stu-id="34bbd-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="34bbd-121">文本值</span><span class="sxs-lookup"><span data-stu-id="34bbd-121">Text value</span></span>

<span data-ttu-id="34bbd-122">文本值表示可以结合使用[EcpUrl (POX)](ecpurl-pox.md)元素的值生成一个 URL，可用于访问用户的短信设置的部分 URL。</span><span class="sxs-lookup"><span data-stu-id="34bbd-122">The text value represents a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access SMS settings for the user.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="34bbd-123">注解</span><span class="sxs-lookup"><span data-stu-id="34bbd-123">Remarks</span></span>

<span data-ttu-id="34bbd-124">**EcpUrl sms**元素是**协议**元素的可选子元素。</span><span class="sxs-lookup"><span data-stu-id="34bbd-124">The **EcpUrl-sms** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="34bbd-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="34bbd-125">See also</span></span>



[<span data-ttu-id="34bbd-126">Exchange POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="34bbd-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

