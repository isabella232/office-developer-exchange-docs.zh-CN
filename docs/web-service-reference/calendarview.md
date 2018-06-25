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
description: CalendarView 元素定义为显示日历中一组中返回日历项 FindItem 操作。
ms.openlocfilehash: 79b5ad268a8013092c1122c99bdcd10d876abf2c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753427"
---
# <a name="calendarview"></a><span data-ttu-id="9338b-103">CalendarView</span><span class="sxs-lookup"><span data-stu-id="9338b-103">CalendarView</span></span>

<span data-ttu-id="9338b-104">**CalendarView**元素定义为显示日历中一组中返回日历项[FindItem 操作](finditem-operation.md)。</span><span class="sxs-lookup"><span data-stu-id="9338b-104">The **CalendarView** element defines a [FindItem operation](finditem-operation.md) as returning calendar items in a set as they appear in a calendar.</span></span> 
  
[<span data-ttu-id="9338b-105">FindItem</span><span class="sxs-lookup"><span data-stu-id="9338b-105">FindItem</span></span>](finditem.md)
  
[<span data-ttu-id="9338b-106">CalendarView</span><span class="sxs-lookup"><span data-stu-id="9338b-106">CalendarView</span></span>](calendarview.md)
  
```XML
<CalendarView MaxEntriesReturned="" StartDate="" EndDate="" />
```

<span data-ttu-id="9338b-107">**CalendarView**</span><span class="sxs-lookup"><span data-stu-id="9338b-107">**CalendarView**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="9338b-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9338b-108">Attributes and elements</span></span>

<span data-ttu-id="9338b-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9338b-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9338b-110">属性</span><span class="sxs-lookup"><span data-stu-id="9338b-110">Attributes</span></span>

|<span data-ttu-id="9338b-111">**属性**</span><span class="sxs-lookup"><span data-stu-id="9338b-111">**Attribute**</span></span>|<span data-ttu-id="9338b-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="9338b-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9338b-113">**MaxEntriesReturned**</span><span class="sxs-lookup"><span data-stu-id="9338b-113">**MaxEntriesReturned**</span></span> <br/> |<span data-ttu-id="9338b-114">最大个数要 FindItem 响应中返回的结果。</span><span class="sxs-lookup"><span data-stu-id="9338b-114">Describes the maximum number of results to return in the FindItem response.</span></span>  <br/> |
|<span data-ttu-id="9338b-115">**StartDate**</span><span class="sxs-lookup"><span data-stu-id="9338b-115">**StartDate**</span></span> <br/> |<span data-ttu-id="9338b-116">标识查询的日历项目的时间范围内的开始。</span><span class="sxs-lookup"><span data-stu-id="9338b-116">Identifies the start of a time span queried for calendar items.</span></span> <span data-ttu-id="9338b-117">具有之前不会返回**StartDate**结束时间的所有日历项。</span><span class="sxs-lookup"><span data-stu-id="9338b-117">All calendar items that have an end time that is before **StartDate** will not be returned.</span></span> <span data-ttu-id="9338b-118">可以采用协调世界时 (UTC) 格式，如 2006年中所示指定的**起始日期**值-01-02T12:00:00Z，或格式为本地时间和时区偏移指定的位置，如所示 2006年-01-02T04:00:00-08:00。</span><span class="sxs-lookup"><span data-stu-id="9338b-118">The value of **StartDate** can be specified in coordinated universal time (UTC) format, as in 2006-01-02T12:00:00Z, or in a format where local time and time zone offset is specified, as in 2006-01-02T04:00:00-08:00.</span></span>  <br/><br/><span data-ttu-id="9338b-119">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="9338b-119">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="9338b-120">**EndDate**</span><span class="sxs-lookup"><span data-stu-id="9338b-120">**EndDate**</span></span> <br/> |<span data-ttu-id="9338b-121">标识查询日历项目的时间范围的末尾。</span><span class="sxs-lookup"><span data-stu-id="9338b-121">Identifies the end of a time span queried for calendar items.</span></span> <span data-ttu-id="9338b-122">不会返回所有已是或**结束日期**之后的开始时间的日历项目。</span><span class="sxs-lookup"><span data-stu-id="9338b-122">All calendar items that have a start time that is on or after **EndDate** will not be returned.</span></span> <span data-ttu-id="9338b-123">**EndDate**的值可以指定以 UTC 格式，如下所示 2006年-02-02T12:00:00Z，或格式为本地时间和时区偏移指定的位置，如所示 2006年-02-02T04:00:00-08:00。</span><span class="sxs-lookup"><span data-stu-id="9338b-123">The value of **EndDate** can be specified in UTC format, as in 2006-02-02T12:00:00Z, or in a format where local time and time zone offset is specified, as in 2006-02-02T04:00:00-08:00.</span></span>  <br/><br/><span data-ttu-id="9338b-124">**EndDate**必须大于或等于**StartDate**;否则将返回错误。</span><span class="sxs-lookup"><span data-stu-id="9338b-124">**EndDate** must be greater than or equal to **StartDate**; otherwise an error is returned.</span></span> <span data-ttu-id="9338b-125">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="9338b-125">This attribute is required.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9338b-126">子元素</span><span class="sxs-lookup"><span data-stu-id="9338b-126">Child elements</span></span>

