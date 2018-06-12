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
description: MergedFreeBusyIntervalInMinutes 元素均表示 FreeBusyMerged 视图中的两个连续插槽之间的时间差异。
ms.openlocfilehash: 99c8c69424a0a9d9594005fdf6b2ceba53e6288a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826451"
---
# <a name="mergedfreebusyintervalinminutes"></a><span data-ttu-id="ef638-103">MergedFreeBusyIntervalInMinutes</span><span class="sxs-lookup"><span data-stu-id="ef638-103">MergedFreeBusyIntervalInMinutes</span></span>

<span data-ttu-id="ef638-104">**MergedFreeBusyIntervalInMinutes**元素均表示**FreeBusyMerged**视图中的两个连续插槽之间的时间差异。</span><span class="sxs-lookup"><span data-stu-id="ef638-104">The **MergedFreeBusyIntervalInMinutes** element represents the time difference between two successive slots in the **FreeBusyMerged** view.</span></span> 
  
[<span data-ttu-id="ef638-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="ef638-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="ef638-106">FreeBusyViewOptions</span><span class="sxs-lookup"><span data-stu-id="ef638-106">FreeBusyViewOptions</span></span>](freebusyviewoptions.md)
  
[<span data-ttu-id="ef638-107">MergedFreeBusyIntervalInMinutes</span><span class="sxs-lookup"><span data-stu-id="ef638-107">MergedFreeBusyIntervalInMinutes</span></span>](mergedfreebusyintervalinminutes.md)
  
```xml
<MergedFreeBusyIntervalInMinutes>...</MergedFreeBusyIntervalInMinutes>
```

 <span data-ttu-id="ef638-108">**int**</span><span class="sxs-lookup"><span data-stu-id="ef638-108">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ef638-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ef638-109">Attributes and elements</span></span>

<span data-ttu-id="ef638-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ef638-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ef638-111">属性</span><span class="sxs-lookup"><span data-stu-id="ef638-111">Attributes</span></span>

<span data-ttu-id="ef638-112">无。</span><span class="sxs-lookup"><span data-stu-id="ef638-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ef638-113">子元素</span><span class="sxs-lookup"><span data-stu-id="ef638-113">Child elements</span></span>

<span data-ttu-id="ef638-114">无。</span><span class="sxs-lookup"><span data-stu-id="ef638-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ef638-115">父元素</span><span class="sxs-lookup"><span data-stu-id="ef638-115">Parent elements</span></span>

|<span data-ttu-id="ef638-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="ef638-116">**Element**</span></span>|<span data-ttu-id="ef638-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="ef638-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ef638-118">FreeBusyViewOptions</span><span class="sxs-lookup"><span data-stu-id="ef638-118">FreeBusyViewOptions</span></span>](freebusyviewoptions.md) <br/> |<span data-ttu-id="ef638-119">指定响应中返回的忙/闲信息的类型。</span><span class="sxs-lookup"><span data-stu-id="ef638-119">Specifies the type of free/busy information returned in the response.</span></span>  <br/> <span data-ttu-id="ef638-120">以下是此元素的 XPath:</span><span class="sxs-lookup"><span data-stu-id="ef638-120">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ef638-121">文本值</span><span class="sxs-lookup"><span data-stu-id="ef638-121">Text value</span></span>

<span data-ttu-id="ef638-122">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="ef638-122">A text value is required.</span></span> <span data-ttu-id="ef638-123">文本值表示以分钟为单位的时间。</span><span class="sxs-lookup"><span data-stu-id="ef638-123">The text value represents time in minutes.</span></span> <span data-ttu-id="ef638-124">默认值为 30 分钟。</span><span class="sxs-lookup"><span data-stu-id="ef638-124">The default value is 30 minutes.</span></span> <span data-ttu-id="ef638-125">六个分钟是最小间隔，一天 （1440 分钟） 是此元素的最大时间间隔。</span><span class="sxs-lookup"><span data-stu-id="ef638-125">Six minutes is the minimum interval and one day (1440 minutes) is the maximum interval for this element.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ef638-126">备注</span><span class="sxs-lookup"><span data-stu-id="ef638-126">Remarks</span></span>

<span data-ttu-id="ef638-127">[RequestedView](requestedview.md)元素等于**MergedOnly**、 **FreeBusyMerged**或**DetailedMerge**时，才使用此值。</span><span class="sxs-lookup"><span data-stu-id="ef638-127">This value is used only if the [RequestedView](requestedview.md) element is equal to **MergedOnly**, **FreeBusyMerged**, or **DetailedMerge**.</span></span> <span data-ttu-id="ef638-128">这是 integer 数据类型。</span><span class="sxs-lookup"><span data-stu-id="ef638-128">This is an integer data type.</span></span> <span data-ttu-id="ef638-129">包含此元素的定义的时间间隔的流[MergedFreeBusy](mergedfreebusy.md)元素中返回。</span><span class="sxs-lookup"><span data-stu-id="ef638-129">The stream that contains the intervals defined by this element is returned in the [MergedFreeBusy](mergedfreebusy.md) element.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="ef638-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="ef638-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ef638-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="ef638-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ef638-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="ef638-132">Schema Name</span></span>  <br/> |<span data-ttu-id="ef638-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="ef638-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="ef638-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="ef638-134">Validation File</span></span>  <br/> |<span data-ttu-id="ef638-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ef638-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ef638-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="ef638-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="ef638-137">False</span><span class="sxs-lookup"><span data-stu-id="ef638-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ef638-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ef638-138">See also</span></span>



[<span data-ttu-id="ef638-139">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="ef638-139">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="ef638-140">GetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="ef638-140">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)


[<span data-ttu-id="ef638-141">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="ef638-141">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

