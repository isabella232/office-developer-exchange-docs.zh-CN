---
title: CalendarView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarView
api_type:
- schema
ms.assetid: a4a953b8-0710-416c-95ef-59e51eba9982
description: CalendarView 元素将 FindItem 操作定义为返回日历中显示的日历项目。
ms.openlocfilehash: e547a4b2db5c09ebefd9a072da6cc4733818002e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462260"
---
# <a name="calendarview"></a><span data-ttu-id="0a142-103">CalendarView</span><span class="sxs-lookup"><span data-stu-id="0a142-103">CalendarView</span></span>

<span data-ttu-id="0a142-104">**CalendarView**元素将[FindItem 操作](finditem-operation.md)定义为返回日历中显示的日历项目。</span><span class="sxs-lookup"><span data-stu-id="0a142-104">The **CalendarView** element defines a [FindItem operation](finditem-operation.md) as returning calendar items in a set as they appear in a calendar.</span></span> 
  
[<span data-ttu-id="0a142-105">FindItem</span><span class="sxs-lookup"><span data-stu-id="0a142-105">FindItem</span></span>](finditem.md)
  
[<span data-ttu-id="0a142-106">CalendarView</span><span class="sxs-lookup"><span data-stu-id="0a142-106">CalendarView</span></span>](calendarview.md)
  
```XML
<CalendarView MaxEntriesReturned="" StartDate="" EndDate="" />
```

<span data-ttu-id="0a142-107">**CalendarView**</span><span class="sxs-lookup"><span data-stu-id="0a142-107">**CalendarView**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="0a142-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0a142-108">Attributes and elements</span></span>

<span data-ttu-id="0a142-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0a142-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0a142-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="0a142-110">Attributes</span></span>

|<span data-ttu-id="0a142-111">**属性**</span><span class="sxs-lookup"><span data-stu-id="0a142-111">**Attribute**</span></span>|<span data-ttu-id="0a142-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="0a142-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0a142-113">**MaxEntriesReturned**</span><span class="sxs-lookup"><span data-stu-id="0a142-113">**MaxEntriesReturned**</span></span> <br/> |<span data-ttu-id="0a142-114">描述在 FindItem 响应中返回的最大结果数。</span><span class="sxs-lookup"><span data-stu-id="0a142-114">Describes the maximum number of results to return in the FindItem response.</span></span>  <br/> |
|<span data-ttu-id="0a142-115">**StartDate**</span><span class="sxs-lookup"><span data-stu-id="0a142-115">**StartDate**</span></span> <br/> |<span data-ttu-id="0a142-116">标识为日历项目查询的时间范围的开始时间。</span><span class="sxs-lookup"><span data-stu-id="0a142-116">Identifies the start of a time span queried for calendar items.</span></span> <span data-ttu-id="0a142-117">将不返回开始**日期**前结束时间的所有日历项目。</span><span class="sxs-lookup"><span data-stu-id="0a142-117">All calendar items that have an end time that is before **StartDate** will not be returned.</span></span> <span data-ttu-id="0a142-118">开始**日期**值可以指定为协调世界时（UTC）格式，如 2006-01-02T12：00：00Z，或以指定本地时间和时区偏移量的格式（如 2006-01-02T04：00：00：00：00：00：00：00：00：00：00）。</span><span class="sxs-lookup"><span data-stu-id="0a142-118">The value of **StartDate** can be specified in coordinated universal time (UTC) format, as in 2006-01-02T12:00:00Z, or in a format where local time and time zone offset is specified, as in 2006-01-02T04:00:00-08:00.</span></span>  <br/><br/><span data-ttu-id="0a142-119">此特性是必需的。</span><span class="sxs-lookup"><span data-stu-id="0a142-119">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="0a142-120">**EndDate**</span><span class="sxs-lookup"><span data-stu-id="0a142-120">**EndDate**</span></span> <br/> |<span data-ttu-id="0a142-121">标识为日历项目查询的时间范围的结束时间。</span><span class="sxs-lookup"><span data-stu-id="0a142-121">Identifies the end of a time span queried for calendar items.</span></span> <span data-ttu-id="0a142-122">将不返回开始时间或**结束时间结束**的所有日历项目。</span><span class="sxs-lookup"><span data-stu-id="0a142-122">All calendar items that have a start time that is on or after **EndDate** will not be returned.</span></span> <span data-ttu-id="0a142-123">**结束**日期的值可以指定为 UTC 格式，如 2006-02-02T12：00：00Z，或以指定本地时间和时区偏移量的格式（如 2006-02-02T04：00： 00-08：00中所示）。</span><span class="sxs-lookup"><span data-stu-id="0a142-123">The value of **EndDate** can be specified in UTC format, as in 2006-02-02T12:00:00Z, or in a format where local time and time zone offset is specified, as in 2006-02-02T04:00:00-08:00.</span></span>  <br/><br/><span data-ttu-id="0a142-124">**结束**日期必须大于或等于开始**日期**;否则，将返回错误。</span><span class="sxs-lookup"><span data-stu-id="0a142-124">**EndDate** must be greater than or equal to **StartDate**; otherwise an error is returned.</span></span> <span data-ttu-id="0a142-125">此特性是必需的。</span><span class="sxs-lookup"><span data-stu-id="0a142-125">This attribute is required.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0a142-126">子元素</span><span class="sxs-lookup"><span data-stu-id="0a142-126">Child elements</span></span>

