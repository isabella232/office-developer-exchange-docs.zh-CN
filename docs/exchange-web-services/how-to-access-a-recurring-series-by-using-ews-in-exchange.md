---
title: 在 Exchange 中使用 EWS 访问定期系列
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 196a5671-2836-4696-b734-d5ecfdbf8962
description: 了解如何在 Exchange 使用 EWS 托管 API 的 EWS 访问定期系列中的日历项。
ms.openlocfilehash: 9f78ef5b51766a69d23fce3f36c55fbb9422fb16
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752726"
---
# <a name="access-a-recurring-series-by-using-ews-in-exchange"></a><span data-ttu-id="a72e0-103">在 Exchange 中使用 EWS 访问定期系列</span><span class="sxs-lookup"><span data-stu-id="a72e0-103">Access a recurring series by using EWS in Exchange</span></span>

<span data-ttu-id="a72e0-104">了解如何在 Exchange 使用 EWS 托管 API 的 EWS 访问定期系列中的日历项。</span><span class="sxs-lookup"><span data-stu-id="a72e0-104">Learn how to access calendar items in a recurring series by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="a72e0-105">一系列定期约会或会议组成定期主控形状，次数系列中的重复设置模式中，根据和 （可选） 的匹配项的已修改且已删除的设置。</span><span class="sxs-lookup"><span data-stu-id="a72e0-105">A recurring series of appointments or meetings is made up of a recurring master, a number of occurrences in a series that repeat according to a set pattern, and, optionally, sets of occurrences that were changed and that were deleted.</span></span> <span data-ttu-id="a72e0-106">您可以使用 EWS 托管 API 的 EWS 访问定期系列中的日历项目。</span><span class="sxs-lookup"><span data-stu-id="a72e0-106">You can use the EWS Managed API or EWS to access calendar items in a recurring series.</span></span> <span data-ttu-id="a72e0-107">这使您能够：</span><span class="sxs-lookup"><span data-stu-id="a72e0-107">This enables you to:</span></span>
  
- <span data-ttu-id="a72e0-108">查看项目 ID 相关联的日历项目是否定期主控形状、 出现系列或一系列的例外。</span><span class="sxs-lookup"><span data-stu-id="a72e0-108">Check to see if a calendar item associated with an item ID is a recurring master, an occurrence in a series, or an exception to a series.</span></span>
    
- <span data-ttu-id="a72e0-109">搜索您的日历文件夹的定期约会。</span><span class="sxs-lookup"><span data-stu-id="a72e0-109">Search your calendar folder for recurrence appointments.</span></span>
    
- <span data-ttu-id="a72e0-110">获取相关的定期日历项目</span><span class="sxs-lookup"><span data-stu-id="a72e0-110">Get related recurrence calendar items</span></span>
    
- <span data-ttu-id="a72e0-111">循环访问一系列、 出现例外或出现删除发生次数。</span><span class="sxs-lookup"><span data-stu-id="a72e0-111">Iterate through occurrences in a series, occurrence exceptions, or occurrence deletions.</span></span>
    
## <a name="get-a-collection-of-recurring-calendar-items-by-using-the-ews-managed-api"></a><span data-ttu-id="a72e0-112">使用 EWS 托管 API 获取定期日历项目的集合</span><span class="sxs-lookup"><span data-stu-id="a72e0-112">Get a collection of recurring calendar items by using the EWS Managed API</span></span>

<span data-ttu-id="a72e0-113">如果您想要检索的约会集合，您可以使用[ExchangeService.FindAppointments](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx)方法检索给定开始和结束日期之间的所有约会，然后添加了一个约会类型为**出现的所有日历项目**或到集，如下面的示例中所示的**异常**。</span><span class="sxs-lookup"><span data-stu-id="a72e0-113">If you want to retrieve a collection of appointments, you can use the [ExchangeService.FindAppointments](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) method to retrieve all appointments between a given start and end date, and then add all calendar items with an appointment type of **Occurrence** or **Exception** to a collection, as shown in the following example.</span></span> 
  
