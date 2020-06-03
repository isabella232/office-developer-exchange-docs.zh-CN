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
description: SuggestionsViewOptions 元素包含用于获取会议建议信息的选项。
ms.openlocfilehash: f584b19997f98760bd4e438dcd48a5c18cc63e4b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44433992"
---
# <a name="suggestionsviewoptions"></a><span data-ttu-id="24d20-103">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="24d20-103">SuggestionsViewOptions</span></span>

<span data-ttu-id="24d20-104">**SuggestionsViewOptions**元素包含用于获取会议建议信息的选项。</span><span class="sxs-lookup"><span data-stu-id="24d20-104">The **SuggestionsViewOptions** element contains the options for obtaining meeting suggestion information.</span></span> 
  
[<span data-ttu-id="24d20-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="24d20-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="24d20-106">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="24d20-106">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md)
  
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

 <span data-ttu-id="24d20-107">**SuggestionsViewOptionsType**</span><span class="sxs-lookup"><span data-stu-id="24d20-107">**SuggestionsViewOptionsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="24d20-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="24d20-108">Attributes and elements</span></span>

<span data-ttu-id="24d20-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="24d20-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="24d20-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="24d20-110">Attributes</span></span>

<span data-ttu-id="24d20-111">无。</span><span class="sxs-lookup"><span data-stu-id="24d20-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="24d20-112">子元素</span><span class="sxs-lookup"><span data-stu-id="24d20-112">Child elements</span></span>

|<span data-ttu-id="24d20-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="24d20-113">**Element**</span></span>|<span data-ttu-id="24d20-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="24d20-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="24d20-115">GoodThreshold</span><span class="sxs-lookup"><span data-stu-id="24d20-115">GoodThreshold</span></span>](goodthreshold.md) <br/> |<span data-ttu-id="24d20-116">指定必须在一段时间内打开时间段的与会者所占的百分比，以限定为合理的建议会议时间。</span><span class="sxs-lookup"><span data-stu-id="24d20-116">Specifies the percentage of attendees that must have the time period open for the time period to qualify as a good suggested meeting time.</span></span>  <br/> |
|[<span data-ttu-id="24d20-117">MaximumResultsByDay</span><span class="sxs-lookup"><span data-stu-id="24d20-117">MaximumResultsByDay</span></span>](maximumresultsbyday.md) <br/> |<span data-ttu-id="24d20-118">指定响应中每日返回的建议会议次数。</span><span class="sxs-lookup"><span data-stu-id="24d20-118">Specifies the number of suggested meeting times per day returned in the response.</span></span>  <br/> |
|[<span data-ttu-id="24d20-119">MaximumNonWorkHourResultsByDay</span><span class="sxs-lookup"><span data-stu-id="24d20-119">MaximumNonWorkHourResultsByDay</span></span>](maximumnonworkhourresultsbyday.md) <br/> |<span data-ttu-id="24d20-120">指定每日常规工作时间之外的会议时间的建议结果数。</span><span class="sxs-lookup"><span data-stu-id="24d20-120">Specifies the number of suggested results for meeting times outside regular working hours per day.</span></span>  <br/> |
|[<span data-ttu-id="24d20-121">MeetingDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="24d20-121">MeetingDurationInMinutes</span></span>](meetingdurationinminutes.md) <br/> |<span data-ttu-id="24d20-122">指定要建议的会议的长度。</span><span class="sxs-lookup"><span data-stu-id="24d20-122">Specifies the length of the meeting to be suggested.</span></span>  <br/> |
|[<span data-ttu-id="24d20-123">MinimumSuggestionQuality</span><span class="sxs-lookup"><span data-stu-id="24d20-123">MinimumSuggestionQuality</span></span>](minimumsuggestionquality.md) <br/> |<span data-ttu-id="24d20-124">指定要在响应中返回的会议建议的质量。</span><span class="sxs-lookup"><span data-stu-id="24d20-124">Specifies the quality of meeting suggestions to be returned in the response.</span></span>  <br/> |
|[<span data-ttu-id="24d20-125">DetailedSuggestionsWindow</span><span class="sxs-lookup"><span data-stu-id="24d20-125">DetailedSuggestionsWindow</span></span>](detailedsuggestionswindow.md) <br/> |<span data-ttu-id="24d20-126">标识查询的时间跨度，以获取有关建议会议时间的详细信息。</span><span class="sxs-lookup"><span data-stu-id="24d20-126">Identifies the time span that is queried for detailed information about suggested meeting times.</span></span>  <br/> |
|[<span data-ttu-id="24d20-127">CurrentMeetingTime</span><span class="sxs-lookup"><span data-stu-id="24d20-127">CurrentMeetingTime</span></span>](currentmeetingtime.md) <br/> |<span data-ttu-id="24d20-128">表示要使用建议的会议时间结果更新的会议的开始时间。</span><span class="sxs-lookup"><span data-stu-id="24d20-128">Represents the start time of a meeting that you want to update with the suggested meeting time results.</span></span>  <br/> |
|[<span data-ttu-id="24d20-129">GlobalObjectId</span><span class="sxs-lookup"><span data-stu-id="24d20-129">GlobalObjectId</span></span>](globalobjectid.md) <br/> |<span data-ttu-id="24d20-130">不使用此元素。</span><span class="sxs-lookup"><span data-stu-id="24d20-130">This element is not used.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="24d20-131">父元素</span><span class="sxs-lookup"><span data-stu-id="24d20-131">Parent elements</span></span>

