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
description: RecipientTrackingEvent 元素包含收件人为一个事件的信息。
ms.openlocfilehash: c5488ba105f9a853a490d6f0f4ff9ff15b537e23
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826989"
---
# <a name="recipienttrackingevent"></a><span data-ttu-id="52281-103">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="52281-103">RecipientTrackingEvent</span></span>

<span data-ttu-id="52281-104">**RecipientTrackingEvent**元素包含收件人为一个事件的信息。</span><span class="sxs-lookup"><span data-stu-id="52281-104">The **RecipientTrackingEvent** element contains information for a single event for a recipient.</span></span> 
  
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

 <span data-ttu-id="52281-105">**RecipientTrackingEventType**</span><span class="sxs-lookup"><span data-stu-id="52281-105">**RecipientTrackingEventType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="52281-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="52281-106">Attributes and elements</span></span>

<span data-ttu-id="52281-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="52281-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="52281-108">属性</span><span class="sxs-lookup"><span data-stu-id="52281-108">Attributes</span></span>

<span data-ttu-id="52281-109">无。</span><span class="sxs-lookup"><span data-stu-id="52281-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="52281-110">子元素</span><span class="sxs-lookup"><span data-stu-id="52281-110">Child elements</span></span>

|<span data-ttu-id="52281-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="52281-111">**Element**</span></span>|<span data-ttu-id="52281-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="52281-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="52281-113">日期 (MessageTracking)</span><span class="sxs-lookup"><span data-stu-id="52281-113">Date (MessageTracking)</span></span>](date-messagetracking.md) <br/> |<span data-ttu-id="52281-114">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="52281-114">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="52281-115">Recipient</span><span class="sxs-lookup"><span data-stu-id="52281-115">Recipient</span></span>](recipient.md) <br/> |<span data-ttu-id="52281-116">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="52281-116">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="52281-117">DeliveryStatus</span><span class="sxs-lookup"><span data-stu-id="52281-117">DeliveryStatus</span></span>](deliverystatus.md) <br/> |<span data-ttu-id="52281-118">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="52281-118">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="52281-119">EventDescription</span><span class="sxs-lookup"><span data-stu-id="52281-119">EventDescription</span></span>](eventdescription.md) <br/> |<span data-ttu-id="52281-120">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="52281-120">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="52281-121">EventData</span><span class="sxs-lookup"><span data-stu-id="52281-121">EventData</span></span>](eventdata.md) <br/> |<span data-ttu-id="52281-122">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="52281-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="52281-123">服务器 (MessageTracking)</span><span class="sxs-lookup"><span data-stu-id="52281-123">Server (MessageTracking)</span></span>](server-messagetracking.md) <br/> |<span data-ttu-id="52281-124">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="52281-124">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="52281-125">InternalId</span><span class="sxs-lookup"><span data-stu-id="52281-125">InternalId</span></span>](internalid.md) <br/> |<span data-ttu-id="52281-126">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="52281-126">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="52281-127">BccRecipient</span><span class="sxs-lookup"><span data-stu-id="52281-127">BccRecipient</span></span>](bccrecipient.md) <br/> |<span data-ttu-id="52281-128">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="52281-128">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="52281-129">HiddenRecipient</span><span class="sxs-lookup"><span data-stu-id="52281-129">HiddenRecipient</span></span>](hiddenrecipient.md) <br/> |<span data-ttu-id="52281-130">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="52281-130">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="52281-131">UniquePathId</span><span class="sxs-lookup"><span data-stu-id="52281-131">UniquePathId</span></span>](uniquepathid.md) <br/> |<span data-ttu-id="52281-132">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="52281-132">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="52281-133">RootAddress</span><span class="sxs-lookup"><span data-stu-id="52281-133">RootAddress</span></span>](rootaddress.md) <br/> |<span data-ttu-id="52281-134">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="52281-134">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="52281-135">属性 (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="52281-135">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="52281-136">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="52281-136">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="52281-137">父元素</span><span class="sxs-lookup"><span data-stu-id="52281-137">Parent elements</span></span>

|<span data-ttu-id="52281-138">**元素**</span><span class="sxs-lookup"><span data-stu-id="52281-138">**Element**</span></span>|<span data-ttu-id="52281-139">**说明**</span><span class="sxs-lookup"><span data-stu-id="52281-139">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="52281-140">RecipientTrackingEvents</span><span class="sxs-lookup"><span data-stu-id="52281-140">RecipientTrackingEvents</span></span>](recipienttrackingevents.md) <br/> |<span data-ttu-id="52281-141">包含一个或多个跟踪事件的列表的收件人。</span><span class="sxs-lookup"><span data-stu-id="52281-141">Contains a list of one or more tracking events for a recipient.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="52281-142">文本值</span><span class="sxs-lookup"><span data-stu-id="52281-142">Text value</span></span>

<span data-ttu-id="52281-143">无。</span><span class="sxs-lookup"><span data-stu-id="52281-143">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="52281-144">备注</span><span class="sxs-lookup"><span data-stu-id="52281-144">Remarks</span></span>

<span data-ttu-id="52281-145">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="52281-145">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="52281-146">元素信息</span><span class="sxs-lookup"><span data-stu-id="52281-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="52281-147">命名空间</span><span class="sxs-lookup"><span data-stu-id="52281-147">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="52281-148">架构名称</span><span class="sxs-lookup"><span data-stu-id="52281-148">Schema Name</span></span>  <br/> |<span data-ttu-id="52281-149">类型架构</span><span class="sxs-lookup"><span data-stu-id="52281-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="52281-150">验证文件</span><span class="sxs-lookup"><span data-stu-id="52281-150">Validation File</span></span>  <br/> |<span data-ttu-id="52281-151">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="52281-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="52281-152">可以为空</span><span class="sxs-lookup"><span data-stu-id="52281-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="52281-153">False</span><span class="sxs-lookup"><span data-stu-id="52281-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="52281-154">另请参阅</span><span class="sxs-lookup"><span data-stu-id="52281-154">See also</span></span>



[<span data-ttu-id="52281-155">GetMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="52281-155">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="52281-156">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="52281-156">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

