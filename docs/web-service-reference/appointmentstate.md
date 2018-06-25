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
ms.openlocfilehash: 05e92a3fea10a84518b0680c425011a91bc43d93
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753248"
---
# <a name="appointmentstate"></a><span data-ttu-id="fb60d-103">AppointmentState</span><span class="sxs-lookup"><span data-stu-id="fb60d-103">AppointmentState</span></span>

<span data-ttu-id="fb60d-104">**AppointmentState**元素指定约会的状态。</span><span class="sxs-lookup"><span data-stu-id="fb60d-104">The **AppointmentState** element specifies the status of the appointment.</span></span> 
  
```XML
<AppointmentState/>
```

 <span data-ttu-id="fb60d-105">**int**</span><span class="sxs-lookup"><span data-stu-id="fb60d-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fb60d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fb60d-106">Attributes and elements</span></span>

<span data-ttu-id="fb60d-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fb60d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fb60d-108">属性</span><span class="sxs-lookup"><span data-stu-id="fb60d-108">Attributes</span></span>

<span data-ttu-id="fb60d-109">无。</span><span class="sxs-lookup"><span data-stu-id="fb60d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fb60d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="fb60d-110">Child elements</span></span>

<span data-ttu-id="fb60d-111">无。</span><span class="sxs-lookup"><span data-stu-id="fb60d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fb60d-112">父元素</span><span class="sxs-lookup"><span data-stu-id="fb60d-112">Parent elements</span></span>

|<span data-ttu-id="fb60d-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="fb60d-113">**Element**</span></span>|<span data-ttu-id="fb60d-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="fb60d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fb60d-115">日历项目</span><span class="sxs-lookup"><span data-stu-id="fb60d-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="fb60d-116">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="fb60d-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="fb60d-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="fb60d-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="fb60d-118">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="fb60d-118">Represents a meeting in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fb60d-119">文本值</span><span class="sxs-lookup"><span data-stu-id="fb60d-119">Text value</span></span>

<span data-ttu-id="fb60d-120">此元素包含代表设置位的文本值。</span><span class="sxs-lookup"><span data-stu-id="fb60d-120">This element contains a text value that represents set bits.</span></span> <span data-ttu-id="fb60d-121">这是整数窗体中。</span><span class="sxs-lookup"><span data-stu-id="fb60d-121">This is in integer form.</span></span> <span data-ttu-id="fb60d-122">此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="fb60d-122">This element is read-only.</span></span> <span data-ttu-id="fb60d-123">仅将在响应中返回它。</span><span class="sxs-lookup"><span data-stu-id="fb60d-123">It will only be returned in a response.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fb60d-124">注解</span><span class="sxs-lookup"><span data-stu-id="fb60d-124">Remarks</span></span>

<span data-ttu-id="fb60d-125">返回的整数值表示的约会状态位掩码。</span><span class="sxs-lookup"><span data-stu-id="fb60d-125">The integer value that is returned represents the appointment state bitmask.</span></span> <span data-ttu-id="fb60d-126">下表介绍了每一位。</span><span class="sxs-lookup"><span data-stu-id="fb60d-126">The following table describes each bit.</span></span>
  
|<span data-ttu-id="fb60d-127">**名称**</span><span class="sxs-lookup"><span data-stu-id="fb60d-127">**Name**</span></span>|<span data-ttu-id="fb60d-128">**位**</span><span class="sxs-lookup"><span data-stu-id="fb60d-128">**Bit**</span></span>|<span data-ttu-id="fb60d-129">**说明**</span><span class="sxs-lookup"><span data-stu-id="fb60d-129">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fb60d-130">无</span><span class="sxs-lookup"><span data-stu-id="fb60d-130">None</span></span>  <br/> |<span data-ttu-id="fb60d-131">0x0000</span><span class="sxs-lookup"><span data-stu-id="fb60d-131">0x0000</span></span>  <br/> |<span data-ttu-id="fb60d-132">已不设置任何标志。</span><span class="sxs-lookup"><span data-stu-id="fb60d-132">No flags have been set.</span></span> <span data-ttu-id="fb60d-133">不包括与会者的约会才使用此选项。</span><span class="sxs-lookup"><span data-stu-id="fb60d-133">This is only used for an appointment that does not include attendees.</span></span>  <br/> |
|<span data-ttu-id="fb60d-134">会议</span><span class="sxs-lookup"><span data-stu-id="fb60d-134">Meeting</span></span>  <br/> |<span data-ttu-id="fb60d-135">0x0001</span><span class="sxs-lookup"><span data-stu-id="fb60d-135">0x0001</span></span>  <br/> |<span data-ttu-id="fb60d-136">该约会是会议。</span><span class="sxs-lookup"><span data-stu-id="fb60d-136">This appointment is a meeting.</span></span>  <br/> |
|<span data-ttu-id="fb60d-137">接收时间</span><span class="sxs-lookup"><span data-stu-id="fb60d-137">Received</span></span>  <br/> |<span data-ttu-id="fb60d-138">0x0002</span><span class="sxs-lookup"><span data-stu-id="fb60d-138">0x0002</span></span>  <br/> |<span data-ttu-id="fb60d-139">已收到此约会。</span><span class="sxs-lookup"><span data-stu-id="fb60d-139">This appointment has been received.</span></span>  <br/> |
|<span data-ttu-id="fb60d-140">已取消</span><span class="sxs-lookup"><span data-stu-id="fb60d-140">Canceled</span></span>  <br/> |<span data-ttu-id="fb60d-141">0x0004</span><span class="sxs-lookup"><span data-stu-id="fb60d-141">0x0004</span></span>  <br/> |<span data-ttu-id="fb60d-142">该约会已被取消。</span><span class="sxs-lookup"><span data-stu-id="fb60d-142">This appointment has been canceled.</span></span>  <br/> |
   
<span data-ttu-id="fb60d-143">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="fb60d-143">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fb60d-144">元素信息</span><span class="sxs-lookup"><span data-stu-id="fb60d-144">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fb60d-145">命名空间</span><span class="sxs-lookup"><span data-stu-id="fb60d-145">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fb60d-146">架构名称</span><span class="sxs-lookup"><span data-stu-id="fb60d-146">Schema name</span></span>  <br/> |<span data-ttu-id="fb60d-147">类型架构</span><span class="sxs-lookup"><span data-stu-id="fb60d-147">Types schema</span></span>  <br/> |
|<span data-ttu-id="fb60d-148">验证文件</span><span class="sxs-lookup"><span data-stu-id="fb60d-148">Validation file</span></span>  <br/> |<span data-ttu-id="fb60d-149">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fb60d-149">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fb60d-150">可以为空</span><span class="sxs-lookup"><span data-stu-id="fb60d-150">Can be empty</span></span>  <br/> |<span data-ttu-id="fb60d-151">False</span><span class="sxs-lookup"><span data-stu-id="fb60d-151">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fb60d-152">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fb60d-152">See also</span></span>

- [<span data-ttu-id="fb60d-153">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="fb60d-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