<span data-ttu-id="9338b-127">无。</span><span class="sxs-lookup"><span data-stu-id="9338b-127">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9338b-128">父元素</span><span class="sxs-lookup"><span data-stu-id="9338b-128">Parent elements</span></span>

|<span data-ttu-id="9338b-129">**元素**</span><span class="sxs-lookup"><span data-stu-id="9338b-129">**Element**</span></span>|<span data-ttu-id="9338b-130">**说明**</span><span class="sxs-lookup"><span data-stu-id="9338b-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9338b-131">FindItem</span><span class="sxs-lookup"><span data-stu-id="9338b-131">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="9338b-132">定义查找邮箱中的项目的请求。</span><span class="sxs-lookup"><span data-stu-id="9338b-132">Defines a request to find items in a mailbox.</span></span><br/><br/> <span data-ttu-id="9338b-133">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="9338b-133">The following is the XPath expression to this element:</span></span>  <br/>  `/FindItem` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9338b-134">注解</span><span class="sxs-lookup"><span data-stu-id="9338b-134">Remarks</span></span>

<span data-ttu-id="9338b-135">如果 FindItem 请求中指定的**CalendarView**元素，则 Web 服务返回的单个日历项和匹配项的**StartDate**和**EndDate**指定的范围内的定期日历项目的列表。</span><span class="sxs-lookup"><span data-stu-id="9338b-135">If the **CalendarView** element is specified in a FindItem request, the Web service returns a list of single calendar items and occurrences of recurring calendar items within the range specified by **StartDate** and **EndDate**.</span></span>
  
<span data-ttu-id="9338b-136">如果未在 FindItem 请求中指定的**CalendarView**元素，Web 服务返回的单个日历项和定期母版日历项目的列表。</span><span class="sxs-lookup"><span data-stu-id="9338b-136">If the **CalendarView** element is not specified in a FindItem request, the Web service returns a list of single calendar items and recurring master calendar items.</span></span> <span data-ttu-id="9338b-137">不展开定期日历项目的日历发生次数。</span><span class="sxs-lookup"><span data-stu-id="9338b-137">Calendar occurrences of a recurring calendar item are not expanded.</span></span> 
  
<span data-ttu-id="9338b-138">应只进行 CalendarView 查询使用下列属性之一，因为它们支持更快的日历查询。</span><span class="sxs-lookup"><span data-stu-id="9338b-138">CalendarView queries should only make use of the following properties since they support faster calendar queries.</span></span>
  
### <a name="recurrence-blob-properties"></a><span data-ttu-id="9338b-139">定期 blob 属性</span><span class="sxs-lookup"><span data-stu-id="9338b-139">Recurrence blob properties</span></span>
  
- <span data-ttu-id="9338b-140">MapiStartTime</span><span class="sxs-lookup"><span data-stu-id="9338b-140">MapiStartTime</span></span>
    
- <span data-ttu-id="9338b-141">MapiEndTime</span><span class="sxs-lookup"><span data-stu-id="9338b-141">MapiEndTime</span></span>
    
- <span data-ttu-id="9338b-142">SubjectPrefixInternal</span><span class="sxs-lookup"><span data-stu-id="9338b-142">SubjectPrefixInternal</span></span>
    
- <span data-ttu-id="9338b-143">NormalizedSubjectInternal</span><span class="sxs-lookup"><span data-stu-id="9338b-143">NormalizedSubjectInternal</span></span>
    
- <span data-ttu-id="9338b-144">MapiSubject</span><span class="sxs-lookup"><span data-stu-id="9338b-144">MapiSubject</span></span>
    
- <span data-ttu-id="9338b-145">位置</span><span class="sxs-lookup"><span data-stu-id="9338b-145">Location</span></span>
    
- <span data-ttu-id="9338b-146">AppointmentColor</span><span class="sxs-lookup"><span data-stu-id="9338b-146">AppointmentColor</span></span>
    
- <span data-ttu-id="9338b-147">MapiIsAllDayEvent</span><span class="sxs-lookup"><span data-stu-id="9338b-147">MapiIsAllDayEvent</span></span>
    
