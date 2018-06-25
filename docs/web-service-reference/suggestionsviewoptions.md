---
title: SuggestionsViewOptions
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SuggestionsViewOptions
api_type:
- schema
ms.assetid: bb04ae38-e62d-4a69-a479-8ff326ca726e
description: SuggestionsViewOptions 元素包含选项的获取会议建议信息。
ms.openlocfilehash: 09ff317ae0b2ebf1eadc89dc3bb1cf5b3ae19dcb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838163"
---
# <a name="suggestionsviewoptions"></a><span data-ttu-id="443ce-103">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="443ce-103">SuggestionsViewOptions</span></span>

<span data-ttu-id="443ce-104">**SuggestionsViewOptions**元素包含选项的获取会议建议信息。</span><span class="sxs-lookup"><span data-stu-id="443ce-104">The **SuggestionsViewOptions** element contains the options for obtaining meeting suggestion information.</span></span> 
  
[<span data-ttu-id="443ce-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="443ce-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="443ce-106">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="443ce-106">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md)
  
```xml
<SuggestionsViewOptions>
   <GoodThreshold>...</GoodThreshold>
   <MaximumResultsByDay>...</MaximumResultsByDay>
   <MaximumNonWorkingHourResultsByDay>...</MaximumNonWorkingHourResultsByDay>
   <MeetingDurationInMinutes>...</MeetingDurationInMinutes>
   <MinimumSuggestionQuality>...</MinimumSuggestionQuality>
   <SuggestionIntervalInMinutes>...</SuggestionIntervalInMinutes>
   <DetailedSuggestionsWindow>...</DetailedSuggestionsWindow>
   <CurrentMeetingTime>...</CurrentMeetingTime>
   <GlobalObjectId>...</GlobalObjectId>
</SuggestionsViewOptions>
```

 <span data-ttu-id="443ce-107">**SuggestionsViewOptionsType**</span><span class="sxs-lookup"><span data-stu-id="443ce-107">**SuggestionsViewOptionsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="443ce-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="443ce-108">Attributes and elements</span></span>

<span data-ttu-id="443ce-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="443ce-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="443ce-110">属性</span><span class="sxs-lookup"><span data-stu-id="443ce-110">Attributes</span></span>

<span data-ttu-id="443ce-111">无。</span><span class="sxs-lookup"><span data-stu-id="443ce-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="443ce-112">子元素</span><span class="sxs-lookup"><span data-stu-id="443ce-112">Child elements</span></span>

|<span data-ttu-id="443ce-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="443ce-113">**Element**</span></span>|<span data-ttu-id="443ce-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="443ce-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="443ce-115">GoodThreshold</span><span class="sxs-lookup"><span data-stu-id="443ce-115">GoodThreshold</span></span>](goodthreshold.md) <br/> |<span data-ttu-id="443ce-116">指定必须打开若要成为合格的良好建议的会议时间的时间段的时间段的与会者的百分比。</span><span class="sxs-lookup"><span data-stu-id="443ce-116">Specifies the percentage of attendees that must have the time period open for the time period to qualify as a good suggested meeting time.</span></span>  <br/> |
|[<span data-ttu-id="443ce-117">MaximumResultsByDay</span><span class="sxs-lookup"><span data-stu-id="443ce-117">MaximumResultsByDay</span></span>](maximumresultsbyday.md) <br/> |<span data-ttu-id="443ce-118">指定的每日响应中返回的建议的会议次数。</span><span class="sxs-lookup"><span data-stu-id="443ce-118">Specifies the number of suggested meeting times per day returned in the response.</span></span>  <br/> |
|[<span data-ttu-id="443ce-119">MaximumNonWorkHourResultsByDay</span><span class="sxs-lookup"><span data-stu-id="443ce-119">MaximumNonWorkHourResultsByDay</span></span>](maximumnonworkhourresultsbyday.md) <br/> |<span data-ttu-id="443ce-120">指定建议的会议时间每天的正常工作时间以外的结果数。</span><span class="sxs-lookup"><span data-stu-id="443ce-120">Specifies the number of suggested results for meeting times outside regular working hours per day.</span></span>  <br/> |
|[<span data-ttu-id="443ce-121">MeetingDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="443ce-121">MeetingDurationInMinutes</span></span>](meetingdurationinminutes.md) <br/> |<span data-ttu-id="443ce-122">指定建议会议的时间长度。</span><span class="sxs-lookup"><span data-stu-id="443ce-122">Specifies the length of the meeting to be suggested.</span></span>  <br/> |
|[<span data-ttu-id="443ce-123">MinimumSuggestionQuality</span><span class="sxs-lookup"><span data-stu-id="443ce-123">MinimumSuggestionQuality</span></span>](minimumsuggestionquality.md) <br/> |<span data-ttu-id="443ce-124">指定会议建议的响应中返回的质量。</span><span class="sxs-lookup"><span data-stu-id="443ce-124">Specifies the quality of meeting suggestions to be returned in the response.</span></span>  <br/> |
|[<span data-ttu-id="443ce-125">DetailedSuggestionsWindow</span><span class="sxs-lookup"><span data-stu-id="443ce-125">DetailedSuggestionsWindow</span></span>](detailedsuggestionswindow.md) <br/> |<span data-ttu-id="443ce-126">标识查询建议的会议时间有关的详细信息的时间跨度。</span><span class="sxs-lookup"><span data-stu-id="443ce-126">Identifies the time span that is queried for detailed information about suggested meeting times.</span></span>  <br/> |
|[<span data-ttu-id="443ce-127">CurrentMeetingTime</span><span class="sxs-lookup"><span data-stu-id="443ce-127">CurrentMeetingTime</span></span>](currentmeetingtime.md) <br/> |<span data-ttu-id="443ce-128">代表要更新与建议会议的会议的开始时间的时间结果。</span><span class="sxs-lookup"><span data-stu-id="443ce-128">Represents the start time of a meeting that you want to update with the suggested meeting time results.</span></span>  <br/> |
|[<span data-ttu-id="443ce-129">GlobalObjectId</span><span class="sxs-lookup"><span data-stu-id="443ce-129">GlobalObjectId</span></span>](globalobjectid.md) <br/> |<span data-ttu-id="443ce-130">不使用此元素。</span><span class="sxs-lookup"><span data-stu-id="443ce-130">This element is not used.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="443ce-131">父元素</span><span class="sxs-lookup"><span data-stu-id="443ce-131">Parent elements</span></span>

