---
title: TimeWindow
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TimeWindow
api_type:
- schema
ms.assetid: 49c79266-353a-4036-a8e2-8a4660d0d8ea
description: TimeWindow 元素标识查询的用户可用性信息的时间跨度。
ms.openlocfilehash: 5c66614520f9d616687d67ad609b3d55d9cf6571
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458927"
---
# <a name="timewindow"></a><span data-ttu-id="320ca-103">TimeWindow</span><span class="sxs-lookup"><span data-stu-id="320ca-103">TimeWindow</span></span>

<span data-ttu-id="320ca-104">**TimeWindow**元素标识查询的用户可用性信息的时间跨度。</span><span class="sxs-lookup"><span data-stu-id="320ca-104">The **TimeWindow** element identifies the time span queried for the user availability information.</span></span> 
  
[<span data-ttu-id="320ca-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="320ca-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="320ca-106">FreeBusyViewOptions</span><span class="sxs-lookup"><span data-stu-id="320ca-106">FreeBusyViewOptions</span></span>](freebusyviewoptions.md)
  
[<span data-ttu-id="320ca-107">TimeWindow</span><span class="sxs-lookup"><span data-stu-id="320ca-107">TimeWindow</span></span>](timewindow.md)
  
```xml
<TimeWindow>
   <StartTime>dateTime</StartTime>
   <EndTime>dateTime</EndTime>
</TimeWindow>
```

 <span data-ttu-id="320ca-108">**Duration**</span><span class="sxs-lookup"><span data-stu-id="320ca-108">**Duration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="320ca-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="320ca-109">Attributes and elements</span></span>

<span data-ttu-id="320ca-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="320ca-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="320ca-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="320ca-111">Attributes</span></span>

<span data-ttu-id="320ca-112">无。</span><span class="sxs-lookup"><span data-stu-id="320ca-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="320ca-113">子元素</span><span class="sxs-lookup"><span data-stu-id="320ca-113">Child elements</span></span>

|<span data-ttu-id="320ca-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="320ca-114">**Element**</span></span>|<span data-ttu-id="320ca-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="320ca-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="320ca-116">StartTime</span><span class="sxs-lookup"><span data-stu-id="320ca-116">StartTime</span></span>](starttime.md) <br/> |<span data-ttu-id="320ca-117">表示为用户可用性信息查询的时间范围的开始时间。</span><span class="sxs-lookup"><span data-stu-id="320ca-117">Represents the start of a time span queried for the user availability information.</span></span>  <br/> |
|[<span data-ttu-id="320ca-118">EndTime</span><span class="sxs-lookup"><span data-stu-id="320ca-118">EndTime</span></span>](endtime.md) <br/> |<span data-ttu-id="320ca-119">表示为用户可用性信息查询的时间范围的结束时间。</span><span class="sxs-lookup"><span data-stu-id="320ca-119">Represents the end of a time span queried for the user availability information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="320ca-120">父元素</span><span class="sxs-lookup"><span data-stu-id="320ca-120">Parent elements</span></span>

|<span data-ttu-id="320ca-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="320ca-121">**Element**</span></span>|<span data-ttu-id="320ca-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="320ca-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="320ca-123">FreeBusyViewOptions</span><span class="sxs-lookup"><span data-stu-id="320ca-123">FreeBusyViewOptions</span></span>](freebusyviewoptions.md) <br/> |<span data-ttu-id="320ca-124">指定响应中返回的忙/闲信息的类型。</span><span class="sxs-lookup"><span data-stu-id="320ca-124">Specifies the type of free/busy information returned in the response.</span></span>  <br/> <span data-ttu-id="320ca-125">以下是此元素的 XPath：</span><span class="sxs-lookup"><span data-stu-id="320ca-125">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="320ca-126">备注</span><span class="sxs-lookup"><span data-stu-id="320ca-126">Remarks</span></span>

<span data-ttu-id="320ca-127">此时间段的最大值为42天。</span><span class="sxs-lookup"><span data-stu-id="320ca-127">The maximum value for this time period is 42 days.</span></span> <span data-ttu-id="320ca-128">可以修改此最大值。</span><span class="sxs-lookup"><span data-stu-id="320ca-128">This maximum value can be modified.</span></span> <span data-ttu-id="320ca-129">任何超出最大值的用户可用性信息请求都将返回错误。</span><span class="sxs-lookup"><span data-stu-id="320ca-129">Any requests for user availability information beyond the maximum value will return an error.</span></span> <span data-ttu-id="320ca-130">如果任何约会在[StartTime](starttime.md)和[EndTime](endtime.md)元素定义的时间范围内部分存在，则该约会将全部包含在内。</span><span class="sxs-lookup"><span data-stu-id="320ca-130">If any appointments are partially in the time span defined by the [StartTime](starttime.md) and [EndTime](endtime.md) elements, that appointment is included in its entirety.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="320ca-131">描述此元素的架构位于运行 Microsoft® Exchange Server 2007 且安装了客户端访问服务器角色的计算机的/EWS/目录中。</span><span class="sxs-lookup"><span data-stu-id="320ca-131">The schema that describes this element is located in the /EWS/ directory of the computer that is running Microsoft® Exchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="320ca-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="320ca-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="320ca-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="320ca-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="320ca-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="320ca-134">Schema Name</span></span>  <br/> |<span data-ttu-id="320ca-135">类型架构</span><span class="sxs-lookup"><span data-stu-id="320ca-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="320ca-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="320ca-136">Validation File</span></span>  <br/> |<span data-ttu-id="320ca-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="320ca-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="320ca-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="320ca-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="320ca-139">False</span><span class="sxs-lookup"><span data-stu-id="320ca-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="320ca-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="320ca-140">See also</span></span>



[<span data-ttu-id="320ca-141">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="320ca-141">GetUserAvailability operation</span></span>](getuseravailability-operation.md)


[<span data-ttu-id="320ca-142">获取用户可用性</span><span class="sxs-lookup"><span data-stu-id="320ca-142">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