- <span data-ttu-id="9338b-148">MapiHasAttachment</span><span class="sxs-lookup"><span data-stu-id="9338b-148">MapiHasAttachment</span></span>
    
- <span data-ttu-id="9338b-149">FreeBusyStatus</span><span class="sxs-lookup"><span data-stu-id="9338b-149">FreeBusyStatus</span></span>
    
- <span data-ttu-id="9338b-150">ReminderIsSetInternal</span><span class="sxs-lookup"><span data-stu-id="9338b-150">ReminderIsSetInternal</span></span>
    
- <span data-ttu-id="9338b-151">ReminderMinutesBeforeStartInternal</span><span class="sxs-lookup"><span data-stu-id="9338b-151">ReminderMinutesBeforeStartInternal</span></span>
    
- <span data-ttu-id="9338b-152">AppointmentState</span><span class="sxs-lookup"><span data-stu-id="9338b-152">AppointmentState</span></span>
    
- <span data-ttu-id="9338b-153">AllAttachmentsHidden</span><span class="sxs-lookup"><span data-stu-id="9338b-153">AllAttachmentsHidden</span></span>
    
- <span data-ttu-id="9338b-154">ChangeHighlight</span><span class="sxs-lookup"><span data-stu-id="9338b-154">ChangeHighlight</span></span>
    
### <a name="calculated-from-the-primary-recurrence-blob-or-master"></a><span data-ttu-id="9338b-155">从主定期 blob 或主控形状计算</span><span class="sxs-lookup"><span data-stu-id="9338b-155">Calculated from the primary recurrence blob or master</span></span>
  
- <span data-ttu-id="9338b-156">ItemId</span><span class="sxs-lookup"><span data-stu-id="9338b-156">ItemId</span></span>
    
- <span data-ttu-id="9338b-157">IsRecurring</span><span class="sxs-lookup"><span data-stu-id="9338b-157">IsRecurring</span></span>
    
- <span data-ttu-id="9338b-158">IsException</span><span class="sxs-lookup"><span data-stu-id="9338b-158">IsException</span></span>
    
- <span data-ttu-id="9338b-159">AppointmentRecurring</span><span class="sxs-lookup"><span data-stu-id="9338b-159">AppointmentRecurring</span></span>
    
- <span data-ttu-id="9338b-160">MapiStartTime</span><span class="sxs-lookup"><span data-stu-id="9338b-160">MapiStartTime</span></span>
    
- <span data-ttu-id="9338b-161">MapiPRStartDate</span><span class="sxs-lookup"><span data-stu-id="9338b-161">MapiPRStartDate</span></span>
    
- <span data-ttu-id="9338b-162">MapiEndTime</span><span class="sxs-lookup"><span data-stu-id="9338b-162">MapiEndTime</span></span>
    
- <span data-ttu-id="9338b-163">MapiPREndDate</span><span class="sxs-lookup"><span data-stu-id="9338b-163">MapiPREndDate</span></span>
    
- <span data-ttu-id="9338b-164">CalendarItemType</span><span class="sxs-lookup"><span data-stu-id="9338b-164">CalendarItemType</span></span>
    
- <span data-ttu-id="9338b-165">GlobalObjectId</span><span class="sxs-lookup"><span data-stu-id="9338b-165">GlobalObjectId</span></span>
    
- <span data-ttu-id="9338b-166">TimeZoneDefinitionStart</span><span class="sxs-lookup"><span data-stu-id="9338b-166">TimeZoneDefinitionStart</span></span>
    
- <span data-ttu-id="9338b-167">TimeZoneDefinitionEnd</span><span class="sxs-lookup"><span data-stu-id="9338b-167">TimeZoneDefinitionEnd</span></span>
    
### <a name="master-calendar-item-properties"></a><span data-ttu-id="9338b-168">母版日历项目属性</span><span class="sxs-lookup"><span data-stu-id="9338b-168">Master calendar item properties</span></span>
  
- <span data-ttu-id="9338b-169">EntryId</span><span class="sxs-lookup"><span data-stu-id="9338b-169">EntryId</span></span>
    
- <span data-ttu-id="9338b-170">更改密钥</span><span class="sxs-lookup"><span data-stu-id="9338b-170">ChangeKey</span></span>
    
- <span data-ttu-id="9338b-171">ItemClass</span><span class="sxs-lookup"><span data-stu-id="9338b-171">ItemClass</span></span>
    
- <span data-ttu-id="9338b-172">SentRepresentingEmailAddress</span><span class="sxs-lookup"><span data-stu-id="9338b-172">SentRepresentingEmailAddress</span></span>
    
- <span data-ttu-id="9338b-173">SentRepresentingDisplayName</span><span class="sxs-lookup"><span data-stu-id="9338b-173">SentRepresentingDisplayName</span></span>
    
