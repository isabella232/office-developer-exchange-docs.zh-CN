---
title: 使用 EWS 在 Exchange 中删除定期系列中的约会
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a9d5244a-bc4a-4e9c-9c6c-ff361e04cbf8
description: 了解如何通过使用 EWS 的 EWS 托管 API 在 Exchange 中删除定期系列中的约会。
ms.openlocfilehash: 5e4d95058808adf8db159000bdf90c1f92945338
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752786"
---
# <a name="delete-appointments-in-a-recurring-series-by-using-ews-in-exchange"></a><span data-ttu-id="918a2-103">使用 EWS 在 Exchange 中删除定期系列中的约会</span><span class="sxs-lookup"><span data-stu-id="918a2-103">Delete appointments in a recurring series by using EWS in Exchange</span></span>

<span data-ttu-id="918a2-104">了解如何通过使用 EWS 的 EWS 托管 API 在 Exchange 中删除定期系列中的约会。</span><span class="sxs-lookup"><span data-stu-id="918a2-104">Learn how to delete appointments in a recurring series by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="918a2-105">您可以使用 EWS 托管 API 或 EWS 删除约会或会议，一系列中的一个实例。</span><span class="sxs-lookup"><span data-stu-id="918a2-105">You can use the EWS Managed API or EWS to delete a series of appointments or meetings, or just one instance in the series.</span></span> <span data-ttu-id="918a2-106">用于删除整个数据系列的过程本质上是您用于删除不仅仅是一个匹配项的过程相同。</span><span class="sxs-lookup"><span data-stu-id="918a2-106">The process you use to delete an entire series is essentially the same as the process you use to delete just a single occurrence.</span></span> <span data-ttu-id="918a2-107">您使用的相同的 EWS 托管 API 方法或您使用来[删除单实例约会或会议](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)的 EWS 操作。</span><span class="sxs-lookup"><span data-stu-id="918a2-107">You use the same EWS Managed API methods or EWS operations that you use to [delete a single instance appointment or meeting](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md).</span></span> <span data-ttu-id="918a2-108">区别在于方法或操作中包含的项 ID。</span><span class="sxs-lookup"><span data-stu-id="918a2-108">The difference is in the item ID that is included in the method or operation.</span></span> <span data-ttu-id="918a2-109">让我们先看如何这两种方案都相同。</span><span class="sxs-lookup"><span data-stu-id="918a2-109">Let's start by looking at how both scenarios are the same.</span></span> 
  
<span data-ttu-id="918a2-110">为了删除定期系列或定期系列中的一个匹配项，您需要查找匹配项或想要删除，然后调用相应的方法或操作，以删除它的系列。</span><span class="sxs-lookup"><span data-stu-id="918a2-110">In order to delete a recurring series or a single occurrence in a recurring series, you need to find the occurrence or series that you want to delete, and then call the appropriate method or operation to remove it.</span></span> <span data-ttu-id="918a2-111">时只可以删除任何类型的约会，我们建议您保持最新的所有与会者或组织者和取消用户已组织的会议，并拒绝用户未不将组织的会议。</span><span class="sxs-lookup"><span data-stu-id="918a2-111">While you can simply delete any type of appointment, we recommend that you keep any attendees or the organizer up to date and cancel meetings that the user has organized and decline meetings that the user did not organize.</span></span>
  
<span data-ttu-id="918a2-112">因此，如何方案不同？</span><span class="sxs-lookup"><span data-stu-id="918a2-112">So how are the scenarios different?</span></span> <span data-ttu-id="918a2-113">它是所有[Appointment](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx)对象用于调用 （对于 EWS 托管 API) 的方法或项目 ID 包含有关的操作请求中 （EWS)。</span><span class="sxs-lookup"><span data-stu-id="918a2-113">It's all about the [Appointment](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) object used to invoke the method (for the EWS Managed API) or the item ID included in the operation request (for EWS).</span></span> <span data-ttu-id="918a2-114">若要删除整个数据系列，您需要定期主**约会**项目或对象 ID。</span><span class="sxs-lookup"><span data-stu-id="918a2-114">To delete an entire series, you need the **Appointment** object or item ID for the recurring master.</span></span> <span data-ttu-id="918a2-115">若要删除的一个匹配项，您需要的**约会**项目或对象 ID 的匹配项。</span><span class="sxs-lookup"><span data-stu-id="918a2-115">To delete a single occurrence, you need the **Appointment** object or item ID for the occurrence.</span></span> 
  
