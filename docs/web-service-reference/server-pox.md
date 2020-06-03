---
title: 服务器（POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 0ce51644-7f3a-408c-a398-814439b658dc
description: Server 元素指定邮件服务器的名称。
ms.openlocfilehash: 6b29b153bc75b8836bfa113e126d122d620c2984
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462008"
---
# <a name="server-pox"></a><span data-ttu-id="1c512-103">服务器（POX）</span><span class="sxs-lookup"><span data-stu-id="1c512-103">Server (POX)</span></span>

<span data-ttu-id="1c512-104">**Server**元素指定邮件服务器的名称。</span><span class="sxs-lookup"><span data-stu-id="1c512-104">The **Server** element specifies the name of the mail server.</span></span> 
  
[<span data-ttu-id="1c512-105">自动发现（POX）</span><span class="sxs-lookup"><span data-stu-id="1c512-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="1c512-106">响应（POX）</span><span class="sxs-lookup"><span data-stu-id="1c512-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="1c512-107">帐户（POX）</span><span class="sxs-lookup"><span data-stu-id="1c512-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="1c512-108">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="1c512-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="1c512-109">服务器（POX）</span><span class="sxs-lookup"><span data-stu-id="1c512-109">Server (POX)</span></span>](server-pox.md)
  
```xml
<Server/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="1c512-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1c512-110">Attributes and elements</span></span>

<span data-ttu-id="1c512-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1c512-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1c512-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="1c512-112">Attributes</span></span>

<span data-ttu-id="1c512-113">无。</span><span class="sxs-lookup"><span data-stu-id="1c512-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1c512-114">子元素</span><span class="sxs-lookup"><span data-stu-id="1c512-114">Child elements</span></span>

<span data-ttu-id="1c512-115">无。</span><span class="sxs-lookup"><span data-stu-id="1c512-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1c512-116">父元素</span><span class="sxs-lookup"><span data-stu-id="1c512-116">Parent elements</span></span>

|<span data-ttu-id="1c512-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="1c512-117">**Element**</span></span>|<span data-ttu-id="1c512-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="1c512-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1c512-119">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="1c512-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="1c512-120">包含用于将客户端连接到运行 Microsoft Exchange Server 2007 且安装了客户端访问服务器角色的计算机的规范。</span><span class="sxs-lookup"><span data-stu-id="1c512-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1c512-121">文本值</span><span class="sxs-lookup"><span data-stu-id="1c512-121">Text value</span></span>

<span data-ttu-id="1c512-122">该文本值标识服务器。</span><span class="sxs-lookup"><span data-stu-id="1c512-122">The text value identifies the server.</span></span> <span data-ttu-id="1c512-123">对于 POP3、SMTP、IMAP 或 NNTP 等协议，此值将为主机名或 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="1c512-123">For protocols such as POP3, SMTP, IMAP, or NNTP, this value will be either a host name or an IP address.</span></span> <span data-ttu-id="1c512-124">对于 DAV 或 WEB 等协议，这将是一个 URL。</span><span class="sxs-lookup"><span data-stu-id="1c512-124">For protocols such as DAV or WEB, this will be a URL.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1c512-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1c512-125">See also</span></span>



[<span data-ttu-id="1c512-126">Exchange 的 POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="1c512-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

