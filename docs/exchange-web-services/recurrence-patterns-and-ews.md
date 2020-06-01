---
title: 定期模式和 EWS
manager: luken
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fd9ef706-1e01-49fa-af6f-2f6d3e173c16
description: 了解 Exchange 中的定期模式和定期系列。
ms.openlocfilehash: 681dfee7e0a66a483b8638810da5e4e0ac0f05ac
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459326"
---
# <a name="recurrence-patterns-and-ews"></a><span data-ttu-id="014ea-103">定期模式和 EWS</span><span class="sxs-lookup"><span data-stu-id="014ea-103">Recurrence patterns and EWS</span></span>

<span data-ttu-id="014ea-104">了解 Exchange 中的定期模式和定期系列。</span><span class="sxs-lookup"><span data-stu-id="014ea-104">Learn about recurrence patterns and recurring series in Exchange.</span></span>
  
<span data-ttu-id="014ea-105">定期系列是根据定义的模式重复的约会或会议。</span><span class="sxs-lookup"><span data-stu-id="014ea-105">A recurring series is an appointment or meeting that repeats according to a defined pattern.</span></span> <span data-ttu-id="014ea-106">定期系列可以有特定次数，也可以无限重复。</span><span class="sxs-lookup"><span data-stu-id="014ea-106">A recurring series can either have a specific number of occurrences or can repeat indefinitely.</span></span> <span data-ttu-id="014ea-107">此外，定期系列也可能具有不遵循其余事件的模式的例外，并且可能会发生已从模式中删除的事件。</span><span class="sxs-lookup"><span data-stu-id="014ea-107">Additionally, a recurring series can have exceptions that don't follow the pattern of the rest of the occurrences, and can have occurrences that have been deleted from the pattern.</span></span> <span data-ttu-id="014ea-108">您可以使用 EWS 托管 API 和 EWS 来处理定期系列及其关联的日历项目。</span><span class="sxs-lookup"><span data-stu-id="014ea-108">You can use the EWS Managed API and EWS to work with recurring series and their associated calendar items.</span></span>
  
## <a name="recurring-calendar-items"></a><span data-ttu-id="014ea-109">定期日历项目</span><span class="sxs-lookup"><span data-stu-id="014ea-109">Recurring calendar items</span></span>

<span data-ttu-id="014ea-110">所有日历项目都属于以下四种类别之一：</span><span class="sxs-lookup"><span data-stu-id="014ea-110">All calendar items fall into one of the following four categories:</span></span>
  
- <span data-ttu-id="014ea-111">非定期日历项目</span><span class="sxs-lookup"><span data-stu-id="014ea-111">Non-recurring calendar items</span></span>
    
- <span data-ttu-id="014ea-112">定期母版</span><span class="sxs-lookup"><span data-stu-id="014ea-112">Recurring masters</span></span>
    
- <span data-ttu-id="014ea-113">系列中的匹配项</span><span class="sxs-lookup"><span data-stu-id="014ea-113">Occurrences in a series</span></span>
    
- <span data-ttu-id="014ea-114">修改了系列（称为 "异常"）中的匹配项</span><span class="sxs-lookup"><span data-stu-id="014ea-114">Modified occurrences in a series, known as exceptions</span></span>
    
<span data-ttu-id="014ea-115">在本文中，我们将查看属于定期系列的三种类型的日历项目。</span><span class="sxs-lookup"><span data-stu-id="014ea-115">In this article, we'll look at the three types of calendar items that are part of a recurring series.</span></span>
  
