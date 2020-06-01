---
title: 在 Exchange 中使用 EWS 访问定期系列
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 196a5671-2836-4696-b734-d5ecfdbf8962
description: 了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS 在定期系列中访问日历项目。
ms.openlocfilehash: dca41472b3b2f775f420b6654d7e43ef456b0583
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456890"
---
# <a name="access-a-recurring-series-by-using-ews-in-exchange"></a><span data-ttu-id="6fcfd-103">在 Exchange 中使用 EWS 访问定期系列</span><span class="sxs-lookup"><span data-stu-id="6fcfd-103">Access a recurring series by using EWS in Exchange</span></span>

<span data-ttu-id="6fcfd-104">了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS 在定期系列中访问日历项目。</span><span class="sxs-lookup"><span data-stu-id="6fcfd-104">Learn how to access calendar items in a recurring series by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="6fcfd-105">定期的约会或会议系列由定期母版组成，系列中根据设置的模式重复的次数，以及已更改和已删除的匹配项的集合（可选）。</span><span class="sxs-lookup"><span data-stu-id="6fcfd-105">A recurring series of appointments or meetings is made up of a recurring master, a number of occurrences in a series that repeat according to a set pattern, and, optionally, sets of occurrences that were changed and that were deleted.</span></span> <span data-ttu-id="6fcfd-106">您可以使用 EWS 托管 API 或 EWS 访问定期系列中的日历项目。</span><span class="sxs-lookup"><span data-stu-id="6fcfd-106">You can use the EWS Managed API or EWS to access calendar items in a recurring series.</span></span> <span data-ttu-id="6fcfd-107">这使您可以执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="6fcfd-107">This enables you to:</span></span>
  
- <span data-ttu-id="6fcfd-108">查看与项目 ID 关联的日历项目是定期主控形状、系列中的事件还是系列例外。</span><span class="sxs-lookup"><span data-stu-id="6fcfd-108">Check to see if a calendar item associated with an item ID is a recurring master, an occurrence in a series, or an exception to a series.</span></span>
    
- <span data-ttu-id="6fcfd-109">在 "日历" 文件夹中搜索定期约会。</span><span class="sxs-lookup"><span data-stu-id="6fcfd-109">Search your calendar folder for recurrence appointments.</span></span>
    
- <span data-ttu-id="6fcfd-110">获取相关的定期日历项目</span><span class="sxs-lookup"><span data-stu-id="6fcfd-110">Get related recurrence calendar items</span></span>
    
- <span data-ttu-id="6fcfd-111">循环访问系列中的事件、事件发生异常或发生删除。</span><span class="sxs-lookup"><span data-stu-id="6fcfd-111">Iterate through occurrences in a series, occurrence exceptions, or occurrence deletions.</span></span>
    
## <a name="get-a-collection-of-recurring-calendar-items-by-using-the-ews-managed-api"></a><span data-ttu-id="6fcfd-112">使用 EWS 托管 API 获取定期日历项的集合</span><span class="sxs-lookup"><span data-stu-id="6fcfd-112">Get a collection of recurring calendar items by using the EWS Managed API</span></span>

<span data-ttu-id="6fcfd-113">如果要检索约会的集合，可以使用[ExchangeService](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx)方法来检索给定开始日期和结束日期之间的所有约会，然后将**发生**或**例外**约会类型的所有日历项目添加到集合中，如下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="6fcfd-113">If you want to retrieve a collection of appointments, you can use the [ExchangeService.FindAppointments](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) method to retrieve all appointments between a given start and end date, and then add all calendar items with an appointment type of **Occurrence** or **Exception** to a collection, as shown in the following example.</span></span> 
  
