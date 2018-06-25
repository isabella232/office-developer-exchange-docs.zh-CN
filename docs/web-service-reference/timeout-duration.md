---
title: 超时 （持续时间）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bb15f9a7-8ea5-4765-9877-762c3f98bf50
description: 超时元素指定服务器超时前请求订阅的时间长度。
ms.openlocfilehash: 23b210dcdd87f2388aecec246068f12ec6c69a78
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838210"
---
# <a name="timeout-duration"></a><span data-ttu-id="29d35-103">超时 （持续时间）</span><span class="sxs-lookup"><span data-stu-id="29d35-103">Timeout (duration)</span></span>

<span data-ttu-id="29d35-104">**超时**元素指定服务器超时前请求订阅的时间长度。</span><span class="sxs-lookup"><span data-stu-id="29d35-104">The **Timeout** element specifies the length of time before a pull subscription is timed out by the server.</span></span> 
  
```XML
<Timeout></Timeout>
```

 <span data-ttu-id="29d35-105">**SubscriptionTimeoutType**</span><span class="sxs-lookup"><span data-stu-id="29d35-105">**SubscriptionTimeoutType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="29d35-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="29d35-106">Attributes and elements</span></span>

<span data-ttu-id="29d35-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="29d35-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="29d35-108">属性</span><span class="sxs-lookup"><span data-stu-id="29d35-108">Attributes</span></span>

<span data-ttu-id="29d35-109">无。</span><span class="sxs-lookup"><span data-stu-id="29d35-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="29d35-110">子元素</span><span class="sxs-lookup"><span data-stu-id="29d35-110">Child elements</span></span>

<span data-ttu-id="29d35-111">无。</span><span class="sxs-lookup"><span data-stu-id="29d35-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="29d35-112">父元素</span><span class="sxs-lookup"><span data-stu-id="29d35-112">Parent elements</span></span>

[<span data-ttu-id="29d35-113">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="29d35-113">PullSubscriptionRequest</span></span>](pullsubscriptionrequest.md)
  
## <a name="text-value"></a><span data-ttu-id="29d35-114">文本值</span><span class="sxs-lookup"><span data-stu-id="29d35-114">Text value</span></span>

<span data-ttu-id="29d35-115">**超时**元素的文本值是时间，以分钟为单位，服务器将请求订阅已超时之前的长度。</span><span class="sxs-lookup"><span data-stu-id="29d35-115">The text value of the **Timeout** element is the length of time, in minutes, before a pull subscription is timed out by the server.</span></span> <span data-ttu-id="29d35-116">最小值为 1;最大值为 1440年。</span><span class="sxs-lookup"><span data-stu-id="29d35-116">The minimum value is 1; the maximum value is 1440.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="29d35-117">备注</span><span class="sxs-lookup"><span data-stu-id="29d35-117">Remarks</span></span>

<span data-ttu-id="29d35-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="29d35-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="29d35-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="29d35-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="29d35-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="29d35-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="29d35-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="29d35-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="29d35-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="29d35-122">Schema name</span></span>  <br/> |<span data-ttu-id="29d35-123">类型架构</span><span class="sxs-lookup"><span data-stu-id="29d35-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="29d35-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="29d35-124">Validation file</span></span>  <br/> |<span data-ttu-id="29d35-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="29d35-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="29d35-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="29d35-126">Can be empty</span></span>  <br/> ||
   