<span data-ttu-id="0a142-127">无。</span><span class="sxs-lookup"><span data-stu-id="0a142-127">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0a142-128">父元素</span><span class="sxs-lookup"><span data-stu-id="0a142-128">Parent elements</span></span>

|<span data-ttu-id="0a142-129">**元素**</span><span class="sxs-lookup"><span data-stu-id="0a142-129">**Element**</span></span>|<span data-ttu-id="0a142-130">**说明**</span><span class="sxs-lookup"><span data-stu-id="0a142-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0a142-131">FindItem</span><span class="sxs-lookup"><span data-stu-id="0a142-131">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="0a142-132">定义在邮箱中查找项目的请求。</span><span class="sxs-lookup"><span data-stu-id="0a142-132">Defines a request to find items in a mailbox.</span></span><br/><br/> <span data-ttu-id="0a142-133">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="0a142-133">The following is the XPath expression to this element:</span></span>  <br/>  `/FindItem` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0a142-134">备注</span><span class="sxs-lookup"><span data-stu-id="0a142-134">Remarks</span></span>

<span data-ttu-id="0a142-135">如果在 FindItem 请求中指定了**CalendarView**元素，则 Web 服务将在**起始日期**和**结束**日期指定的范围内返回单个日历项目和定期日历项目的匹配项的列表。</span><span class="sxs-lookup"><span data-stu-id="0a142-135">If the **CalendarView** element is specified in a FindItem request, the Web service returns a list of single calendar items and occurrences of recurring calendar items within the range specified by **StartDate** and **EndDate**.</span></span>
  
<span data-ttu-id="0a142-136">如果 FindItem 请求中未指定**CalendarView**元素，则 Web 服务将返回单个日历项目和定期主日历项目的列表。</span><span class="sxs-lookup"><span data-stu-id="0a142-136">If the **CalendarView** element is not specified in a FindItem request, the Web service returns a list of single calendar items and recurring master calendar items.</span></span> <span data-ttu-id="0a142-137">不展开定期日历项目的日历事件。</span><span class="sxs-lookup"><span data-stu-id="0a142-137">Calendar occurrences of a recurring calendar item are not expanded.</span></span> 
  
<span data-ttu-id="0a142-138">CalendarView 查询应仅使用下列属性，因为它们支持更快的日历查询。</span><span class="sxs-lookup"><span data-stu-id="0a142-138">CalendarView queries should only make use of the following properties since they support faster calendar queries.</span></span>
  
