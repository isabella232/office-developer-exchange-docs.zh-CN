---
title: EcpUrl tm (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f35d5ac-55be-4d3a-ad03-7d6e9349d923
description: EcpUrl tm 元素指定可以结合使用 EcpUrl (POX) 元素的值生成一个可用于访问其中的所有站点邮箱的已启用邮件的用户是当前成员的列表的 URL 的部分 URL。
ms.openlocfilehash: 786459cab98f8c169f768b6ef850792e8111761a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754013"
---
# <a name="ecpurl-tm-pox"></a><span data-ttu-id="26524-103">EcpUrl tm (POX)</span><span class="sxs-lookup"><span data-stu-id="26524-103">EcpUrl-tm (POX)</span></span>

<span data-ttu-id="26524-104">**EcpUrl tm**元素指定可以结合使用[EcpUrl (POX)](ecpurl-pox.md)元素的值生成一个可用于访问其中的所有站点邮箱的已启用邮件的用户是当前成员的列表的 URL 的部分 URL。</span><span class="sxs-lookup"><span data-stu-id="26524-104">The **EcpUrl-tm** element specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access a list of all site mailboxes of which a mail-enabled user is currently a member.</span></span> 
  
[<span data-ttu-id="26524-105">自动发现 (POX)</span><span class="sxs-lookup"><span data-stu-id="26524-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="26524-106">响应 (POX)</span><span class="sxs-lookup"><span data-stu-id="26524-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="26524-107">帐户 (POX)</span><span class="sxs-lookup"><span data-stu-id="26524-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="26524-108">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="26524-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="26524-109">EcpUrl tm (POX)</span><span class="sxs-lookup"><span data-stu-id="26524-109">EcpUrl-tm (POX)</span></span>](ecpurl-tm-pox.md)
  
```XML
<EcpUrl-tm/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="26524-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="26524-110">Attributes and elements</span></span>

<span data-ttu-id="26524-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="26524-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="26524-112">属性</span><span class="sxs-lookup"><span data-stu-id="26524-112">Attributes</span></span>

<span data-ttu-id="26524-113">无。</span><span class="sxs-lookup"><span data-stu-id="26524-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="26524-114">子元素</span><span class="sxs-lookup"><span data-stu-id="26524-114">Child elements</span></span>

<span data-ttu-id="26524-115">无。</span><span class="sxs-lookup"><span data-stu-id="26524-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="26524-116">父元素</span><span class="sxs-lookup"><span data-stu-id="26524-116">Parent elements</span></span>

|<span data-ttu-id="26524-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="26524-117">**Element**</span></span>|<span data-ttu-id="26524-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="26524-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="26524-119">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="26524-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="26524-120">包含客户端连接到运行 Microsoft Exchange Server 已安装了客户端访问服务器角色的计算机的规格。</span><span class="sxs-lookup"><span data-stu-id="26524-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="26524-121">文本值</span><span class="sxs-lookup"><span data-stu-id="26524-121">Text value</span></span>

<span data-ttu-id="26524-122">文本值表示可以结合使用[EcpUrl (POX)](ecpurl-pox.md)元素的值生成一个可用于访问用户的站点邮箱的列表的 URL 的部分 URL。</span><span class="sxs-lookup"><span data-stu-id="26524-122">The text value represents a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access a list of site mailboxes for the user.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="26524-123">注解</span><span class="sxs-lookup"><span data-stu-id="26524-123">Remarks</span></span>

<span data-ttu-id="26524-124">**EcpUrl tm**元素是**协议**元素的可选子元素。</span><span class="sxs-lookup"><span data-stu-id="26524-124">The **EcpUrl-tm** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="26524-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="26524-125">See also</span></span>



[<span data-ttu-id="26524-126">Exchange POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="26524-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

