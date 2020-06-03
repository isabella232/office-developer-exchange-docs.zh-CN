---
title: 错误（POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 91c63b62-ab68-4c32-a2f7-5a87c188335b
description: Error 元素包含自动发现错误响应。
ms.openlocfilehash: 1a1a3e83898674e605921cb75371036a8a561a95
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530647"
---
# <a name="error-pox"></a><span data-ttu-id="ce188-103">错误（POX）</span><span class="sxs-lookup"><span data-stu-id="ce188-103">Error (POX)</span></span>

<span data-ttu-id="ce188-104">**Error**元素包含自动发现错误响应。</span><span class="sxs-lookup"><span data-stu-id="ce188-104">The **Error** element contains an Autodiscover error response.</span></span> 
  
[<span data-ttu-id="ce188-105">自动发现（POX）</span><span class="sxs-lookup"><span data-stu-id="ce188-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="ce188-106">响应（POX）</span><span class="sxs-lookup"><span data-stu-id="ce188-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="ce188-107">帐户（POX）</span><span class="sxs-lookup"><span data-stu-id="ce188-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="ce188-108">错误（POX）</span><span class="sxs-lookup"><span data-stu-id="ce188-108">Error (POX)</span></span>](error-pox.md)
  
```xml
<Error Time="" Id="">
   <ErrorCode/>
   <Message/>
   <DebugData/>
</Error>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="ce188-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ce188-109">Attributes and elements</span></span>

<span data-ttu-id="ce188-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ce188-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ce188-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="ce188-111">Attributes</span></span>

|<span data-ttu-id="ce188-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="ce188-112">**Attribute**</span></span>|<span data-ttu-id="ce188-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="ce188-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ce188-114">Time</span><span class="sxs-lookup"><span data-stu-id="ce188-114">Time</span></span>  <br/> |<span data-ttu-id="ce188-115">表示返回错误响应的时间。</span><span class="sxs-lookup"><span data-stu-id="ce188-115">Represents the time when the error response was returned.</span></span>  <br/> |
|<span data-ttu-id="ce188-116">Id</span><span class="sxs-lookup"><span data-stu-id="ce188-116">Id</span></span>  <br/> |<span data-ttu-id="ce188-117">表示运行 Microsoft Exchange Server 2007 且安装了客户端访问服务器角色的计算机的名称的哈希值。</span><span class="sxs-lookup"><span data-stu-id="ce188-117">Represents a hash of the name of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ce188-118">子元素</span><span class="sxs-lookup"><span data-stu-id="ce188-118">Child elements</span></span>

|<span data-ttu-id="ce188-119">**元素**</span><span class="sxs-lookup"><span data-stu-id="ce188-119">**Element**</span></span>|<span data-ttu-id="ce188-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="ce188-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ce188-121">ErrorCode （POX）</span><span class="sxs-lookup"><span data-stu-id="ce188-121">ErrorCode (POX)</span></span>](errorcode-pox.md) <br/> |<span data-ttu-id="ce188-122">包含错误发现响应的错误代码。</span><span class="sxs-lookup"><span data-stu-id="ce188-122">Contains the error code for an error Autodiscover response.</span></span>  <br/> |
|[<span data-ttu-id="ce188-123">Message （POX）</span><span class="sxs-lookup"><span data-stu-id="ce188-123">Message (POX)</span></span>](message-pox.md) <br/> |<span data-ttu-id="ce188-124">包含错误发现响应的错误消息。</span><span class="sxs-lookup"><span data-stu-id="ce188-124">Contains the error message for an error Autodiscover response.</span></span>  <br/> |
|[<span data-ttu-id="ce188-125">DebugData （POX）</span><span class="sxs-lookup"><span data-stu-id="ce188-125">DebugData (POX)</span></span>](debugdata-pox.md) <br/> |<span data-ttu-id="ce188-126">包含错误发现响应的调试数据。</span><span class="sxs-lookup"><span data-stu-id="ce188-126">Contains the debug data for an error Autodiscover response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ce188-127">父元素</span><span class="sxs-lookup"><span data-stu-id="ce188-127">Parent elements</span></span>

|<span data-ttu-id="ce188-128">**元素**</span><span class="sxs-lookup"><span data-stu-id="ce188-128">**Element**</span></span>|<span data-ttu-id="ce188-129">**说明**</span><span class="sxs-lookup"><span data-stu-id="ce188-129">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ce188-130">帐户（POX）</span><span class="sxs-lookup"><span data-stu-id="ce188-130">Account (POX)</span></span>](account-pox.md) <br/> |<span data-ttu-id="ce188-131">包含自动发现错误响应。</span><span class="sxs-lookup"><span data-stu-id="ce188-131">Contains an Autodiscover error response.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ce188-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ce188-132">See also</span></span>



[<span data-ttu-id="ce188-133">Exchange 的 POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="ce188-133">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

