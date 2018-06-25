---
title: FreeBusyView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FreeBusyView
api_type:
- schema
ms.assetid: cb18434f-5f41-4e05-a5ce-d921b2721a8c
description: FreeBusyView 元素包含特定用户的可用性信息。
ms.openlocfilehash: d0d603f18642a94e841a1a6bb8e8849aa6b5b273
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754428"
---
# <a name="freebusyview"></a><span data-ttu-id="45e34-103">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="45e34-103">FreeBusyView</span></span>

<span data-ttu-id="45e34-104">**FreeBusyView**元素包含特定用户的可用性信息。</span><span class="sxs-lookup"><span data-stu-id="45e34-104">The **FreeBusyView** element contains availability information for a specific user.</span></span> 
  
[<span data-ttu-id="45e34-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="45e34-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="45e34-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="45e34-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="45e34-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="45e34-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="45e34-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="45e34-108">FreeBusyView</span></span>](freebusyview.md)
  
```xml
<FreeBusyView>
   <FreeBusyViewType>...</FreeBusyViewType>
   <MergedFreeBusy>...</MergedFreeBusy>
   <CalendarEventArray>...</CalendarEventArray>
   <WorkingHours>...</WorkingHours>
</FreeBusyView>
```

 <span data-ttu-id="45e34-109">**FreeBusyView**</span><span class="sxs-lookup"><span data-stu-id="45e34-109">**FreeBusyView**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="45e34-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="45e34-110">Attributes and elements</span></span>

<span data-ttu-id="45e34-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="45e34-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="45e34-112">属性</span><span class="sxs-lookup"><span data-stu-id="45e34-112">Attributes</span></span>

<span data-ttu-id="45e34-113">无。</span><span class="sxs-lookup"><span data-stu-id="45e34-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="45e34-114">子元素</span><span class="sxs-lookup"><span data-stu-id="45e34-114">Child elements</span></span>

|<span data-ttu-id="45e34-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="45e34-115">**Element**</span></span>|<span data-ttu-id="45e34-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="45e34-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="45e34-117">FreeBusyViewType</span><span class="sxs-lookup"><span data-stu-id="45e34-117">FreeBusyViewType</span></span>](freebusyviewtype.md) <br/> |<span data-ttu-id="45e34-118">表示请求响应中返回的忙/闲信息的类型。</span><span class="sxs-lookup"><span data-stu-id="45e34-118">Represents the type of requested free/busy information returned in the response.</span></span>  <br/> |
|[<span data-ttu-id="45e34-119">MergedFreeBusy</span><span class="sxs-lookup"><span data-stu-id="45e34-119">MergedFreeBusy</span></span>](mergedfreebusy.md) <br/> |<span data-ttu-id="45e34-120">包含合并的忙/闲数据流。</span><span class="sxs-lookup"><span data-stu-id="45e34-120">Contains the merged free/busy stream of data.</span></span>  <br/> |
|[<span data-ttu-id="45e34-121">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="45e34-121">CalendarEventArray</span></span>](calendareventarray.md) <br/> |<span data-ttu-id="45e34-122">包含一组唯一的日历项目事件表示所请求的用户的可用性。</span><span class="sxs-lookup"><span data-stu-id="45e34-122">Contains a set of unique calendar item occurrences that represent the requested user's availability.</span></span>  <br/> |
|[<span data-ttu-id="45e34-123">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="45e34-123">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md) <br/> |<span data-ttu-id="45e34-124">表示所在的时区设置和请求的邮箱用户的工作时间。</span><span class="sxs-lookup"><span data-stu-id="45e34-124">Represents the time zone settings and working hours for the requested mailbox user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="45e34-125">父元素</span><span class="sxs-lookup"><span data-stu-id="45e34-125">Parent elements</span></span>

|<span data-ttu-id="45e34-126">**元素**</span><span class="sxs-lookup"><span data-stu-id="45e34-126">**Element**</span></span>|<span data-ttu-id="45e34-127">**说明**</span><span class="sxs-lookup"><span data-stu-id="45e34-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="45e34-128">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="45e34-128">FreeBusyResponse</span></span>](freebusyresponse.md) <br/> |<span data-ttu-id="45e34-129">包含单个邮箱用户的忙/闲信息。</span><span class="sxs-lookup"><span data-stu-id="45e34-129">Contains the free/busy information for a single mailbox user.</span></span>  <br/> <span data-ttu-id="45e34-130">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="45e34-130">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="45e34-131">注解</span><span class="sxs-lookup"><span data-stu-id="45e34-131">Remarks</span></span>

<span data-ttu-id="45e34-132">中发生的顺序排列的所有子元素。</span><span class="sxs-lookup"><span data-stu-id="45e34-132">All the child elements are listed in the sequence in which they occur.</span></span> <span data-ttu-id="45e34-133">提供此元素的详细程度取决于所请求者授予的权限。</span><span class="sxs-lookup"><span data-stu-id="45e34-133">The level of detail provided by this element depends on the permissions granted to the requestor.</span></span>
  
<span data-ttu-id="45e34-134">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="45e34-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="45e34-135">元素信息</span><span class="sxs-lookup"><span data-stu-id="45e34-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="45e34-136">命名空间</span><span class="sxs-lookup"><span data-stu-id="45e34-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="45e34-137">架构名称</span><span class="sxs-lookup"><span data-stu-id="45e34-137">Schema Name</span></span>  <br/> |<span data-ttu-id="45e34-138">类型架构</span><span class="sxs-lookup"><span data-stu-id="45e34-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="45e34-139">验证文件</span><span class="sxs-lookup"><span data-stu-id="45e34-139">Validation File</span></span>  <br/> |<span data-ttu-id="45e34-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="45e34-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="45e34-141">可以为空</span><span class="sxs-lookup"><span data-stu-id="45e34-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="45e34-142">False</span><span class="sxs-lookup"><span data-stu-id="45e34-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="45e34-143">另请参阅</span><span class="sxs-lookup"><span data-stu-id="45e34-143">See also</span></span>



[<span data-ttu-id="45e34-144">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="45e34-144">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="45e34-145">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="45e34-145">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="45e34-146">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="45e34-146">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

