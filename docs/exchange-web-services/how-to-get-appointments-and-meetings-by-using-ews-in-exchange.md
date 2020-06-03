---
title: 使用 Exchange 中的 EWS 获取约会和会议
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 1bae582a-8cb3-4e77-be2a-7e107fad26fe
description: 了解如何使用 Exchange 中的 EWS 托管 API 或 EWS 获取约会和会议。
localization_priority: Priority
ms.openlocfilehash: d951bfeccdf50ae1397ecdd4887ed05548b25001
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528088"
---
# <a name="get-appointments-and-meetings-by-using-ews-in-exchange"></a><span data-ttu-id="0751c-103">使用 Exchange 中的 EWS 获取约会和会议</span><span class="sxs-lookup"><span data-stu-id="0751c-103">Get appointments and meetings by using EWS in Exchange</span></span>

<span data-ttu-id="0751c-104">了解如何使用 Exchange 中的 EWS 托管 API 或 EWS 获取约会和会议。</span><span class="sxs-lookup"><span data-stu-id="0751c-104">Learn how to get appointments and meetings by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="0751c-105">您可以使用[CalendarFolder](https://msdn.microsoft.com/library/dd636179%28v=exchg.80%29.aspx) EWS 托管 API 方法或[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) ews 操作从 "日历" 文件夹中检索约会和会议。</span><span class="sxs-lookup"><span data-stu-id="0751c-105">You can retrieve appointments and meetings from a calendar folder by using the [CalendarFolder.FindAppointments](https://msdn.microsoft.com/library/dd636179%28v=exchg.80%29.aspx) EWS Managed API method or the [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) EWS operation.</span></span> 
  
## <a name="get-appointments-by-using-the-ews-managed-api"></a><span data-ttu-id="0751c-106">使用 EWS 托管 API 获取约会</span><span class="sxs-lookup"><span data-stu-id="0751c-106">Get appointments by using the EWS Managed API</span></span>
<span data-ttu-id="0751c-107"><a name="bk_retrieveappsEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="0751c-107"><a name="bk_retrieveappsEWSMA"> </a></span></span>

<span data-ttu-id="0751c-108">下面的代码示例演示如何使用 EWS 托管 API 检索介于指定开始时间和结束时间之间的用户约会。</span><span class="sxs-lookup"><span data-stu-id="0751c-108">The following code example shows how to use the EWS Managed API to retrieve a user's appointments that fall between a specified start and end time.</span></span>
  
```cs
       // Initialize values for the start and end times, and the number of appointments to retrieve.
            DateTime startDate = DateTime.Now;
            DateTime endDate = startDate.AddDays(30);
            const int NUM_APPTS = 5;
            // Initialize the calendar folder object with only the folder ID. 
            CalendarFolder calendar = CalendarFolder.Bind(service, WellKnownFolderName.Calendar, new PropertySet());
            // Set the start and end time and number of appointments to retrieve.
            CalendarView cView = new CalendarView(startDate, endDate, NUM_APPTS);
            // Limit the properties returned to the appointment's subject, start time, and end time.
            cView.PropertySet = new PropertySet(AppointmentSchema.Subject, AppointmentSchema.Start, AppointmentSchema.End);
            // Retrieve a collection of appointments by using the calendar view.
            FindItemsResults<Appointment> appointments = calendar.FindAppointments(cView);
            Console.WriteLine("\nThe first " + NUM_APPTS + " appointments on your calendar from " + startDate.Date.ToShortDateString() + 
                              " to " + endDate.Date.ToShortDateString() + " are: \n");
            
            foreach (Appointment a in appointments)
            {
                Console.Write("Subject: " + a.Subject.ToString() + " ");
                Console.Write("Start: " + a.Start.ToString() + " ");
                Console.Write("End: " + a.End.ToString());
                Console.WriteLine();
            }

```

<br/>

<span data-ttu-id="0751c-109">以下是代码示例中的输出。</span><span class="sxs-lookup"><span data-stu-id="0751c-109">The following is the output from the code example.</span></span>
  
```text
The first five appointments on your calendar from 8/21/2013 to 9/20/2013 are: 
  
Subject: Contoso devs team meeting Start: 8/21/2013 12:30:00 PM End: 8/21/2013 1:00:00 PM
  
Subject: Daily status meeting Start: 8/21/2013 1:00:00 PM End: 8/21/2013 2:00:00 PM
  
Subject: Lunch with sales team Start: 8/21/2013 2:30:00 PM End: 8/21/2013 3:30:00 PM
  
Subject: Tennis at the club Start: 8/22/2013 11:00:00 AM End: 8/22/2013 12:00:00 PM
  
Subject: Online training webcast: 8/22/2013 2:00:00 PM End: 8/22/2013 3:00:00 PM
```

## <a name="get-appointments-by-using-ews"></a><span data-ttu-id="0751c-110">使用 EWS 获取约会</span><span class="sxs-lookup"><span data-stu-id="0751c-110">Get appointments by using EWS</span></span>
<span data-ttu-id="0751c-111"><a name="bk_xml"> </a></span><span class="sxs-lookup"><span data-stu-id="0751c-111"><a name="bk_xml"> </a></span></span>

<span data-ttu-id="0751c-112">下面的 XML 显示[GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx)操作请求，以返回[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)操作的文件夹 ID。</span><span class="sxs-lookup"><span data-stu-id="0751c-112">The following XML shows a [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) operation request to return a folder ID for the [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) operation.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
       xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
       xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:GetFolder>
      <m:FolderShape>
        <t:BaseShape>IdOnly</t:BaseShape>
      </m:FolderShape>
      <m:FolderIds>
        <t:DistinguishedFolderId Id="calendar" />
      </m:FolderIds>
    </m:GetFolder>
  </soap:Body>
</soap:Envelope>
```

<br/>

<span data-ttu-id="0751c-113">下面的 XML 显示**GetFolder**响应。</span><span class="sxs-lookup"><span data-stu-id="0751c-113">The following XML shows the **GetFolder** response.</span></span> <span data-ttu-id="0751c-114">请注意， **FolderID**和**ChangeKey**属性会因可读性而缩短。</span><span class="sxs-lookup"><span data-stu-id="0751c-114">Note that the **FolderID** and **ChangeKey** attributes are shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="731" MinorBuildNumber="10" Version="V2_3" 
 xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:CalendarFolder>
              <t:FolderId Id="AAMk" ChangeKey="AgAA" />
            </t:CalendarFolder>
          </m:Folders>
        </m:GetFolderResponseMessage>
      </m:ResponseMessages>
    </m:GetFolderResponse>
  </s:Body>
</s:Envelope>
```

<br/>

<span data-ttu-id="0751c-115">下面的 XML 显示了用于返回请求的约会的**FindItem**请求。</span><span class="sxs-lookup"><span data-stu-id="0751c-115">The following XML shows the **FindItem** request used to return the requested appointments.</span></span> <span data-ttu-id="0751c-116">请注意， **FolderID**和**ChangeKey**属性会因可读性而缩短。</span><span class="sxs-lookup"><span data-stu-id="0751c-116">Note that the **FolderID** and **ChangeKey** attributes are shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
       xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
       xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="calendar:Start" />
          <t:FieldURI FieldURI="calendar:End" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:CalendarView MaxEntriesReturned="5" StartDate="2013-08-21T17:30:24.127Z" EndDate="2013-09-20T17:30:24.127Z" />
      <m:ParentFolderIds>
        <t:FolderId Id="AAMk" ChangeKey="AgAA" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

<br/>

<span data-ttu-id="0751c-117">下面的 XML 显示**FindItem**响应。</span><span class="sxs-lookup"><span data-stu-id="0751c-117">The following XML shows the **FindItem** response.</span></span> <span data-ttu-id="0751c-118">请注意， **ItemID**和**ChangeKey**属性将缩短以提高可读性。</span><span class="sxs-lookup"><span data-stu-id="0751c-118">Note that the **ItemID** and **ChangeKey** attributes are shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="731" MinorBuildNumber="10" Version="V2_3" 
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
          <m:RootFolder TotalItemsInView="33" IncludesLastItemInRange="false">
            <t:Items>
              <t:CalendarItem>
                <t:ItemId Id="AAMk" ChangeKey="DwAA" />
                <t:Subject>Contoso devs team meeting</t:Subject>
                <t:Start>2013-08-21T19:30:00Z</t:Start>
                <t:End>2013-08-21T20:00:00Z</t:End>
              </t:CalendarItem>
              <t:CalendarItem>
                <t:ItemId Id="AAMk" ChangeKey="DwAA" />
                <t:Subject>Daily status meeting</t:Subject>
                <t:Start>2013-08-21T20:00:00Z</t:Start>
                <t:End>2013-08-21T21:00:00Z</t:End>
              </t:CalendarItem>
              <t:CalendarItem>
                <t:ItemId Id="AAMk" ChangeKey="DwAA" />
                <t:Subject>Lunch with sales team</t:Subject>
                <t:Start>2013-08-21T21:30:00Z</t:Start>
                <t:End>2013-08-21T22:30:00Z</t:End>
              </t:CalendarItem>
              <t:CalendarItem>
                <t:ItemId Id="AAMk" ChangeKey="DwAA" />
                <t:Subject>Tennis at the club</t:Subject>
                <t:Start>2013-08-22T18:00:00Z</t:Start>
                <t:End>2013-08-22T19:00:00Z</t:End>
              </t:CalendarItem>
              <t:CalendarItem>
                <t:ItemId Id="AAMkA" ChangeKey="DwAA" />
                <t:Subject>Online training webcast</t:Subject>
                <t:Start>2013-08-22T21:00:00Z</t:Start>
                <t:End>2013-08-22T22:00:00Z</t:End>
              </t:CalendarItem>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

## <a name="recurring-meetings-and-the-calendar-view"></a><span data-ttu-id="0751c-119">定期会议和日历视图</span><span class="sxs-lookup"><span data-stu-id="0751c-119">Recurring meetings and the calendar view</span></span>
<span data-ttu-id="0751c-120"><a name="bk_recurring"> </a></span><span class="sxs-lookup"><span data-stu-id="0751c-120"><a name="bk_recurring"> </a></span></span>

<span data-ttu-id="0751c-121">"日历" 文件夹与邮箱中的其他文件夹略有不同，因为定期系列中的事件和定期系列的例外并不是邮箱中的实际项目，而是作为定期母版的附件在内部存储。</span><span class="sxs-lookup"><span data-stu-id="0751c-121">The calendar folder is a little different from other folders in a mailbox because occurrences in a recurring series and exceptions to a recurring series are not actual items in the mailbox, but rather are stored internally as attachments to a recurring master.</span></span> <span data-ttu-id="0751c-122">这意味着，尽管您可以使用 EWS 托管 API **FindItems**重载方法（如[EXCHANGESERVICE FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)或 EWS [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)操作）创建在一组**开始**值和**结束**值之间返回值的 EWS 请求，但 ews 不会在每个日历项的附件表中查找异常和匹配项。</span><span class="sxs-lookup"><span data-stu-id="0751c-122">This means that although you can create an EWS request that returns values between a set of **start** and **end** values by using one of the EWS Managed API **FindItems** overload methods, such as [ExchangeService.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) or the EWS [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) operation, EWS would not look through the attachment table of every calendar item to find exceptions and occurrences.</span></span> 
  
<span data-ttu-id="0751c-123">相反，您真正想要做的是，使用[CalendarView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx)对象将*Dataview*应用到两个 SQL 表的联合中是类似的。</span><span class="sxs-lookup"><span data-stu-id="0751c-123">Instead, what you really want to do is something akin to applying a  *Dataview*  onto a union of two SQL tables, using a [CalendarView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx) object.</span></span> <span data-ttu-id="0751c-124">请注意，出于性能原因，建议使用[PropertySet](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx)属性来限制响应的大小，方法是指明要返回的约会或会议的数目，以及所需的特定属性。</span><span class="sxs-lookup"><span data-stu-id="0751c-124">Note that for performance reasons, we recommend that you use the [PropertySet](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) property to limit the size of the response by indicating the number of appointments or meetings you want returned, as well as the specific properties you want.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0751c-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0751c-125">See also</span></span>
<span data-ttu-id="0751c-126"><a name="bk_additional"> </a></span><span class="sxs-lookup"><span data-stu-id="0751c-126"><a name="bk_additional"> </a></span></span>

- [<span data-ttu-id="0751c-127">Calendars and EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="0751c-127">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)   
- [<span data-ttu-id="0751c-128">使用 Exchange 2013 中的 EWS 创建约会和会议</span><span class="sxs-lookup"><span data-stu-id="0751c-128">Create appointments and meetings by using EWS in Exchange 2013</span></span>](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)  
- [<span data-ttu-id="0751c-129">使用 Exchange 中的 EWS 更新约会和会议</span><span class="sxs-lookup"><span data-stu-id="0751c-129">Update appointments and meetings by using EWS in Exchange</span></span>](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)  
- [<span data-ttu-id="0751c-130">使用 Exchange 中的 EWS 删除约会和取消会议</span><span class="sxs-lookup"><span data-stu-id="0751c-130">Delete appointments and cancel meetings by using EWS in Exchange</span></span>](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md) 
- [<span data-ttu-id="0751c-131">开发 Exchange Web 服务客户端</span><span class="sxs-lookup"><span data-stu-id="0751c-131">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    

