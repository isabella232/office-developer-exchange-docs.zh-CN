---
title: WorkingHours
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- WorkingHours
api_type:
- schema
ms.assetid: bbe97777-f728-46c5-b2aa-565112c24f3a
description: WorkingHours 元素表示所请求的邮箱用户的时区设置和工作时间。
ms.openlocfilehash: 9cb21e72f7024b96b4b5f252a8a3b85bb704e67c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468339"
---
# <a name="workinghours"></a><span data-ttu-id="385bf-103">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="385bf-103">WorkingHours</span></span>

<span data-ttu-id="385bf-104">**WorkingHours**元素表示所请求的邮箱用户的时区设置和工作时间。</span><span class="sxs-lookup"><span data-stu-id="385bf-104">The **WorkingHours** element represents the time zone settings and working hours for the requested mailbox user.</span></span> 
  
[<span data-ttu-id="385bf-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="385bf-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="385bf-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="385bf-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="385bf-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="385bf-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="385bf-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="385bf-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="385bf-109">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="385bf-109">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md)
  
```xml
<WorkingHours>
   <TimeZone>...</TimeZone>
   <WorkingPeriodArray>...</WorkingPeriodArray>
</WorkingHours>
```

 <span data-ttu-id="385bf-110">**WorkingHours**</span><span class="sxs-lookup"><span data-stu-id="385bf-110">**WorkingHours**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="385bf-111">属性和元素</span><span class="sxs-lookup"><span data-stu-id="385bf-111">Attributes and elements</span></span>

<span data-ttu-id="385bf-112">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="385bf-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="385bf-113">Attributes</span><span class="sxs-lookup"><span data-stu-id="385bf-113">Attributes</span></span>

<span data-ttu-id="385bf-114">无。</span><span class="sxs-lookup"><span data-stu-id="385bf-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="385bf-115">子元素</span><span class="sxs-lookup"><span data-stu-id="385bf-115">Child elements</span></span>

|<span data-ttu-id="385bf-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="385bf-116">**Element**</span></span>|<span data-ttu-id="385bf-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="385bf-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="385bf-118">时区（可用性）</span><span class="sxs-lookup"><span data-stu-id="385bf-118">TimeZone (Availability)</span></span>](timezone-availability.md) <br/> |<span data-ttu-id="385bf-119">包含标识时区信息的元素。</span><span class="sxs-lookup"><span data-stu-id="385bf-119">Contains elements that identify time zone information.</span></span> <span data-ttu-id="385bf-120">此元素还包含有关标准时间和夏时制之间转换的信息。</span><span class="sxs-lookup"><span data-stu-id="385bf-120">This element also contains information about the transition between standard time and daylight saving time.</span></span> <span data-ttu-id="385bf-121">如果使用**WorkingHours**元素，则此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="385bf-121">This element is required if the **WorkingHours** element is used.</span></span>  <br/> |
|[<span data-ttu-id="385bf-122">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="385bf-122">WorkingPeriodArray</span></span>](workingperiodarray.md) <br/> |<span data-ttu-id="385bf-123">包含邮箱用户的工作时间段信息。</span><span class="sxs-lookup"><span data-stu-id="385bf-123">Contains working period information for the mailbox user.</span></span> <span data-ttu-id="385bf-124">如果使用**WorkingHours**元素，则此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="385bf-124">This element is required if the **WorkingHours** element is used.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="385bf-125">父元素</span><span class="sxs-lookup"><span data-stu-id="385bf-125">Parent elements</span></span>

|<span data-ttu-id="385bf-126">**元素**</span><span class="sxs-lookup"><span data-stu-id="385bf-126">**Element**</span></span>|<span data-ttu-id="385bf-127">**说明**</span><span class="sxs-lookup"><span data-stu-id="385bf-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="385bf-128">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="385bf-128">FreeBusyView</span></span>](freebusyview.md) <br/> |<span data-ttu-id="385bf-129">包含特定用户的可用性信息。</span><span class="sxs-lookup"><span data-stu-id="385bf-129">Contains availability information for a specific user.</span></span>  <br/> <span data-ttu-id="385bf-130">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="385bf-130">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="385bf-131">备注</span><span class="sxs-lookup"><span data-stu-id="385bf-131">Remarks</span></span>

<span data-ttu-id="385bf-132">所有子元素都按它们出现的顺序列出。</span><span class="sxs-lookup"><span data-stu-id="385bf-132">All the child elements are listed in the sequence in which they occur.</span></span> <span data-ttu-id="385bf-133">此元素提供的详细信息级别取决于授予请求者的权限。</span><span class="sxs-lookup"><span data-stu-id="385bf-133">The level of detail provided by this element depends on the permissions granted to the requestor.</span></span>
  
<span data-ttu-id="385bf-134">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="385bf-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="385bf-135">元素信息</span><span class="sxs-lookup"><span data-stu-id="385bf-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="385bf-136">命名空间</span><span class="sxs-lookup"><span data-stu-id="385bf-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="385bf-137">架构名称</span><span class="sxs-lookup"><span data-stu-id="385bf-137">Schema Name</span></span>  <br/> |<span data-ttu-id="385bf-138">类型架构</span><span class="sxs-lookup"><span data-stu-id="385bf-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="385bf-139">验证文件</span><span class="sxs-lookup"><span data-stu-id="385bf-139">Validation File</span></span>  <br/> |<span data-ttu-id="385bf-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="385bf-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="385bf-141">可以为空</span><span class="sxs-lookup"><span data-stu-id="385bf-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="385bf-142">False</span><span class="sxs-lookup"><span data-stu-id="385bf-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="385bf-143">另请参阅</span><span class="sxs-lookup"><span data-stu-id="385bf-143">See also</span></span>



[<span data-ttu-id="385bf-144">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="385bf-144">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="385bf-145">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="385bf-145">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="385bf-146">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="385bf-146">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