## <a name="delete-a-recurring-appointment-by-using-the-ews-managed-api"></a><span data-ttu-id="918a2-116">使用 EWS 托管 API 中删除的定期约会</span><span class="sxs-lookup"><span data-stu-id="918a2-116">Delete a recurring appointment by using the EWS Managed API</span></span>

<span data-ttu-id="918a2-117">此示例假定您具有身份验证向 Exchange 服务器，并已获取名为**服务** [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象。</span><span class="sxs-lookup"><span data-stu-id="918a2-117">This example assumes that you have authenticated to an Exchange server and have acquired an [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> <span data-ttu-id="918a2-118">_RecurringItem_参数是定期的主控形状或一次的**约会**对象。</span><span class="sxs-lookup"><span data-stu-id="918a2-118">The  _recurringItem_ parameter is an **Appointment** object for either the recurring master or a single occurrence.</span></span> <span data-ttu-id="918a2-119">_DeleteEntireSeries_参数，指示是否删除整个数据系列的_recurringItem_的一部分。</span><span class="sxs-lookup"><span data-stu-id="918a2-119">The  _deleteEntireSeries_ parameter indicates whether to delete the entire series that the  _recurringItem_ is a part of.</span></span> 
  
```cs
public static bool DeleteRecurringItem(ExchangeService service, Appointment recurringItem, bool deleteEntireSeries)
{
    Appointment appointmentToDelete = null;
    // If the item is a single appointment, fail.
    if (recurringItem.AppointmentType == AppointmentType.Single)
    {
        Console.WriteLine("ERROR: The item to delete is not part of a recurring series.");
        return false;
    }
    // Check the Appointment that was passed. Is it
    // an occurrence or the recurring master?
    if (recurringItem.AppointmentType == AppointmentType.RecurringMaster)
    {
        if (!deleteEntireSeries)
        {
            // The item is the recurring master, so deleting it will delete
            // the entire series. The caller indicated that the entire series
            // should not be deleted, so fail.
            Console.WriteLine("ERROR: The item to delete is the recurring master of the series. Deleting it will delete the entire series.");
            return false;
        }
        else
        {
            appointmentToDelete = recurringItem;
        }
    }
    else
    {
        if (deleteEntireSeries)
        {
            // The item passed is not the recurring master, but the caller
            // wants to delete the entire series. Bind to the recurring
            // master to delete it.
            try
            {
                appointmentToDelete = Appointment.BindToRecurringMaster(service, recurringItem.Id);
            }
            catch (Exception ex)
            {
                Console.WriteLine("ERROR: {0}", ex.Message);
                return false;
            }
        }
        else
        {
            // The item passed is not the recurring master, but the caller
            // only wants to delete the occurrence, so just
            // delete the passed item.
            appointmentToDelete = recurringItem;
        }
    }
    if (appointmentToDelete != null)
    {
        // Remove the item, depending on the scenario. 
        if (appointmentToDelete.IsMeeting)
        {
            CalendarActionResults results;
            // If it's a meeting and the user is the organizer, cancel it.
            // Determine this by testing the AppointmentState bitmask for 
            // the presence of the second bit. This bit indicates that the appointment
            // was received, which means that someone sent it to the user. Therefore,
            // they're not the organizer.
            int isReceived = 2;
            if ((appointmentToDelete.AppointmentState &amp; isReceived) == 0)
            {
                results = appointmentToDelete.CancelMeeting("Cancelling this meeting.");
                return true;
            }
            // If it's a meeting and the user is not the organizer, decline it.
            else
            {
                results = appointmentToDelete.Decline(true);
                return true;
            }
        }
        else
        {
            // The item isn't a meeting, so just delete it.
            appointmentToDelete.Delete(DeleteMode.MoveToDeletedItems);
            return true;
        }
    }
    return false;
}
```

<span data-ttu-id="918a2-120">若要使用此示例，您需要[将绑定到匹配项或定期主控形状](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)，并将生成的**Appointment**对象传递给方法。</span><span class="sxs-lookup"><span data-stu-id="918a2-120">In order to use this example, you need to [bind to either an occurrence or the recurring master](how-to-access-a-recurring-series-by-using-ews-in-exchange.md), and pass the resulting **Appointment** object to the method.</span></span> <span data-ttu-id="918a2-121">请记住如果通过使用[CalendarView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx)类访问约会，生成的项目的所有单个匹配项。</span><span class="sxs-lookup"><span data-stu-id="918a2-121">Keep in mind that if you access appointments by using a [CalendarView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx) class, the resulting items are all single occurrences.</span></span> <span data-ttu-id="918a2-122">相反，如果您使用的[属性查看](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx)类，生成的项目是定期的所有主控形状。</span><span class="sxs-lookup"><span data-stu-id="918a2-122">Conversely, if you use the [ItemView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx) class, the resulting items are all recurring masters.</span></span> 
  
## <a name="delete-a-recurring-appointment-by-using-ews"></a><span data-ttu-id="918a2-123">使用 EWS 删除的定期约会</span><span class="sxs-lookup"><span data-stu-id="918a2-123">Delete a recurring appointment by using EWS</span></span>

<span data-ttu-id="918a2-124">使用 EWS 删除定期系列是[删除单个会议](how-to-delete-appointments-in-a-recurring-series-by-using-ews-in-exchange.md)相同。</span><span class="sxs-lookup"><span data-stu-id="918a2-124">Deleting a recurring series by using EWS is the same as [deleting a single-instance meeting](how-to-delete-appointments-in-a-recurring-series-by-using-ews-in-exchange.md).</span></span> <span data-ttu-id="918a2-125">实际上，SOAP 请求带有相同的格式。</span><span class="sxs-lookup"><span data-stu-id="918a2-125">In fact, the SOAP requests take the same format.</span></span> <span data-ttu-id="918a2-126">同样的密钥是请求中使用的项 ID。</span><span class="sxs-lookup"><span data-stu-id="918a2-126">Again, the key is the item ID used in the request.</span></span> <span data-ttu-id="918a2-127">如果项目 ID 对应的定期母版，则将删除整个数据系列。</span><span class="sxs-lookup"><span data-stu-id="918a2-127">If the item ID corresponds to the recurring master, the entire series will be deleted.</span></span> <span data-ttu-id="918a2-128">如果项目 ID 对应的一个匹配项，将删除仅的匹配项。</span><span class="sxs-lookup"><span data-stu-id="918a2-128">If the item ID corresponds to a single occurrence, only that occurrence will be deleted.</span></span>
  
> [!NOTE]
> <span data-ttu-id="918a2-129">在下面的代码示例，以便于阅读缩短**ItemId**、**更改密钥**，和**RecurringMasterId**属性。</span><span class="sxs-lookup"><span data-stu-id="918a2-129">In the code examples that follow, the **ItemId**, **ChangeKey**, and **RecurringMasterId** attributes are shortened for readability.</span></span> 
  
<span data-ttu-id="918a2-130">此示例使用[CreateItem operation，](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx)与[CancelCalendarItem](http://msdn.microsoft.com/library/a2046402-a176-44d5-b4b3-adb696581935%28Office.15%29.aspx)元素取消其用户是组织者的会议。</span><span class="sxs-lookup"><span data-stu-id="918a2-130">This example uses the [CreateItem operation](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) with a [CancelCalendarItem](http://msdn.microsoft.com/library/a2046402-a176-44d5-b4b3-adb696581935%28Office.15%29.aspx) element to cancel a meeting for which the user is the organizer.</span></span> <span data-ttu-id="918a2-131">[ReferenceItemId](http://msdn.microsoft.com/library/8fd4bb12-a94b-43f5-be3b-f435684e311d%28Office.15%29.aspx)元素的值指示的项，若要取消，并且可以定期主控形状或单个匹配项的项 ID。</span><span class="sxs-lookup"><span data-stu-id="918a2-131">The value of the [ReferenceItemId](http://msdn.microsoft.com/library/8fd4bb12-a94b-43f5-be3b-f435684e311d%28Office.15%29.aspx) element indicates the item to cancel, and can be the item ID of a recurring master or a single occurrence.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Eastern Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:CreateItem MessageDisposition="SendAndSaveCopy">
      <m:Items>
        <t:CancelCalendarItem>
          <t:ReferenceItemId Id="AAMkADA5..." ChangeKey="DwAAABYA..." />
          <t:NewBodyContent BodyType="HTML">Cancelling this meeting.</t:NewBodyContent>
        </t:CancelCalendarItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="918a2-132">此示例使用**CreateItem operation，** 与[DeclineItem](http://msdn.microsoft.com/library/2d8d2389-924e-4d03-a324-35d56cf0d6b1%28Office.15%29.aspx)元素拒绝其用户不是组织者的会议。</span><span class="sxs-lookup"><span data-stu-id="918a2-132">This example uses the **CreateItem operation** with a [DeclineItem](http://msdn.microsoft.com/library/2d8d2389-924e-4d03-a324-35d56cf0d6b1%28Office.15%29.aspx) element to decline a meeting for which the user is not the organizer.</span></span> <span data-ttu-id="918a2-133">与前面的示例， **ReferenceItemId**元素的值指示要拒绝的项，并且可以是定期主控形状或单个匹配项的项 ID。</span><span class="sxs-lookup"><span data-stu-id="918a2-133">As in the previous example, the value of the **ReferenceItemId** element indicates the item to decline, and can be the item ID of a recurring master or a single occurrence.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Eastern Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:CreateItem MessageDisposition="SendAndSaveCopy">
      <m:Items>
        <t:DeclineItem>
          <t:ReferenceItemId Id="AAMkADA6..." ChangeKey="DwAAABYA..." />
        </t:DeclineItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="918a2-134">此示例使用[删除项操作](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx)删除没有与会者的约会发生一次。</span><span class="sxs-lookup"><span data-stu-id="918a2-134">This example uses the [DeleteItem operation](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) to delete a single occurrence of an appointment with no attendees.</span></span> <span data-ttu-id="918a2-135">指定要删除的匹配项[OccurrenceItemId](http://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx)元素，后者在构建的定期主项目 ID 和匹配项的索引。</span><span class="sxs-lookup"><span data-stu-id="918a2-135">The occurrence to delete is specified by the [OccurrenceItemId](http://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) element, which is constructed from the item ID of the recurring master and the index of the occurrence.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Eastern Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:DeleteItem DeleteType="MoveToDeletedItems" SendMeetingCancellations="SendToAllAndSaveCopy">
      <m:ItemIds>
        <t:OccurrenceItemId RecurringMasterId="AAMkADA8..." InstanceIndex="3" />
      </m:ItemIds>
    </m:DeleteItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="918a2-136">请注意，您可以通过**OccurrenceItemId**元素替换[ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)元素，其中包含的匹配项的项 ID，如下所示获取相同的结果。</span><span class="sxs-lookup"><span data-stu-id="918a2-136">Note that you can get the same result by replacing the **OccurrenceItemId** element with an [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) element that contains the item ID of the occurrence, as shown.</span></span> 
  
```XML
<m:ItemIds>
  <t:ItemId Id="AAMkADA7..." ChangeKey="DwAAABYA..." />
</m:ItemIds>

```

## <a name="see-also"></a><span data-ttu-id="918a2-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="918a2-137">See also</span></span>


- [<span data-ttu-id="918a2-138">定期模式和 EWS</span><span class="sxs-lookup"><span data-stu-id="918a2-138">Recurrence patterns and EWS</span></span>](recurrence-patterns-and-ews.md)
    
- [<span data-ttu-id="918a2-139">在 Exchange 中使用 EWS 访问定期系列</span><span class="sxs-lookup"><span data-stu-id="918a2-139">Access a recurring series by using EWS in Exchange</span></span>](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="918a2-140">使用 EWS 在 Exchange 中创建定期系列</span><span class="sxs-lookup"><span data-stu-id="918a2-140">Create a recurring series by using EWS in Exchange</span></span>](how-to-create-a-recurring-series-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="918a2-141">使用 EWS 更新定期系列</span><span class="sxs-lookup"><span data-stu-id="918a2-141">Update a recurring series by using EWS</span></span>](how-to-update-a-recurring-series-by-using-ews.md)
    
- [<span data-ttu-id="918a2-142">在 Exchange 使用 EWS 更新定期系列</span><span class="sxs-lookup"><span data-stu-id="918a2-142">Update a recurring series by using EWS in Exchange</span></span>](how-to-update-a-recurring-series-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="918a2-143">Calendars and EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="918a2-143">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    
- [<span data-ttu-id="918a2-144">使用 Exchange 2013 中的 EWS 中创建约会和会议</span><span class="sxs-lookup"><span data-stu-id="918a2-144">Create appointments and meetings by using EWS in Exchange 2013</span></span>](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [<span data-ttu-id="918a2-145">删除约会，并在 Exchange 使用 EWS 取消会议</span><span class="sxs-lookup"><span data-stu-id="918a2-145">Delete appointments and cancel meetings by using EWS in Exchange</span></span>](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    