<span data-ttu-id="a72e0-114">此示例假定您具有身份验证向 Exchange 服务器，并已获取名为**服务** [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象。</span><span class="sxs-lookup"><span data-stu-id="a72e0-114">This example assumes that you have authenticated to an Exchange server and have acquired an [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> 
  
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

<span data-ttu-id="a72e0-115">请注意，定期母版日历项目不会返回**FindAppointments**将调用。</span><span class="sxs-lookup"><span data-stu-id="a72e0-115">Note that recurring master calendar items aren't returned in a call to **FindAppointments**.</span></span> <span data-ttu-id="a72e0-116">如果您想要检索定期主控形状，或者需要检索日历项目的更多常规方法，您需要使用[ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="a72e0-116">If you want to retrieve recurring masters, or you want a more general approach to retrieving calendar items, you need to use [ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx).</span></span> <span data-ttu-id="a72e0-117">然后可以使用的搜索筛选器来检索仅开始日期大于或等于您选择，日期和项目视图限制的项目数，返回的项目。</span><span class="sxs-lookup"><span data-stu-id="a72e0-117">You can then use a search filter to retrieve only items with a start date greater than or equal to a date you choose, and an item view to limit the number of items to return.</span></span> <span data-ttu-id="a72e0-118">定期开始与主日期早于将未找到您所搜索的开始日期，即使在此范围中出现匹配项的注释。</span><span class="sxs-lookup"><span data-stu-id="a72e0-118">Note that a recurring master with a start date earlier than the start date in your search will not be found, even if occurrences occur in this range.</span></span>
  
<span data-ttu-id="a72e0-119">此示例假定您具有身份验证向 Exchange 服务器，并已获取名为**服务** [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象。</span><span class="sxs-lookup"><span data-stu-id="a72e0-119">This example assumes that you have authenticated to an Exchange server and have acquired an [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> 
  
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

## <a name="get-related-recurrence-calendar-items-by-using-the-ews-managed-api"></a><span data-ttu-id="a72e0-120">通过使用 EWS 托管 API 获取相关的定期日历项目</span><span class="sxs-lookup"><span data-stu-id="a72e0-120">Get related recurrence calendar items by using the EWS Managed API</span></span>

<span data-ttu-id="a72e0-121">有时，您必须解决难题，一段，但是若要解决此问题，您需要部分的其余部分。</span><span class="sxs-lookup"><span data-stu-id="a72e0-121">Sometimes you have one piece of the puzzle, but to solve it you need the rest of the pieces.</span></span> <span data-ttu-id="a72e0-122">如果您有定期日历项目的项 ID，您可以使用几个 EWS 托管 API 属性或方法之一所需的其他部分。</span><span class="sxs-lookup"><span data-stu-id="a72e0-122">If you have the item ID for a recurrence calendar item, you can get the other pieces you need by using one of several EWS Managed API properties or methods.</span></span>
  
<span data-ttu-id="a72e0-123">**表 1。EWS 托管 API 属性或方法用于获取相关的定期日历项目**</span><span class="sxs-lookup"><span data-stu-id="a72e0-123">**Table 1. EWS Managed API property or method to use to get related recurrence calendar items**</span></span>

|<span data-ttu-id="a72e0-124">**如果您具有的项 ID...**</span><span class="sxs-lookup"><span data-stu-id="a72e0-124">**If you have the item ID for…**</span></span>|<span data-ttu-id="a72e0-125">**您可以获取...**</span><span class="sxs-lookup"><span data-stu-id="a72e0-125">**You can get…**</span></span>|<span data-ttu-id="a72e0-126">**使用...**</span><span class="sxs-lookup"><span data-stu-id="a72e0-126">**By using the…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a72e0-127">定期的主控形状的日历项目</span><span class="sxs-lookup"><span data-stu-id="a72e0-127">The recurring master calendar item</span></span>  <br/> | <span data-ttu-id="a72e0-128">首次出现系列</span><span class="sxs-lookup"><span data-stu-id="a72e0-128">The first occurrence in a series</span></span>  <br/>  <span data-ttu-id="a72e0-129">最后一次在一系列</span><span class="sxs-lookup"><span data-stu-id="a72e0-129">The last occurrence in a series</span></span>  <br/>  <span data-ttu-id="a72e0-130">一系列的例外</span><span class="sxs-lookup"><span data-stu-id="a72e0-130">The exceptions to a series</span></span>  <br/>  <span data-ttu-id="a72e0-131">在一系列中已删除的约会</span><span class="sxs-lookup"><span data-stu-id="a72e0-131">The deleted appointments in a series</span></span>  <br/>  <span data-ttu-id="a72e0-132">（给定索引） 的任何匹配项</span><span class="sxs-lookup"><span data-stu-id="a72e0-132">Any occurrence (given its index)</span></span>  <br/> |<span data-ttu-id="a72e0-133">[Appointment.FirstOccurrence](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.firstoccurrence%28v=exchg.80%29.aspx)属性</span><span class="sxs-lookup"><span data-stu-id="a72e0-133">[Appointment.FirstOccurrence](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.firstoccurrence%28v=exchg.80%29.aspx) property</span></span>  <br/> <span data-ttu-id="a72e0-134">[Appointment.LastOccurrence](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.lastoccurrence%28v=exchg.80%29.aspx)属性</span><span class="sxs-lookup"><span data-stu-id="a72e0-134">[Appointment.LastOccurrence](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.lastoccurrence%28v=exchg.80%29.aspx) property</span></span>  <br/> <span data-ttu-id="a72e0-135">[Appointment.ModifiedOccurrences](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.modifiedoccurrences%28v=exchg.80%29.aspx)属性</span><span class="sxs-lookup"><span data-stu-id="a72e0-135">[Appointment.ModifiedOccurrences](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.modifiedoccurrences%28v=exchg.80%29.aspx) property</span></span>  <br/> <span data-ttu-id="a72e0-136">[Appointment.DeletedOccurrences](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.deletedoccurrences%28v=exchg.80%29.aspx)属性</span><span class="sxs-lookup"><span data-stu-id="a72e0-136">[Appointment.DeletedOccurrences](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.deletedoccurrences%28v=exchg.80%29.aspx) property</span></span>  <br/> <span data-ttu-id="a72e0-137">[Appointment.BindToOccurrence](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.appointment.bindtooccurrence%28v=exchg.80%29.aspx)方法</span><span class="sxs-lookup"><span data-stu-id="a72e0-137">[Appointment.BindToOccurrence](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.appointment.bindtooccurrence%28v=exchg.80%29.aspx) method</span></span>  <br/> |
|<span data-ttu-id="a72e0-138">在一系列中单个匹配项</span><span class="sxs-lookup"><span data-stu-id="a72e0-138">A single occurrence in a series</span></span>  <br/> |<span data-ttu-id="a72e0-139">定期母版</span><span class="sxs-lookup"><span data-stu-id="a72e0-139">The recurring master</span></span>  <br/> |<span data-ttu-id="a72e0-140">[Appointment.BindToRecurringMaster](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.appointment.bindtorecurringmaster%28v=exchg.80%29.aspx)方法</span><span class="sxs-lookup"><span data-stu-id="a72e0-140">[Appointment.BindToRecurringMaster](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.appointment.bindtorecurringmaster%28v=exchg.80%29.aspx) method</span></span>  <br/> |
|<span data-ttu-id="a72e0-141">任何日历项目 （ [Appointment](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx)对象）</span><span class="sxs-lookup"><span data-stu-id="a72e0-141">Any calendar item (an [Appointment](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) object)</span></span>  <br/> |<span data-ttu-id="a72e0-142">[约会类型](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.appointmenttype%28v=exchg.80%29.aspx)的枚举值</span><span class="sxs-lookup"><span data-stu-id="a72e0-142">The [appointment type](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.appointmenttype%28v=exchg.80%29.aspx) enumeration value</span></span>  <br/> |<span data-ttu-id="a72e0-143">[Appointment.AppointmentType](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.appointment.appointmenttype%28v=exchg.80%29.aspx)属性</span><span class="sxs-lookup"><span data-stu-id="a72e0-143">[Appointment.AppointmentType](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.appointment.appointmenttype%28v=exchg.80%29.aspx) property</span></span>  <br/> |
   
<span data-ttu-id="a72e0-144">下面的代码示例演示如何获取定期主控形状、 名字或姓氏出现系列或出现给定索引。</span><span class="sxs-lookup"><span data-stu-id="a72e0-144">The following code example shows how to get a recurring master, the first or last occurrence in a series, or an occurrence given its index.</span></span>
  
<span data-ttu-id="a72e0-145">此示例假定您具有身份验证向 Exchange 服务器，并已获取名为**服务** [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象。</span><span class="sxs-lookup"><span data-stu-id="a72e0-145">This example assumes that you have authenticated to an Exchange server and have acquired an [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> 
  
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

## <a name="access-calendar-items-in-a-recurring-series-by-using-ews"></a><span data-ttu-id="a72e0-146">使用 EWS 定期系列中的 access 日历项目</span><span class="sxs-lookup"><span data-stu-id="a72e0-146">Access calendar items in a recurring series by using EWS</span></span>

<span data-ttu-id="a72e0-147">访问定期系列中的日历项目是非常类似于访问的日历项目的单个实例。</span><span class="sxs-lookup"><span data-stu-id="a72e0-147">Accessing calendar items in a recurring series is very similar to accessing single instances of calendar items.</span></span> <span data-ttu-id="a72e0-148">您使用[GetItem](http://msdn.microsoft.com/library/769df8eb-9c72-48b5-a49f-82c6b86bc5fc%28Office.15%29.aspx)操作请求，与所需的约会实例[OccurrenceItemId](http://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx)指定所需的属性。</span><span class="sxs-lookup"><span data-stu-id="a72e0-148">You use a [GetItem](http://msdn.microsoft.com/library/769df8eb-9c72-48b5-a49f-82c6b86bc5fc%28Office.15%29.aspx) operation request, specifying the properties you want, with the [OccurrenceItemId](http://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) of the appointment instance you need.</span></span> <span data-ttu-id="a72e0-149">[OccurrenceItemId](http://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx)包含**ItemID**定期主控形状的匹配项，以及其系列中的索引值。</span><span class="sxs-lookup"><span data-stu-id="a72e0-149">The [OccurrenceItemId](http://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) contains the **ItemID** of the occurrence's recurring master, as well as its index value in the series.</span></span> 
  
<span data-ttu-id="a72e0-150">以下 XML 显示了用于返回出现系列由其索引指定的[GetItem](http://msdn.microsoft.com/library/769df8eb-9c72-48b5-a49f-82c6b86bc5fc%28Office.15%29.aspx)请求。</span><span class="sxs-lookup"><span data-stu-id="a72e0-150">The following XML shows the [GetItem](http://msdn.microsoft.com/library/769df8eb-9c72-48b5-a49f-82c6b86bc5fc%28Office.15%29.aspx) request used to return an occurrence in a series specified by its index.</span></span> <span data-ttu-id="a72e0-151">请注意，已为便于阅读缩短**ItemID**定期主控形状。</span><span class="sxs-lookup"><span data-stu-id="a72e0-151">Note that the **ItemID** of the recurring master has been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="a72e0-152">服务器响应**GetItem**请求[GetItemResponse](http://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx)邮件包含的[ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx)值**NoError**，这表明已成功创建电子邮件，以及[ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)的新创建的消息。</span><span class="sxs-lookup"><span data-stu-id="a72e0-152">The server responds to the **GetItem** request with a [GetItemResponse](http://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the email was created successfully, and the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the newly created message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a72e0-153">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a72e0-153">See also</span></span>


- [<span data-ttu-id="a72e0-154">Calendars and EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="a72e0-154">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
- [<span data-ttu-id="a72e0-155">在 Exchange 使用 EWS 获取约会和会议</span><span class="sxs-lookup"><span data-stu-id="a72e0-155">Get appointments and meetings by using EWS in Exchange</span></span>](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)
    

