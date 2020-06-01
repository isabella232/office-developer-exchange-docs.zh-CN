---
title: TTL （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 178eefa1-995c-4bea-930b-e51293961191
description: TTL 元素指定设置保持有效的生存时间（以小时为单位）。
ms.openlocfilehash: 9a17cbe4e669d1afe9f3ef4a24f2a9a2889a7d52
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467380"
---
# <a name="ttl-pox"></a><span data-ttu-id="6e97a-103">TTL （POX）</span><span class="sxs-lookup"><span data-stu-id="6e97a-103">TTL (POX)</span></span>

<span data-ttu-id="6e97a-104">**TTL**元素指定设置保持有效的生存时间（以小时为单位）。</span><span class="sxs-lookup"><span data-stu-id="6e97a-104">The **TTL** element specifies the Time to Live, in hours, during which the settings remain valid.</span></span> 
  
[<span data-ttu-id="6e97a-105">自动发现（POX）</span><span class="sxs-lookup"><span data-stu-id="6e97a-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="6e97a-106">响应（POX）</span><span class="sxs-lookup"><span data-stu-id="6e97a-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="6e97a-107">帐户（POX）</span><span class="sxs-lookup"><span data-stu-id="6e97a-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="6e97a-108">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="6e97a-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="6e97a-109">TTL （POX）</span><span class="sxs-lookup"><span data-stu-id="6e97a-109">TTL (POX)</span></span>](ttl-pox.md)
  
```xml
<TTL/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="6e97a-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6e97a-110">Attributes and elements</span></span>

<span data-ttu-id="6e97a-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6e97a-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6e97a-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="6e97a-112">Attributes</span></span>

<span data-ttu-id="6e97a-113">无。</span><span class="sxs-lookup"><span data-stu-id="6e97a-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6e97a-114">子元素</span><span class="sxs-lookup"><span data-stu-id="6e97a-114">Child elements</span></span>

<span data-ttu-id="6e97a-115">无。</span><span class="sxs-lookup"><span data-stu-id="6e97a-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6e97a-116">父元素</span><span class="sxs-lookup"><span data-stu-id="6e97a-116">Parent elements</span></span>

|<span data-ttu-id="6e97a-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="6e97a-117">**Element**</span></span>|<span data-ttu-id="6e97a-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="6e97a-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6e97a-119">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="6e97a-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="6e97a-120">包含用于将客户端连接到安装了客户端访问服务器角色的 Exchange Server 2007 计算机的规范。</span><span class="sxs-lookup"><span data-stu-id="6e97a-120">Contains the specifications for connecting a client to the Exchange Server 2007 computer on which the Client Access server role is installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6e97a-121">文本值</span><span class="sxs-lookup"><span data-stu-id="6e97a-121">Text value</span></span>

<span data-ttu-id="6e97a-122">Text 值表示设置保持有效的生存时间（以小时为单位）。</span><span class="sxs-lookup"><span data-stu-id="6e97a-122">The text value represents the Time to Live, in hours, during which the settings remain valid.</span></span> <span data-ttu-id="6e97a-123">0值表示不需要重新发现。</span><span class="sxs-lookup"><span data-stu-id="6e97a-123">A value of zero indicates that rediscovery is not required.</span></span> <span data-ttu-id="6e97a-124">如果未指定任何值，则此元素的默认值为1小时。</span><span class="sxs-lookup"><span data-stu-id="6e97a-124">If no value is specified, the default value for this element is 1 hour.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6e97a-125">备注</span><span class="sxs-lookup"><span data-stu-id="6e97a-125">Remarks</span></span>

<span data-ttu-id="6e97a-126">**TTL**元素所表示的时间过后，应使用自动发现请求 rediscovered 这些设置。</span><span class="sxs-lookup"><span data-stu-id="6e97a-126">After the time that is represented by the **TTL** element has elapsed, the settings should be rediscovered by using an Autodiscover request.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6e97a-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6e97a-127">See also</span></span>



[<span data-ttu-id="6e97a-128">Exchange 的 POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="6e97a-128">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