|<span data-ttu-id="443ce-132">**元素**</span><span class="sxs-lookup"><span data-stu-id="443ce-132">**Element**</span></span>|<span data-ttu-id="443ce-133">**说明**</span><span class="sxs-lookup"><span data-stu-id="443ce-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="443ce-134">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="443ce-134">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md) <br/> |<span data-ttu-id="443ce-135">包含用于获取用户的可用性信息的参数。</span><span class="sxs-lookup"><span data-stu-id="443ce-135">Contains the arguments used to obtain user availability information.</span></span> <span data-ttu-id="443ce-136">这是根元素。</span><span class="sxs-lookup"><span data-stu-id="443ce-136">This is a root element.</span></span>  <br/> <span data-ttu-id="443ce-137">以下是此元素的 XPath:</span><span class="sxs-lookup"><span data-stu-id="443ce-137">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="443ce-138">注解</span><span class="sxs-lookup"><span data-stu-id="443ce-138">Remarks</span></span>

<span data-ttu-id="443ce-139">此元素不需要，并且如果使用可以只发生一次。</span><span class="sxs-lookup"><span data-stu-id="443ce-139">This element is not required and can only occur once if used.</span></span> <span data-ttu-id="443ce-140">如果[FreeBusyViewOptions](freebusyviewoptions.md)元素的值不为 null，则此值可以是 null。</span><span class="sxs-lookup"><span data-stu-id="443ce-140">This value can be null if the value of the [FreeBusyViewOptions](freebusyviewoptions.md) element is not null.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="443ce-141">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="443ce-141">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="443ce-142">元素信息</span><span class="sxs-lookup"><span data-stu-id="443ce-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="443ce-143">命名空间</span><span class="sxs-lookup"><span data-stu-id="443ce-143">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="443ce-144">架构名称</span><span class="sxs-lookup"><span data-stu-id="443ce-144">Schema Name</span></span>  <br/> |<span data-ttu-id="443ce-145">类型架构</span><span class="sxs-lookup"><span data-stu-id="443ce-145">Types schema</span></span>  <br/> |
|<span data-ttu-id="443ce-146">验证文件</span><span class="sxs-lookup"><span data-stu-id="443ce-146">Validation File</span></span>  <br/> |<span data-ttu-id="443ce-147">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="443ce-147">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="443ce-148">可以为空</span><span class="sxs-lookup"><span data-stu-id="443ce-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="443ce-149">False</span><span class="sxs-lookup"><span data-stu-id="443ce-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="443ce-150">另请参阅</span><span class="sxs-lookup"><span data-stu-id="443ce-150">See also</span></span>



[<span data-ttu-id="443ce-151">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="443ce-151">GetUserAvailability operation</span></span>](getuseravailability-operation.md)


[<span data-ttu-id="443ce-152">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="443ce-152">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

