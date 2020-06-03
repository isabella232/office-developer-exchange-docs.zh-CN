---
title: 使用 Exchange 中的 EWS 执行分组搜索
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 55de92eb-8e8b-4156-8ad9-dd3828024242
description: 了解如何在面向 Exchange 的 EWS 托管 API 或 EWS 应用程序中执行分组搜索。
ms.openlocfilehash: 65c6f75ea6b8ab848a263349dcceceead52fa210
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527918"
---
# <a name="perform-grouped-searches-by-using-ews-in-exchange"></a><span data-ttu-id="479f0-103">使用 Exchange 中的 EWS 执行分组搜索</span><span class="sxs-lookup"><span data-stu-id="479f0-103">Perform grouped searches by using EWS in Exchange</span></span>

<span data-ttu-id="479f0-104">了解如何在面向 Exchange 的 EWS 托管 API 或 EWS 应用程序中执行分组搜索。</span><span class="sxs-lookup"><span data-stu-id="479f0-104">Find out how to perform grouped searches in your EWS Managed API or EWS application that targets Exchange.</span></span>
  
<span data-ttu-id="479f0-105">分组搜索可用于控制搜索结果的组织方式。</span><span class="sxs-lookup"><span data-stu-id="479f0-105">Grouped searches are useful in that they gives you control over how search results are organized.</span></span> <span data-ttu-id="479f0-106">组织的搜索结果可使应用程序更轻松地处理结果，或以可管理的方式将其显示给最终用户。</span><span class="sxs-lookup"><span data-stu-id="479f0-106">Organized search results can make it easier for your application to process results or display them to an end user in a manageable way.</span></span>
  
<span data-ttu-id="479f0-107">通过将结果集中具有相同的特定字段值的所有项放入一个组中，可以进行分组。</span><span class="sxs-lookup"><span data-stu-id="479f0-107">Grouping works by putting all items within the result set that have the same value of a specific field into a group.</span></span> <span data-ttu-id="479f0-108">例如，您可以按发件人对结果进行分组，同一个人中的所有项目都将位于单独的组中，并且每个组中的项目将根据您在视图中指定的顺序进行排序。</span><span class="sxs-lookup"><span data-stu-id="479f0-108">For example, you can group your results by the sender, and all items from the same person will be in a separate group, and the items within each group will be sorted according to the order you specify on the view.</span></span> <span data-ttu-id="479f0-109">根据所选的字段，组本身按聚合值进行排序。</span><span class="sxs-lookup"><span data-stu-id="479f0-109">The groups themselves are sorted by an aggregate value based on a field you choose.</span></span>
  
<span data-ttu-id="479f0-110">**表1。用于组织搜索结果的 EWS 托管 API 方法和 EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="479f0-110">**Table 1. EWS Managed API methods and EWS operations for organizing search results**</span></span>

