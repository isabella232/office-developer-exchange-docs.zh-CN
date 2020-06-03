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
description: Timeout 元素表示订阅可以保持空闲状态的持续时间（以分钟为单位），而无需客户端的 GetEvents 请求。
ms.openlocfilehash: 6f3228cd480bf0eaf259c4f321bc74d0845b9bba
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459894"
---
# <a name="timeout"></a><span data-ttu-id="c6bf4-103">Timeout</span><span class="sxs-lookup"><span data-stu-id="c6bf4-103">Timeout</span></span>

<span data-ttu-id="c6bf4-104">**Timeout**元素表示订阅可以保持空闲状态的持续时间（以分钟为单位），而无需客户端的 GetEvents 请求。</span><span class="sxs-lookup"><span data-stu-id="c6bf4-104">The **Timeout** element represents the duration, in minutes, that the subscription can remain idle without a GetEvents request from the client.</span></span> 
  
```xml
<Timeout/>
```

 <span data-ttu-id="c6bf4-105">**int**</span><span class="sxs-lookup"><span data-stu-id="c6bf4-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c6bf4-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c6bf4-106">Attributes and elements</span></span>

<span data-ttu-id="c6bf4-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c6bf4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c6bf4-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="c6bf4-108">Attributes</span></span>

<span data-ttu-id="c6bf4-109">无。</span><span class="sxs-lookup"><span data-stu-id="c6bf4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c6bf4-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c6bf4-110">Child elements</span></span>

<span data-ttu-id="c6bf4-111">无。</span><span class="sxs-lookup"><span data-stu-id="c6bf4-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c6bf4-112">父元素</span><span class="sxs-lookup"><span data-stu-id="c6bf4-112">Parent elements</span></span>

|<span data-ttu-id="c6bf4-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="c6bf4-113">**Element**</span></span>|<span data-ttu-id="c6bf4-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="c6bf4-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c6bf4-115">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="c6bf4-115">PullSubscriptionRequest</span></span>](pullsubscriptionrequest.md) <br/> |<span data-ttu-id="c6bf4-116">表示对基于请求的事件通知订阅的订阅。</span><span class="sxs-lookup"><span data-stu-id="c6bf4-116">Represents a subscription to a pull-based event notification subscription.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c6bf4-117">文本值</span><span class="sxs-lookup"><span data-stu-id="c6bf4-117">Text value</span></span>

<span data-ttu-id="c6bf4-118">如果使用此元素，则需要一个表示整数的文本值。</span><span class="sxs-lookup"><span data-stu-id="c6bf4-118">A text value that represents an integer is required if this element is used.</span></span> <span data-ttu-id="c6bf4-119">此元素的可能值为1到1440（包含这两个值）。</span><span class="sxs-lookup"><span data-stu-id="c6bf4-119">The possible values for this element are 1 to 1440, inclusive.</span></span> <span data-ttu-id="c6bf4-120">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="c6bf4-120">This element is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c6bf4-121">备注</span><span class="sxs-lookup"><span data-stu-id="c6bf4-121">Remarks</span></span>

<span data-ttu-id="c6bf4-122">订阅的超时计时器由成功的 GetEvents 请求重置。</span><span class="sxs-lookup"><span data-stu-id="c6bf4-122">The timeout timer for the subscription is reset by a successful GetEvents request.</span></span>
  
<span data-ttu-id="c6bf4-123">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c6bf4-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="c6bf4-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="c6bf4-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c6bf4-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="c6bf4-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c6bf4-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="c6bf4-126">Schema name</span></span>  <br/> |<span data-ttu-id="c6bf4-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="c6bf4-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="c6bf4-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="c6bf4-128">Validation file</span></span>  <br/> |<span data-ttu-id="c6bf4-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c6bf4-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c6bf4-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="c6bf4-130">Can be empty</span></span>  <br/> |<span data-ttu-id="c6bf4-131">False</span><span class="sxs-lookup"><span data-stu-id="c6bf4-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c6bf4-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c6bf4-132">See also</span></span>



[<span data-ttu-id="c6bf4-133">订阅操作</span><span class="sxs-lookup"><span data-stu-id="c6bf4-133">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="c6bf4-134">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="c6bf4-134">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="c6bf4-135">取消订阅操作</span><span class="sxs-lookup"><span data-stu-id="c6bf4-135">Unsubscribe operation</span></span>](unsubscribe-operation.md)

