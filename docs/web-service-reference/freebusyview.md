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
ms.openlocfilehash: e5cc3bea6b57d5c400dd9be44bf9f9aaf9e43eb9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456099"
---
# <a name="freebusyview"></a><span data-ttu-id="7e4bc-103">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="7e4bc-103">FreeBusyView</span></span>

<span data-ttu-id="7e4bc-104">**FreeBusyView**元素包含特定用户的可用性信息。</span><span class="sxs-lookup"><span data-stu-id="7e4bc-104">The **FreeBusyView** element contains availability information for a specific user.</span></span> 
  
[<span data-ttu-id="7e4bc-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="7e4bc-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="7e4bc-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="7e4bc-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="7e4bc-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="7e4bc-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="7e4bc-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="7e4bc-108">FreeBusyView</span></span>](freebusyview.md)
  
```xml
<FreeBusyView>
   <FreeBusyViewType>...</FreeBusyViewType>
   <MergedFreeBusy>...</MergedFreeBusy>
   <CalendarEventArray>...</CalendarEventArray>
   <WorkingHours>...</WorkingHours>
</FreeBusyView>
```

 <span data-ttu-id="7e4bc-109">**FreeBusyView**</span><span class="sxs-lookup"><span data-stu-id="7e4bc-109">**FreeBusyView**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7e4bc-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7e4bc-110">Attributes and elements</span></span>

<span data-ttu-id="7e4bc-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7e4bc-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7e4bc-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="7e4bc-112">Attributes</span></span>

<span data-ttu-id="7e4bc-113">无。</span><span class="sxs-lookup"><span data-stu-id="7e4bc-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7e4bc-114">子元素</span><span class="sxs-lookup"><span data-stu-id="7e4bc-114">Child elements</span></span>

|<span data-ttu-id="7e4bc-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="7e4bc-115">**Element**</span></span>|<span data-ttu-id="7e4bc-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="7e4bc-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7e4bc-117">FreeBusyViewType</span><span class="sxs-lookup"><span data-stu-id="7e4bc-117">FreeBusyViewType</span></span>](freebusyviewtype.md) <br/> |<span data-ttu-id="7e4bc-118">表示响应中返回的请求的忙/闲信息的类型。</span><span class="sxs-lookup"><span data-stu-id="7e4bc-118">Represents the type of requested free/busy information returned in the response.</span></span>  <br/> |
|[<span data-ttu-id="7e4bc-119">MergedFreeBusy</span><span class="sxs-lookup"><span data-stu-id="7e4bc-119">MergedFreeBusy</span></span>](mergedfreebusy.md) <br/> |<span data-ttu-id="7e4bc-120">包含合并的忙/闲数据流。</span><span class="sxs-lookup"><span data-stu-id="7e4bc-120">Contains the merged free/busy stream of data.</span></span>  <br/> |
|[<span data-ttu-id="7e4bc-121">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="7e4bc-121">CalendarEventArray</span></span>](calendareventarray.md) <br/> |<span data-ttu-id="7e4bc-122">包含一组代表所请求用户的可用性的唯一的日历项目匹配项。</span><span class="sxs-lookup"><span data-stu-id="7e4bc-122">Contains a set of unique calendar item occurrences that represent the requested user's availability.</span></span>  <br/> |
|[<span data-ttu-id="7e4bc-123">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="7e4bc-123">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md) <br/> |<span data-ttu-id="7e4bc-124">表示所请求的邮箱用户的时区设置和工作时间。</span><span class="sxs-lookup"><span data-stu-id="7e4bc-124">Represents the time zone settings and working hours for the requested mailbox user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7e4bc-125">父元素</span><span class="sxs-lookup"><span data-stu-id="7e4bc-125">Parent elements</span></span>

|<span data-ttu-id="7e4bc-126">**元素**</span><span class="sxs-lookup"><span data-stu-id="7e4bc-126">**Element**</span></span>|<span data-ttu-id="7e4bc-127">**说明**</span><span class="sxs-lookup"><span data-stu-id="7e4bc-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7e4bc-128">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="7e4bc-128">FreeBusyResponse</span></span>](freebusyresponse.md) <br/> |<span data-ttu-id="7e4bc-129">包含单个邮箱用户的忙/闲信息。</span><span class="sxs-lookup"><span data-stu-id="7e4bc-129">Contains the free/busy information for a single mailbox user.</span></span>  <br/> <span data-ttu-id="7e4bc-130">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="7e4bc-130">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7e4bc-131">备注</span><span class="sxs-lookup"><span data-stu-id="7e4bc-131">Remarks</span></span>

<span data-ttu-id="7e4bc-132">所有子元素都按它们出现的顺序列出。</span><span class="sxs-lookup"><span data-stu-id="7e4bc-132">All the child elements are listed in the sequence in which they occur.</span></span> <span data-ttu-id="7e4bc-133">此元素提供的详细信息级别取决于授予请求者的权限。</span><span class="sxs-lookup"><span data-stu-id="7e4bc-133">The level of detail provided by this element depends on the permissions granted to the requestor.</span></span>
  
<span data-ttu-id="7e4bc-134">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7e4bc-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7e4bc-135">元素信息</span><span class="sxs-lookup"><span data-stu-id="7e4bc-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7e4bc-136">命名空间</span><span class="sxs-lookup"><span data-stu-id="7e4bc-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7e4bc-137">架构名称</span><span class="sxs-lookup"><span data-stu-id="7e4bc-137">Schema Name</span></span>  <br/> |<span data-ttu-id="7e4bc-138">类型架构</span><span class="sxs-lookup"><span data-stu-id="7e4bc-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="7e4bc-139">验证文件</span><span class="sxs-lookup"><span data-stu-id="7e4bc-139">Validation File</span></span>  <br/> |<span data-ttu-id="7e4bc-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7e4bc-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7e4bc-141">可以为空</span><span class="sxs-lookup"><span data-stu-id="7e4bc-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="7e4bc-142">False</span><span class="sxs-lookup"><span data-stu-id="7e4bc-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7e4bc-143">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7e4bc-143">See also</span></span>



[<span data-ttu-id="7e4bc-144">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="7e4bc-144">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="7e4bc-145">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="7e4bc-145">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="7e4bc-146">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="7e4bc-146">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

