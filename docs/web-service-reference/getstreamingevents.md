---
title: GetStreamingEvents
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetStreamingEvents
api_type:
- schema
ms.assetid: dbe83857-c4f8-4d98-813f-e03c289697a1
description: GetStreamingEvents 元素均表示客户端用于从服务器请求流通知的操作。
ms.openlocfilehash: b07015541cf9c2fbbbc11ebc9f10421bdb9ee84f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825679"
---
# <a name="getstreamingevents"></a><span data-ttu-id="3c68c-103">GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="3c68c-103">GetStreamingEvents</span></span>

<span data-ttu-id="3c68c-104">**GetStreamingEvents**元素均表示客户端用于从服务器请求流通知的操作。</span><span class="sxs-lookup"><span data-stu-id="3c68c-104">The **GetStreamingEvents** element represents the operation that is used by clients to request streaming notifications from the server.</span></span> 
  
[<span data-ttu-id="3c68c-105">GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="3c68c-105">GetStreamingEvents</span></span>](getstreamingevents.md)
  
```XML
<GetStreamingEvents>
   <SubscriptionId/>
   <ConnectionTimeout/>
</GetStreamingEvents>
```

 <span data-ttu-id="3c68c-106">**GetStreamingEventsType**</span><span class="sxs-lookup"><span data-stu-id="3c68c-106">**GetStreamingEventsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3c68c-107">属性和元素</span><span class="sxs-lookup"><span data-stu-id="3c68c-107">Attributes and elements</span></span>

<span data-ttu-id="3c68c-108">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3c68c-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3c68c-109">属性</span><span class="sxs-lookup"><span data-stu-id="3c68c-109">Attributes</span></span>

<span data-ttu-id="3c68c-110">无。</span><span class="sxs-lookup"><span data-stu-id="3c68c-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3c68c-111">子元素</span><span class="sxs-lookup"><span data-stu-id="3c68c-111">Child elements</span></span>

|<span data-ttu-id="3c68c-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="3c68c-112">**Element**</span></span>|<span data-ttu-id="3c68c-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="3c68c-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3c68c-114">SubscriptionId (GetStreamingEvents)</span><span class="sxs-lookup"><span data-stu-id="3c68c-114">SubscriptionId (GetStreamingEvents)</span></span>](subscriptionid-getstreamingevents.md) <br/> |<span data-ttu-id="3c68c-115">表示查询事件的订阅标识符。</span><span class="sxs-lookup"><span data-stu-id="3c68c-115">Represents the identifier for a subscription that is queried for events.</span></span>  <br/> |
|[<span data-ttu-id="3c68c-116">ConnectionTimeout</span><span class="sxs-lookup"><span data-stu-id="3c68c-116">ConnectionTimeout</span></span>](connectiontimeout.md) <br/> |<span data-ttu-id="3c68c-117">代表要保持连接处于打开状态的分钟数。</span><span class="sxs-lookup"><span data-stu-id="3c68c-117">Represents the number of minutes to keep a connection open.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3c68c-118">父元素</span><span class="sxs-lookup"><span data-stu-id="3c68c-118">Parent elements</span></span>

<span data-ttu-id="3c68c-119">无。</span><span class="sxs-lookup"><span data-stu-id="3c68c-119">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="3c68c-120">文本值</span><span class="sxs-lookup"><span data-stu-id="3c68c-120">Text value</span></span>

<span data-ttu-id="3c68c-121">无。</span><span class="sxs-lookup"><span data-stu-id="3c68c-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3c68c-122">备注</span><span class="sxs-lookup"><span data-stu-id="3c68c-122">Remarks</span></span>

<span data-ttu-id="3c68c-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="3c68c-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3c68c-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="3c68c-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3c68c-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="3c68c-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3c68c-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="3c68c-126">Schema name</span></span>  <br/> |<span data-ttu-id="3c68c-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="3c68c-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3c68c-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="3c68c-128">Validation file</span></span>  <br/> |<span data-ttu-id="3c68c-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3c68c-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3c68c-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="3c68c-130">Can be empty</span></span>  <br/> |<span data-ttu-id="3c68c-131">False</span><span class="sxs-lookup"><span data-stu-id="3c68c-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3c68c-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3c68c-132">See also</span></span>



[<span data-ttu-id="3c68c-133">订阅操作</span><span class="sxs-lookup"><span data-stu-id="3c68c-133">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="3c68c-134">GetStreamingEvents 操作</span><span class="sxs-lookup"><span data-stu-id="3c68c-134">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)
  
[<span data-ttu-id="3c68c-135">取消操作</span><span class="sxs-lookup"><span data-stu-id="3c68c-135">Unsubscribe operation</span></span>](unsubscribe-operation.md)


- [<span data-ttu-id="3c68c-136">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="3c68c-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
