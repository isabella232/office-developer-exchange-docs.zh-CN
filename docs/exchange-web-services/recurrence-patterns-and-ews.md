---
title: 定期模式和 EWS
manager: luken
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fd9ef706-1e01-49fa-af6f-2f6d3e173c16
description: 在 Exchange 中了解有关定期模式和定期系列。
ms.openlocfilehash: ac10e9b9a347abb5907b77f0e0e7315e4e86d97a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753012"
---
# <a name="recurrence-patterns-and-ews"></a><span data-ttu-id="cdd35-103">定期模式和 EWS</span><span class="sxs-lookup"><span data-stu-id="cdd35-103">Recurrence patterns and EWS</span></span>

<span data-ttu-id="cdd35-104">在 Exchange 中了解有关定期模式和定期系列。</span><span class="sxs-lookup"><span data-stu-id="cdd35-104">Learn about recurrence patterns and recurring series in Exchange.</span></span>
  
<span data-ttu-id="cdd35-105">定期系列是约会或会议的重复根据定义的模式。</span><span class="sxs-lookup"><span data-stu-id="cdd35-105">A recurring series is an appointment or meeting that repeats according to a defined pattern.</span></span> <span data-ttu-id="cdd35-106">定期系列可以特定次数，也可以无限期重复。</span><span class="sxs-lookup"><span data-stu-id="cdd35-106">A recurring series can either have a specific number of occurrences or can repeat indefinitely.</span></span> <span data-ttu-id="cdd35-107">此外，定期系列可以具有不继承的匹配项，其余的模式，它可以从模式已删除的匹配项的例外。</span><span class="sxs-lookup"><span data-stu-id="cdd35-107">Additionally, a recurring series can have exceptions that don't follow the pattern of the rest of the occurrences, and can have occurrences that have been deleted from the pattern.</span></span> <span data-ttu-id="cdd35-108">您可以使用 EWS 托管 API 和 EWS 使用定期系列和其关联的日历项目。</span><span class="sxs-lookup"><span data-stu-id="cdd35-108">You can use the EWS Managed API and EWS to work with recurring series and their associated calendar items.</span></span>
  
## <a name="recurring-calendar-items"></a><span data-ttu-id="cdd35-109">定期日历项目</span><span class="sxs-lookup"><span data-stu-id="cdd35-109">Recurring calendar items</span></span>

<span data-ttu-id="cdd35-110">所有日历项目都分为以下四个类别：</span><span class="sxs-lookup"><span data-stu-id="cdd35-110">All calendar items fall into one of the following four categories:</span></span>
  
- <span data-ttu-id="cdd35-111">非定期日历项目</span><span class="sxs-lookup"><span data-stu-id="cdd35-111">Non-recurring calendar items</span></span>
    
- <span data-ttu-id="cdd35-112">定期母版</span><span class="sxs-lookup"><span data-stu-id="cdd35-112">Recurring masters</span></span>
    
- <span data-ttu-id="cdd35-113">出现系列</span><span class="sxs-lookup"><span data-stu-id="cdd35-113">Occurrences in a series</span></span>
    
- <span data-ttu-id="cdd35-114">修改的出现系列，称作异常</span><span class="sxs-lookup"><span data-stu-id="cdd35-114">Modified occurrences in a series, known as exceptions</span></span>
    
<span data-ttu-id="cdd35-115">在本文中，我们来看看是定期系列的一部分的日历项目的三种类型。</span><span class="sxs-lookup"><span data-stu-id="cdd35-115">In this article, we'll look at the three types of calendar items that are part of a recurring series.</span></span>
  
<span data-ttu-id="cdd35-116">它是有助于您了解如何定期系列的 Exchange 服务器上实现。</span><span class="sxs-lookup"><span data-stu-id="cdd35-116">It's helpful to understand how recurring series are implemented on the Exchange server.</span></span> <span data-ttu-id="cdd35-117">而不是定期系列中创建一个单独的不同项，每次，服务器在日历中，称为定期主创建只有一个实际项。</span><span class="sxs-lookup"><span data-stu-id="cdd35-117">Instead of creating a separate distinct item for each occurrence in a recurring series, the server creates only one actual item in the calendar, known as the recurring master.</span></span> <span data-ttu-id="cdd35-118">定期主控形状的格式为非常类似于非定期约会，并添加了定期模式信息。</span><span class="sxs-lookup"><span data-stu-id="cdd35-118">The format of a recurring master is very similar to a non-recurring appointment, with the addition of recurrence pattern information.</span></span> <span data-ttu-id="cdd35-119">然后，服务器会生成基于定期模式的约会信息，使用此过程称为扩展的客户端请求的响应中的匹配项。</span><span class="sxs-lookup"><span data-stu-id="cdd35-119">The server then generates occurrences based on the recurrence pattern in response to client requests for appointment information, using a process called expansion.</span></span> <span data-ttu-id="cdd35-120">这些生成的匹配项不会永久存储在服务器上。</span><span class="sxs-lookup"><span data-stu-id="cdd35-120">These generated occurrences are not permanently stored on the server.</span></span> <span data-ttu-id="cdd35-121">这是重要了解，因为您搜索的日历项目的方式确定您将收到哪些信息以及是否扩展发生此事件。</span><span class="sxs-lookup"><span data-stu-id="cdd35-121">This is important to understand because the way that you search for calendar items determines what information you receive and whether expansion occurs.</span></span>
  
