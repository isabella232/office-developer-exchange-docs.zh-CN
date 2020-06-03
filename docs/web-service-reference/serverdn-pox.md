---
title: ServerDN （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 2ef73d13-e8bb-43f6-96c7-3ee157fed739
description: ServerDN 元素指定运行 Microsoft Exchange Server 2007 的计算机的可分辨名称。
ms.openlocfilehash: 16c6e7368e221b7e54c8d7d63532bb29464a7e54
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461994"
---
# <a name="serverdn-pox"></a><span data-ttu-id="fc14e-103">ServerDN （POX）</span><span class="sxs-lookup"><span data-stu-id="fc14e-103">ServerDN (POX)</span></span>

<span data-ttu-id="fc14e-104">**ServerDN**元素指定运行 Microsoft Exchange Server 2007 的计算机的可分辨名称。</span><span class="sxs-lookup"><span data-stu-id="fc14e-104">The **ServerDN** element specifies the distinguished name of the computer that is running Microsoft Exchange Server 2007.</span></span> 
  
[<span data-ttu-id="fc14e-105">自动发现（POX）</span><span class="sxs-lookup"><span data-stu-id="fc14e-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="fc14e-106">响应（POX）</span><span class="sxs-lookup"><span data-stu-id="fc14e-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="fc14e-107">帐户（POX）</span><span class="sxs-lookup"><span data-stu-id="fc14e-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="fc14e-108">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="fc14e-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="fc14e-109">ServerDN （POX）</span><span class="sxs-lookup"><span data-stu-id="fc14e-109">ServerDN (POX)</span></span>](serverdn-pox.md)
  
```xml
<ServerDN/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="fc14e-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fc14e-110">Attributes and elements</span></span>

<span data-ttu-id="fc14e-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fc14e-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fc14e-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="fc14e-112">Attributes</span></span>

<span data-ttu-id="fc14e-113">无。</span><span class="sxs-lookup"><span data-stu-id="fc14e-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fc14e-114">子元素</span><span class="sxs-lookup"><span data-stu-id="fc14e-114">Child elements</span></span>

<span data-ttu-id="fc14e-115">无。</span><span class="sxs-lookup"><span data-stu-id="fc14e-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fc14e-116">父元素</span><span class="sxs-lookup"><span data-stu-id="fc14e-116">Parent elements</span></span>

|<span data-ttu-id="fc14e-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="fc14e-117">**Element**</span></span>|<span data-ttu-id="fc14e-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="fc14e-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fc14e-119">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="fc14e-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="fc14e-120">包含用于将客户端连接到运行 Microsoft Exchange Server 2007 且安装了客户端访问服务器角色的计算机的规范。</span><span class="sxs-lookup"><span data-stu-id="fc14e-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fc14e-121">文本值</span><span class="sxs-lookup"><span data-stu-id="fc14e-121">Text value</span></span>

<span data-ttu-id="fc14e-122">该文本值表示的是 Exchange 服务器的可分辨名称。</span><span class="sxs-lookup"><span data-stu-id="fc14e-122">The text value represents the distinguished name of the Exchange server.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fc14e-123">备注</span><span class="sxs-lookup"><span data-stu-id="fc14e-123">Remarks</span></span>

<span data-ttu-id="fc14e-124">仅当[Type （POX）](type-pox.md)等于 EXCH 时，才使用**ServerDN**值。</span><span class="sxs-lookup"><span data-stu-id="fc14e-124">The **ServerDN** value is only used when [Type (POX)](type-pox.md) is equal to EXCH.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fc14e-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fc14e-125">See also</span></span>



[<span data-ttu-id="fc14e-126">Exchange 的 POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="fc14e-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

