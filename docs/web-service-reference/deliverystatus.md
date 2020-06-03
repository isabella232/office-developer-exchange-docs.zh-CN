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
description: DeliveryStatus 元素指定邮件的状态。
ms.openlocfilehash: ae32202284d3dd272f693fbb7b76070cb6019d28
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461399"
---
# <a name="deliverystatus"></a><span data-ttu-id="e2e5a-103">DeliveryStatus</span><span class="sxs-lookup"><span data-stu-id="e2e5a-103">DeliveryStatus</span></span>

<span data-ttu-id="e2e5a-104">**DeliveryStatus**元素指定邮件的状态。</span><span class="sxs-lookup"><span data-stu-id="e2e5a-104">The **DeliveryStatus** element specifies the status for a message.</span></span> 
  
```XML
<DeliveryStatus>Unsuccessful | Pending | Delivered | Transferred | Read</DeliveryStatus>
```

 <span data-ttu-id="e2e5a-105">**MessageTrackingDeliveryStatusType**</span><span class="sxs-lookup"><span data-stu-id="e2e5a-105">**MessageTrackingDeliveryStatusType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e2e5a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e2e5a-106">Attributes and elements</span></span>

<span data-ttu-id="e2e5a-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e2e5a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e2e5a-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="e2e5a-108">Attributes</span></span>

<span data-ttu-id="e2e5a-109">无。</span><span class="sxs-lookup"><span data-stu-id="e2e5a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e2e5a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e2e5a-110">Child elements</span></span>

<span data-ttu-id="e2e5a-111">无。</span><span class="sxs-lookup"><span data-stu-id="e2e5a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e2e5a-112">父元素</span><span class="sxs-lookup"><span data-stu-id="e2e5a-112">Parent elements</span></span>

|<span data-ttu-id="e2e5a-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="e2e5a-113">**Element**</span></span>|<span data-ttu-id="e2e5a-114">**描述**</span><span class="sxs-lookup"><span data-stu-id="e2e5a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e2e5a-115">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="e2e5a-115">RecipientTrackingEvent</span></span>](recipienttrackingevent.md) <br/> |<span data-ttu-id="e2e5a-116">包含收件人的单个事件的信息。</span><span class="sxs-lookup"><span data-stu-id="e2e5a-116">Contains information for a single event for a recipient.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e2e5a-117">文本值</span><span class="sxs-lookup"><span data-stu-id="e2e5a-117">Text value</span></span>

<span data-ttu-id="e2e5a-118">下表列出了**DeliveryStatus**元素的可能的文本值。</span><span class="sxs-lookup"><span data-stu-id="e2e5a-118">The following table lists the possible text values for the **DeliveryStatus** element.</span></span> 
  
<span data-ttu-id="e2e5a-119">**DeliveryStatus 元素值**</span><span class="sxs-lookup"><span data-stu-id="e2e5a-119">**DeliveryStatus element values**</span></span>

|<span data-ttu-id="e2e5a-120">**值**</span><span class="sxs-lookup"><span data-stu-id="e2e5a-120">**Value**</span></span>|<span data-ttu-id="e2e5a-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="e2e5a-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e2e5a-122">多次</span><span class="sxs-lookup"><span data-stu-id="e2e5a-122">Unsuccessful</span></span>  <br/> |<span data-ttu-id="e2e5a-123">指定邮件未送达。</span><span class="sxs-lookup"><span data-stu-id="e2e5a-123">Specifies that a message was not delivered.</span></span>  <br/> |
|<span data-ttu-id="e2e5a-124">Pending</span><span class="sxs-lookup"><span data-stu-id="e2e5a-124">Pending</span></span>  <br/> |<span data-ttu-id="e2e5a-125">指定邮件正在等待来自审阅者的审批。</span><span class="sxs-lookup"><span data-stu-id="e2e5a-125">Specifies that the message is waiting for approval from a moderator.</span></span>  <br/> |
|<span data-ttu-id="e2e5a-126">附带</span><span class="sxs-lookup"><span data-stu-id="e2e5a-126">Delivered</span></span>  <br/> |<span data-ttu-id="e2e5a-127">指定邮件已传递给所有指定的收件人。</span><span class="sxs-lookup"><span data-stu-id="e2e5a-127">Specifies that the message was delivered to all of the specified recipients.</span></span>  <br/> |
|<span data-ttu-id="e2e5a-128">传递</span><span class="sxs-lookup"><span data-stu-id="e2e5a-128">Transferred</span></span>  <br/> |<span data-ttu-id="e2e5a-129">指定将邮件传输到搜索范围之外的服务器。</span><span class="sxs-lookup"><span data-stu-id="e2e5a-129">Specifies that the message was transferred to a server outside the search scope.</span></span>  <br/> |
|<span data-ttu-id="e2e5a-130">阅读</span><span class="sxs-lookup"><span data-stu-id="e2e5a-130">Read</span></span>  <br/> |<span data-ttu-id="e2e5a-131">指定邮件已被收件人传递和读取。</span><span class="sxs-lookup"><span data-stu-id="e2e5a-131">Specifies that the message was delivered and read by the recipients.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e2e5a-132">备注</span><span class="sxs-lookup"><span data-stu-id="e2e5a-132">Remarks</span></span>

<span data-ttu-id="e2e5a-133">**DeliveryStatus**元素为 Exchange Server 2010 中的**MessageTrackingDeliveryStatusType**类型。</span><span class="sxs-lookup"><span data-stu-id="e2e5a-133">The **DeliveryStatus** element was of type **MessageTrackingDeliveryStatusType** in Exchange Server 2010.</span></span> 
  
<span data-ttu-id="e2e5a-134">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e2e5a-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e2e5a-135">元素信息</span><span class="sxs-lookup"><span data-stu-id="e2e5a-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e2e5a-136">命名空间</span><span class="sxs-lookup"><span data-stu-id="e2e5a-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e2e5a-137">架构名称</span><span class="sxs-lookup"><span data-stu-id="e2e5a-137">Schema Name</span></span>  <br/> |<span data-ttu-id="e2e5a-138">类型架构</span><span class="sxs-lookup"><span data-stu-id="e2e5a-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="e2e5a-139">验证文件</span><span class="sxs-lookup"><span data-stu-id="e2e5a-139">Validation File</span></span>  <br/> |<span data-ttu-id="e2e5a-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e2e5a-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e2e5a-141">可以为空</span><span class="sxs-lookup"><span data-stu-id="e2e5a-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="e2e5a-142">False</span><span class="sxs-lookup"><span data-stu-id="e2e5a-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e2e5a-143">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e2e5a-143">See also</span></span>

- [<span data-ttu-id="e2e5a-144">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e2e5a-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

