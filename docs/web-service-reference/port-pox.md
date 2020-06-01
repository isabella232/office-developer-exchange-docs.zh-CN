---
title: 端口（POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 4046821a-d6f3-4764-82be-4011221ce7a3
description: Port 元素指定用于连接到存储区的端口。
ms.openlocfilehash: 2da59e03a57b44fb12d14368d1b585ba845eacfe
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464012"
---
# <a name="port-pox"></a><span data-ttu-id="95293-103">端口（POX）</span><span class="sxs-lookup"><span data-stu-id="95293-103">Port (POX)</span></span>

<span data-ttu-id="95293-104">**Port**元素指定用于连接到存储区的端口。</span><span class="sxs-lookup"><span data-stu-id="95293-104">The **Port** element specifies the port that is used to connect to the store.</span></span> 
  
[<span data-ttu-id="95293-105">自动发现（POX）</span><span class="sxs-lookup"><span data-stu-id="95293-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="95293-106">响应（POX）</span><span class="sxs-lookup"><span data-stu-id="95293-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="95293-107">帐户（POX）</span><span class="sxs-lookup"><span data-stu-id="95293-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="95293-108">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="95293-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="95293-109">端口（POX）</span><span class="sxs-lookup"><span data-stu-id="95293-109">Port (POX)</span></span>](port-pox.md)
  
```xml
<Port/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="95293-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="95293-110">Attributes and elements</span></span>

<span data-ttu-id="95293-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="95293-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="95293-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="95293-112">Attributes</span></span>

<span data-ttu-id="95293-113">无。</span><span class="sxs-lookup"><span data-stu-id="95293-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="95293-114">子元素</span><span class="sxs-lookup"><span data-stu-id="95293-114">Child elements</span></span>

<span data-ttu-id="95293-115">无。</span><span class="sxs-lookup"><span data-stu-id="95293-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="95293-116">父元素</span><span class="sxs-lookup"><span data-stu-id="95293-116">Parent elements</span></span>

|<span data-ttu-id="95293-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="95293-117">**Element**</span></span>|<span data-ttu-id="95293-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="95293-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="95293-119">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="95293-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="95293-120">包含用于将客户端连接到运行 Microsoft Exchange Server 2007 且安装了客户端访问服务器角色的计算机的规范。</span><span class="sxs-lookup"><span data-stu-id="95293-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="95293-121">文本值</span><span class="sxs-lookup"><span data-stu-id="95293-121">Text value</span></span>

<span data-ttu-id="95293-122">该文本值表示用于访问 Exchange 服务器的端口。</span><span class="sxs-lookup"><span data-stu-id="95293-122">The text value represents the port that is used to access the Exchange server.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="95293-123">备注</span><span class="sxs-lookup"><span data-stu-id="95293-123">Remarks</span></span>

<span data-ttu-id="95293-124">如果[Server （POX）](server-pox.md)元素包含 URL，则不使用该**端口**值。</span><span class="sxs-lookup"><span data-stu-id="95293-124">The **Port** value is not used if the [Server (POX)](server-pox.md) element contains a URL.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="95293-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="95293-125">See also</span></span>



[<span data-ttu-id="95293-126">Exchange 的 POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="95293-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

