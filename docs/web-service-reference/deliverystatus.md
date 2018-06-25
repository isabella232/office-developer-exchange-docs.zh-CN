---
title: DeliveryStatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeliveryStatus
api_type:
- schema
ms.assetid: eab55db3-affb-42be-a586-5caa04052433
description: DeliveryStatus 元素指定一条消息的状态。
ms.openlocfilehash: 4e6f31e8ef4f98d8e838ba91167c7dd5d6ab2590
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753832"
---
# <a name="deliverystatus"></a><span data-ttu-id="970b3-103">DeliveryStatus</span><span class="sxs-lookup"><span data-stu-id="970b3-103">DeliveryStatus</span></span>

<span data-ttu-id="970b3-104">**DeliveryStatus**元素指定一条消息的状态。</span><span class="sxs-lookup"><span data-stu-id="970b3-104">The **DeliveryStatus** element specifies the status for a message.</span></span> 
  
```XML
<DeliveryStatus>Unsuccessful | Pending | Delivered | Transferred | Read</DeliveryStatus>
```

 <span data-ttu-id="970b3-105">**MessageTrackingDeliveryStatusType**</span><span class="sxs-lookup"><span data-stu-id="970b3-105">**MessageTrackingDeliveryStatusType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="970b3-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="970b3-106">Attributes and elements</span></span>

<span data-ttu-id="970b3-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="970b3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="970b3-108">属性</span><span class="sxs-lookup"><span data-stu-id="970b3-108">Attributes</span></span>

<span data-ttu-id="970b3-109">无。</span><span class="sxs-lookup"><span data-stu-id="970b3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="970b3-110">子元素</span><span class="sxs-lookup"><span data-stu-id="970b3-110">Child elements</span></span>

<span data-ttu-id="970b3-111">无。</span><span class="sxs-lookup"><span data-stu-id="970b3-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="970b3-112">父元素</span><span class="sxs-lookup"><span data-stu-id="970b3-112">Parent elements</span></span>

|<span data-ttu-id="970b3-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="970b3-113">**Element**</span></span>|<span data-ttu-id="970b3-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="970b3-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="970b3-115">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="970b3-115">RecipientTrackingEvent</span></span>](recipienttrackingevent.md) <br/> |<span data-ttu-id="970b3-116">包含收件人为一个事件的信息。</span><span class="sxs-lookup"><span data-stu-id="970b3-116">Contains information for a single event for a recipient.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="970b3-117">文本值</span><span class="sxs-lookup"><span data-stu-id="970b3-117">Text value</span></span>

<span data-ttu-id="970b3-118">下表列出了**DeliveryStatus**元素的可能的文本值。</span><span class="sxs-lookup"><span data-stu-id="970b3-118">The following table lists the possible text values for the **DeliveryStatus** element.</span></span> 
  
<span data-ttu-id="970b3-119">**DeliveryStatus 元素的值**</span><span class="sxs-lookup"><span data-stu-id="970b3-119">**DeliveryStatus element values**</span></span>

|<span data-ttu-id="970b3-120">**值**</span><span class="sxs-lookup"><span data-stu-id="970b3-120">**Value**</span></span>|<span data-ttu-id="970b3-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="970b3-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="970b3-122">失败</span><span class="sxs-lookup"><span data-stu-id="970b3-122">Unsuccessful</span></span>  <br/> |<span data-ttu-id="970b3-123">指定一条消息未送达。</span><span class="sxs-lookup"><span data-stu-id="970b3-123">Specifies that a message was not delivered.</span></span>  <br/> |
|<span data-ttu-id="970b3-124">挂起</span><span class="sxs-lookup"><span data-stu-id="970b3-124">Pending</span></span>  <br/> |<span data-ttu-id="970b3-125">指定邮件正等待审阅者的批准。</span><span class="sxs-lookup"><span data-stu-id="970b3-125">Specifies that the message is waiting for approval from a moderator.</span></span>  <br/> |
|<span data-ttu-id="970b3-126">传送</span><span class="sxs-lookup"><span data-stu-id="970b3-126">Delivered</span></span>  <br/> |<span data-ttu-id="970b3-127">指定邮件已送达所有指定的收件人。</span><span class="sxs-lookup"><span data-stu-id="970b3-127">Specifies that the message was delivered to all of the specified recipients.</span></span>  <br/> |
|<span data-ttu-id="970b3-128">转接</span><span class="sxs-lookup"><span data-stu-id="970b3-128">Transferred</span></span>  <br/> |<span data-ttu-id="970b3-129">指定邮件已转接到的搜索范围之外的服务器。</span><span class="sxs-lookup"><span data-stu-id="970b3-129">Specifies that the message was transferred to a server outside the search scope.</span></span>  <br/> |
|<span data-ttu-id="970b3-130">已阅读</span><span class="sxs-lookup"><span data-stu-id="970b3-130">Read</span></span>  <br/> |<span data-ttu-id="970b3-131">指定邮件已发送和读取的收件人。</span><span class="sxs-lookup"><span data-stu-id="970b3-131">Specifies that the message was delivered and read by the recipients.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="970b3-132">注解</span><span class="sxs-lookup"><span data-stu-id="970b3-132">Remarks</span></span>

<span data-ttu-id="970b3-133">**DeliveryStatus**元素是类型**MessageTrackingDeliveryStatusType**在 Exchange Server 2010。</span><span class="sxs-lookup"><span data-stu-id="970b3-133">The **DeliveryStatus** element was of type **MessageTrackingDeliveryStatusType** in Exchange Server 2010.</span></span> 
  
<span data-ttu-id="970b3-134">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="970b3-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="970b3-135">元素信息</span><span class="sxs-lookup"><span data-stu-id="970b3-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="970b3-136">命名空间</span><span class="sxs-lookup"><span data-stu-id="970b3-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="970b3-137">架构名称</span><span class="sxs-lookup"><span data-stu-id="970b3-137">Schema Name</span></span>  <br/> |<span data-ttu-id="970b3-138">类型架构</span><span class="sxs-lookup"><span data-stu-id="970b3-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="970b3-139">验证文件</span><span class="sxs-lookup"><span data-stu-id="970b3-139">Validation File</span></span>  <br/> |<span data-ttu-id="970b3-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="970b3-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="970b3-141">可以为空</span><span class="sxs-lookup"><span data-stu-id="970b3-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="970b3-142">False</span><span class="sxs-lookup"><span data-stu-id="970b3-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="970b3-143">另请参阅</span><span class="sxs-lookup"><span data-stu-id="970b3-143">See also</span></span>

- [<span data-ttu-id="970b3-144">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="970b3-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

