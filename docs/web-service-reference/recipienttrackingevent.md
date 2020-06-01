---
title: RecipientTrackingEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RecipientTrackingEvent
api_type:
- schema
ms.assetid: 2bffdac7-c2f5-4805-ae7e-bd865301acb6
description: RecipientTrackingEvent 元素包含收件人的单个事件的信息。
ms.openlocfilehash: e9a014cdfac122f112205cfa5032535a770f9d82
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465483"
---
# <a name="recipienttrackingevent"></a><span data-ttu-id="7778f-103">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="7778f-103">RecipientTrackingEvent</span></span>

<span data-ttu-id="7778f-104">**RecipientTrackingEvent**元素包含收件人的单个事件的信息。</span><span class="sxs-lookup"><span data-stu-id="7778f-104">The **RecipientTrackingEvent** element contains information for a single event for a recipient.</span></span> 
  
```XML
<RecipientTrackingEvent>
   <Date/>
   <Recipient/>
   <DeliveryStatus/>
   <EventDescription/>
   <EventData/>
   <Server/>
   <InternalId/>
   <BccRecipient/>
   <HiddenRecipient/>
   <UniquePathId/>
   <RootAddress/>
   <Properties/>
</RecipientTrackingEvent>
```

 <span data-ttu-id="7778f-105">**RecipientTrackingEventType**</span><span class="sxs-lookup"><span data-stu-id="7778f-105">**RecipientTrackingEventType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7778f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7778f-106">Attributes and elements</span></span>

<span data-ttu-id="7778f-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7778f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7778f-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="7778f-108">Attributes</span></span>

<span data-ttu-id="7778f-109">无。</span><span class="sxs-lookup"><span data-stu-id="7778f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7778f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="7778f-110">Child elements</span></span>

|<span data-ttu-id="7778f-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="7778f-111">**Element**</span></span>|<span data-ttu-id="7778f-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="7778f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7778f-113">Date （MessageTracking）</span><span class="sxs-lookup"><span data-stu-id="7778f-113">Date (MessageTracking)</span></span>](date-messagetracking.md) <br/> |<span data-ttu-id="7778f-114">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="7778f-114">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="7778f-115">收件人</span><span class="sxs-lookup"><span data-stu-id="7778f-115">Recipient</span></span>](recipient.md) <br/> |<span data-ttu-id="7778f-116">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="7778f-116">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="7778f-117">DeliveryStatus</span><span class="sxs-lookup"><span data-stu-id="7778f-117">DeliveryStatus</span></span>](deliverystatus.md) <br/> |<span data-ttu-id="7778f-118">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="7778f-118">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="7778f-119">EventDescription</span><span class="sxs-lookup"><span data-stu-id="7778f-119">EventDescription</span></span>](eventdescription.md) <br/> |<span data-ttu-id="7778f-120">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="7778f-120">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="7778f-121">EventData</span><span class="sxs-lookup"><span data-stu-id="7778f-121">EventData</span></span>](eventdata.md) <br/> |<span data-ttu-id="7778f-122">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="7778f-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="7778f-123">服务器（MessageTracking）</span><span class="sxs-lookup"><span data-stu-id="7778f-123">Server (MessageTracking)</span></span>](server-messagetracking.md) <br/> |<span data-ttu-id="7778f-124">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="7778f-124">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="7778f-125">InternalId</span><span class="sxs-lookup"><span data-stu-id="7778f-125">InternalId</span></span>](internalid.md) <br/> |<span data-ttu-id="7778f-126">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="7778f-126">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="7778f-127">BccRecipient</span><span class="sxs-lookup"><span data-stu-id="7778f-127">BccRecipient</span></span>](bccrecipient.md) <br/> |<span data-ttu-id="7778f-128">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="7778f-128">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="7778f-129">HiddenRecipient</span><span class="sxs-lookup"><span data-stu-id="7778f-129">HiddenRecipient</span></span>](hiddenrecipient.md) <br/> |<span data-ttu-id="7778f-130">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="7778f-130">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="7778f-131">UniquePathId</span><span class="sxs-lookup"><span data-stu-id="7778f-131">UniquePathId</span></span>](uniquepathid.md) <br/> |<span data-ttu-id="7778f-132">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="7778f-132">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="7778f-133">RootAddress</span><span class="sxs-lookup"><span data-stu-id="7778f-133">RootAddress</span></span>](rootaddress.md) <br/> |<span data-ttu-id="7778f-134">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="7778f-134">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="7778f-135">Properties （ArrayOfTrackingPropertiesType）</span><span class="sxs-lookup"><span data-stu-id="7778f-135">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="7778f-136">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="7778f-136">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7778f-137">父元素</span><span class="sxs-lookup"><span data-stu-id="7778f-137">Parent elements</span></span>

|<span data-ttu-id="7778f-138">**元素**</span><span class="sxs-lookup"><span data-stu-id="7778f-138">**Element**</span></span>|<span data-ttu-id="7778f-139">**说明**</span><span class="sxs-lookup"><span data-stu-id="7778f-139">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7778f-140">RecipientTrackingEvents</span><span class="sxs-lookup"><span data-stu-id="7778f-140">RecipientTrackingEvents</span></span>](recipienttrackingevents.md) <br/> |<span data-ttu-id="7778f-141">包含收件人的一个或多个跟踪事件的列表。</span><span class="sxs-lookup"><span data-stu-id="7778f-141">Contains a list of one or more tracking events for a recipient.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7778f-142">文本值</span><span class="sxs-lookup"><span data-stu-id="7778f-142">Text value</span></span>

<span data-ttu-id="7778f-143">无。</span><span class="sxs-lookup"><span data-stu-id="7778f-143">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7778f-144">说明</span><span class="sxs-lookup"><span data-stu-id="7778f-144">Remarks</span></span>

<span data-ttu-id="7778f-145">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7778f-145">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7778f-146">元素信息</span><span class="sxs-lookup"><span data-stu-id="7778f-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7778f-147">命名空间</span><span class="sxs-lookup"><span data-stu-id="7778f-147">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7778f-148">架构名称</span><span class="sxs-lookup"><span data-stu-id="7778f-148">Schema Name</span></span>  <br/> |<span data-ttu-id="7778f-149">类型架构</span><span class="sxs-lookup"><span data-stu-id="7778f-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="7778f-150">验证文件</span><span class="sxs-lookup"><span data-stu-id="7778f-150">Validation File</span></span>  <br/> |<span data-ttu-id="7778f-151">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7778f-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7778f-152">可以为空</span><span class="sxs-lookup"><span data-stu-id="7778f-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="7778f-153">False</span><span class="sxs-lookup"><span data-stu-id="7778f-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7778f-154">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7778f-154">See also</span></span>



[<span data-ttu-id="7778f-155">GetMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="7778f-155">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="7778f-156">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="7778f-156">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

