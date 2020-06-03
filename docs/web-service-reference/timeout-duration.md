---
title: 超时（持续时间）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bb15f9a7-8ea5-4765-9877-762c3f98bf50
description: Timeout 元素指定服务器在请求订阅超时之前的时间长度。
ms.openlocfilehash: b5b0e77d794080cd8e0da1e14acf4cb059b80b08
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460279"
---
# <a name="timeout-duration"></a><span data-ttu-id="60846-103">超时（持续时间）</span><span class="sxs-lookup"><span data-stu-id="60846-103">Timeout (duration)</span></span>

<span data-ttu-id="60846-104">**Timeout**元素指定服务器在请求订阅超时之前的时间长度。</span><span class="sxs-lookup"><span data-stu-id="60846-104">The **Timeout** element specifies the length of time before a pull subscription is timed out by the server.</span></span> 
  
```XML
<Timeout></Timeout>
```

 <span data-ttu-id="60846-105">**SubscriptionTimeoutType**</span><span class="sxs-lookup"><span data-stu-id="60846-105">**SubscriptionTimeoutType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="60846-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="60846-106">Attributes and elements</span></span>

<span data-ttu-id="60846-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="60846-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="60846-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="60846-108">Attributes</span></span>

<span data-ttu-id="60846-109">无。</span><span class="sxs-lookup"><span data-stu-id="60846-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="60846-110">子元素</span><span class="sxs-lookup"><span data-stu-id="60846-110">Child elements</span></span>

<span data-ttu-id="60846-111">无。</span><span class="sxs-lookup"><span data-stu-id="60846-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="60846-112">父元素</span><span class="sxs-lookup"><span data-stu-id="60846-112">Parent elements</span></span>

[<span data-ttu-id="60846-113">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="60846-113">PullSubscriptionRequest</span></span>](pullsubscriptionrequest.md)
  
## <a name="text-value"></a><span data-ttu-id="60846-114">文本值</span><span class="sxs-lookup"><span data-stu-id="60846-114">Text value</span></span>

<span data-ttu-id="60846-115">**Timeout**元素的文本值是服务器在请求订阅超时前的时间长度（以分钟为单位）。</span><span class="sxs-lookup"><span data-stu-id="60846-115">The text value of the **Timeout** element is the length of time, in minutes, before a pull subscription is timed out by the server.</span></span> <span data-ttu-id="60846-116">最小值为 1;最大值为1440。</span><span class="sxs-lookup"><span data-stu-id="60846-116">The minimum value is 1; the maximum value is 1440.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="60846-117">备注</span><span class="sxs-lookup"><span data-stu-id="60846-117">Remarks</span></span>

<span data-ttu-id="60846-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="60846-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="60846-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="60846-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="60846-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="60846-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="60846-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="60846-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="60846-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="60846-122">Schema name</span></span>  <br/> |<span data-ttu-id="60846-123">类型架构</span><span class="sxs-lookup"><span data-stu-id="60846-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="60846-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="60846-124">Validation file</span></span>  <br/> |<span data-ttu-id="60846-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="60846-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="60846-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="60846-126">Can be empty</span></span>  <br/> ||
   