<span data-ttu-id="014ea-116">了解如何在 Exchange 服务器上实施定期系列。</span><span class="sxs-lookup"><span data-stu-id="014ea-116">It's helpful to understand how recurring series are implemented on the Exchange server.</span></span> <span data-ttu-id="014ea-117">服务器只会在日历中创建一个实际项目（称为 "定期母版"），而不是为定期系列中的每个事件创建单独的不同项目。</span><span class="sxs-lookup"><span data-stu-id="014ea-117">Instead of creating a separate distinct item for each occurrence in a recurring series, the server creates only one actual item in the calendar, known as the recurring master.</span></span> <span data-ttu-id="014ea-118">定期母版的格式与非定期约会非常相似，并且添加了定期模式信息。</span><span class="sxs-lookup"><span data-stu-id="014ea-118">The format of a recurring master is very similar to a non-recurring appointment, with the addition of recurrence pattern information.</span></span> <span data-ttu-id="014ea-119">然后，服务器将根据定期模式（使用一个名为 "展开" 的过程）来响应客户端对约会信息的请求生成事件。</span><span class="sxs-lookup"><span data-stu-id="014ea-119">The server then generates occurrences based on the recurrence pattern in response to client requests for appointment information, using a process called expansion.</span></span> <span data-ttu-id="014ea-120">这些生成的事件不会永久存储在服务器上。</span><span class="sxs-lookup"><span data-stu-id="014ea-120">These generated occurrences are not permanently stored on the server.</span></span> <span data-ttu-id="014ea-121">这一点很重要，因为您搜索日历项目的方式将决定您接收的信息以及是否进行扩展。</span><span class="sxs-lookup"><span data-stu-id="014ea-121">This is important to understand because the way that you search for calendar items determines what information you receive and whether expansion occurs.</span></span>
  
## <a name="recurrence-patterns"></a><span data-ttu-id="014ea-122">定期模式</span><span class="sxs-lookup"><span data-stu-id="014ea-122">Recurrence patterns</span></span>

<span data-ttu-id="014ea-123">可使扩展成为可能的定期系列的关键部分是定期模式。</span><span class="sxs-lookup"><span data-stu-id="014ea-123">The key piece to a recurring series that makes expansion possible is the recurrence pattern.</span></span> <span data-ttu-id="014ea-124">定期母版中发现定期模式，并介绍了一组依据定期母版的日期和时间计算具体值的条件。</span><span class="sxs-lookup"><span data-stu-id="014ea-124">The recurrence pattern is found on the recurring master, and describes a set of criteria for calculating occurrences based on the date and time of the recurring master.</span></span>
  
<span data-ttu-id="014ea-125">**表1。可用定期模式**</span><span class="sxs-lookup"><span data-stu-id="014ea-125">**Table 1. Available recurrence patterns**</span></span>

