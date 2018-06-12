---
title: 错误 (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 91c63b62-ab68-4c32-a2f7-5a87c188335b
description: Error 元素包含自动发现错误响应。
ms.openlocfilehash: 3135a352365fe3000ce2d202ad78452d5c8ccc7f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754144"
---
# <a name="error-pox"></a><span data-ttu-id="0d7e2-103">错误 (POX)</span><span class="sxs-lookup"><span data-stu-id="0d7e2-103">Error (POX)</span></span>

<span data-ttu-id="0d7e2-104">**Error**元素包含自动发现错误响应。</span><span class="sxs-lookup"><span data-stu-id="0d7e2-104">The **Error** element contains an Autodiscover error response.</span></span> 
  
[<span data-ttu-id="0d7e2-105">自动发现 (POX)</span><span class="sxs-lookup"><span data-stu-id="0d7e2-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="0d7e2-106">响应 (POX)</span><span class="sxs-lookup"><span data-stu-id="0d7e2-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="0d7e2-107">帐户 (POX)</span><span class="sxs-lookup"><span data-stu-id="0d7e2-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="0d7e2-108">错误 (POX)</span><span class="sxs-lookup"><span data-stu-id="0d7e2-108">Error (POX)</span></span>](error-pox.md)
  
```xml
<Error Time="" Id="">
   <ErrorCode/>
   <Message/>
   <DebugData/>
</Error>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="0d7e2-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0d7e2-109">Attributes and elements</span></span>

<span data-ttu-id="0d7e2-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0d7e2-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0d7e2-111">属性</span><span class="sxs-lookup"><span data-stu-id="0d7e2-111">Attributes</span></span>

|<span data-ttu-id="0d7e2-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="0d7e2-112">**Attribute**</span></span>|<span data-ttu-id="0d7e2-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="0d7e2-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0d7e2-114">时间</span><span class="sxs-lookup"><span data-stu-id="0d7e2-114">Time</span></span>  <br/> |<span data-ttu-id="0d7e2-115">表示时返回的错误响应时间。</span><span class="sxs-lookup"><span data-stu-id="0d7e2-115">Represents the time when the error response was returned.</span></span>  <br/> |
|<span data-ttu-id="0d7e2-116">Id</span><span class="sxs-lookup"><span data-stu-id="0d7e2-116">Id</span></span>  <br/> |<span data-ttu-id="0d7e2-117">代表为运行 Microsoft Exchange Server 2007 的安装了客户端访问服务器角色的计算机的名称的哈希值。</span><span class="sxs-lookup"><span data-stu-id="0d7e2-117">Represents a hash of the name of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0d7e2-118">子元素</span><span class="sxs-lookup"><span data-stu-id="0d7e2-118">Child elements</span></span>

|<span data-ttu-id="0d7e2-119">**元素**</span><span class="sxs-lookup"><span data-stu-id="0d7e2-119">**Element**</span></span>|<span data-ttu-id="0d7e2-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="0d7e2-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0d7e2-121">ErrorCode (POX)</span><span class="sxs-lookup"><span data-stu-id="0d7e2-121">ErrorCode (POX)</span></span>](errorcode-pox.md) <br/> |<span data-ttu-id="0d7e2-122">包含自动发现响应的错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="0d7e2-122">Contains the error code for an error Autodiscover response.</span></span>  <br/> |
|[<span data-ttu-id="0d7e2-123">消息 (POX)</span><span class="sxs-lookup"><span data-stu-id="0d7e2-123">Message (POX)</span></span>](message-pox.md) <br/> |<span data-ttu-id="0d7e2-124">包含错误自动发现响应的错误消息。</span><span class="sxs-lookup"><span data-stu-id="0d7e2-124">Contains the error message for an error Autodiscover response.</span></span>  <br/> |
|[<span data-ttu-id="0d7e2-125">DebugData (POX)</span><span class="sxs-lookup"><span data-stu-id="0d7e2-125">DebugData (POX)</span></span>](debugdata-pox.md) <br/> |<span data-ttu-id="0d7e2-126">包含错误自动发现响应的调试数据。</span><span class="sxs-lookup"><span data-stu-id="0d7e2-126">Contains the debug data for an error Autodiscover response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0d7e2-127">父元素</span><span class="sxs-lookup"><span data-stu-id="0d7e2-127">Parent elements</span></span>

|<span data-ttu-id="0d7e2-128">**元素**</span><span class="sxs-lookup"><span data-stu-id="0d7e2-128">**Element**</span></span>|<span data-ttu-id="0d7e2-129">**说明**</span><span class="sxs-lookup"><span data-stu-id="0d7e2-129">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0d7e2-130">帐户 (POX)</span><span class="sxs-lookup"><span data-stu-id="0d7e2-130">Account (POX)</span></span>](account-pox.md) <br/> |<span data-ttu-id="0d7e2-131">包含自动发现错误响应。</span><span class="sxs-lookup"><span data-stu-id="0d7e2-131">Contains an Autodiscover error response.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0d7e2-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0d7e2-132">See also</span></span>



[<span data-ttu-id="0d7e2-133">Exchange POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="0d7e2-133">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