|<span data-ttu-id="24d20-132">**元素**</span><span class="sxs-lookup"><span data-stu-id="24d20-132">**Element**</span></span>|<span data-ttu-id="24d20-133">**说明**</span><span class="sxs-lookup"><span data-stu-id="24d20-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="24d20-134">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="24d20-134">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md) <br/> |<span data-ttu-id="24d20-135">包含用于获取用户可用性信息的参数。</span><span class="sxs-lookup"><span data-stu-id="24d20-135">Contains the arguments used to obtain user availability information.</span></span> <span data-ttu-id="24d20-136">这是一个根元素。</span><span class="sxs-lookup"><span data-stu-id="24d20-136">This is a root element.</span></span>  <br/> <span data-ttu-id="24d20-137">以下是此元素的 XPath：</span><span class="sxs-lookup"><span data-stu-id="24d20-137">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="24d20-138">备注</span><span class="sxs-lookup"><span data-stu-id="24d20-138">Remarks</span></span>

<span data-ttu-id="24d20-139">此元素不是必需的，并且仅在使用时才会出现一次。</span><span class="sxs-lookup"><span data-stu-id="24d20-139">This element is not required and can only occur once if used.</span></span> <span data-ttu-id="24d20-140">如果[FreeBusyViewOptions](freebusyviewoptions.md)元素的值不为 null，则此值可以为 null。</span><span class="sxs-lookup"><span data-stu-id="24d20-140">This value can be null if the value of the [FreeBusyViewOptions](freebusyviewoptions.md) element is not null.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="24d20-141">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="24d20-141">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="24d20-142">元素信息</span><span class="sxs-lookup"><span data-stu-id="24d20-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="24d20-143">命名空间</span><span class="sxs-lookup"><span data-stu-id="24d20-143">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="24d20-144">架构名称</span><span class="sxs-lookup"><span data-stu-id="24d20-144">Schema Name</span></span>  <br/> |<span data-ttu-id="24d20-145">类型架构</span><span class="sxs-lookup"><span data-stu-id="24d20-145">Types schema</span></span>  <br/> |
|<span data-ttu-id="24d20-146">验证文件</span><span class="sxs-lookup"><span data-stu-id="24d20-146">Validation File</span></span>  <br/> |<span data-ttu-id="24d20-147">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="24d20-147">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="24d20-148">可以为空</span><span class="sxs-lookup"><span data-stu-id="24d20-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="24d20-149">False</span><span class="sxs-lookup"><span data-stu-id="24d20-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="24d20-150">另请参阅</span><span class="sxs-lookup"><span data-stu-id="24d20-150">See also</span></span>



[<span data-ttu-id="24d20-151">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="24d20-151">GetUserAvailability operation</span></span>](getuseravailability-operation.md)


[<span data-ttu-id="24d20-152">获取用户可用性</span><span class="sxs-lookup"><span data-stu-id="24d20-152">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