|<span data-ttu-id="014ea-126">**EWS 托管 API 类**</span><span class="sxs-lookup"><span data-stu-id="014ea-126">**EWS Managed API class**</span></span>|<span data-ttu-id="014ea-127">**EWS 元素**</span><span class="sxs-lookup"><span data-stu-id="014ea-127">**EWS element**</span></span>|<span data-ttu-id="014ea-128">**示例**</span><span class="sxs-lookup"><span data-stu-id="014ea-128">**Examples**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="014ea-129">DailyPattern</span><span class="sxs-lookup"><span data-stu-id="014ea-129">Recurrence.DailyPattern</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.dailypattern%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="014ea-130">DailyRecurrence</span><span class="sxs-lookup"><span data-stu-id="014ea-130">DailyRecurrence</span></span>](https://msdn.microsoft.com/library/0aaf265d-b723-49c6-8e9c-9ba60141e9ab%28Office.15%29.aspx) <br/> |<span data-ttu-id="014ea-131">每日重复一次。</span><span class="sxs-lookup"><span data-stu-id="014ea-131">Repeat every day.</span></span>  <br/> <span data-ttu-id="014ea-132">每隔一天重复一次。</span><span class="sxs-lookup"><span data-stu-id="014ea-132">Repeat every other day.</span></span>  <br/> |
|[<span data-ttu-id="014ea-133">MonthlyPattern</span><span class="sxs-lookup"><span data-stu-id="014ea-133">Recurrence.MonthlyPattern</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.monthlypattern%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="014ea-134">AbsoluteMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="014ea-134">AbsoluteMonthlyRecurrence</span></span>](https://msdn.microsoft.com/library/178fa0ae-9dfc-417f-933c-d657d31c2161%28Office.15%29.aspx) <br/> |<span data-ttu-id="014ea-135">每月的第十天重复一次。</span><span class="sxs-lookup"><span data-stu-id="014ea-135">Repeat every month on the tenth day of the month.</span></span>  <br/> <span data-ttu-id="014ea-136">每隔一个月的第二十天重复每个月。</span><span class="sxs-lookup"><span data-stu-id="014ea-136">Repeat every other month on the twenty-first day of the month.</span></span>  <br/> |
|[<span data-ttu-id="014ea-137">RelativeMonthlyPattern</span><span class="sxs-lookup"><span data-stu-id="014ea-137">Recurrence.RelativeMonthlyPattern</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.relativemonthlypattern%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="014ea-138">RelativeMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="014ea-138">RelativeMonthlyRecurrence</span></span>](https://msdn.microsoft.com/library/a76595db-7460-44ac-ac2a-53241caa33a7%28Office.15%29.aspx) <br/> |<span data-ttu-id="014ea-139">在每月的第二个星期二重复此操作。</span><span class="sxs-lookup"><span data-stu-id="014ea-139">Repeat on the second Tuesday of every month.</span></span>  <br/> <span data-ttu-id="014ea-140">在每三个月的每月的第三个星期四重复。</span><span class="sxs-lookup"><span data-stu-id="014ea-140">Repeat on the third Thursday of the month every three months.</span></span>  <br/> |
|[<span data-ttu-id="014ea-141">RelativeYearlyPattern</span><span class="sxs-lookup"><span data-stu-id="014ea-141">Recurrence.RelativeYearlyPattern</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.relativeyearlypattern%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="014ea-142">RelativeYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="014ea-142">RelativeYearlyRecurrence</span></span>](https://msdn.microsoft.com/library/25b67876-9979-4a30-a637-357ea10a93b8%28Office.15%29.aspx) <br/> |<span data-ttu-id="014ea-143">在每年8月的第一个星期一重复此操作。</span><span class="sxs-lookup"><span data-stu-id="014ea-143">Repeat on the first Monday of August every year.</span></span>  <br/> |
|[<span data-ttu-id="014ea-144">WeeklyPattern</span><span class="sxs-lookup"><span data-stu-id="014ea-144">Recurrence.WeeklyPattern</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.weeklypattern%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="014ea-145">WeeklyRecurrence</span><span class="sxs-lookup"><span data-stu-id="014ea-145">WeeklyRecurrence</span></span>](https://msdn.microsoft.com/library/69c41dd5-597c-45bc-be3f-e2f2b5615aa3%28Office.15%29.aspx) <br/> |<span data-ttu-id="014ea-146">每星期一重复一次。</span><span class="sxs-lookup"><span data-stu-id="014ea-146">Repeat every Monday.</span></span>  <br/> <span data-ttu-id="014ea-147">每隔一个星期重复每个星期二和星期四。</span><span class="sxs-lookup"><span data-stu-id="014ea-147">Repeat every Tuesday and Thursday every other week.</span></span>  <br/> |
|[<span data-ttu-id="014ea-148">YearlyPattern</span><span class="sxs-lookup"><span data-stu-id="014ea-148">Recurrence.YearlyPattern</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.yearlypattern%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="014ea-149">AbsoluteYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="014ea-149">AbsoluteYearlyRecurrence</span></span>](https://msdn.microsoft.com/library/96f53e2c-3893-4f6e-a78a-ac179f45c5db%28Office.15%29.aspx) <br/> |<span data-ttu-id="014ea-150">每年的第9月重复一次。</span><span class="sxs-lookup"><span data-stu-id="014ea-150">Repeat on September 1st every year.</span></span>  <br/> |
   
<span data-ttu-id="014ea-151">定期模式的另一条重要信息是定期结束的时间。</span><span class="sxs-lookup"><span data-stu-id="014ea-151">The other important piece of information for a recurrence pattern is when the recurrence ends.</span></span> <span data-ttu-id="014ea-152">这可表示为一组的出现次数、结束日期或没有结束日期。</span><span class="sxs-lookup"><span data-stu-id="014ea-152">This can be expressed as either a set number of occurrences, as an end date, or as having no end.</span></span>
  
<span data-ttu-id="014ea-153">**表2。定期系列结束的选项**</span><span class="sxs-lookup"><span data-stu-id="014ea-153">**Table 2. Options for the end of a recurring series**</span></span>

|<span data-ttu-id="014ea-154">**EWS 托管 API 方法/属性**</span><span class="sxs-lookup"><span data-stu-id="014ea-154">**EWS Managed API method/property**</span></span>|<span data-ttu-id="014ea-155">**EWS 元素**</span><span class="sxs-lookup"><span data-stu-id="014ea-155">**EWS element**</span></span>|<span data-ttu-id="014ea-156">**说明**</span><span class="sxs-lookup"><span data-stu-id="014ea-156">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="014ea-157">NumberOfOccurrences</span><span class="sxs-lookup"><span data-stu-id="014ea-157">Recurrence.NumberOfOccurrences</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.numberofoccurrences%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="014ea-158">NumberedRecurrence</span><span class="sxs-lookup"><span data-stu-id="014ea-158">NumberedRecurrence</span></span>](https://msdn.microsoft.com/library/53746909-ef21-4764-8715-a7769b943cca%28Office.15%29.aspx) <br/> |<span data-ttu-id="014ea-159">此属性或元素的值指定出现的次数。</span><span class="sxs-lookup"><span data-stu-id="014ea-159">The value of this property or element specifies the number of occurrences.</span></span>  <br/> |
|[<span data-ttu-id="014ea-160">定期结束日期</span><span class="sxs-lookup"><span data-stu-id="014ea-160">Recurrence.EndDate</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.enddate%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="014ea-161">EndDateRecurrence</span><span class="sxs-lookup"><span data-stu-id="014ea-161">EndDateRecurrence</span></span>](https://msdn.microsoft.com/library/a5ee2504-db84-49ee-870c-cca9269f2e26%28Office.15%29.aspx) <br/> |<span data-ttu-id="014ea-162">系列中的最后一个匹配项位于此属性或元素指定的日期之前或之前。</span><span class="sxs-lookup"><span data-stu-id="014ea-162">The last occurrence in the series falls on or before the date specified by this property or element.</span></span>  <br/> |
|[<span data-ttu-id="014ea-163">HasEnd</span><span class="sxs-lookup"><span data-stu-id="014ea-163">Recurrence.HasEnd</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.hasend%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="014ea-164">NeverEnds</span><span class="sxs-lookup"><span data-stu-id="014ea-164">Recurrence.NeverEnds</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.neverends%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="014ea-165">NoEndRecurrence</span><span class="sxs-lookup"><span data-stu-id="014ea-165">NoEndRecurrence</span></span>](https://msdn.microsoft.com/library/ab2ebd9c-388e-45f1-abf9-56e293ef123b%28Office.15%29.aspx) <br/> |<span data-ttu-id="014ea-166">系列没有结尾。</span><span class="sxs-lookup"><span data-stu-id="014ea-166">The series has no end.</span></span>  <br/> |
   
## <a name="expanded-vs-non-expanded-views"></a><span data-ttu-id="014ea-167">展开和未展开的视图</span><span class="sxs-lookup"><span data-stu-id="014ea-167">Expanded vs. non-expanded views</span></span>

<span data-ttu-id="014ea-168">在 EWS 托管 API （或使用 EWS 中的**CalendarView**元素的**FindItem**操作）中使用**FindAppointments**方法可调用展开进程。</span><span class="sxs-lookup"><span data-stu-id="014ea-168">Using the **FindAppointments** method in the EWS Managed API (or the **FindItem** operation with a **CalendarView** element in EWS) invokes the expansion process.</span></span> <span data-ttu-id="014ea-169">这将从结果集中隐藏定期主约会，而是显示该定期系列的展开视图。</span><span class="sxs-lookup"><span data-stu-id="014ea-169">This hides recurring master appointments from the result set, and instead presents an expanded view of that recurring series.</span></span> <span data-ttu-id="014ea-170">在 "日历" 视图的参数中的定期主控形状的出现和例外情况将包含在结果集中。</span><span class="sxs-lookup"><span data-stu-id="014ea-170">Occurrences of and exceptions to the recurring master that fall within the parameters of the calendar view are included in the result set.</span></span> <span data-ttu-id="014ea-171">与此相反，在 EWS 托管 API （或在 EWS 中使用**IndexedPageItemView**或**FractionalPageItemView**元素的**FindItem**操作）中使用**FindItems**方法不会调用展开过程，并且不会包含事件和异常。</span><span class="sxs-lookup"><span data-stu-id="014ea-171">Conversely, using the **FindItems** method in the EWS Managed API (or the **FindItem** operation with a **IndexedPageItemView** or **FractionalPageItemView** element in EWS), does not invoke the expansion process, and occurrences and exceptions are not included.</span></span> <span data-ttu-id="014ea-172">我们来看一个比较这两种方法的示例。</span><span class="sxs-lookup"><span data-stu-id="014ea-172">Let's look at an example comparing the two methods.</span></span> 
  
<span data-ttu-id="014ea-173">**表3。查找约会的方法和操作**</span><span class="sxs-lookup"><span data-stu-id="014ea-173">**Table 3. Methods and operations for finding appointments**</span></span>

|<span data-ttu-id="014ea-174">**EWS 托管的 API 方法**</span><span class="sxs-lookup"><span data-stu-id="014ea-174">**EWS Managed API method**</span></span>|<span data-ttu-id="014ea-175">**EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="014ea-175">**EWS operation**</span></span>|<span data-ttu-id="014ea-176">**扩展系列？**</span><span class="sxs-lookup"><span data-stu-id="014ea-176">**Expands series?**</span></span>|<span data-ttu-id="014ea-177">**结果中包含的项**</span><span class="sxs-lookup"><span data-stu-id="014ea-177">**Items included in results**</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="014ea-178">ExchangeService。 FindAppointments</span><span class="sxs-lookup"><span data-stu-id="014ea-178">ExchangeService.FindAppointments</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="014ea-179">带有[CalendarView](https://msdn.microsoft.com/library/a4a953b8-0710-416c-95ef-59e51eba9982%28Office.15%29.aspx)元素的[FindItem 操作](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="014ea-179">[FindItem operation](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) with a [CalendarView](https://msdn.microsoft.com/library/a4a953b8-0710-416c-95ef-59e51eba9982%28Office.15%29.aspx) element</span></span>  <br/> |<span data-ttu-id="014ea-180">是</span><span class="sxs-lookup"><span data-stu-id="014ea-180">Yes</span></span>  <br/> |<span data-ttu-id="014ea-181">非定期约会、定期系列的单个事件和定期系列的例外</span><span class="sxs-lookup"><span data-stu-id="014ea-181">Non-recurring appointments, single occurrences of recurring series, and exceptions to recurring series</span></span>  <br/> |
|[<span data-ttu-id="014ea-182">ExchangeService。 FindItems</span><span class="sxs-lookup"><span data-stu-id="014ea-182">ExchangeService.FindItems</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="014ea-183">带有[IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx)元素或[FractionalPageItemView](https://msdn.microsoft.com/library/4111afec-35e7-4c6f-b291-9bbba603f633%28Office.15%29.aspx)元素的[FindItem 操作](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="014ea-183">[FindItem operation](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) with an [IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) element or [FractionalPageItemView](https://msdn.microsoft.com/library/4111afec-35e7-4c6f-b291-9bbba603f633%28Office.15%29.aspx) element</span></span>  <br/> |<span data-ttu-id="014ea-184">否</span><span class="sxs-lookup"><span data-stu-id="014ea-184">No</span></span>  <br/> |<span data-ttu-id="014ea-185">非定期约会和定期主约会</span><span class="sxs-lookup"><span data-stu-id="014ea-185">Non-recurring appointments and recurring master appointments</span></span>  <br/> |
   
<span data-ttu-id="014ea-186">Sadie 已为我们的 "泳道" 团队注册了她的儿子。</span><span class="sxs-lookup"><span data-stu-id="014ea-186">Sadie has just signed her son up for swim team.</span></span> <span data-ttu-id="014ea-187">团队每星期三上午8:30 上午（从7月2日）开始，最后一次实践在8月6日进行练习。</span><span class="sxs-lookup"><span data-stu-id="014ea-187">The team has practice every Wednesday morning at 8:30 AM, starting July 2, with the last practice being on August 6.</span></span> <span data-ttu-id="014ea-188">如果不想忘记实践，Sadie 会将定期约会添加到其日历以提醒她。</span><span class="sxs-lookup"><span data-stu-id="014ea-188">Not wanting to forget about practice, Sadie adds a recurring appointment to her calendar to remind her.</span></span>
  
<span data-ttu-id="014ea-189">**表4。Sadie 的定期约会**</span><span class="sxs-lookup"><span data-stu-id="014ea-189">**Table 4. Sadie's recurring appointment**</span></span>

|<span data-ttu-id="014ea-190">**约会域**</span><span class="sxs-lookup"><span data-stu-id="014ea-190">**Appointment field**</span></span>|<span data-ttu-id="014ea-191">**值**</span><span class="sxs-lookup"><span data-stu-id="014ea-191">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="014ea-192">Subject</span><span class="sxs-lookup"><span data-stu-id="014ea-192">Subject</span></span>  <br/> |<span data-ttu-id="014ea-193">泳道团队实践</span><span class="sxs-lookup"><span data-stu-id="014ea-193">Swim Team Practice</span></span>  <br/> |
|<span data-ttu-id="014ea-194">开始</span><span class="sxs-lookup"><span data-stu-id="014ea-194">Start</span></span>  <br/> |<span data-ttu-id="014ea-195">7月2日，2014 8:30 AM</span><span class="sxs-lookup"><span data-stu-id="014ea-195">July 2, 2014 8:30 AM</span></span>  <br/> |
|<span data-ttu-id="014ea-196">End</span><span class="sxs-lookup"><span data-stu-id="014ea-196">End</span></span>  <br/> |<span data-ttu-id="014ea-197">7月2日，2014 10:00 AM</span><span class="sxs-lookup"><span data-stu-id="014ea-197">July 2, 2014 10:00 AM</span></span>  <br/> |
|<span data-ttu-id="014ea-198">再次</span><span class="sxs-lookup"><span data-stu-id="014ea-198">Recurs</span></span>  <br/> |<span data-ttu-id="014ea-199">每个星期三</span><span class="sxs-lookup"><span data-stu-id="014ea-199">Every Wednesday</span></span>  <br/> |
|<span data-ttu-id="014ea-200">最后一个匹配项</span><span class="sxs-lookup"><span data-stu-id="014ea-200">Last occurrence</span></span>  <br/> |<span data-ttu-id="014ea-201">8月6日，2014 8:30 AM</span><span class="sxs-lookup"><span data-stu-id="014ea-201">August 6, 2014 8:30 AM</span></span>  <br/> |
   
<span data-ttu-id="014ea-202">快速查看 "日历" 表示该团队总共有六个实践。</span><span class="sxs-lookup"><span data-stu-id="014ea-202">A quick look at a calendar shows that the team will have a total of six practices.</span></span> <span data-ttu-id="014ea-203">但是，日历中没有六个截然不同的约会项目。</span><span class="sxs-lookup"><span data-stu-id="014ea-203">However, there aren't six distinct appointment items in the calendar.</span></span> <span data-ttu-id="014ea-204">相反，只有一个定期主机约会代表系列。</span><span class="sxs-lookup"><span data-stu-id="014ea-204">Instead, there is just one recurring master appointment representing the series.</span></span>
  
<span data-ttu-id="014ea-205">现在，我们来看看在 Sadie 的日历中查找七月发生的约会。</span><span class="sxs-lookup"><span data-stu-id="014ea-205">Now let's look at finding appointments on Sadie's calendar that occur within the month of July.</span></span> <span data-ttu-id="014ea-206">下面的代码示例使用 Exchange 托管 API 中的**FindItems**方法生成 Sadie 的日历的非展开视图。</span><span class="sxs-lookup"><span data-stu-id="014ea-206">The following code example uses the **FindItems** method in the Exchange Managed API to produce a non-expanded view of Sadie's calendar.</span></span> 
  
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

<span data-ttu-id="014ea-207">该代码将导致以下带有[IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx)元素的[FindItem 操作](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)请求。</span><span class="sxs-lookup"><span data-stu-id="014ea-207">That code results in the following [FindItem operation](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) request with an [IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) element.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="014ea-208">服务器响应仅包括单个项目，即定期主控形状，由[CalendarItemType](https://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx)元素值**RecurringMaster**指示。</span><span class="sxs-lookup"><span data-stu-id="014ea-208">The server's response includes only a single item, the recurring master, indicated by the [CalendarItemType](https://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx) element value of **RecurringMaster**.</span></span> <span data-ttu-id="014ea-209">为了提高可读性， [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)元素的值已缩短。</span><span class="sxs-lookup"><span data-stu-id="014ea-209">The value of the [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) element has been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="939" MinorBuildNumber="16" Version="V2_11" 
        xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="014ea-210">现在，让我们与展开的视图进行比较。</span><span class="sxs-lookup"><span data-stu-id="014ea-210">Now let's compare with an expanded view.</span></span> <span data-ttu-id="014ea-211">下面的代码示例使用 EWS 托管 API 中的**FindAppointments**方法来创建 Sadie 的日历的展开视图。</span><span class="sxs-lookup"><span data-stu-id="014ea-211">The following code example uses the **FindAppointments** method in the EWS Managed API to create an expanded view of Sadie's calendar.</span></span> 
  
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

<span data-ttu-id="014ea-212">此代码将导致以下带有[CalendarView](https://msdn.microsoft.com/library/a4a953b8-0710-416c-95ef-59e51eba9982%28Office.15%29.aspx)元素的[FindItem 操作](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)请求。</span><span class="sxs-lookup"><span data-stu-id="014ea-212">This code results in the following [FindItem operation](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) request with a [CalendarView](https://msdn.microsoft.com/library/a4a953b8-0710-416c-95ef-59e51eba9982%28Office.15%29.aspx) element.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="014ea-213">这次，服务器响应包含五次，每个7月一个星期三。</span><span class="sxs-lookup"><span data-stu-id="014ea-213">This time, the server response includes five occurrences, one for each Wednesday in July.</span></span> <span data-ttu-id="014ea-214">这些项上的[CalendarItemType](https://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx)元素都有值**发生**。</span><span class="sxs-lookup"><span data-stu-id="014ea-214">The [CalendarItemType](https://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx) elements on these items all have a value of **Occurrence**.</span></span> <span data-ttu-id="014ea-215">请注意，响应中不存在定期主控形状。</span><span class="sxs-lookup"><span data-stu-id="014ea-215">Note that the recurring master is not present in the response.</span></span> <span data-ttu-id="014ea-216">为了提高可读性， [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)元素的值已缩短。</span><span class="sxs-lookup"><span data-stu-id="014ea-216">The values of the [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="939" MinorBuildNumber="16" Version="V2_11" 
        xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="014ea-217">在有一个定期母版、一个事件或例外的情况下，您始终可以[检索其他相关项目](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="014ea-217">After you have a recurring master, an occurrence, or an exception, you can always [retrieve the other related items](how-to-access-a-recurring-series-by-using-ews-in-exchange.md).</span></span> <span data-ttu-id="014ea-218">在出现或异常的情况下，您可以检索定期母版，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="014ea-218">Given an occurrence or exception, you can retrieve the recurring master, and vice versa.</span></span>
  
## <a name="working-with-recurring-calendar-items"></a><span data-ttu-id="014ea-219">使用定期日历项目</span><span class="sxs-lookup"><span data-stu-id="014ea-219">Working with recurring calendar items</span></span>

<span data-ttu-id="014ea-220">您可以使用所有相同的方法和操作与定期系列配合使用，以处理非定期日历项目。</span><span class="sxs-lookup"><span data-stu-id="014ea-220">You use all the same methods and operations to work with recurring series as you use to work with non-recurring calendar items.</span></span> <span data-ttu-id="014ea-221">不同之处在于，根据您用于调用这些方法或操作的项目，所执行的操作可以应用于整个系列，也可以只应用于单个事件。</span><span class="sxs-lookup"><span data-stu-id="014ea-221">The difference is that, depending on the item you use to invoke those methods or operations, the actions you take can apply to the entire series, or just a single occurrence.</span></span> <span data-ttu-id="014ea-222">[对定期母版执行的操作](how-to-update-a-recurring-series-by-using-ews-in-exchange.md)将应用于系列中的所有事件，而[对单个事件或例外项执行的操作](how-to-update-a-recurring-series-by-using-ews.md)只会应用于该事件或例外。</span><span class="sxs-lookup"><span data-stu-id="014ea-222">[Actions taken on the recurring master](how-to-update-a-recurring-series-by-using-ews-in-exchange.md) will apply to all occurrences in the series, while [actions taken to a single occurrence or exception](how-to-update-a-recurring-series-by-using-ews.md) will only apply to that occurrence or exception.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="014ea-223">本节内容</span><span class="sxs-lookup"><span data-stu-id="014ea-223">In this section</span></span>

- [<span data-ttu-id="014ea-224">在 Exchange 中使用 EWS 访问定期系列</span><span class="sxs-lookup"><span data-stu-id="014ea-224">Access a recurring series by using EWS in Exchange</span></span>](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="014ea-225">使用 Exchange 中的 EWS 创建定期系列</span><span class="sxs-lookup"><span data-stu-id="014ea-225">Create a recurring series by using EWS in Exchange</span></span>](how-to-create-a-recurring-series-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="014ea-226">在 Exchange 中使用 EWS 删除定期系列中的约会</span><span class="sxs-lookup"><span data-stu-id="014ea-226">Delete appointments in a recurring series by using EWS in Exchange</span></span>](how-to-delete-appointments-in-a-recurring-series-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="014ea-227">使用 EWS 更新定期系列</span><span class="sxs-lookup"><span data-stu-id="014ea-227">Update a recurring series by using EWS</span></span>](how-to-update-a-recurring-series-by-using-ews.md)
    
- [<span data-ttu-id="014ea-228">在 Exchange 中使用 EWS 更新定期系列</span><span class="sxs-lookup"><span data-stu-id="014ea-228">Update a recurring series by using EWS in Exchange</span></span>](how-to-update-a-recurring-series-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="014ea-229">另请参阅</span><span class="sxs-lookup"><span data-stu-id="014ea-229">See also</span></span>


- [<span data-ttu-id="014ea-230">Calendars and EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="014ea-230">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    
- [<span data-ttu-id="014ea-231">开发 Exchange Web 服务客户端</span><span class="sxs-lookup"><span data-stu-id="014ea-231">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    
- [<span data-ttu-id="014ea-232">使用 Exchange 中的 EWS 获取约会和会议</span><span class="sxs-lookup"><span data-stu-id="014ea-232">Get appointments and meetings by using EWS in Exchange</span></span>](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)
    

