---
title: AppointmentState
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AppointmentState
api_type:
- schema
ms.assetid: ab3f5d04-ace1-4a15-9107-cefa6c41abc7
description: AppointmentState 元素指定约会的状态。
ms.openlocfilehash: 8b0e827d02e9051f31d43199503dc286c50e2125
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463473"
---
# <a name="appointmentstate"></a><span data-ttu-id="f9113-103">AppointmentState</span><span class="sxs-lookup"><span data-stu-id="f9113-103">AppointmentState</span></span>

<span data-ttu-id="f9113-104">**AppointmentState**元素指定约会的状态。</span><span class="sxs-lookup"><span data-stu-id="f9113-104">The **AppointmentState** element specifies the status of the appointment.</span></span> 
  
```XML
<AppointmentState/>
```

 <span data-ttu-id="f9113-105">**int**</span><span class="sxs-lookup"><span data-stu-id="f9113-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f9113-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f9113-106">Attributes and elements</span></span>

<span data-ttu-id="f9113-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f9113-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f9113-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="f9113-108">Attributes</span></span>

<span data-ttu-id="f9113-109">无。</span><span class="sxs-lookup"><span data-stu-id="f9113-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f9113-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f9113-110">Child elements</span></span>

<span data-ttu-id="f9113-111">无。</span><span class="sxs-lookup"><span data-stu-id="f9113-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f9113-112">父元素</span><span class="sxs-lookup"><span data-stu-id="f9113-112">Parent elements</span></span>

|<span data-ttu-id="f9113-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="f9113-113">**Element**</span></span>|<span data-ttu-id="f9113-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="f9113-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f9113-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="f9113-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="f9113-116">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="f9113-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="f9113-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="f9113-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="f9113-118">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="f9113-118">Represents a meeting in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f9113-119">文本值</span><span class="sxs-lookup"><span data-stu-id="f9113-119">Text value</span></span>

<span data-ttu-id="f9113-120">此元素包含表示设置位的文本值。</span><span class="sxs-lookup"><span data-stu-id="f9113-120">This element contains a text value that represents set bits.</span></span> <span data-ttu-id="f9113-121">这是整数形式。</span><span class="sxs-lookup"><span data-stu-id="f9113-121">This is in integer form.</span></span> <span data-ttu-id="f9113-122">此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="f9113-122">This element is read-only.</span></span> <span data-ttu-id="f9113-123">它只会在响应中返回。</span><span class="sxs-lookup"><span data-stu-id="f9113-123">It will only be returned in a response.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f9113-124">备注</span><span class="sxs-lookup"><span data-stu-id="f9113-124">Remarks</span></span>

<span data-ttu-id="f9113-125">返回的整数值表示约会状态位掩码。</span><span class="sxs-lookup"><span data-stu-id="f9113-125">The integer value that is returned represents the appointment state bitmask.</span></span> <span data-ttu-id="f9113-126">下表介绍了每个位。</span><span class="sxs-lookup"><span data-stu-id="f9113-126">The following table describes each bit.</span></span>
  
|<span data-ttu-id="f9113-127">**名称**</span><span class="sxs-lookup"><span data-stu-id="f9113-127">**Name**</span></span>|<span data-ttu-id="f9113-128">**位**</span><span class="sxs-lookup"><span data-stu-id="f9113-128">**Bit**</span></span>|<span data-ttu-id="f9113-129">**说明**</span><span class="sxs-lookup"><span data-stu-id="f9113-129">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f9113-130">无</span><span class="sxs-lookup"><span data-stu-id="f9113-130">None</span></span>  <br/> |<span data-ttu-id="f9113-131">0x0000</span><span class="sxs-lookup"><span data-stu-id="f9113-131">0x0000</span></span>  <br/> |<span data-ttu-id="f9113-132">未设置任何标志。</span><span class="sxs-lookup"><span data-stu-id="f9113-132">No flags have been set.</span></span> <span data-ttu-id="f9113-133">此功能仅用于不包含与会者的约会。</span><span class="sxs-lookup"><span data-stu-id="f9113-133">This is only used for an appointment that does not include attendees.</span></span>  <br/> |
|<span data-ttu-id="f9113-134">要求</span><span class="sxs-lookup"><span data-stu-id="f9113-134">Meeting</span></span>  <br/> |<span data-ttu-id="f9113-135">0x0001</span><span class="sxs-lookup"><span data-stu-id="f9113-135">0x0001</span></span>  <br/> |<span data-ttu-id="f9113-136">此约会是一种会议。</span><span class="sxs-lookup"><span data-stu-id="f9113-136">This appointment is a meeting.</span></span>  <br/> |
|<span data-ttu-id="f9113-137">接收时间</span><span class="sxs-lookup"><span data-stu-id="f9113-137">Received</span></span>  <br/> |<span data-ttu-id="f9113-138">0x0002</span><span class="sxs-lookup"><span data-stu-id="f9113-138">0x0002</span></span>  <br/> |<span data-ttu-id="f9113-139">已收到此约会。</span><span class="sxs-lookup"><span data-stu-id="f9113-139">This appointment has been received.</span></span>  <br/> |
|<span data-ttu-id="f9113-140">已取消</span><span class="sxs-lookup"><span data-stu-id="f9113-140">Canceled</span></span>  <br/> |<span data-ttu-id="f9113-141">0x0004</span><span class="sxs-lookup"><span data-stu-id="f9113-141">0x0004</span></span>  <br/> |<span data-ttu-id="f9113-142">此约会已被取消。</span><span class="sxs-lookup"><span data-stu-id="f9113-142">This appointment has been canceled.</span></span>  <br/> |
   
<span data-ttu-id="f9113-143">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f9113-143">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f9113-144">元素信息</span><span class="sxs-lookup"><span data-stu-id="f9113-144">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f9113-145">命名空间</span><span class="sxs-lookup"><span data-stu-id="f9113-145">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f9113-146">架构名称</span><span class="sxs-lookup"><span data-stu-id="f9113-146">Schema name</span></span>  <br/> |<span data-ttu-id="f9113-147">类型架构</span><span class="sxs-lookup"><span data-stu-id="f9113-147">Types schema</span></span>  <br/> |
|<span data-ttu-id="f9113-148">验证文件</span><span class="sxs-lookup"><span data-stu-id="f9113-148">Validation file</span></span>  <br/> |<span data-ttu-id="f9113-149">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f9113-149">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f9113-150">可以为空</span><span class="sxs-lookup"><span data-stu-id="f9113-150">Can be empty</span></span>  <br/> |<span data-ttu-id="f9113-151">False</span><span class="sxs-lookup"><span data-stu-id="f9113-151">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f9113-152">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f9113-152">See also</span></span>

- [<span data-ttu-id="f9113-153">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f9113-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