|<span data-ttu-id="479f0-111">**如果您想要 .。。**</span><span class="sxs-lookup"><span data-stu-id="479f0-111">**If you want to…**</span></span>|<span data-ttu-id="479f0-112">**在 EWS 托管 API 中，使用 .。。**</span><span class="sxs-lookup"><span data-stu-id="479f0-112">**In the EWS Managed API, use…**</span></span>|<span data-ttu-id="479f0-113">**在 EWS 中，使用 .。。**</span><span class="sxs-lookup"><span data-stu-id="479f0-113">**In EWS, use…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="479f0-114">将结果中的特定属性中具有相同值的项目组织为组</span><span class="sxs-lookup"><span data-stu-id="479f0-114">Organize items with the same value in a specific property in your results into groups</span></span>  <br/> |[<span data-ttu-id="479f0-115">分组。 GroupOn</span><span class="sxs-lookup"><span data-stu-id="479f0-115">Grouping.GroupOn</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping.groupon%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="479f0-116">[FieldURI](https://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx)元素作为[GroupBy](https://msdn.microsoft.com/library/9728619b-4674-4b9d-9f6c-e75c6165966c%28Office.15%29.aspx)元素的子元素</span><span class="sxs-lookup"><span data-stu-id="479f0-116">[FieldURI](https://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) element as a child of the [GroupBy](https://msdn.microsoft.com/library/9728619b-4674-4b9d-9f6c-e75c6165966c%28Office.15%29.aspx) element</span></span>  <br/> |
|<span data-ttu-id="479f0-117">按特定属性中的值对每个组中的项目进行排序</span><span class="sxs-lookup"><span data-stu-id="479f0-117">Sort items within each group by the value in a specific property</span></span>  <br/> |[<span data-ttu-id="479f0-118">ItemView</span><span class="sxs-lookup"><span data-stu-id="479f0-118">ItemView.OrderBy</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview.orderby%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="479f0-119">[SortOrder](https://msdn.microsoft.com/library/c2413f0b-8c03-46ae-9990-13338b3c53a6%28Office.15%29.aspx)元素</span><span class="sxs-lookup"><span data-stu-id="479f0-119">[SortOrder](https://msdn.microsoft.com/library/c2413f0b-8c03-46ae-9990-13338b3c53a6%28Office.15%29.aspx) element</span></span>  <br/> |
|<span data-ttu-id="479f0-120">对组进行排序</span><span class="sxs-lookup"><span data-stu-id="479f0-120">Sort the groups</span></span>  <br/> |[<span data-ttu-id="479f0-121">分组。 AggregateOn</span><span class="sxs-lookup"><span data-stu-id="479f0-121">Grouping.AggregateOn</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping.aggregateon%28v=exchg.80%29.aspx) <br/><br/> [<span data-ttu-id="479f0-122">分组。 AggregateType</span><span class="sxs-lookup"><span data-stu-id="479f0-122">Grouping.AggregateType</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping.aggregatetype%28v=exchg.80%29.aspx) <br/><br/> [<span data-ttu-id="479f0-123">分组。 SortDirection</span><span class="sxs-lookup"><span data-stu-id="479f0-123">Grouping.SortDirection</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping.sortdirection%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="479f0-124">**FieldURI**元素作为[AggregateOn](https://msdn.microsoft.com/library/9b0a03f2-3282-46e1-b1a0-cbb9a0fbe9bb%28Office.15%29.aspx)元素的子元素</span><span class="sxs-lookup"><span data-stu-id="479f0-124">**FieldURI** element as a child of the [AggregateOn](https://msdn.microsoft.com/library/9b0a03f2-3282-46e1-b1a0-cbb9a0fbe9bb%28Office.15%29.aspx) element</span></span><br/><br/> <span data-ttu-id="479f0-125">**AggregateOn**元素上的**聚合**属性</span><span class="sxs-lookup"><span data-stu-id="479f0-125">**Aggregate** attribute on the **AggregateOn** element</span></span><br/><br/><span data-ttu-id="479f0-126">**GroupBy**元素上的**Order**属性</span><span class="sxs-lookup"><span data-stu-id="479f0-126">**Order** attribute on the **GroupBy** element</span></span>  <br/> |
   
<span data-ttu-id="479f0-127">让我们逐步执行此操作。</span><span class="sxs-lookup"><span data-stu-id="479f0-127">Let's take it step by step.</span></span>
  
## <a name="group-results-by-a-specific-property"></a><span data-ttu-id="479f0-128">按特定属性对结果进行分组</span><span class="sxs-lookup"><span data-stu-id="479f0-128">Group results by a specific property</span></span>
<span data-ttu-id="479f0-129"><a name="bk_GroupResults"> </a></span><span class="sxs-lookup"><span data-stu-id="479f0-129"><a name="bk_GroupResults"> </a></span></span>

<span data-ttu-id="479f0-130">使用分组的第一步是选择属性或 Exchange 存储中项的属性，以进行分组。</span><span class="sxs-lookup"><span data-stu-id="479f0-130">The first step to using grouping is to select a property, or attribute on the items in the Exchange store, to group by.</span></span> <span data-ttu-id="479f0-131">EWS 托管 API 在相应的类上将它们作为类属性公开，而 EWS 将它们公开为 XML 元素。</span><span class="sxs-lookup"><span data-stu-id="479f0-131">The EWS Managed API exposes these as class properties on the corresponding classes, while EWS exposes them as XML elements.</span></span> <span data-ttu-id="479f0-132">您可以选择任何属性，包括自定义或扩展属性，但它有助于了解如何根据所选属性的值对项目进行分组。</span><span class="sxs-lookup"><span data-stu-id="479f0-132">You can choose any property, including custom or extended properties, but it is helpful to understand how items are grouped based on the value of the property you choose.</span></span> 

<span data-ttu-id="479f0-133">选择 "分组依据" 属性中具有相同值的所有项目将组合在一起。</span><span class="sxs-lookup"><span data-stu-id="479f0-133">All items that have the same value in the property you choose to group by will be grouped together.</span></span> <span data-ttu-id="479f0-134">这看起来可能很明显，但这是一个重要的详细信息。</span><span class="sxs-lookup"><span data-stu-id="479f0-134">This might seem obvious, but it is an important detail.</span></span> <span data-ttu-id="479f0-135">如果按日期/时间属性（如在 EWS 托管 API 中的[DateTimeReceived](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.datetimereceived%28v=exchg.80%29.aspx)或 ews 中的[DateTimeReceived](https://msdn.microsoft.com/library/8f489bd4-2434-4d0a-91fe-1b5ba7eb5765%28Office.15%29.aspx)元素）进行分组，请考虑所发生的情况。</span><span class="sxs-lookup"><span data-stu-id="479f0-135">Consider what happens if you group by a date/time property, such as [Item.DateTimeReceived](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.datetimereceived%28v=exchg.80%29.aspx) in the EWS Managed API, or the [DateTimeReceived](https://msdn.microsoft.com/library/8f489bd4-2434-4d0a-91fe-1b5ba7eb5765%28Office.15%29.aspx) element in EWS.</span></span> <span data-ttu-id="479f0-136">目的可能是将结果组织到组中，每个组包含同一天的项目。</span><span class="sxs-lookup"><span data-stu-id="479f0-136">The intent might be to organize the results into groups, with each group containing items from the same day.</span></span> <span data-ttu-id="479f0-137">但是，分组将查看整个值，其中包括时间。</span><span class="sxs-lookup"><span data-stu-id="479f0-137">However, grouping looks at the entire value, which includes the time.</span></span> 

<span data-ttu-id="479f0-138">最终结果是将对项目进行分组，以便同时收到的项目在其自己的组中。</span><span class="sxs-lookup"><span data-stu-id="479f0-138">The end result is that the items will be grouped so that items received at the same time, down to the second, are in their own groups.</span></span> <span data-ttu-id="479f0-139">结果很可能被分类为大量的组，其中每个组中的项目数较少。</span><span class="sxs-lookup"><span data-stu-id="479f0-139">The results will most likely be sorted into a large number of groups with a small number of items in each group.</span></span> 
  
<span data-ttu-id="479f0-140">若要获取包含较少组以及每个组中的项目数较多的结果集，请选择一个可能具有较小数量的值的属性，例如[EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.from%28v=exchg.80%29.aspx)或 ews 中的[条目。](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.categories%28v=exchg.80%29.aspx)在 ews 托管 API 中的类别或从 ews 中[的](https://msdn.microsoft.com/library/5a52d644-3677-4049-874c-12bd5c3080dc%28Office.15%29.aspx)[类别](https://msdn.microsoft.com/library/d84d4927-b524-4e62-bf3d-1f12fec8c21a%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="479f0-140">To get a results set with a smaller number of groups and a larger number of items in each group, choose a property that is likely to have a smaller number of values, such as [EmailMessage.From](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.from%28v=exchg.80%29.aspx) or [Item.Categories](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.categories%28v=exchg.80%29.aspx) in the EWS Managed API, or [From](https://msdn.microsoft.com/library/5a52d644-3677-4049-874c-12bd5c3080dc%28Office.15%29.aspx) or [Categories](https://msdn.microsoft.com/library/d84d4927-b524-4e62-bf3d-1f12fec8c21a%28Office.15%29.aspx) in EWS.</span></span> <span data-ttu-id="479f0-141">下图显示了在收件箱中显示的电子邮件的列表。</span><span class="sxs-lookup"><span data-stu-id="479f0-141">The following figure shows a list of emails that appear in an Inbox.</span></span> 
  
<span data-ttu-id="479f0-142">**图1。收件箱中的邮件**</span><span class="sxs-lookup"><span data-stu-id="479f0-142">**Figure 1. Messages in an Inbox**</span></span>

![用户收件箱中的示例邮件列表。](media/Ex15_GroupedSearch_MsgList.png)
  
<span data-ttu-id="479f0-144">如果按**EmailMessage**属性对图1中的项进行分组，则结果将为两个组，一个用于由 "等待总额" 发送的邮件，另一个用于由 "Sadie Daniels" 发送的邮件。</span><span class="sxs-lookup"><span data-stu-id="479f0-144">If you group the items in Figure 1 by the **EmailMessage.From** property, the result will be two groups, one for messages sent by Hope Gross, and one for messages sent by Sadie Daniels.</span></span> 
  
<span data-ttu-id="479f0-145">**图2。根据 From 属性拆分为组的邮件**</span><span class="sxs-lookup"><span data-stu-id="479f0-145">**Figure 2. Messages separated into groups based on the From property**</span></span>

![此图显示按照发件人属性分为两个列表的邮件。](media/Ex15_GroupedSearch_SeparateGroups.png)
  
## <a name="sort-the-items-within-groups"></a><span data-ttu-id="479f0-147">对组中的项目进行排序</span><span class="sxs-lookup"><span data-stu-id="479f0-147">Sort the items within groups</span></span>
<span data-ttu-id="479f0-148"><a name="bk_SortItems"> </a></span><span class="sxs-lookup"><span data-stu-id="479f0-148"><a name="bk_SortItems"> </a></span></span>

<span data-ttu-id="479f0-149">您可以使用 EWS 托管 API 中的[ItemView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview.orderby%28v=exchg.80%29.aspx)属性或 ews 中的[SortOrder](https://msdn.microsoft.com/library/c2413f0b-8c03-46ae-9990-13338b3c53a6%28Office.15%29.aspx)元素，控制项目在每个组中的排序方式。</span><span class="sxs-lookup"><span data-stu-id="479f0-149">You can control how items are sorted within each group by using the [ItemView.OrderBy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview.orderby%28v=exchg.80%29.aspx) property in the EWS Managed API, or the [SortOrder](https://msdn.microsoft.com/library/c2413f0b-8c03-46ae-9990-13338b3c53a6%28Office.15%29.aspx) element in EWS.</span></span> <span data-ttu-id="479f0-150">此排序适用于每个组。</span><span class="sxs-lookup"><span data-stu-id="479f0-150">The same ordering applies to each group.</span></span> <span data-ttu-id="479f0-151">例如，如果按项目的顺序对图1中的项进行排序，则**DateTimeReceived**属性以降序排序，最近从 "期望总" 组中接收的项目将成为 "期望总" 组中的第一个，并且最近从 Sadie Daniels 收到的项目将是 Sadie Daniels 组中的第一个。</span><span class="sxs-lookup"><span data-stu-id="479f0-151">For example, if you sort the items from Figure 1 by the **Item.DateTimeReceived** property, in descending order, the item most recently received from Hope Gross will be first in the Hope Gross group, and the item most recently received from Sadie Daniels will be first in the Sadie Daniels group.</span></span> <span data-ttu-id="479f0-152">图2中的组可以方便地以这种方式排序。</span><span class="sxs-lookup"><span data-stu-id="479f0-152">Conveniently, the groups in Figure 2 are already sorted this way.</span></span> 
  
## <a name="sort-the-groups"></a><span data-ttu-id="479f0-153">对组进行排序</span><span class="sxs-lookup"><span data-stu-id="479f0-153">Sort the groups</span></span>
<span data-ttu-id="479f0-154"><a name="bk_SortGroups"> </a></span><span class="sxs-lookup"><span data-stu-id="479f0-154"><a name="bk_SortGroups"> </a></span></span>

<span data-ttu-id="479f0-155">现在，您已对组进行了结算，最后一步是对组本身进行排序。</span><span class="sxs-lookup"><span data-stu-id="479f0-155">Now that you have your groups settled, the final step is sorting the groups themselves.</span></span> <span data-ttu-id="479f0-156">由于组本身没有特定的值，因此分组过程必须将一个排序值分配给每个组。</span><span class="sxs-lookup"><span data-stu-id="479f0-156">Because the groups themselves have no specific values, the grouping process has to assign a sort value to each group.</span></span> <span data-ttu-id="479f0-157">这是通过对每个组中的特定属性的值（由 EWS 托管 API 中的[AggregateOn](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping.aggregateon%28v=exchg.80%29.aspx)属性指定）或[FieldURI](https://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx)元素（以 ews 中的[AggregateOn](https://msdn.microsoft.com/library/9b0a03f2-3282-46e1-b1a0-cbb9a0fbe9bb%28Office.15%29.aspx)元素的子元素）聚合来实现的。</span><span class="sxs-lookup"><span data-stu-id="479f0-157">This is done by aggregation of the values of a specific property within each group, specified by the [Grouping.AggregateOn](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping.aggregateon%28v=exchg.80%29.aspx) property in the EWS Managed API, or the [FieldURI](https://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) element as a child of the [AggregateOn](https://msdn.microsoft.com/library/9b0a03f2-3282-46e1-b1a0-cbb9a0fbe9bb%28Office.15%29.aspx) element in EWS.</span></span> <span data-ttu-id="479f0-158">EWS 托管 API （或 EWS 中**AggregateOn**元素的**Aggregate**属性）中的[AggregateType](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping.aggregatetype%28v=exchg.80%29.aspx)属性指定将每个组中的项目的值分配给该组的排序值（最大值或最小值）。</span><span class="sxs-lookup"><span data-stu-id="479f0-158">The [Grouping.AggregateType](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping.aggregatetype%28v=exchg.80%29.aspx) property in the EWS Managed API (or the **Aggregate** attribute on the **AggregateOn** element in EWS) specifies which value from the items within each group is assigned to the sort value for the group — either the largest value or the smallest value.</span></span> <span data-ttu-id="479f0-159">最后，排序顺序（降序或升序）由 EWS 托管 API 中的[SortDirection](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping.sortdirection%28v=exchg.80%29.aspx)属性或 ews 中的[GroupBy](https://msdn.microsoft.com/library/9728619b-4674-4b9d-9f6c-e75c6165966c%28Office.15%29.aspx)元素的**order**属性指定。</span><span class="sxs-lookup"><span data-stu-id="479f0-159">Finally, the sort order (descending or ascending) is specified by the [Grouping.SortDirection](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping.sortdirection%28v=exchg.80%29.aspx) property in the EWS Managed API, or the **Order** attribute on the [GroupBy](https://msdn.microsoft.com/library/9728619b-4674-4b9d-9f6c-e75c6165966c%28Office.15%29.aspx) element in EWS.</span></span> 
  
<span data-ttu-id="479f0-160">例如，如果按**DateTimeReceived**属性上的聚合对图2中的组进行排序，使用最小值并按降序排序，则按图3所示的顺序返回这些项。</span><span class="sxs-lookup"><span data-stu-id="479f0-160">For example, if the groups from Figure 2 are sorted by aggregating on the **Item.DateTimeReceived** property, using the smallest value, and sorting in descending order, the items are returned in the order in shown Figure 3.</span></span> 
  
<span data-ttu-id="479f0-161">**图3。按 DateTimeReceived 属性排序的组的分组搜索结果**</span><span class="sxs-lookup"><span data-stu-id="479f0-161">**Figure 3. Grouped search results with the groups sorted by the DateTimeReceived property**</span></span>

![此图显示邮件的已排序列表，按照发件人属性分组，各组按照接收的最小日期/时间排序。](media/Ex15_GroupedSearch_Results.png)
  
<span data-ttu-id="479f0-163">以下各节介绍了如何在代码中一起提取分组和排序。</span><span class="sxs-lookup"><span data-stu-id="479f0-163">The next sections show you how you might pull grouping and sorting together in code.</span></span>
  
## <a name="example-perform-a-grouped-search-by-using-the-ews-managed-api"></a><span data-ttu-id="479f0-164">示例：使用 EWS 托管 API 执行分组搜索</span><span class="sxs-lookup"><span data-stu-id="479f0-164">Example: Perform a grouped search by using the EWS Managed API</span></span>
<span data-ttu-id="479f0-165"><a name="bk_GroupSearchEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="479f0-165"><a name="bk_GroupSearchEWSMA"> </a></span></span>

<span data-ttu-id="479f0-166">下面的 EWS 托管 API 方法可以使用分组：</span><span class="sxs-lookup"><span data-stu-id="479f0-166">The following EWS Managed API methods can use grouping:</span></span>
  
- [<span data-ttu-id="479f0-167">ExchangeService。 FindItems</span><span class="sxs-lookup"><span data-stu-id="479f0-167">ExchangeService.FindItems</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="479f0-168">FindItems</span><span class="sxs-lookup"><span data-stu-id="479f0-168">Folder.FindItems</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)
    
<span data-ttu-id="479f0-169">下面的示例使用 FindItems 方法; **ExchangeService**但是，相同的规则和概念也适用于**FindItems**方法。</span><span class="sxs-lookup"><span data-stu-id="479f0-169">The following example uses the **ExchangeService.FindItems** method; however, the same rules and concepts apply to the **Folder.FindItems** method.</span></span> <span data-ttu-id="479f0-170">在此示例中，定义了一个名为**GroupItemsByFrom**的方法。</span><span class="sxs-lookup"><span data-stu-id="479f0-170">In this example, a method called **GroupItemsByFrom** is defined.</span></span> <span data-ttu-id="479f0-171">它采用[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象和[WellKnownFolderName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx)对象作为参数。</span><span class="sxs-lookup"><span data-stu-id="479f0-171">It takes an [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and a [WellKnownFolderName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) object as parameters.</span></span> <span data-ttu-id="479f0-172">它请求文件夹中的前50个项目，这些项目按**EmailMessage**属性分组，按**DateTimeReceived**属性的降序排列。</span><span class="sxs-lookup"><span data-stu-id="479f0-172">It requests the first 50 items in the folder, grouped by the **EmailMessage.From** property, sorted by the **Item.DateTimeReceived** property in descending order.</span></span> <span data-ttu-id="479f0-173">组本身按项目的最小**DateTimeReceived**属性值进行排序，以降序排列。</span><span class="sxs-lookup"><span data-stu-id="479f0-173">The groups themselves are sorted by the smallest **Item.DateTimeReceived** property value on their items, in descending order.</span></span> 
  
<span data-ttu-id="479f0-174">此示例假定已使用[凭据](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx)和[Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx)属性中的有效值对**ExchangeService**对象进行了初始化。</span><span class="sxs-lookup"><span data-stu-id="479f0-174">This example assumes that the **ExchangeService** object has been initialized with valid values in the [Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) and [Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) properties.</span></span> 
  
```cs
static void GroupItemsByFrom(ExchangeService service, WellKnownFolderName folder)
{
    // Limit the result set to 50 items.
    ItemView view = new ItemView(50);
    view.PropertySet = new PropertySet(ItemSchema.Subject,
                                       ItemSchema.DateTimeReceived,
                                       EmailMessageSchema.From,
                                       ItemSchema.Categories);
    // Item searches do not support Deep traversal.
    view.Traversal = ItemTraversal.Shallow;
    // Specify the sorting done within the groups.
    view.OrderBy.Add(ItemSchema.DateTimeReceived, SortDirection.Descending);
    // Configure grouping.
    Grouping groupByFrom = new Grouping();
    groupByFrom.GroupOn = EmailMessageSchema.From;
    groupByFrom.AggregateOn = ItemSchema.DateTimeReceived;
    groupByFrom.AggregateType = AggregateType.Minimum;
    groupByFrom.SortDirection = SortDirection.Descending;
    try
    {
        GroupedFindItemsResults<Item> results = service.FindItems(folder,
            view, groupByFrom);
        foreach (ItemGroup<Item> group in results.ItemGroups)
        {
            Console.WriteLine("Group: {0}", group.GroupIndex);
            foreach (Item item in group.Items)
            {
                if (item is EmailMessage)
                {
                    EmailMessage message = item as EmailMessage;
                    Console.WriteLine("From: {0}", message.From);
                    Console.WriteLine("Subject: {0}", message.Subject);
                    Console.WriteLine("Id: {0}\n", message.Id.ToString());
                }
            }
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine("Exception while enumerating results: {0}", ex.Message);
    }
}
```

## <a name="example-perform-a-grouped-search-by-using-ews"></a><span data-ttu-id="479f0-175">示例：使用 EWS 执行分组搜索</span><span class="sxs-lookup"><span data-stu-id="479f0-175">Example: Perform a grouped search by using EWS</span></span>
<span data-ttu-id="479f0-176"><a name="bk_GroupSearchEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="479f0-176"><a name="bk_GroupSearchEWS"> </a></span></span>

<span data-ttu-id="479f0-177">以下请求示例显示文件夹中前50个项目的[FindItem 操作](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)请求，这些项目按**From**元素分组，按**DateTimeReceived**元素以降序排序。</span><span class="sxs-lookup"><span data-stu-id="479f0-177">The following request example shows a [FindItem operation](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) request for the first 50 items in the folder, grouped by the **From** element, sorted by the **DateTimeReceived** element in descending order.</span></span> <span data-ttu-id="479f0-178">组本身按其项的最小**DateTimeReceived**元素值进行排序，以降序排列。</span><span class="sxs-lookup"><span data-stu-id="479f0-178">The groups themselves are sorted by the smallest **DateTimeReceived** element value on their items, in descending order.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Eastern Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="item:DateTimeReceived" />
          <t:FieldURI FieldURI="message:From" />
          <t:FieldURI FieldURI="item:Categories" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="50" Offset="0" BasePoint="Beginning" />
      <m:GroupBy Order="Descending">
        <t:FieldURI FieldURI="message:From" />
        <t:AggregateOn Aggregate="Minimum">
          <t:FieldURI FieldURI="item:DateTimeReceived" />
        </t:AggregateOn>
      </m:GroupBy>
      <m:SortOrder>
        <t:FieldOrder Order="Descending">
          <t:FieldURI FieldURI="item:DateTimeReceived" />
        </t:FieldOrder>
      </m:SortOrder>
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="479f0-179">服务器将返回以下响应。</span><span class="sxs-lookup"><span data-stu-id="479f0-179">The server returns the following response.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="712" MinorBuildNumber="22" Version="V2_3" 
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
          <m:RootFolder IndexedPagingOffset="10" TotalItemsInView="8" IncludesLastItemInRange="true">
            <t:Groups>
              <t:GroupedItems>
                <t:GroupIndex>0</t:GroupIndex>
                <t:Items>
                  <t:Message>
                    <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                    <t:Subject>Planning resources</t:Subject>
                    <t:DateTimeReceived>2013-12-10T17:41:05Z</t:DateTimeReceived>
                    <t:From>
                      <t:Mailbox>
                        <t:Name>Sadie Daniels</t:Name>
                        <t:EmailAddress>/O=FIRST ORGANIZATION/OU=EXCHANGE ADMINISTRATIVE GROUP (FYDIBOHF23SPDLT)/CN=RECIPIENTS/CN=8D84A3F4CBB34D48838A3AECF99795C0-SADIE</t:EmailAddress>
                        <t:RoutingType>EX</t:RoutingType>
                      </t:Mailbox>
                    </t:From>
                  </t:Message>
                  <t:Message>
                    <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                    <t:Subject>Timeline</t:Subject>
                    <t:DateTimeReceived>2013-12-10T17:40:37Z</t:DateTimeReceived>
                    <t:Categories>
                      <t:String>Project</t:String>
                    </t:Categories>
                    <t:From>
                      <t:Mailbox>
                        <t:Name>Sadie Daniels</t:Name>
                        <t:EmailAddress>/O=FIRST ORGANIZATION/OU=EXCHANGE ADMINISTRATIVE GROUP (FYDIBOHF23SPDLT)/CN=RECIPIENTS/CN=8D84A3F4CBB34D48838A3AECF99795C0-SADIE</t:EmailAddress>
                        <t:RoutingType>EX</t:RoutingType>
                      </t:Mailbox>
                    </t:From>
                  </t:Message>
                  <t:Message>
                    <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                    <t:Subject>For your perusal</t:Subject>
                    <t:DateTimeReceived>2013-11-20T21:51:16Z</t:DateTimeReceived>
                    <t:From>
                      <t:Mailbox>
                        <t:Name>Sadie Daniels</t:Name>
                        <t:EmailAddress>/O=FIRST ORGANIZATION/OU=EXCHANGE ADMINISTRATIVE GROUP (FYDIBOHF23SPDLT)/CN=RECIPIENTS/CN=8D84A3F4CBB34D48838A3AECF99795C0-SADIE</t:EmailAddress>
                        <t:RoutingType>EX</t:RoutingType>
                      </t:Mailbox>
                    </t:From>
                  </t:Message>
                  <t:Message>
                    <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                    <t:Subject>meeting notes</t:Subject>
                    <t:DateTimeReceived>2013-11-20T21:18:51Z</t:DateTimeReceived>
                    <t:Categories>
                      <t:String>Blue category</t:String>
                    </t:Categories>
                    <t:From>
                      <t:Mailbox>
                        <t:Name>Sadie Daniels</t:Name>
                        <t:EmailAddress>/O=FIRST ORGANIZATION/OU=EXCHANGE ADMINISTRATIVE GROUP (FYDIBOHF23SPDLT)/CN=RECIPIENTS/CN=8D84A3F4CBB34D48838A3AECF99795C0-SADIE</t:EmailAddress>
                        <t:RoutingType>EX</t:RoutingType>
                      </t:Mailbox>
                    </t:From>
                  </t:Message>
                  <t:Message>
                    <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                    <t:Subject>Meeting notes</t:Subject>
                    <t:DateTimeReceived>2013-11-20T21:18:51Z</t:DateTimeReceived>
                    <t:From>
                      <t:Mailbox>
                        <t:Name>Sadie Daniels</t:Name>
                        <t:EmailAddress>/O=FIRST ORGANIZATION/OU=EXCHANGE ADMINISTRATIVE GROUP (FYDIBOHF23SPDLT)/CN=RECIPIENTS/CN=8D84A3F4CBB34D48838A3AECF99795C0-SADIE</t:EmailAddress>
                        <t:RoutingType>EX</t:RoutingType>
                      </t:Mailbox>
                    </t:From>
                  </t:Message>
                </t:Items>
              </t:GroupedItems>
              <t:GroupedItems>
                <t:GroupIndex>1</t:GroupIndex>
                <t:Items>
                  <t:Message>
                    <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                    <t:Subject>Query</t:Subject>
                    <t:DateTimeReceived>2013-12-10T17:43:15Z</t:DateTimeReceived>
                    <t:From>
                      <t:Mailbox>
                        <t:Name>Hope Gross</t:Name>
                        <t:EmailAddress>/O=FIRST ORGANIZATION/OU=EXCHANGE ADMINISTRATIVE GROUP (FYDIBOHF23SPDLT)/CN=RECIPIENTS/CN=9B55E4100C064D9D8C5F72FF36802ED3-HOPE</t:EmailAddress>
                        <t:RoutingType>EX</t:RoutingType>
                      </t:Mailbox>
                    </t:From>
                  </t:Message>
                  <t:Message>
                    <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                    <t:Subject>Update</t:Subject>
                    <t:DateTimeReceived>2013-12-10T17:42:33Z</t:DateTimeReceived>
                    <t:Categories>
                      <t:String>Project</t:String>
                      <t:String>Blue category</t:String>
                    </t:Categories>
                    <t:From>
                      <t:Mailbox>
                        <t:Name>Hope Gross</t:Name>
                        <t:EmailAddress>/O=FIRST ORGANIZATION/OU=EXCHANGE ADMINISTRATIVE GROUP (FYDIBOHF23SPDLT)/CN=RECIPIENTS/CN=9B55E4100C064D9D8C5F72FF36802ED3-HOPE</t:EmailAddress>
                        <t:RoutingType>EX</t:RoutingType>
                      </t:Mailbox>
                    </t:From>
                  </t:Message>
                  <t:Message>
                    <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                    <t:Subject>This cat is hilarious!</t:Subject>
                    <t:DateTimeReceived>2013-10-15T20:22:12Z</t:DateTimeReceived>
                    <t:From>
                      <t:Mailbox>
                        <t:Name>Hope Gross</t:Name>
                        <t:EmailAddress>/O=FIRST ORGANIZATION/OU=EXCHANGE ADMINISTRATIVE GROUP (FYDIBOHF23SPDLT)/CN=RECIPIENTS/CN=9B55E4100C064D9D8C5F72FF36802ED3-HOPE</t:EmailAddress>
                        <t:RoutingType>EX</t:RoutingType>
                      </t:Mailbox>
                    </t:From>
                  </t:Message>
                </t:Items>
              </t:GroupedItems>
            </t:Groups>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

## <a name="version-differences"></a><span data-ttu-id="479f0-180">版本差异</span><span class="sxs-lookup"><span data-stu-id="479f0-180">Version differences</span></span>
<span data-ttu-id="479f0-181"><a name="bk_VersionDiffs"> </a></span><span class="sxs-lookup"><span data-stu-id="479f0-181"><a name="bk_VersionDiffs"> </a></span></span>

<span data-ttu-id="479f0-182">Exchange 的版本从主要版本15开始，到 build 15.0.775.38 返回**Group**元素（类型**GROUPEDITEMSTYPE**）替换 SOAP 响应中的[GroupedItems](https://msdn.microsoft.com/library/53170df4-4272-4b37-b23f-cd8e2d4a7396%28Office.15%29.aspx)元素。</span><span class="sxs-lookup"><span data-stu-id="479f0-182">Versions of Exchange starting with major version 15 and ending with build 15.0.775.38 return **Group** elements (of type **GroupedItemsType**) in place of [GroupedItems](https://msdn.microsoft.com/library/53170df4-4272-4b37-b23f-cd8e2d4a7396%28Office.15%29.aspx) elements in the SOAP response.</span></span> <span data-ttu-id="479f0-183">如果使用 EWS 托管 API，这将导致[GroupedFindItemsResults](https://msdn.microsoft.com/library/office/dd633961%28v=exchg.80%29.aspx)集合包含0个对象。</span><span class="sxs-lookup"><span data-stu-id="479f0-183">If you are using the EWS Managed API, this will cause the [GroupedFindItemsResults.ItemGroups](https://msdn.microsoft.com/library/office/dd633961%28v=exchg.80%29.aspx) collection to contain 0 objects.</span></span> <span data-ttu-id="479f0-184">如果使用 EWS，则应将**组**元素作为**GroupedItems**元素进行处理。</span><span class="sxs-lookup"><span data-stu-id="479f0-184">If you are using EWS, **Group** elements should be handled as **GroupedItems** elements.</span></span> 
  
<span data-ttu-id="479f0-185">从主要版本15开始的 Exchange 版本返回额外的**Group**或**GroupedItems**元素，其中**XSI： nil**属性在 SOAP 响应中设置为**true** 。</span><span class="sxs-lookup"><span data-stu-id="479f0-185">Versions of Exchange starting with major version 15 return extra **Group** or **GroupedItems** elements with the **xsi:nil** attribute set to **true** in the SOAP response.</span></span> <span data-ttu-id="479f0-186">如果使用 EWS 托管 API，这些额外的元素将导致[ServiceXmlDeserializationException](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.servicexmldeserializationexception%28v=exchg.80%29.aspx)引发。</span><span class="sxs-lookup"><span data-stu-id="479f0-186">If you are using the EWS Managed API, these extra elements will cause a [ServiceXmlDeserializationException](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.servicexmldeserializationexception%28v=exchg.80%29.aspx) to be thrown.</span></span> <span data-ttu-id="479f0-187">如果使用 EWS，则应忽略这些额外的元素。</span><span class="sxs-lookup"><span data-stu-id="479f0-187">If you are using EWS, these extra elements should be ignored.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="479f0-188">另请参阅</span><span class="sxs-lookup"><span data-stu-id="479f0-188">See also</span></span>

- [<span data-ttu-id="479f0-189">搜索和交换中的 EWS</span><span class="sxs-lookup"><span data-stu-id="479f0-189">Search and EWS in Exchange</span></span>](search-and-ews-in-exchange.md)    
- [<span data-ttu-id="479f0-190">ExchangeService。 FindItems</span><span class="sxs-lookup"><span data-stu-id="479f0-190">ExchangeService.FindItems</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)    
- [<span data-ttu-id="479f0-191">FindItems</span><span class="sxs-lookup"><span data-stu-id="479f0-191">Folder.FindItems</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)   
- [<span data-ttu-id="479f0-192">分组类</span><span class="sxs-lookup"><span data-stu-id="479f0-192">Grouping class</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.grouping%28v=exchg.80%29.aspx)    
- [<span data-ttu-id="479f0-193">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="479f0-193">FindItem operation</span></span>](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    

