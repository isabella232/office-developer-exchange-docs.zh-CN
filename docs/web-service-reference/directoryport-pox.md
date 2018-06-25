---
title: DirectoryPort (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: ab436b54-ceba-4cd9-aeb4-134f9b93986d
description: DirectoryPort 元素指定用于连接到目录时使用的名称服务提供程序界面 (NSPI) 协议的端口。
ms.openlocfilehash: 1b73b9cd1d21c73f4e897684371993312f741322
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753877"
---
# <a name="directoryport-pox"></a><span data-ttu-id="c5dc2-103">DirectoryPort (POX)</span><span class="sxs-lookup"><span data-stu-id="c5dc2-103">DirectoryPort (POX)</span></span>

<span data-ttu-id="c5dc2-104">**DirectoryPort**元素指定用于连接到目录时使用的名称服务提供程序界面 (NSPI) 协议的端口。</span><span class="sxs-lookup"><span data-stu-id="c5dc2-104">The **DirectoryPort** element specifies the port that is used to connect to the directory when the Name Service Provider Interface (NSPI) protocol is used.</span></span> 
  
- [<span data-ttu-id="c5dc2-105">自动发现 (POX)</span><span class="sxs-lookup"><span data-stu-id="c5dc2-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md) 
- [<span data-ttu-id="c5dc2-106">响应 (POX)</span><span class="sxs-lookup"><span data-stu-id="c5dc2-106">Response (POX)</span></span>](response-pox.md)  
- [<span data-ttu-id="c5dc2-107">帐户 (POX)</span><span class="sxs-lookup"><span data-stu-id="c5dc2-107">Account (POX)</span></span>](account-pox.md)  
- [<span data-ttu-id="c5dc2-108">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="c5dc2-108">Protocol (POX)</span></span>](protocol-pox.md)  
- [<span data-ttu-id="c5dc2-109">DirectoryPort (POX)</span><span class="sxs-lookup"><span data-stu-id="c5dc2-109">DirectoryPort (POX)</span></span>](directoryport-pox.md)
  
```xml
<DirectoryPort/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="c5dc2-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c5dc2-110">Attributes and elements</span></span>

<span data-ttu-id="c5dc2-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c5dc2-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c5dc2-112">属性</span><span class="sxs-lookup"><span data-stu-id="c5dc2-112">Attributes</span></span>

<span data-ttu-id="c5dc2-113">无。</span><span class="sxs-lookup"><span data-stu-id="c5dc2-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c5dc2-114">子元素</span><span class="sxs-lookup"><span data-stu-id="c5dc2-114">Child elements</span></span>

<span data-ttu-id="c5dc2-115">无。</span><span class="sxs-lookup"><span data-stu-id="c5dc2-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c5dc2-116">父元素</span><span class="sxs-lookup"><span data-stu-id="c5dc2-116">Parent elements</span></span>

|<span data-ttu-id="c5dc2-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="c5dc2-117">**Element**</span></span>|<span data-ttu-id="c5dc2-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="c5dc2-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c5dc2-119">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="c5dc2-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="c5dc2-120">包含客户端连接到运行 Microsoft Exchange Server 2007 的安装了客户端访问服务器角色的计算机的规格。</span><span class="sxs-lookup"><span data-stu-id="c5dc2-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c5dc2-121">文本值</span><span class="sxs-lookup"><span data-stu-id="c5dc2-121">Text value</span></span>

<span data-ttu-id="c5dc2-122">文本值表示用于访问 Exchange 服务器的端口。</span><span class="sxs-lookup"><span data-stu-id="c5dc2-122">The text value represents the port that is used to access the Exchange server.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c5dc2-123">注解</span><span class="sxs-lookup"><span data-stu-id="c5dc2-123">Remarks</span></span>

<span data-ttu-id="c5dc2-124">[类型 (POX)](type-pox.md)元素等于 EXCH 或 EXPR 时才使用**DirectoryPort**元素。</span><span class="sxs-lookup"><span data-stu-id="c5dc2-124">The **DirectoryPort** element is only used when the [Type (POX)](type-pox.md) element equals EXCH or EXPR.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c5dc2-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c5dc2-125">See also</span></span>

- [<span data-ttu-id="c5dc2-126">Exchange POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="c5dc2-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