### <a name="recurrence-blob-properties"></a><span data-ttu-id="0a142-139">定期 blob 属性</span><span class="sxs-lookup"><span data-stu-id="0a142-139">Recurrence blob properties</span></span>
  
- <span data-ttu-id="0a142-140">MapiStartTime</span><span class="sxs-lookup"><span data-stu-id="0a142-140">MapiStartTime</span></span>
    
- <span data-ttu-id="0a142-141">MapiEndTime</span><span class="sxs-lookup"><span data-stu-id="0a142-141">MapiEndTime</span></span>
    
- <span data-ttu-id="0a142-142">SubjectPrefixInternal</span><span class="sxs-lookup"><span data-stu-id="0a142-142">SubjectPrefixInternal</span></span>
    
- <span data-ttu-id="0a142-143">NormalizedSubjectInternal</span><span class="sxs-lookup"><span data-stu-id="0a142-143">NormalizedSubjectInternal</span></span>
    
- <span data-ttu-id="0a142-144">MapiSubject</span><span class="sxs-lookup"><span data-stu-id="0a142-144">MapiSubject</span></span>
    
- <span data-ttu-id="0a142-145">位置</span><span class="sxs-lookup"><span data-stu-id="0a142-145">Location</span></span>
    
- <span data-ttu-id="0a142-146">AppointmentColor</span><span class="sxs-lookup"><span data-stu-id="0a142-146">AppointmentColor</span></span>
    
- <span data-ttu-id="0a142-147">MapiIsAllDayEvent</span><span class="sxs-lookup"><span data-stu-id="0a142-147">MapiIsAllDayEvent</span></span>
    
- <span data-ttu-id="0a142-148">MapiHasAttachment</span><span class="sxs-lookup"><span data-stu-id="0a142-148">MapiHasAttachment</span></span>
    
- <span data-ttu-id="0a142-149">FreeBusyStatus</span><span class="sxs-lookup"><span data-stu-id="0a142-149">FreeBusyStatus</span></span>
    
- <span data-ttu-id="0a142-150">ReminderIsSetInternal</span><span class="sxs-lookup"><span data-stu-id="0a142-150">ReminderIsSetInternal</span></span>
    
- <span data-ttu-id="0a142-151">ReminderMinutesBeforeStartInternal</span><span class="sxs-lookup"><span data-stu-id="0a142-151">ReminderMinutesBeforeStartInternal</span></span>
    
- <span data-ttu-id="0a142-152">AppointmentState</span><span class="sxs-lookup"><span data-stu-id="0a142-152">AppointmentState</span></span>
    
- <span data-ttu-id="0a142-153">AllAttachmentsHidden</span><span class="sxs-lookup"><span data-stu-id="0a142-153">AllAttachmentsHidden</span></span>
    
- <span data-ttu-id="0a142-154">ChangeHighlight</span><span class="sxs-lookup"><span data-stu-id="0a142-154">ChangeHighlight</span></span>
    
### <a name="calculated-from-the-primary-recurrence-blob-or-master"></a><span data-ttu-id="0a142-155">通过主定期 blob 或主机计算</span><span class="sxs-lookup"><span data-stu-id="0a142-155">Calculated from the primary recurrence blob or master</span></span>
  
- <span data-ttu-id="0a142-156">ItemId</span><span class="sxs-lookup"><span data-stu-id="0a142-156">ItemId</span></span>
    
- <span data-ttu-id="0a142-157">IsRecurring</span><span class="sxs-lookup"><span data-stu-id="0a142-157">IsRecurring</span></span>
    
- <span data-ttu-id="0a142-158">IsException</span><span class="sxs-lookup"><span data-stu-id="0a142-158">IsException</span></span>
    
