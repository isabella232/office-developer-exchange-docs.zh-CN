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
description: MoreEvents 元素指示队列中是否存在要传递到客户端的更多事件。
ms.openlocfilehash: fd12dd2e2e64ce1711e553ba5eb29bd0eb64c892
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462729"
---
# <a name="moreevents"></a><span data-ttu-id="69df9-103">MoreEvents</span><span class="sxs-lookup"><span data-stu-id="69df9-103">MoreEvents</span></span>

<span data-ttu-id="69df9-104">**MoreEvents**元素指示队列中是否存在要传递到客户端的更多事件。</span><span class="sxs-lookup"><span data-stu-id="69df9-104">The **MoreEvents** element indicates whether there are more events in the queue to be delivered to the client.</span></span> 
  
```xml
<MoreEvents/>
```

 <span data-ttu-id="69df9-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="69df9-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="69df9-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="69df9-106">Attributes and elements</span></span>

<span data-ttu-id="69df9-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="69df9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="69df9-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="69df9-108">Attributes</span></span>

<span data-ttu-id="69df9-109">无。</span><span class="sxs-lookup"><span data-stu-id="69df9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="69df9-110">子元素</span><span class="sxs-lookup"><span data-stu-id="69df9-110">Child elements</span></span>

<span data-ttu-id="69df9-111">无。</span><span class="sxs-lookup"><span data-stu-id="69df9-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="69df9-112">父元素</span><span class="sxs-lookup"><span data-stu-id="69df9-112">Parent elements</span></span>

|<span data-ttu-id="69df9-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="69df9-113">**Element**</span></span>|<span data-ttu-id="69df9-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="69df9-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="69df9-115">通知</span><span class="sxs-lookup"><span data-stu-id="69df9-115">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="69df9-116">包含有关订阅以及上次通知之后发生的事件的信息。</span><span class="sxs-lookup"><span data-stu-id="69df9-116">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="69df9-117">文本值</span><span class="sxs-lookup"><span data-stu-id="69df9-117">Text value</span></span>

<span data-ttu-id="69df9-118">该文本值表示一个布尔值。</span><span class="sxs-lookup"><span data-stu-id="69df9-118">The text value represents a Boolean value.</span></span> <span data-ttu-id="69df9-119">**如果值为 true，则**表示队列中有更多事件。</span><span class="sxs-lookup"><span data-stu-id="69df9-119">A value of **true** indicates that more events are in the queue.</span></span> <span data-ttu-id="69df9-120">**如果值为 false** ，则表示队列中没有其他事件。</span><span class="sxs-lookup"><span data-stu-id="69df9-120">A value of **false** indicates that no more events are in the queue.</span></span> <span data-ttu-id="69df9-121">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="69df9-121">This property is read-only.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="69df9-122">备注</span><span class="sxs-lookup"><span data-stu-id="69df9-122">Remarks</span></span>

<span data-ttu-id="69df9-123">在请求通知的情况下，此元素中的**true**值指示客户端应发出另一个 GetEvents 请求，以获取剩余事件。</span><span class="sxs-lookup"><span data-stu-id="69df9-123">In the case of Pull notifications, a **true** value in this element indicates to the client that another GetEvents request should be issued to get the remaining events.</span></span> <span data-ttu-id="69df9-124">假定客户端规范要求的事件通知的最低延迟，则 GetEvents 请求应持续持续连续，直到返回**false** **MoreEvents**值。</span><span class="sxs-lookup"><span data-stu-id="69df9-124">Assuming that the client specifications require minimum latency for event notifications, GetEvents requests should continue in a continuous succession until a **false** **MoreEvents** value is returned.</span></span> 
  
<span data-ttu-id="69df9-125">在推送通知的情况下， **MoreEvents**的**true**值向客户端指明将向客户端发送另一个通知请求，以传递其余事件。</span><span class="sxs-lookup"><span data-stu-id="69df9-125">In the case of Push notifications, a **true** value for **MoreEvents** indicates to the client that another notification request will be sent to the client to deliver the remaining events.</span></span> <span data-ttu-id="69df9-126">与 Pull 通知类似，这些后续请求将继续连续持续连续，直到客户端访问服务器上的事件队列为空。</span><span class="sxs-lookup"><span data-stu-id="69df9-126">Similar to Pull notifications, these follow-up requests will continue in continuous succession until the event queue on the Client Access server is empty.</span></span> 
  
<span data-ttu-id="69df9-127">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="69df9-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="69df9-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="69df9-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="69df9-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="69df9-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="69df9-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="69df9-130">Schema Name</span></span>  <br/> |<span data-ttu-id="69df9-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="69df9-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="69df9-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="69df9-132">Validation File</span></span>  <br/> |<span data-ttu-id="69df9-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="69df9-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="69df9-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="69df9-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="69df9-135">False</span><span class="sxs-lookup"><span data-stu-id="69df9-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="69df9-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="69df9-136">See also</span></span>



[<span data-ttu-id="69df9-137">订阅操作</span><span class="sxs-lookup"><span data-stu-id="69df9-137">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="69df9-138">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="69df9-138">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="69df9-139">取消订阅操作</span><span class="sxs-lookup"><span data-stu-id="69df9-139">Unsubscribe operation</span></span>](unsubscribe-operation.md)

