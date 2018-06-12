---
title: GetEvents
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetEvents
api_type:
- schema
ms.assetid: 22d4da6b-d8a8-484f-82c4-3e4b8f5431cd
description: GetEvents 元素均表示从服务器请求通知使用拉客户端的操作。
ms.openlocfilehash: e7b24207bff579a2f5230676d6520452f96fe0ce
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754530"
---
# <a name="getevents"></a><span data-ttu-id="cc90a-103">GetEvents</span><span class="sxs-lookup"><span data-stu-id="cc90a-103">GetEvents</span></span>

<span data-ttu-id="cc90a-104">**GetEvents**元素均表示从服务器请求通知使用拉客户端的操作。</span><span class="sxs-lookup"><span data-stu-id="cc90a-104">The **GetEvents** element represents the operation used by pull clients to request notifications from the server.</span></span> 
  
[<span data-ttu-id="cc90a-105">GetEvents</span><span class="sxs-lookup"><span data-stu-id="cc90a-105">GetEvents</span></span>](getevents.md)
  
```xml
<GetEvents>
   <SubscriptionId/>
   <Watermark/>
</GetEvents>
```

 <span data-ttu-id="cc90a-106">**GetEventsType**</span><span class="sxs-lookup"><span data-stu-id="cc90a-106">**GetEventsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cc90a-107">属性和元素</span><span class="sxs-lookup"><span data-stu-id="cc90a-107">Attributes and elements</span></span>

<span data-ttu-id="cc90a-108">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="cc90a-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cc90a-109">属性</span><span class="sxs-lookup"><span data-stu-id="cc90a-109">Attributes</span></span>

<span data-ttu-id="cc90a-110">无。</span><span class="sxs-lookup"><span data-stu-id="cc90a-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cc90a-111">子元素</span><span class="sxs-lookup"><span data-stu-id="cc90a-111">Child elements</span></span>

|<span data-ttu-id="cc90a-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="cc90a-112">**Element**</span></span>|<span data-ttu-id="cc90a-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="cc90a-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cc90a-114">SubscriptionId (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="cc90a-114">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md) <br/> |<span data-ttu-id="cc90a-115">表示查询事件的订阅标识符。</span><span class="sxs-lookup"><span data-stu-id="cc90a-115">Represents the identifier for a subscription that is queried for events.</span></span>  <br/> |
|[<span data-ttu-id="cc90a-116">水印</span><span class="sxs-lookup"><span data-stu-id="cc90a-116">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="cc90a-117">表示上次水印返回到客户端。</span><span class="sxs-lookup"><span data-stu-id="cc90a-117">Represents the last watermark returned to the client.</span></span> <span data-ttu-id="cc90a-118">如果尚未为此订阅调用 GetEvents，客户端将使用从 Subscribe 请求返回水印。</span><span class="sxs-lookup"><span data-stu-id="cc90a-118">If GetEvents has not been called for this subscription, the client uses the watermark returned from the Subscribe request.</span></span> <span data-ttu-id="cc90a-119">否则，将使用从最后一个 GetEvents 响应中的最后一个事件水印。</span><span class="sxs-lookup"><span data-stu-id="cc90a-119">Otherwise, the watermark from the last event in the last GetEvents response is used.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cc90a-120">父元素</span><span class="sxs-lookup"><span data-stu-id="cc90a-120">Parent elements</span></span>

<span data-ttu-id="cc90a-121">无。</span><span class="sxs-lookup"><span data-stu-id="cc90a-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cc90a-122">备注</span><span class="sxs-lookup"><span data-stu-id="cc90a-122">Remarks</span></span>

<span data-ttu-id="cc90a-123">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="cc90a-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cc90a-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="cc90a-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cc90a-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="cc90a-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cc90a-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="cc90a-126">Schema name</span></span>  <br/> |<span data-ttu-id="cc90a-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="cc90a-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="cc90a-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="cc90a-128">Validation file</span></span>  <br/> |<span data-ttu-id="cc90a-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="cc90a-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cc90a-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="cc90a-130">Can be empty</span></span>  <br/> |<span data-ttu-id="cc90a-131">false</span><span class="sxs-lookup"><span data-stu-id="cc90a-131">false</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cc90a-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cc90a-132">See also</span></span>



[<span data-ttu-id="cc90a-133">订阅操作</span><span class="sxs-lookup"><span data-stu-id="cc90a-133">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="cc90a-134">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="cc90a-134">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="cc90a-135">取消操作</span><span class="sxs-lookup"><span data-stu-id="cc90a-135">Unsubscribe operation</span></span>](unsubscribe-operation.md)

