---
title: MoreEvents
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MoreEvents
api_type:
- schema
ms.assetid: 76a7ea58-a44f-49b8-baba-d21302d742ad
description: MoreEvents 元素指示队列传送到客户端中是否有多个事件。
ms.openlocfilehash: cc3f7ed3b4b5f5ce27a9d45d508506bfa62e5086
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826489"
---
# <a name="moreevents"></a><span data-ttu-id="45431-103">MoreEvents</span><span class="sxs-lookup"><span data-stu-id="45431-103">MoreEvents</span></span>

<span data-ttu-id="45431-104">**MoreEvents**元素指示队列传送到客户端中是否有多个事件。</span><span class="sxs-lookup"><span data-stu-id="45431-104">The **MoreEvents** element indicates whether there are more events in the queue to be delivered to the client.</span></span> 
  
```xml
<MoreEvents/>
```

 <span data-ttu-id="45431-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="45431-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="45431-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="45431-106">Attributes and elements</span></span>

<span data-ttu-id="45431-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="45431-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="45431-108">属性</span><span class="sxs-lookup"><span data-stu-id="45431-108">Attributes</span></span>

<span data-ttu-id="45431-109">无。</span><span class="sxs-lookup"><span data-stu-id="45431-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="45431-110">子元素</span><span class="sxs-lookup"><span data-stu-id="45431-110">Child elements</span></span>

<span data-ttu-id="45431-111">无。</span><span class="sxs-lookup"><span data-stu-id="45431-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="45431-112">父元素</span><span class="sxs-lookup"><span data-stu-id="45431-112">Parent elements</span></span>

|<span data-ttu-id="45431-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="45431-113">**Element**</span></span>|<span data-ttu-id="45431-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="45431-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="45431-115">通知</span><span class="sxs-lookup"><span data-stu-id="45431-115">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="45431-116">包含有关订阅和自上次通知以来发生的事件的信息。</span><span class="sxs-lookup"><span data-stu-id="45431-116">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="45431-117">文本值</span><span class="sxs-lookup"><span data-stu-id="45431-117">Text value</span></span>

<span data-ttu-id="45431-118">文本值表示的布尔值。</span><span class="sxs-lookup"><span data-stu-id="45431-118">The text value represents a Boolean value.</span></span> <span data-ttu-id="45431-119">值为**true**指示多个事件队列中。</span><span class="sxs-lookup"><span data-stu-id="45431-119">A value of **true** indicates that more events are in the queue.</span></span> <span data-ttu-id="45431-120">如果值为**false**指示的多个事件不会在队列中。</span><span class="sxs-lookup"><span data-stu-id="45431-120">A value of **false** indicates that no more events are in the queue.</span></span> <span data-ttu-id="45431-121">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="45431-121">This property is read-only.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="45431-122">备注</span><span class="sxs-lookup"><span data-stu-id="45431-122">Remarks</span></span>

<span data-ttu-id="45431-123">对于出现通知，此元素中的一个**true**值指示客户端应发出另一个 GetEvents 请求以获取剩余的事件。</span><span class="sxs-lookup"><span data-stu-id="45431-123">In the case of Pull notifications, a **true** value in this element indicates to the client that another GetEvents request should be issued to get the remaining events.</span></span> <span data-ttu-id="45431-124">假定客户端规范需要事件通知的最小的延迟，GetEvents 请求应继续连续连续，直到**false** **MoreEvents**值返回。</span><span class="sxs-lookup"><span data-stu-id="45431-124">Assuming that the client specifications require minimum latency for event notifications, GetEvents requests should continue in a continuous succession until a **false** **MoreEvents** value is returned.</span></span> 
  
<span data-ttu-id="45431-125">对于推送通知**MoreEvents** **true**值指示客户端，另一个通知请求将发送到客户端提供剩余的事件。</span><span class="sxs-lookup"><span data-stu-id="45431-125">In the case of Push notifications, a **true** value for **MoreEvents** indicates to the client that another notification request will be sent to the client to deliver the remaining events.</span></span> <span data-ttu-id="45431-126">类似于出现通知，这些后续请求将继续连续连续直到客户端访问服务器上的事件队列为空。</span><span class="sxs-lookup"><span data-stu-id="45431-126">Similar to Pull notifications, these follow-up requests will continue in continuous succession until the event queue on the Client Access server is empty.</span></span> 
  
<span data-ttu-id="45431-127">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="45431-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="45431-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="45431-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="45431-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="45431-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="45431-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="45431-130">Schema Name</span></span>  <br/> |<span data-ttu-id="45431-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="45431-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="45431-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="45431-132">Validation File</span></span>  <br/> |<span data-ttu-id="45431-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="45431-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="45431-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="45431-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="45431-135">False</span><span class="sxs-lookup"><span data-stu-id="45431-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="45431-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="45431-136">See also</span></span>



[<span data-ttu-id="45431-137">订阅操作</span><span class="sxs-lookup"><span data-stu-id="45431-137">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="45431-138">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="45431-138">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="45431-139">取消操作</span><span class="sxs-lookup"><span data-stu-id="45431-139">Unsubscribe operation</span></span>](unsubscribe-operation.md)