- <span data-ttu-id="9338b-174">SentRepresentingEntryId</span><span class="sxs-lookup"><span data-stu-id="9338b-174">SentRepresentingEntryId</span></span>
    
- <span data-ttu-id="9338b-175">AppointmentRecurrenceBlob</span><span class="sxs-lookup"><span data-stu-id="9338b-175">AppointmentRecurrenceBlob</span></span>
    
- <span data-ttu-id="9338b-176">TimeZone</span><span class="sxs-lookup"><span data-stu-id="9338b-176">TimeZone</span></span>
    
- <span data-ttu-id="9338b-177">TimeZoneBlob</span><span class="sxs-lookup"><span data-stu-id="9338b-177">TimeZoneBlob</span></span>
    
- <span data-ttu-id="9338b-178">TimeZoneDefinitionRecurring</span><span class="sxs-lookup"><span data-stu-id="9338b-178">TimeZoneDefinitionRecurring</span></span>
    
- <span data-ttu-id="9338b-179">CleanGlobalObjectId</span><span class="sxs-lookup"><span data-stu-id="9338b-179">CleanGlobalObjectId</span></span>
    
- <span data-ttu-id="9338b-180">AppointmentRecurring</span><span class="sxs-lookup"><span data-stu-id="9338b-180">AppointmentRecurring</span></span>
    
- <span data-ttu-id="9338b-181">IsException</span><span class="sxs-lookup"><span data-stu-id="9338b-181">IsException</span></span>
    
- <span data-ttu-id="9338b-182">IsRecurring</span><span class="sxs-lookup"><span data-stu-id="9338b-182">IsRecurring</span></span>
    
- <span data-ttu-id="9338b-183">MapiSensitivity</span><span class="sxs-lookup"><span data-stu-id="9338b-183">MapiSensitivity</span></span>
    
- <span data-ttu-id="9338b-184">ContainerClass</span><span class="sxs-lookup"><span data-stu-id="9338b-184">ContainerClass</span></span>
    
- <span data-ttu-id="9338b-185">MapiPRStartDate</span><span class="sxs-lookup"><span data-stu-id="9338b-185">MapiPRStartDate</span></span>
    
- <span data-ttu-id="9338b-186">MapiPREndDate</span><span class="sxs-lookup"><span data-stu-id="9338b-186">MapiPREndDate</span></span>
    
- <span data-ttu-id="9338b-187">类别</span><span class="sxs-lookup"><span data-stu-id="9338b-187">Categories</span></span>
    
<span data-ttu-id="9338b-188">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9338b-188">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="example"></a><span data-ttu-id="9338b-189">示例</span><span class="sxs-lookup"><span data-stu-id="9338b-189">Example</span></span>

<span data-ttu-id="9338b-190">下面的示例演示一个 FindItem 请求。</span><span class="sxs-lookup"><span data-stu-id="9338b-190">The following example shows a FindItem request.</span></span> <span data-ttu-id="9338b-191">成功的请求返回一个响应，其中包括在 2006年启动的日历项目-05-18T00:00:00-08:00 或之后和已结束之前 2006年-05-19T00:00:00-08:00。</span><span class="sxs-lookup"><span data-stu-id="9338b-191">A successful request returns a response that includes calendar items that started at 2006-05-18T00:00:00-08:00 or after and ended before 2006-05-19T00:00:00-08:00.</span></span>
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem Traversal="Shallow" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="element-information"></a><span data-ttu-id="9338b-192">元素信息</span><span class="sxs-lookup"><span data-stu-id="9338b-192">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9338b-193">命名空间</span><span class="sxs-lookup"><span data-stu-id="9338b-193">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9338b-194">架构名称</span><span class="sxs-lookup"><span data-stu-id="9338b-194">Schema Name</span></span>  <br/> |<span data-ttu-id="9338b-195">消息架构</span><span class="sxs-lookup"><span data-stu-id="9338b-195">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9338b-196">验证文件</span><span class="sxs-lookup"><span data-stu-id="9338b-196">Validation File</span></span>  <br/> |<span data-ttu-id="9338b-197">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9338b-197">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9338b-198">可以为空</span><span class="sxs-lookup"><span data-stu-id="9338b-198">Can be Empty</span></span>  <br/> |<span data-ttu-id="9338b-199">False</span><span class="sxs-lookup"><span data-stu-id="9338b-199">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9338b-200">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9338b-200">See also</span></span>

- [<span data-ttu-id="9338b-201">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="9338b-201">FindItem operation</span></span>](finditem-operation.md)
- [<span data-ttu-id="9338b-202">查找项目</span><span class="sxs-lookup"><span data-stu-id="9338b-202">Finding Items</span></span>](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