## <a name="recurrence-patterns"></a><span data-ttu-id="cdd35-122">定期模式</span><span class="sxs-lookup"><span data-stu-id="cdd35-122">Recurrence patterns</span></span>

<span data-ttu-id="cdd35-123">定期系列，使扩展关键是定期模式。</span><span class="sxs-lookup"><span data-stu-id="cdd35-123">The key piece to a recurring series that makes expansion possible is the recurrence pattern.</span></span> <span data-ttu-id="cdd35-124">定期模式在定期主机上，找到并描述了一组条件的计算依据的日期和时间的定期主控形状。</span><span class="sxs-lookup"><span data-stu-id="cdd35-124">The recurrence pattern is found on the recurring master, and describes a set of criteria for calculating occurrences based on the date and time of the recurring master.</span></span>
  
<span data-ttu-id="cdd35-125">**表 1。可用的定期模式**</span><span class="sxs-lookup"><span data-stu-id="cdd35-125">**Table 1. Available recurrence patterns**</span></span>

|<span data-ttu-id="cdd35-126">**EWS 托管 API 类**</span><span class="sxs-lookup"><span data-stu-id="cdd35-126">**EWS Managed API class**</span></span>|<span data-ttu-id="cdd35-127">**EWS 元素**</span><span class="sxs-lookup"><span data-stu-id="cdd35-127">**EWS element**</span></span>|<span data-ttu-id="cdd35-128">**示例**</span><span class="sxs-lookup"><span data-stu-id="cdd35-128">**Examples**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cdd35-129">Recurrence.DailyPattern</span><span class="sxs-lookup"><span data-stu-id="cdd35-129">Recurrence.DailyPattern</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.recurrence.dailypattern%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="cdd35-130">DailyRecurrence</span><span class="sxs-lookup"><span data-stu-id="cdd35-130">DailyRecurrence</span></span>](http://msdn.microsoft.com/library/0aaf265d-b723-49c6-8e9c-9ba60141e9ab%28Office.15%29.aspx) <br/> |<span data-ttu-id="cdd35-131">重复每天。</span><span class="sxs-lookup"><span data-stu-id="cdd35-131">Repeat every day.</span></span>  <br/> <span data-ttu-id="cdd35-132">重复每隔一天。</span><span class="sxs-lookup"><span data-stu-id="cdd35-132">Repeat every other day.</span></span>  <br/> |
|[<span data-ttu-id="cdd35-133">Recurrence.MonthlyPattern</span><span class="sxs-lookup"><span data-stu-id="cdd35-133">Recurrence.MonthlyPattern</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.recurrence.monthlypattern%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="cdd35-134">AbsoluteMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="cdd35-134">AbsoluteMonthlyRecurrence</span></span>](http://msdn.microsoft.com/library/178fa0ae-9dfc-417f-933c-d657d31c2161%28Office.15%29.aspx) <br/> |<span data-ttu-id="cdd35-135">相应月份的第十个天每月重复。</span><span class="sxs-lookup"><span data-stu-id="cdd35-135">Repeat every month on the tenth day of the month.</span></span>  <br/> <span data-ttu-id="cdd35-136">重复上个月的第二十一个天的其他每月。</span><span class="sxs-lookup"><span data-stu-id="cdd35-136">Repeat every other month on the twenty-first day of the month.</span></span>  <br/> |
|[<span data-ttu-id="cdd35-137">Recurrence.RelativeMonthlyPattern</span><span class="sxs-lookup"><span data-stu-id="cdd35-137">Recurrence.RelativeMonthlyPattern</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.recurrence.relativemonthlypattern%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="cdd35-138">RelativeMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="cdd35-138">RelativeMonthlyRecurrence</span></span>](http://msdn.microsoft.com/library/a76595db-7460-44ac-ac2a-53241caa33a7%28Office.15%29.aspx) <br/> |<span data-ttu-id="cdd35-139">每月的第二个星期二重复。</span><span class="sxs-lookup"><span data-stu-id="cdd35-139">Repeat on the second Tuesday of every month.</span></span>  <br/> <span data-ttu-id="cdd35-140">重复上个月每三个月的第三个星期四。</span><span class="sxs-lookup"><span data-stu-id="cdd35-140">Repeat on the third Thursday of the month every three months.</span></span>  <br/> |
|[<span data-ttu-id="cdd35-141">Recurrence.RelativeYearlyPattern</span><span class="sxs-lookup"><span data-stu-id="cdd35-141">Recurrence.RelativeYearlyPattern</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.recurrence.relativeyearlypattern%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="cdd35-142">RelativeYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="cdd35-142">RelativeYearlyRecurrence</span></span>](http://msdn.microsoft.com/library/25b67876-9979-4a30-a637-357ea10a93b8%28Office.15%29.aspx) <br/> |<span data-ttu-id="cdd35-143">每年重复年 8 月的第一个星期一。</span><span class="sxs-lookup"><span data-stu-id="cdd35-143">Repeat on the first Monday of August every year.</span></span>  <br/> |
|[<span data-ttu-id="cdd35-144">Recurrence.WeeklyPattern</span><span class="sxs-lookup"><span data-stu-id="cdd35-144">Recurrence.WeeklyPattern</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.recurrence.weeklypattern%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="cdd35-145">WeeklyRecurrence</span><span class="sxs-lookup"><span data-stu-id="cdd35-145">WeeklyRecurrence</span></span>](http://msdn.microsoft.com/library/69c41dd5-597c-45bc-be3f-e2f2b5615aa3%28Office.15%29.aspx) <br/> |<span data-ttu-id="cdd35-146">重复每个星期一。</span><span class="sxs-lookup"><span data-stu-id="cdd35-146">Repeat every Monday.</span></span>  <br/> <span data-ttu-id="cdd35-147">对每个星期二和星期四重复每隔一周。</span><span class="sxs-lookup"><span data-stu-id="cdd35-147">Repeat every Tuesday and Thursday every other week.</span></span>  <br/> |
|[<span data-ttu-id="cdd35-148">Recurrence.YearlyPattern</span><span class="sxs-lookup"><span data-stu-id="cdd35-148">Recurrence.YearlyPattern</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.recurrence.yearlypattern%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="cdd35-149">AbsoluteYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="cdd35-149">AbsoluteYearlyRecurrence</span></span>](http://msdn.microsoft.com/library/96f53e2c-3893-4f6e-a78a-ac179f45c5db%28Office.15%29.aspx) <br/> |<span data-ttu-id="cdd35-150">重复上年 9 月 1st 每年。</span><span class="sxs-lookup"><span data-stu-id="cdd35-150">Repeat on September 1st every year.</span></span>  <br/> |
   
<span data-ttu-id="cdd35-151">定期结束时的其他重要的定期模式的信息。</span><span class="sxs-lookup"><span data-stu-id="cdd35-151">The other important piece of information for a recurrence pattern is when the recurrence ends.</span></span> <span data-ttu-id="cdd35-152">这可以表示任一设置次数为、 结束日期，或为具有无结束。</span><span class="sxs-lookup"><span data-stu-id="cdd35-152">This can be expressed as either a set number of occurrences, as an end date, or as having no end.</span></span>
  
<span data-ttu-id="cdd35-153">**表 2。结束的定期系列选项**</span><span class="sxs-lookup"><span data-stu-id="cdd35-153">**Table 2. Options for the end of a recurring series**</span></span>

|<span data-ttu-id="cdd35-154">**EWS 托管 API 方法/属性**</span><span class="sxs-lookup"><span data-stu-id="cdd35-154">**EWS Managed API method/property**</span></span>|<span data-ttu-id="cdd35-155">**EWS 元素**</span><span class="sxs-lookup"><span data-stu-id="cdd35-155">**EWS element**</span></span>|<span data-ttu-id="cdd35-156">**说明**</span><span class="sxs-lookup"><span data-stu-id="cdd35-156">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cdd35-157">Recurrence.NumberOfOccurrences</span><span class="sxs-lookup"><span data-stu-id="cdd35-157">Recurrence.NumberOfOccurrences</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.recurrence.numberofoccurrences%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="cdd35-158">NumberedRecurrence</span><span class="sxs-lookup"><span data-stu-id="cdd35-158">NumberedRecurrence</span></span>](http://msdn.microsoft.com/library/53746909-ef21-4764-8715-a7769b943cca%28Office.15%29.aspx) <br/> |<span data-ttu-id="cdd35-159">此属性或元素的值指定次数。</span><span class="sxs-lookup"><span data-stu-id="cdd35-159">The value of this property or element specifies the number of occurrences.</span></span>  <br/> |
|[<span data-ttu-id="cdd35-160">Recurrence.EndDate</span><span class="sxs-lookup"><span data-stu-id="cdd35-160">Recurrence.EndDate</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.recurrence.enddate%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="cdd35-161">EndDateRecurrence</span><span class="sxs-lookup"><span data-stu-id="cdd35-161">EndDateRecurrence</span></span>](http://msdn.microsoft.com/library/a5ee2504-db84-49ee-870c-cca9269f2e26%28Office.15%29.aspx) <br/> |<span data-ttu-id="cdd35-162">此属性或元素指定日期或之前，将位于系列中的最后一个匹配项。</span><span class="sxs-lookup"><span data-stu-id="cdd35-162">The last occurrence in the series falls on or before the date specified by this property or element.</span></span>  <br/> |
|[<span data-ttu-id="cdd35-163">Recurrence.HasEnd</span><span class="sxs-lookup"><span data-stu-id="cdd35-163">Recurrence.HasEnd</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.recurrence.hasend%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="cdd35-164">Recurrence.NeverEnds</span><span class="sxs-lookup"><span data-stu-id="cdd35-164">Recurrence.NeverEnds</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.recurrence.neverends%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="cdd35-165">NoEndRecurrence</span><span class="sxs-lookup"><span data-stu-id="cdd35-165">NoEndRecurrence</span></span>](http://msdn.microsoft.com/library/ab2ebd9c-388e-45f1-abf9-56e293ef123b%28Office.15%29.aspx) <br/> |<span data-ttu-id="cdd35-166">数据系列有无结束。</span><span class="sxs-lookup"><span data-stu-id="cdd35-166">The series has no end.</span></span>  <br/> |
   
## <a name="expanded-vs-non-expanded-views"></a><span data-ttu-id="cdd35-167">与非扩展视图扩展</span><span class="sxs-lookup"><span data-stu-id="cdd35-167">Expanded vs. non-expanded views</span></span>

<span data-ttu-id="cdd35-168">使用 EWS 托管 API （或与**CalendarView**元素中的 ews **FindItem**操作） 中的**FindAppointments**方法调用只有展开过程。</span><span class="sxs-lookup"><span data-stu-id="cdd35-168">Using the **FindAppointments** method in the EWS Managed API (or the **FindItem** operation with a **CalendarView** element in EWS) invokes the expansion process.</span></span> <span data-ttu-id="cdd35-169">这隐藏定期主约会从结果集中，并且改为向该定期系列的展开的视图。</span><span class="sxs-lookup"><span data-stu-id="cdd35-169">This hides recurring master appointments from the result set, and instead presents an expanded view of that recurring series.</span></span> <span data-ttu-id="cdd35-170">在结果集中包含的匹配项和定期主例外的范围内的日历视图的参数。</span><span class="sxs-lookup"><span data-stu-id="cdd35-170">Occurrences of and exceptions to the recurring master that fall within the parameters of the calendar view are included in the result set.</span></span> <span data-ttu-id="cdd35-171">相反，使用 EWS 托管 API （或与**IndexedPageItemView**或**FractionalPageItemView**元素中的 ews **FindItem**操作） 中的**FindItems**方法不会调用只有展开过程，以及出现和不包括例外。</span><span class="sxs-lookup"><span data-stu-id="cdd35-171">Conversely, using the **FindItems** method in the EWS Managed API (or the **FindItem** operation with a **IndexedPageItemView** or **FractionalPageItemView** element in EWS), does not invoke the expansion process, and occurrences and exceptions are not included.</span></span> <span data-ttu-id="cdd35-172">让我们看一下示例进行比较的两种方法。</span><span class="sxs-lookup"><span data-stu-id="cdd35-172">Let's look at an example comparing the two methods.</span></span> 
  
<span data-ttu-id="cdd35-173">**表 3。方法和查找约会的操作**</span><span class="sxs-lookup"><span data-stu-id="cdd35-173">**Table 3. Methods and operations for finding appointments**</span></span>

|<span data-ttu-id="cdd35-174">**EWS 托管的 API 方法**</span><span class="sxs-lookup"><span data-stu-id="cdd35-174">**EWS Managed API method**</span></span>|<span data-ttu-id="cdd35-175">**EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="cdd35-175">**EWS operation**</span></span>|<span data-ttu-id="cdd35-176">**展开系列？**</span><span class="sxs-lookup"><span data-stu-id="cdd35-176">**Expands series?**</span></span>|<span data-ttu-id="cdd35-177">**在结果中包含的项目**</span><span class="sxs-lookup"><span data-stu-id="cdd35-177">**Items included in results**</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="cdd35-178">ExchangeService.FindAppointments</span><span class="sxs-lookup"><span data-stu-id="cdd35-178">ExchangeService.FindAppointments</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="cdd35-179">[FindItem 操作](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) [CalendarView](http://msdn.microsoft.com/library/a4a953b8-0710-416c-95ef-59e51eba9982%28Office.15%29.aspx)元素</span><span class="sxs-lookup"><span data-stu-id="cdd35-179">[FindItem operation](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) with a [CalendarView](http://msdn.microsoft.com/library/a4a953b8-0710-416c-95ef-59e51eba9982%28Office.15%29.aspx) element</span></span>  <br/> |<span data-ttu-id="cdd35-180">是</span><span class="sxs-lookup"><span data-stu-id="cdd35-180">Yes</span></span>  <br/> |<span data-ttu-id="cdd35-181">非定期约会的定期系列和定期系列的例外的单个匹配项</span><span class="sxs-lookup"><span data-stu-id="cdd35-181">Non-recurring appointments, single occurrences of recurring series, and exceptions to recurring series</span></span>  <br/> |
|[<span data-ttu-id="cdd35-182">ExchangeService.FindItems</span><span class="sxs-lookup"><span data-stu-id="cdd35-182">ExchangeService.FindItems</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="cdd35-183">[FindItem 操作](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)与[IndexedPageItemView](http://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx)元素或[FractionalPageItemView](http://msdn.microsoft.com/library/4111afec-35e7-4c6f-b291-9bbba603f633%28Office.15%29.aspx)元素</span><span class="sxs-lookup"><span data-stu-id="cdd35-183">[FindItem operation](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) with an [IndexedPageItemView](http://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) element or [FractionalPageItemView](http://msdn.microsoft.com/library/4111afec-35e7-4c6f-b291-9bbba603f633%28Office.15%29.aspx) element</span></span>  <br/> |<span data-ttu-id="cdd35-184">否</span><span class="sxs-lookup"><span data-stu-id="cdd35-184">No</span></span>  <br/> |<span data-ttu-id="cdd35-185">非定期约会和主控形状的定期约会</span><span class="sxs-lookup"><span data-stu-id="cdd35-185">Non-recurring appointments and recurring master appointments</span></span>  <br/> |
   
<span data-ttu-id="cdd35-186">Sadie 只是已签名她的孩子为游泳团队。</span><span class="sxs-lookup"><span data-stu-id="cdd35-186">Sadie has just signed her son up for swim team.</span></span> <span data-ttu-id="cdd35-187">团队有实践上午 8:30，在每个星期三上午开头 7 月 2 日，最后一个实践正在上年 8 月 6。</span><span class="sxs-lookup"><span data-stu-id="cdd35-187">The team has practice every Wednesday morning at 8:30 AM, starting July 2, with the last practice being on August 6.</span></span> <span data-ttu-id="cdd35-188">不希望忘记实践，Sadie 添加到其日历提醒她的定期约会。</span><span class="sxs-lookup"><span data-stu-id="cdd35-188">Not wanting to forget about practice, Sadie adds a recurring appointment to her calendar to remind her.</span></span>
  
<span data-ttu-id="cdd35-189">**表 4。Sadie 的定期约会**</span><span class="sxs-lookup"><span data-stu-id="cdd35-189">**Table 4. Sadie's recurring appointment**</span></span>

|<span data-ttu-id="cdd35-190">**约会字段**</span><span class="sxs-lookup"><span data-stu-id="cdd35-190">**Appointment field**</span></span>|<span data-ttu-id="cdd35-191">**值**</span><span class="sxs-lookup"><span data-stu-id="cdd35-191">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cdd35-192">主题</span><span class="sxs-lookup"><span data-stu-id="cdd35-192">Subject</span></span>  <br/> |<span data-ttu-id="cdd35-193">Swim 团队实践</span><span class="sxs-lookup"><span data-stu-id="cdd35-193">Swim Team Practice</span></span>  <br/> |
|<span data-ttu-id="cdd35-194">入门</span><span class="sxs-lookup"><span data-stu-id="cdd35-194">Start</span></span>  <br/> |<span data-ttu-id="cdd35-195">上午 8:30 2014 年 7 月 2日日</span><span class="sxs-lookup"><span data-stu-id="cdd35-195">July 2, 2014 8:30 AM</span></span>  <br/> |
|<span data-ttu-id="cdd35-196">End</span><span class="sxs-lookup"><span data-stu-id="cdd35-196">End</span></span>  <br/> |<span data-ttu-id="cdd35-197">10:00 2014 年 7 月 2日日</span><span class="sxs-lookup"><span data-stu-id="cdd35-197">July 2, 2014 10:00 AM</span></span>  <br/> |
|<span data-ttu-id="cdd35-198">重复</span><span class="sxs-lookup"><span data-stu-id="cdd35-198">Recurs</span></span>  <br/> |<span data-ttu-id="cdd35-199">每个星期三</span><span class="sxs-lookup"><span data-stu-id="cdd35-199">Every Wednesday</span></span>  <br/> |
|<span data-ttu-id="cdd35-200">最后一个匹配项</span><span class="sxs-lookup"><span data-stu-id="cdd35-200">Last occurrence</span></span>  <br/> |<span data-ttu-id="cdd35-201">上午 8:30 2014 年 8 月 6日日</span><span class="sxs-lookup"><span data-stu-id="cdd35-201">August 6, 2014 8:30 AM</span></span>  <br/> |
   
<span data-ttu-id="cdd35-202">快速介绍一下日历显示小组有六个实践总数。</span><span class="sxs-lookup"><span data-stu-id="cdd35-202">A quick look at a calendar shows that the team will have a total of six practices.</span></span> <span data-ttu-id="cdd35-203">但是，没有在日历中的六个不同的约会项目。</span><span class="sxs-lookup"><span data-stu-id="cdd35-203">However, there aren't six distinct appointment items in the calendar.</span></span> <span data-ttu-id="cdd35-204">而是只有一个代表系列的定期主约会。</span><span class="sxs-lookup"><span data-stu-id="cdd35-204">Instead, there is just one recurring master appointment representing the series.</span></span>
  
<span data-ttu-id="cdd35-205">现在让我们看一下查找 Sadie 的日历年 7 月内发生的约会。</span><span class="sxs-lookup"><span data-stu-id="cdd35-205">Now let's look at finding appointments on Sadie's calendar that occur within the month of July.</span></span> <span data-ttu-id="cdd35-206">下面的代码示例使用 Exchange 托管 API 中的**FindItems**方法，以生成 Sadie 的日历的非扩展视图。</span><span class="sxs-lookup"><span data-stu-id="cdd35-206">The following code example uses the **FindItems** method in the Exchange Managed API to produce a non-expanded view of Sadie's calendar.</span></span> 
  
```cs
PropertySet propSet = new PropertySet(AppointmentSchema.Subject,
                                      AppointmentSchema.Location,
                                      AppointmentSchema.Start, 
                                      AppointmentSchema.End,
                                      AppointmentSchema.AppointmentType);
#region FindItems + ItemView method
ItemView itemView = new ItemView(100);
itemView.PropertySet = propSet;
List<SearchFilter> filterList = new List<SearchFilter>();
// Find appointments that start after midnight on July 1, 2014.
SearchFilter.IsGreaterThan startFilter = new SearchFilter.IsGreaterThan(AppointmentSchema.Start,
    new DateTime(2014, 7, 1));
// Find appointments that end before midnight on July 31, 2014
SearchFilter.IsLessThan endFilter = new SearchFilter.IsLessThan(AppointmentSchema.End,
    new DateTime(2014, 7, 31));
filterList.Add(startFilter);
filterList.Add(endFilter);
SearchFilter.SearchFilterCollection calendarFilter = new SearchFilter.SearchFilterCollection(LogicalOperator.And, filterList);
// This results in a call to EWS.
FindItemsResults<Item> results = service.FindItems(WellKnownFolderName.Calendar, calendarFilter, itemView);
foreach(Item appt in results.Items)
{
    Console.WriteLine(appt.Subject);
}
```

<span data-ttu-id="cdd35-207">该代码将导致以下[FindItem 操作](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)请求与[IndexedPageItemView](http://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx)元素。</span><span class="sxs-lookup"><span data-stu-id="cdd35-207">That code results in the following [FindItem operation](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) request with an [IndexedPageItemView](http://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) element.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Pacific Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="calendar:Location" />
          <t:FieldURI FieldURI="calendar:Start" />
          <t:FieldURI FieldURI="calendar:End" />
          <t:FieldURI FieldURI="calendar:CalendarItemType" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="100" Offset="0" BasePoint="Beginning" />
      <m:Restriction>
        <t:And>
          <t:IsGreaterThan>
            <t:FieldURI FieldURI="calendar:Start" />
            <t:FieldURIOrConstant>
              <t:Constant Value="2014-07-01T07:00:00.000Z" />
            </t:FieldURIOrConstant>
          </t:IsGreaterThan>
          <t:IsLessThan>
            <t:FieldURI FieldURI="calendar:End" />
            <t:FieldURIOrConstant>
              <t:Constant Value="2014-07-31T07:00:00.000Z" />
            </t:FieldURIOrConstant>
          </t:IsLessThan>
        </t:And>
      </m:Restriction>
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="calendar" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="cdd35-208">服务器响应包含只有一个项目，定期主控形状，由**RecurringMaster** [CalendarItemType](http://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx)元素值。</span><span class="sxs-lookup"><span data-stu-id="cdd35-208">The server's response includes only a single item, the recurring master, indicated by the [CalendarItemType](http://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx) element value of **RecurringMaster**.</span></span> <span data-ttu-id="cdd35-209">为便于阅读缩短了[ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)元素的值。</span><span class="sxs-lookup"><span data-stu-id="cdd35-209">The value of the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) element has been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="939" MinorBuildNumber="16" Version="V2_11" 
        xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="1" TotalItemsInView="1" IncludesLastItemInRange="true">
            <t:Items>
              <t:CalendarItem>
                <t:ItemId Id="AAMkADA5..." ChangeKey="DwAAABYA..." />
                <t:Subject>Swim Team Practice</t:Subject>
                <t:Start>2014-07-02T15:30:00Z</t:Start>
                <t:End>2014-07-02T17:00:00Z</t:End>
                <t:Location>Neighborhood Swimming Pool</t:Location>
                <t:CalendarItemType>RecurringMaster</t:CalendarItemType>
              </t:CalendarItem>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="cdd35-210">现在让我们比较与扩展视图。</span><span class="sxs-lookup"><span data-stu-id="cdd35-210">Now let's compare with an expanded view.</span></span> <span data-ttu-id="cdd35-211">下面的代码示例使用 EWS 托管 API 中的**FindAppointments**方法来创建扩展的 Sadie 的日历视图。</span><span class="sxs-lookup"><span data-stu-id="cdd35-211">The following code example uses the **FindAppointments** method in the EWS Managed API to create an expanded view of Sadie's calendar.</span></span> 
  
```cs
PropertySet propSet = new PropertySet(AppointmentSchema.Subject,
                                      AppointmentSchema.Location,
                                      AppointmentSchema.Start, 
                                      AppointmentSchema.End,
                                      AppointmentSchema.AppointmentType);
CalendarView calView = new CalendarView(new DateTime(2014, 7, 1),
    new DateTime(2014, 7, 31));
calView.PropertySet = propSet;
FindItemsResults<Appointment> results = service.FindAppointments(WellKnownFolderName.Calendar, calView);
foreach(Appointment appt in results.Items)
{
    Console.WriteLine(appt.Subject);
}
```

<span data-ttu-id="cdd35-212">此代码将导致以下[FindItem 操作](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)请求[CalendarView](http://msdn.microsoft.com/library/a4a953b8-0710-416c-95ef-59e51eba9982%28Office.15%29.aspx)元素。</span><span class="sxs-lookup"><span data-stu-id="cdd35-212">This code results in the following [FindItem operation](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) request with a [CalendarView](http://msdn.microsoft.com/library/a4a953b8-0710-416c-95ef-59e51eba9982%28Office.15%29.aspx) element.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Pacific Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="calendar:Location" />
          <t:FieldURI FieldURI="calendar:Start" />
          <t:FieldURI FieldURI="calendar:End" />
          <t:FieldURI FieldURI="calendar:CalendarItemType" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:CalendarView StartDate="2014-07-01T07:00:00.000Z" EndDate="2014-07-31T07:00:00.000Z" />
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="calendar" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="cdd35-213">此时，服务器响应包括五个匹配项，一个用于年 7 月中的每个星期三。</span><span class="sxs-lookup"><span data-stu-id="cdd35-213">This time, the server response includes five occurrences, one for each Wednesday in July.</span></span> <span data-ttu-id="cdd35-214">所有这些项上的[CalendarItemType](http://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx)元素具有**匹配项**的值。</span><span class="sxs-lookup"><span data-stu-id="cdd35-214">The [CalendarItemType](http://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx) elements on these items all have a value of **Occurrence**.</span></span> <span data-ttu-id="cdd35-215">请注意定期主不存在的响应中。</span><span class="sxs-lookup"><span data-stu-id="cdd35-215">Note that the recurring master is not present in the response.</span></span> <span data-ttu-id="cdd35-216">为便于阅读变短了[ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)元素的值。</span><span class="sxs-lookup"><span data-stu-id="cdd35-216">The values of the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="939" MinorBuildNumber="16" Version="V2_11" 
        xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder TotalItemsInView="5" IncludesLastItemInRange="true">
            <t:Items>
              <t:CalendarItem>
                <t:ItemId Id="AAMkADA6..." ChangeKey="DwAAABYA..." />
                <t:Subject>Swim Team Practice</t:Subject>
                <t:Start>2014-07-02T15:30:00Z</t:Start>
                <t:End>2014-07-02T17:00:00Z</t:End>
                <t:Location>Neighborhood Swimming Pool</t:Location>
                <t:CalendarItemType>Occurrence</t:CalendarItemType>
              </t:CalendarItem>
              <t:CalendarItem>
                <t:ItemId Id="AAMkADA7..." ChangeKey="DwAAABYA..." />
                <t:Subject>Swim Team Practice</t:Subject>
                <t:Start>2014-07-09T15:30:00Z</t:Start>
                <t:End>2014-07-09T17:00:00Z</t:End>
                <t:Location>Neighborhood Swimming Pool</t:Location>
                <t:CalendarItemType>Occurrence</t:CalendarItemType>
              </t:CalendarItem>
              <t:CalendarItem>
                <t:ItemId Id="AAMkADA8..." ChangeKey="DwAAABYA..." />
                <t:Subject>Swim Team Practice</t:Subject>
                <t:Start>2014-07-16T15:30:00Z</t:Start>
                <t:End>2014-07-16T17:00:00Z</t:End>
                <t:Location>Neighborhood Swimming Pool</t:Location>
                <t:CalendarItemType>Occurrence</t:CalendarItemType>
              </t:CalendarItem>
              <t:CalendarItem>
                <t:ItemId Id="AAMkADA9..." ChangeKey="DwAAABYA..." />
                <t:Subject>Swim Team Practice</t:Subject>
                <t:Start>2014-07-23T15:30:00Z</t:Start>
                <t:End>2014-07-23T17:00:00Z</t:End>
                <t:Location>Neighborhood Swimming Pool</t:Location>
                <t:CalendarItemType>Occurrence</t:CalendarItemType>
              </t:CalendarItem>
              <t:CalendarItem>
                <t:ItemId Id="AAMkADAA..." ChangeKey="DwAAABYA..." />
                <t:Subject>Swim Team Practice</t:Subject>
                <t:Start>2014-07-30T15:30:00Z</t:Start>
                <t:End>2014-07-30T17:00:00Z</t:End>
                <t:Location>Neighborhood Swimming Pool</t:Location>
                <t:CalendarItemType>Occurrence</t:CalendarItemType>
              </t:CalendarItem>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="cdd35-217">定期主控形状、 发生或异常后，您始终可以[检索的其他相关的项](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="cdd35-217">After you have a recurring master, an occurrence, or an exception, you can always [retrieve the other related items](how-to-access-a-recurring-series-by-using-ews-in-exchange.md).</span></span> <span data-ttu-id="cdd35-218">给定的匹配项或异常，您可以检索定期主控形状，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="cdd35-218">Given an occurrence or exception, you can retrieve the recurring master, and vice versa.</span></span>
  
## <a name="working-with-recurring-calendar-items"></a><span data-ttu-id="cdd35-219">使用定期日历项目</span><span class="sxs-lookup"><span data-stu-id="cdd35-219">Working with recurring calendar items</span></span>

<span data-ttu-id="cdd35-220">您使用统一的方法和操作来处理定期系列使用以使用非定期日历项目。</span><span class="sxs-lookup"><span data-stu-id="cdd35-220">You use all the same methods and operations to work with recurring series as you use to work with non-recurring calendar items.</span></span> <span data-ttu-id="cdd35-221">不同之处在于，具体取决于您使用这些操作或方法调用该项目，您采取的操作可以应用于整个数据系列或只发生一次。</span><span class="sxs-lookup"><span data-stu-id="cdd35-221">The difference is that, depending on the item you use to invoke those methods or operations, the actions you take can apply to the entire series, or just a single occurrence.</span></span> <span data-ttu-id="cdd35-222">[定期母版上执行的操作](how-to-update-a-recurring-series-by-using-ews-in-exchange.md)将应用于系列中所有匹配项时[执行一次或异常的操作](how-to-update-a-recurring-series-by-using-ews.md)将只应用于该出现或异常。</span><span class="sxs-lookup"><span data-stu-id="cdd35-222">[Actions taken on the recurring master](how-to-update-a-recurring-series-by-using-ews-in-exchange.md) will apply to all occurrences in the series, while [actions taken to a single occurrence or exception](how-to-update-a-recurring-series-by-using-ews.md) will only apply to that occurrence or exception.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="cdd35-223">本节内容</span><span class="sxs-lookup"><span data-stu-id="cdd35-223">In this section</span></span>

- [<span data-ttu-id="cdd35-224">在 Exchange 中使用 EWS 访问定期系列</span><span class="sxs-lookup"><span data-stu-id="cdd35-224">Access a recurring series by using EWS in Exchange</span></span>](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="cdd35-225">使用 EWS 在 Exchange 中创建定期系列</span><span class="sxs-lookup"><span data-stu-id="cdd35-225">Create a recurring series by using EWS in Exchange</span></span>](how-to-create-a-recurring-series-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="cdd35-226">使用 EWS 在 Exchange 中删除定期系列中的约会</span><span class="sxs-lookup"><span data-stu-id="cdd35-226">Delete appointments in a recurring series by using EWS in Exchange</span></span>](how-to-delete-appointments-in-a-recurring-series-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="cdd35-227">使用 EWS 更新定期系列</span><span class="sxs-lookup"><span data-stu-id="cdd35-227">Update a recurring series by using EWS</span></span>](how-to-update-a-recurring-series-by-using-ews.md)
    
- [<span data-ttu-id="cdd35-228">在 Exchange 使用 EWS 更新定期系列</span><span class="sxs-lookup"><span data-stu-id="cdd35-228">Update a recurring series by using EWS in Exchange</span></span>](how-to-update-a-recurring-series-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="cdd35-229">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cdd35-229">See also</span></span>


- [<span data-ttu-id="cdd35-230">Calendars and EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="cdd35-230">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    
- [<span data-ttu-id="cdd35-231">开发 Exchange Web 服务客户端</span><span class="sxs-lookup"><span data-stu-id="cdd35-231">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    
- [<span data-ttu-id="cdd35-232">在 Exchange 使用 EWS 获取约会和会议</span><span class="sxs-lookup"><span data-stu-id="cdd35-232">Get appointments and meetings by using EWS in Exchange</span></span>](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)
    

