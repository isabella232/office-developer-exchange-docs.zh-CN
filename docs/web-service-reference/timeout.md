---
title: Timeout
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Timeout
api_type:
- schema
ms.assetid: c2e1ca5a-6667-4f6f-aac4-89de33bddc54
description: 超时元素均表示的工期，以分钟为单位订阅可以持续为空闲状态 GetEvents 请求从客户端。
ms.openlocfilehash: 0a26002689e131959f09318b01d97ffb73b605f9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838234"
---
# <a name="timeout"></a><span data-ttu-id="21460-103">Timeout</span><span class="sxs-lookup"><span data-stu-id="21460-103">Timeout</span></span>

<span data-ttu-id="21460-104">**超时**元素均表示的工期，以分钟为单位订阅可以持续为空闲状态 GetEvents 请求从客户端。</span><span class="sxs-lookup"><span data-stu-id="21460-104">The **Timeout** element represents the duration, in minutes, that the subscription can remain idle without a GetEvents request from the client.</span></span> 
  
```xml
<Timeout/>
```

 <span data-ttu-id="21460-105">**int**</span><span class="sxs-lookup"><span data-stu-id="21460-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="21460-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="21460-106">Attributes and elements</span></span>

<span data-ttu-id="21460-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="21460-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="21460-108">属性</span><span class="sxs-lookup"><span data-stu-id="21460-108">Attributes</span></span>

<span data-ttu-id="21460-109">无。</span><span class="sxs-lookup"><span data-stu-id="21460-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="21460-110">子元素</span><span class="sxs-lookup"><span data-stu-id="21460-110">Child elements</span></span>

<span data-ttu-id="21460-111">无。</span><span class="sxs-lookup"><span data-stu-id="21460-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="21460-112">父元素</span><span class="sxs-lookup"><span data-stu-id="21460-112">Parent elements</span></span>

|<span data-ttu-id="21460-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="21460-113">**Element**</span></span>|<span data-ttu-id="21460-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="21460-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="21460-115">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="21460-115">PullSubscriptionRequest</span></span>](pullsubscriptionrequest.md) <br/> |<span data-ttu-id="21460-116">代表对基于请求的事件通知订阅的订阅。</span><span class="sxs-lookup"><span data-stu-id="21460-116">Represents a subscription to a pull-based event notification subscription.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="21460-117">文本值</span><span class="sxs-lookup"><span data-stu-id="21460-117">Text value</span></span>

<span data-ttu-id="21460-118">如果使用此元素，则需要表示一个整数的文本值。</span><span class="sxs-lookup"><span data-stu-id="21460-118">A text value that represents an integer is required if this element is used.</span></span> <span data-ttu-id="21460-119">此元素的可能值是 1 到 1440 之间，非独占。</span><span class="sxs-lookup"><span data-stu-id="21460-119">The possible values for this element are 1 to 1440, inclusive.</span></span> <span data-ttu-id="21460-120">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="21460-120">This element is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="21460-121">注解</span><span class="sxs-lookup"><span data-stu-id="21460-121">Remarks</span></span>

<span data-ttu-id="21460-122">成功的 GetEvents 请求重置订阅超时计时器。</span><span class="sxs-lookup"><span data-stu-id="21460-122">The timeout timer for the subscription is reset by a successful GetEvents request.</span></span>
  
<span data-ttu-id="21460-123">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="21460-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="21460-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="21460-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="21460-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="21460-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="21460-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="21460-126">Schema name</span></span>  <br/> |<span data-ttu-id="21460-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="21460-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="21460-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="21460-128">Validation file</span></span>  <br/> |<span data-ttu-id="21460-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="21460-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="21460-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="21460-130">Can be empty</span></span>  <br/> |<span data-ttu-id="21460-131">False</span><span class="sxs-lookup"><span data-stu-id="21460-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="21460-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="21460-132">See also</span></span>



[<span data-ttu-id="21460-133">订阅操作</span><span class="sxs-lookup"><span data-stu-id="21460-133">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="21460-134">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="21460-134">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="21460-135">取消操作</span><span class="sxs-lookup"><span data-stu-id="21460-135">Unsubscribe operation</span></span>](unsubscribe-operation.md)

