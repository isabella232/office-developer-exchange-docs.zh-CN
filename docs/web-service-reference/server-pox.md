---
title: 服务器 (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 0ce51644-7f3a-408c-a398-814439b658dc
description: 服务器元素指定的邮件服务器的名称。
ms.openlocfilehash: fafd6684d0857bd8b7e1bac0aae0ed162a6a938a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827369"
---
# <a name="server-pox"></a><span data-ttu-id="6875c-103">服务器 (POX)</span><span class="sxs-lookup"><span data-stu-id="6875c-103">Server (POX)</span></span>

<span data-ttu-id="6875c-104">**服务器**元素指定的邮件服务器的名称。</span><span class="sxs-lookup"><span data-stu-id="6875c-104">The **Server** element specifies the name of the mail server.</span></span> 
  
[<span data-ttu-id="6875c-105">自动发现 (POX)</span><span class="sxs-lookup"><span data-stu-id="6875c-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="6875c-106">响应 (POX)</span><span class="sxs-lookup"><span data-stu-id="6875c-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="6875c-107">帐户 (POX)</span><span class="sxs-lookup"><span data-stu-id="6875c-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="6875c-108">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="6875c-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="6875c-109">服务器 (POX)</span><span class="sxs-lookup"><span data-stu-id="6875c-109">Server (POX)</span></span>](server-pox.md)
  
```xml
<Server/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="6875c-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6875c-110">Attributes and elements</span></span>

<span data-ttu-id="6875c-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6875c-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6875c-112">属性</span><span class="sxs-lookup"><span data-stu-id="6875c-112">Attributes</span></span>

<span data-ttu-id="6875c-113">无。</span><span class="sxs-lookup"><span data-stu-id="6875c-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6875c-114">子元素</span><span class="sxs-lookup"><span data-stu-id="6875c-114">Child elements</span></span>

<span data-ttu-id="6875c-115">无。</span><span class="sxs-lookup"><span data-stu-id="6875c-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6875c-116">父元素</span><span class="sxs-lookup"><span data-stu-id="6875c-116">Parent elements</span></span>

|<span data-ttu-id="6875c-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="6875c-117">**Element**</span></span>|<span data-ttu-id="6875c-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="6875c-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6875c-119">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="6875c-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="6875c-120">包含客户端连接到运行 Microsoft Exchange Server 2007 的安装了客户端访问服务器角色的计算机的规格。</span><span class="sxs-lookup"><span data-stu-id="6875c-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6875c-121">文本值</span><span class="sxs-lookup"><span data-stu-id="6875c-121">Text value</span></span>

<span data-ttu-id="6875c-122">文本值标识该服务器。</span><span class="sxs-lookup"><span data-stu-id="6875c-122">The text value identifies the server.</span></span> <span data-ttu-id="6875c-123">对于协议，如 POP3、 SMTP、 IMAP 或 NNTP，此值将为主机名称或 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="6875c-123">For protocols such as POP3, SMTP, IMAP, or NNTP, this value will be either a host name or an IP address.</span></span> <span data-ttu-id="6875c-124">对于如 DAV 或 WEB 协议，这将是一个 URL。</span><span class="sxs-lookup"><span data-stu-id="6875c-124">For protocols such as DAV or WEB, this will be a URL.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6875c-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6875c-125">See also</span></span>



[<span data-ttu-id="6875c-126">Exchange POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="6875c-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