<span data-ttu-id="6fcfd-114">此示例假定您已通过 Exchange 服务器的身份验证，并获取了名为 "**服务**" 的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象。</span><span class="sxs-lookup"><span data-stu-id="6fcfd-114">This example assumes that you have authenticated to an Exchange server and have acquired an [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> 
  
```cs
public static Collection<Appointment> FindRecurringCalendarItems(ExchangeService service, 
                                                                    DateTime startSearchDate, 
                                                                    DateTime endSearchDate)
{
    // Instantiate a collection to hold occurrences and exception calendar items.
    Collection<Appointment> foundAppointments = new Collection<Appointment>();
    // Create a calendar view to search the calendar folder and specify the properties to return.
    CalendarView calView = new CalendarView(startSearchDate, endSearchDate);
    calView.PropertySet = new PropertySet(BasePropertySet.IdOnly, 
                                            AppointmentSchema.Subject, 
                                            AppointmentSchema.Start, 
                                            AppointmentSchema.IsRecurring, 
                                            AppointmentSchema.AppointmentType);
    // Retrieve a collection of calendar items.
    FindItemsResults<Appointment> findResults = service.FindAppointments(WellKnownFolderName.Calendar, calView);
    // Add all calendar items in your view that are occurrences or exceptions to your collection.
    foreach (Appointment appt in findResults.Items)
    {
        if (appt.AppointmentType == AppointmentType.Occurrence || appt.AppointmentType == AppointmentType.Exception)
        {
            foundAppointments.Add(appt);
        }
        else
        {
            Console.WriteLine("Discarding calendar item of type {0}.", appt.AppointmentType);
        }
    }
    return foundAppointments;
}

```

<span data-ttu-id="6fcfd-115">请注意，在对**FindAppointments**的调用中不会返回定期主日历项目。</span><span class="sxs-lookup"><span data-stu-id="6fcfd-115">Note that recurring master calendar items aren't returned in a call to **FindAppointments**.</span></span> <span data-ttu-id="6fcfd-116">如果要检索定期母版，或者希望更常规的方法来检索日历项目，则需要使用[ExchangeService. FindItems](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="6fcfd-116">If you want to retrieve recurring masters, or you want a more general approach to retrieving calendar items, you need to use [ExchangeService.FindItems](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx).</span></span> <span data-ttu-id="6fcfd-117">然后，您可以使用搜索筛选器仅检索开始日期大于或等于所选日期的项目，以及用于限制要返回的项目数的项目视图。</span><span class="sxs-lookup"><span data-stu-id="6fcfd-117">You can then use a search filter to retrieve only items with a start date greater than or equal to a date you choose, and an item view to limit the number of items to return.</span></span> <span data-ttu-id="6fcfd-118">请注意，在搜索中，开始日期早于开始日期的定期母版将找不到，即使在此范围内发生。</span><span class="sxs-lookup"><span data-stu-id="6fcfd-118">Note that a recurring master with a start date earlier than the start date in your search will not be found, even if occurrences occur in this range.</span></span>
  
<span data-ttu-id="6fcfd-119">此示例假定您已通过 Exchange 服务器的身份验证，并获取了名为 "**服务**" 的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象。</span><span class="sxs-lookup"><span data-stu-id="6fcfd-119">This example assumes that you have authenticated to an Exchange server and have acquired an [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> 
  
```cs
public static Collection<Appointment> FindCalendarItemsByAppointmentType(ExchangeService service, 
                                                                         AppointmentType myAppointmentType, 
                                                                         DateTime startSearchDate)
{
    Collection<Appointment> foundAppointments = new Collection<Appointment>();
    // Create a search filter based on the start search date.
    SearchFilter.SearchFilterCollection searchFilter = new SearchFilter.SearchFilterCollection();
    searchFilter.Add(new SearchFilter.IsGreaterThanOrEqualTo(AppointmentSchema.Start, startSearchDate));
    // Create an item view to specify which properties to return.
    ItemView view = new ItemView(20);
    view.PropertySet = new PropertySet(BasePropertySet.IdOnly, 
                                       AppointmentSchema.Subject, 
                                       AppointmentSchema.Start, 
                                       AppointmentSchema.AppointmentType,
                                       AppointmentSchema.IsRecurring);
    // Get the appointment items from the server with the properties we specified.
    FindItemsResults<Item> findResults = service.FindItems(WellKnownFolderName.Calendar, searchFilter, view);
    // Add each of the appointments of the type you want to the collection.
    foreach (Item item in findResults.Items)
    {
        Appointment appt = item as Appointment;
        if (appt.AppointmentType == myAppointmentType)
        {
            foundAppointments.Add(appt);
        }
    }
    return foundAppointments;
}

```

## <a name="get-related-recurrence-calendar-items-by-using-the-ews-managed-api"></a><span data-ttu-id="6fcfd-120">使用 EWS 托管 API 获取相关的定期日历项</span><span class="sxs-lookup"><span data-stu-id="6fcfd-120">Get related recurrence calendar items by using the EWS Managed API</span></span>

<span data-ttu-id="6fcfd-121">有时，您有一个谜题，但要解决它，需要剩下的部分。</span><span class="sxs-lookup"><span data-stu-id="6fcfd-121">Sometimes you have one piece of the puzzle, but to solve it you need the rest of the pieces.</span></span> <span data-ttu-id="6fcfd-122">如果您具有定期日历项目的项目 ID，则可以使用多个 EWS 托管 API 属性或方法之一获取所需的其他部分。</span><span class="sxs-lookup"><span data-stu-id="6fcfd-122">If you have the item ID for a recurrence calendar item, you can get the other pieces you need by using one of several EWS Managed API properties or methods.</span></span>
  
<span data-ttu-id="6fcfd-123">**表1。用于获取相关定期日历项目的 EWS 托管 API 属性或方法**</span><span class="sxs-lookup"><span data-stu-id="6fcfd-123">**Table 1. EWS Managed API property or method to use to get related recurrence calendar items**</span></span>

|<span data-ttu-id="6fcfd-124">**如果您具有的项目 ID 为 .。。**</span><span class="sxs-lookup"><span data-stu-id="6fcfd-124">**If you have the item ID for…**</span></span>|<span data-ttu-id="6fcfd-125">**你可以获取 .。。**</span><span class="sxs-lookup"><span data-stu-id="6fcfd-125">**You can get…**</span></span>|<span data-ttu-id="6fcfd-126">**通过使用 .。。**</span><span class="sxs-lookup"><span data-stu-id="6fcfd-126">**By using the…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6fcfd-127">定期主日历项目</span><span class="sxs-lookup"><span data-stu-id="6fcfd-127">The recurring master calendar item</span></span>  <br/> | <span data-ttu-id="6fcfd-128">系列中的第一个匹配项</span><span class="sxs-lookup"><span data-stu-id="6fcfd-128">The first occurrence in a series</span></span>  <br/>  <span data-ttu-id="6fcfd-129">系列中的最后一个匹配项</span><span class="sxs-lookup"><span data-stu-id="6fcfd-129">The last occurrence in a series</span></span>  <br/>  <span data-ttu-id="6fcfd-130">系列的例外</span><span class="sxs-lookup"><span data-stu-id="6fcfd-130">The exceptions to a series</span></span>  <br/>  <span data-ttu-id="6fcfd-131">系列中已删除的约会</span><span class="sxs-lookup"><span data-stu-id="6fcfd-131">The deleted appointments in a series</span></span>  <br/>  <span data-ttu-id="6fcfd-132">任何事件（给定的索引）</span><span class="sxs-lookup"><span data-stu-id="6fcfd-132">Any occurrence (given its index)</span></span>  <br/> |<span data-ttu-id="6fcfd-133">[FirstOccurrence](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.firstoccurrence%28v=exchg.80%29.aspx)属性</span><span class="sxs-lookup"><span data-stu-id="6fcfd-133">[Appointment.FirstOccurrence](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.firstoccurrence%28v=exchg.80%29.aspx) property</span></span>  <br/> <span data-ttu-id="6fcfd-134">[LastOccurrence](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.lastoccurrence%28v=exchg.80%29.aspx)属性</span><span class="sxs-lookup"><span data-stu-id="6fcfd-134">[Appointment.LastOccurrence](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.lastoccurrence%28v=exchg.80%29.aspx) property</span></span>  <br/> <span data-ttu-id="6fcfd-135">[ModifiedOccurrences](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.modifiedoccurrences%28v=exchg.80%29.aspx)属性</span><span class="sxs-lookup"><span data-stu-id="6fcfd-135">[Appointment.ModifiedOccurrences](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.modifiedoccurrences%28v=exchg.80%29.aspx) property</span></span>  <br/> <span data-ttu-id="6fcfd-136">[DeletedOccurrences](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.deletedoccurrences%28v=exchg.80%29.aspx)属性</span><span class="sxs-lookup"><span data-stu-id="6fcfd-136">[Appointment.DeletedOccurrences](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.deletedoccurrences%28v=exchg.80%29.aspx) property</span></span>  <br/> <span data-ttu-id="6fcfd-137">[BindToOccurrence](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.appointment.bindtooccurrence%28v=exchg.80%29.aspx)方法</span><span class="sxs-lookup"><span data-stu-id="6fcfd-137">[Appointment.BindToOccurrence](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.appointment.bindtooccurrence%28v=exchg.80%29.aspx) method</span></span>  <br/> |
|<span data-ttu-id="6fcfd-138">系列中的单个事件</span><span class="sxs-lookup"><span data-stu-id="6fcfd-138">A single occurrence in a series</span></span>  <br/> |<span data-ttu-id="6fcfd-139">定期母版</span><span class="sxs-lookup"><span data-stu-id="6fcfd-139">The recurring master</span></span>  <br/> |<span data-ttu-id="6fcfd-140">[BindToRecurringMaster](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.appointment.bindtorecurringmaster%28v=exchg.80%29.aspx)方法</span><span class="sxs-lookup"><span data-stu-id="6fcfd-140">[Appointment.BindToRecurringMaster](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.appointment.bindtorecurringmaster%28v=exchg.80%29.aspx) method</span></span>  <br/> |
|<span data-ttu-id="6fcfd-141">任何日历项目（[约会](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx)对象）</span><span class="sxs-lookup"><span data-stu-id="6fcfd-141">Any calendar item (an [Appointment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) object)</span></span>  <br/> |<span data-ttu-id="6fcfd-142">[约会类型](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.appointmenttype%28v=exchg.80%29.aspx)枚举值</span><span class="sxs-lookup"><span data-stu-id="6fcfd-142">The [appointment type](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.appointmenttype%28v=exchg.80%29.aspx) enumeration value</span></span>  <br/> |<span data-ttu-id="6fcfd-143">[AppointmentType](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.appointment.appointmenttype%28v=exchg.80%29.aspx)属性</span><span class="sxs-lookup"><span data-stu-id="6fcfd-143">[Appointment.AppointmentType](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.appointment.appointmenttype%28v=exchg.80%29.aspx) property</span></span>  <br/> |
   
<span data-ttu-id="6fcfd-144">下面的代码示例演示如何获取定期母版、系列中的第一个或最后一个匹配项或给定其索引的事件。</span><span class="sxs-lookup"><span data-stu-id="6fcfd-144">The following code example shows how to get a recurring master, the first or last occurrence in a series, or an occurrence given its index.</span></span>
  
<span data-ttu-id="6fcfd-145">此示例假定您已通过 Exchange 服务器的身份验证，并获取了名为 "**服务**" 的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象。</span><span class="sxs-lookup"><span data-stu-id="6fcfd-145">This example assumes that you have authenticated to an Exchange server and have acquired an [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> 
  
```cs
public static void GetRelatedRecurrenceCalendarItems(ExchangeService service, ItemId itemId)
{
    Appointment calendarItem = Appointment.Bind(service, itemId, new PropertySet(AppointmentSchema.AppointmentType));
    Appointment recurrMaster = new Appointment(service);
    PropertySet props = new PropertySet(AppointmentSchema.AppointmentType,
                                        AppointmentSchema.Subject,
                                        AppointmentSchema.FirstOccurrence,
                                        AppointmentSchema.LastOccurrence,
                                        AppointmentSchema.ModifiedOccurrences,
                                        AppointmentSchema.DeletedOccurrences);
    // If the item ID is not for a recurring master, retrieve the recurring master for the series.
    switch (calendarItem.AppointmentType)
    {
        // Calendar item is a recurring master so use Appointment.Bind
        case AppointmentType.RecurringMaster:
            recurrMaster = Appointment.Bind(service, itemId, props);
            break;
        // The calendar item is a single instance meeting, so there are no instances to modify or delete.
        case AppointmentType.Single:
            Console.WriteLine("Item id must reference a calendar item that is part of a recurring series.");
            return;
        // The calendar item is an occurrence in the series, so use BindToRecurringMaster.
        case AppointmentType.Occurrence:
            recurrMaster = Appointment.BindToRecurringMaster(service, itemId, props);
            break;
        // The calendar item is an exception to the series, so use BindToRecurringMaster.                
        case AppointmentType.Exception:
            recurrMaster = Appointment.BindToRecurringMaster(service, itemId, props);
            break;
    }
    // View the first occurrence, last occurrence, and number of modified and deleted occurrences associated with the recurring master.
    Console.WriteLine("Information for the {0} recurring series:", recurrMaster.Subject);
    Console.WriteLine("The start time for the first appointment with id \t{0} was on \t{1}.", 
                        recurrMaster.FirstOccurrence.ItemId.ToString().Substring(144), 
                        recurrMaster.FirstOccurrence.Start.ToString());
    Console.WriteLine("The start time for the last appointment with id \t{0} will be on \t{1}.", 
                        recurrMaster.LastOccurrence.ItemId.ToString().Substring(144), 
                        recurrMaster.LastOccurrence.Start.ToString());
    Console.WriteLine("There are {0} modified occurrences and {1} deleted occurrences.", 
                        recurrMaster.ModifiedOccurrences == null ? "no" : recurrMaster.ModifiedOccurrences.Count.ToString(), 
                        recurrMaster.DeletedOccurrences == null ? "no" : recurrMaster.DeletedOccurrences.Count.ToString());
    // Bind to the first occurrence of a series by using its index.
    Appointment firstOccurrence = Appointment.BindToOccurrence(service, 
                                                                recurrMaster.Id, 
                                                                1, // Index of first item is 1, not 0.
                                                                new PropertySet(AppointmentSchema.AppointmentType,
                                                                                AppointmentSchema.Start));
    Console.WriteLine("Compare the start times for a recurring master's first occurrence " + 
                        "and the occurrence found at index 1 using the BindToOccurrence method:");
    Console.WriteLine("The appointment at index 1 has a start time of\t\t\t\t {0}\n" +
                        "Which matches that of the first occurrence on the recurring master: \t {1}",
                        firstOccurrence.Start.ToString(),
                        recurrMaster.FirstOccurrence.Start.ToString());
}

```

## <a name="access-calendar-items-in-a-recurring-series-by-using-ews"></a><span data-ttu-id="6fcfd-146">使用 EWS 访问定期系列中的日历项目</span><span class="sxs-lookup"><span data-stu-id="6fcfd-146">Access calendar items in a recurring series by using EWS</span></span>

<span data-ttu-id="6fcfd-147">访问定期系列中的日历项目与访问日历项目的单个实例非常相似。</span><span class="sxs-lookup"><span data-stu-id="6fcfd-147">Accessing calendar items in a recurring series is very similar to accessing single instances of calendar items.</span></span> <span data-ttu-id="6fcfd-148">您可以使用[GetItem](https://msdn.microsoft.com/library/769df8eb-9c72-48b5-a49f-82c6b86bc5fc%28Office.15%29.aspx)操作请求（指定所需的属性）和所需的约会实例的[OccurrenceItemId](https://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="6fcfd-148">You use a [GetItem](https://msdn.microsoft.com/library/769df8eb-9c72-48b5-a49f-82c6b86bc5fc%28Office.15%29.aspx) operation request, specifying the properties you want, with the [OccurrenceItemId](https://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) of the appointment instance you need.</span></span> <span data-ttu-id="6fcfd-149">[OccurrenceItemId](https://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx)包含发生的定期主机的**ItemID** ，以及该系列中的索引值。</span><span class="sxs-lookup"><span data-stu-id="6fcfd-149">The [OccurrenceItemId](https://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) contains the **ItemID** of the occurrence's recurring master, as well as its index value in the series.</span></span> 
  
<span data-ttu-id="6fcfd-150">下面的 XML 显示了用于返回其索引所指定的系列中的事件的[GetItem](https://msdn.microsoft.com/library/769df8eb-9c72-48b5-a49f-82c6b86bc5fc%28Office.15%29.aspx)请求。</span><span class="sxs-lookup"><span data-stu-id="6fcfd-150">The following XML shows the [GetItem](https://msdn.microsoft.com/library/769df8eb-9c72-48b5-a49f-82c6b86bc5fc%28Office.15%29.aspx) request used to return an occurrence in a series specified by its index.</span></span> <span data-ttu-id="6fcfd-151">请注意，定期主控形状的**ItemID**已缩短，以提高可读性。</span><span class="sxs-lookup"><span data-stu-id="6fcfd-151">Note that the **ItemID** of the recurring master has been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:GetItem>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="calendar:CalendarItemType" />
          <t:FieldURI FieldURI="calendar:Start" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:ItemIds>
        <t:OccurrenceItemId RecurringMasterId="AAMkA" InstanceIndex="1" />
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="6fcfd-152">服务器使用[GetItemResponse](https://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx)邮件响应**GetItem**请求，其中包括 ResponseCode 值为**NoError**的[ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx)值，这表示电子邮件已成功创建，以及新创建的邮件的[ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="6fcfd-152">The server responds to the **GetItem** request with a [GetItemResponse](https://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the email was created successfully, and the [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the newly created message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6fcfd-153">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6fcfd-153">See also</span></span>


- [<span data-ttu-id="6fcfd-154">Calendars and EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="6fcfd-154">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
- [<span data-ttu-id="6fcfd-155">使用 Exchange 中的 EWS 获取约会和会议</span><span class="sxs-lookup"><span data-stu-id="6fcfd-155">Get appointments and meetings by using EWS in Exchange</span></span>](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)
    