- <span data-ttu-id="0a142-159">AppointmentRecurring</span><span class="sxs-lookup"><span data-stu-id="0a142-159">AppointmentRecurring</span></span>
    
- <span data-ttu-id="0a142-160">MapiStartTime</span><span class="sxs-lookup"><span data-stu-id="0a142-160">MapiStartTime</span></span>
    
- <span data-ttu-id="0a142-161">MapiPRStartDate</span><span class="sxs-lookup"><span data-stu-id="0a142-161">MapiPRStartDate</span></span>
    
- <span data-ttu-id="0a142-162">MapiEndTime</span><span class="sxs-lookup"><span data-stu-id="0a142-162">MapiEndTime</span></span>
    
- <span data-ttu-id="0a142-163">MapiPREndDate</span><span class="sxs-lookup"><span data-stu-id="0a142-163">MapiPREndDate</span></span>
    
- <span data-ttu-id="0a142-164">CalendarItemType</span><span class="sxs-lookup"><span data-stu-id="0a142-164">CalendarItemType</span></span>
    
- <span data-ttu-id="0a142-165">GlobalObjectId</span><span class="sxs-lookup"><span data-stu-id="0a142-165">GlobalObjectId</span></span>
    
- <span data-ttu-id="0a142-166">TimeZoneDefinitionStart</span><span class="sxs-lookup"><span data-stu-id="0a142-166">TimeZoneDefinitionStart</span></span>
    
- <span data-ttu-id="0a142-167">TimeZoneDefinitionEnd</span><span class="sxs-lookup"><span data-stu-id="0a142-167">TimeZoneDefinitionEnd</span></span>
    
### <a name="master-calendar-item-properties"></a><span data-ttu-id="0a142-168">主日历项目属性</span><span class="sxs-lookup"><span data-stu-id="0a142-168">Master calendar item properties</span></span>
  
- <span data-ttu-id="0a142-169">EntryId</span><span class="sxs-lookup"><span data-stu-id="0a142-169">EntryId</span></span>
    
- <span data-ttu-id="0a142-170">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="0a142-170">ChangeKey</span></span>
    
- <span data-ttu-id="0a142-171">ItemClass</span><span class="sxs-lookup"><span data-stu-id="0a142-171">ItemClass</span></span>
    
- <span data-ttu-id="0a142-172">SentRepresentingEmailAddress</span><span class="sxs-lookup"><span data-stu-id="0a142-172">SentRepresentingEmailAddress</span></span>
    
- <span data-ttu-id="0a142-173">SentRepresentingDisplayName</span><span class="sxs-lookup"><span data-stu-id="0a142-173">SentRepresentingDisplayName</span></span>
    
- <span data-ttu-id="0a142-174">SentRepresentingEntryId</span><span class="sxs-lookup"><span data-stu-id="0a142-174">SentRepresentingEntryId</span></span>
    
- <span data-ttu-id="0a142-175">AppointmentRecurrenceBlob</span><span class="sxs-lookup"><span data-stu-id="0a142-175">AppointmentRecurrenceBlob</span></span>
    
- <span data-ttu-id="0a142-176">TimeZone</span><span class="sxs-lookup"><span data-stu-id="0a142-176">TimeZone</span></span>
    
- <span data-ttu-id="0a142-177">TimeZoneBlob</span><span class="sxs-lookup"><span data-stu-id="0a142-177">TimeZoneBlob</span></span>
    
- <span data-ttu-id="0a142-178">TimeZoneDefinitionRecurring</span><span class="sxs-lookup"><span data-stu-id="0a142-178">TimeZoneDefinitionRecurring</span></span>
    
- <span data-ttu-id="0a142-179">CleanGlobalObjectId</span><span class="sxs-lookup"><span data-stu-id="0a142-179">CleanGlobalObjectId</span></span>
    
- <span data-ttu-id="0a142-180">AppointmentRecurring</span><span class="sxs-lookup"><span data-stu-id="0a142-180">AppointmentRecurring</span></span>
    
