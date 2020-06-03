---
title: MergedFreeBusyIntervalInMinutes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MergedFreeBusyIntervalInMinutes
api_type:
- schema
ms.assetid: 481cdbc6-d5aa-49fa-a3fa-9d119d3dca99
description: MergedFreeBusyIntervalInMinutes 元素表示 FreeBusyMerged 视图中两个连续的插槽之间的时间差。
ms.openlocfilehash: 6228ee5b66202634e6bb3b6c1ad6b8897a109d58
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468787"
---
# <a name="mergedfreebusyintervalinminutes"></a><span data-ttu-id="62e64-103">MergedFreeBusyIntervalInMinutes</span><span class="sxs-lookup"><span data-stu-id="62e64-103">MergedFreeBusyIntervalInMinutes</span></span>

<span data-ttu-id="62e64-104">**MergedFreeBusyIntervalInMinutes**元素表示**FreeBusyMerged**视图中两个连续的插槽之间的时间差。</span><span class="sxs-lookup"><span data-stu-id="62e64-104">The **MergedFreeBusyIntervalInMinutes** element represents the time difference between two successive slots in the **FreeBusyMerged** view.</span></span> 
  
[<span data-ttu-id="62e64-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="62e64-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="62e64-106">FreeBusyViewOptions</span><span class="sxs-lookup"><span data-stu-id="62e64-106">FreeBusyViewOptions</span></span>](freebusyviewoptions.md)
  
[<span data-ttu-id="62e64-107">MergedFreeBusyIntervalInMinutes</span><span class="sxs-lookup"><span data-stu-id="62e64-107">MergedFreeBusyIntervalInMinutes</span></span>](mergedfreebusyintervalinminutes.md)
  
```xml
<MergedFreeBusyIntervalInMinutes>...</MergedFreeBusyIntervalInMinutes>
```

 <span data-ttu-id="62e64-108">**int**</span><span class="sxs-lookup"><span data-stu-id="62e64-108">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="62e64-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="62e64-109">Attributes and elements</span></span>

<span data-ttu-id="62e64-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="62e64-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="62e64-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="62e64-111">Attributes</span></span>

<span data-ttu-id="62e64-112">无。</span><span class="sxs-lookup"><span data-stu-id="62e64-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="62e64-113">子元素</span><span class="sxs-lookup"><span data-stu-id="62e64-113">Child elements</span></span>

<span data-ttu-id="62e64-114">无。</span><span class="sxs-lookup"><span data-stu-id="62e64-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="62e64-115">父元素</span><span class="sxs-lookup"><span data-stu-id="62e64-115">Parent elements</span></span>

|<span data-ttu-id="62e64-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="62e64-116">**Element**</span></span>|<span data-ttu-id="62e64-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="62e64-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="62e64-118">FreeBusyViewOptions</span><span class="sxs-lookup"><span data-stu-id="62e64-118">FreeBusyViewOptions</span></span>](freebusyviewoptions.md) <br/> |<span data-ttu-id="62e64-119">指定响应中返回的忙/闲信息的类型。</span><span class="sxs-lookup"><span data-stu-id="62e64-119">Specifies the type of free/busy information returned in the response.</span></span>  <br/> <span data-ttu-id="62e64-120">以下是此元素的 XPath：</span><span class="sxs-lookup"><span data-stu-id="62e64-120">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="62e64-121">文本值</span><span class="sxs-lookup"><span data-stu-id="62e64-121">Text value</span></span>

<span data-ttu-id="62e64-122">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="62e64-122">A text value is required.</span></span> <span data-ttu-id="62e64-123">该文本值表示以分钟为单位的时间。</span><span class="sxs-lookup"><span data-stu-id="62e64-123">The text value represents time in minutes.</span></span> <span data-ttu-id="62e64-124">默认值为 30 分钟。</span><span class="sxs-lookup"><span data-stu-id="62e64-124">The default value is 30 minutes.</span></span> <span data-ttu-id="62e64-125">6分钟是最小时间间隔，一天（1440分钟）是此元素的最大时间间隔。</span><span class="sxs-lookup"><span data-stu-id="62e64-125">Six minutes is the minimum interval and one day (1440 minutes) is the maximum interval for this element.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="62e64-126">备注</span><span class="sxs-lookup"><span data-stu-id="62e64-126">Remarks</span></span>

<span data-ttu-id="62e64-127">仅当[RequestedView](requestedview.md)元素等于**MergedOnly**、 **FreeBusyMerged**或**DetailedMerge**时，才使用此值。</span><span class="sxs-lookup"><span data-stu-id="62e64-127">This value is used only if the [RequestedView](requestedview.md) element is equal to **MergedOnly**, **FreeBusyMerged**, or **DetailedMerge**.</span></span> <span data-ttu-id="62e64-128">这是 integer 数据类型。</span><span class="sxs-lookup"><span data-stu-id="62e64-128">This is an integer data type.</span></span> <span data-ttu-id="62e64-129">包含此元素定义的间隔的流在[MergedFreeBusy](mergedfreebusy.md)元素中返回。</span><span class="sxs-lookup"><span data-stu-id="62e64-129">The stream that contains the intervals defined by this element is returned in the [MergedFreeBusy](mergedfreebusy.md) element.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="62e64-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="62e64-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="62e64-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="62e64-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="62e64-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="62e64-132">Schema Name</span></span>  <br/> |<span data-ttu-id="62e64-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="62e64-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="62e64-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="62e64-134">Validation File</span></span>  <br/> |<span data-ttu-id="62e64-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="62e64-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="62e64-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="62e64-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="62e64-137">False</span><span class="sxs-lookup"><span data-stu-id="62e64-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="62e64-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="62e64-138">See also</span></span>



[<span data-ttu-id="62e64-139">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="62e64-139">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="62e64-140">GetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="62e64-140">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)


[<span data-ttu-id="62e64-141">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="62e64-141">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