- <span data-ttu-id="0a142-181">IsException</span><span class="sxs-lookup"><span data-stu-id="0a142-181">IsException</span></span>
    
- <span data-ttu-id="0a142-182">IsRecurring</span><span class="sxs-lookup"><span data-stu-id="0a142-182">IsRecurring</span></span>
    
- <span data-ttu-id="0a142-183">MapiSensitivity</span><span class="sxs-lookup"><span data-stu-id="0a142-183">MapiSensitivity</span></span>
    
- <span data-ttu-id="0a142-184">ContainerClass</span><span class="sxs-lookup"><span data-stu-id="0a142-184">ContainerClass</span></span>
    
- <span data-ttu-id="0a142-185">MapiPRStartDate</span><span class="sxs-lookup"><span data-stu-id="0a142-185">MapiPRStartDate</span></span>
    
- <span data-ttu-id="0a142-186">MapiPREndDate</span><span class="sxs-lookup"><span data-stu-id="0a142-186">MapiPREndDate</span></span>
    
- <span data-ttu-id="0a142-187">类别</span><span class="sxs-lookup"><span data-stu-id="0a142-187">Categories</span></span>
    
<span data-ttu-id="0a142-188">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0a142-188">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="example"></a><span data-ttu-id="0a142-189">示例</span><span class="sxs-lookup"><span data-stu-id="0a142-189">Example</span></span>

<span data-ttu-id="0a142-190">下面的示例展示了一个 FindItem 请求。</span><span class="sxs-lookup"><span data-stu-id="0a142-190">The following example shows a FindItem request.</span></span> <span data-ttu-id="0a142-191">成功的请求将返回一个响应，其中包括在2006年-18T00：00：00：00：00：00：00：00：00：00：00：00：00：00：00： 00-08：00之前开始的日历项目。</span><span class="sxs-lookup"><span data-stu-id="0a142-191">A successful request returns a response that includes calendar items that started at 2006-05-18T00:00:00-08:00 or after and ended before 2006-05-19T00:00:00-08:00.</span></span>
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem Traversal="Shallow" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="calendar:Start"/>
          <t:FieldURI FieldURI="calendar:End"/>
          <t:FieldURI FieldURI="item:Subject"/>
        </t:AdditionalProperties>
      </ItemShape>
      <CalendarView MaxEntriesReturned="2" StartDate="2006-05-18T00:00:00-08:00" EndDate="2006-05-19T00:00:00-08:00"/>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="calendar"/>
      </ParentFolderIds>
    </FindItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a><span data-ttu-id="0a142-192">元素信息</span><span class="sxs-lookup"><span data-stu-id="0a142-192">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0a142-193">命名空间</span><span class="sxs-lookup"><span data-stu-id="0a142-193">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0a142-194">架构名称</span><span class="sxs-lookup"><span data-stu-id="0a142-194">Schema Name</span></span>  <br/> |<span data-ttu-id="0a142-195">消息架构</span><span class="sxs-lookup"><span data-stu-id="0a142-195">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0a142-196">验证文件</span><span class="sxs-lookup"><span data-stu-id="0a142-196">Validation File</span></span>  <br/> |<span data-ttu-id="0a142-197">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0a142-197">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0a142-198">可以为空</span><span class="sxs-lookup"><span data-stu-id="0a142-198">Can be Empty</span></span>  <br/> |<span data-ttu-id="0a142-199">False</span><span class="sxs-lookup"><span data-stu-id="0a142-199">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0a142-200">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0a142-200">See also</span></span>

- [<span data-ttu-id="0a142-201">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="0a142-201">FindItem operation</span></span>](finditem-operation.md)
- [<span data-ttu-id="0a142-202">查找项目</span><span class="sxs-lookup"><span data-stu-id="0a142-202">Finding Items</span></span>](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

