---
title: 在 Exchange 使用 EWS 获取约会和会议
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1bae582a-8cb3-4e77-be2a-7e107fad26fe
description: 了解如何在 Exchange 使用 EWS 托管 API 或 EWS 获取约会和会议。
ms.openlocfilehash: 0f5eb135142e807f30f48f01d7948fbdbf147ac2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752776"
---
# <a name="get-appointments-and-meetings-by-using-ews-in-exchange"></a><span data-ttu-id="cd5c6-103">在 Exchange 使用 EWS 获取约会和会议</span><span class="sxs-lookup"><span data-stu-id="cd5c6-103">Get appointments and meetings by using EWS in Exchange</span></span>

<span data-ttu-id="cd5c6-104">了解如何在 Exchange 使用 EWS 托管 API 或 EWS 获取约会和会议。</span><span class="sxs-lookup"><span data-stu-id="cd5c6-104">Learn how to get appointments and meetings by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="cd5c6-105">可以通过使用[CalendarFolder.FindAppointments](http://msdn.microsoft.com/en-us/library/dd636179%28v=exchg.80%29.aspx) EWS 托管 API 方法或[FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) EWS 操作从日历文件夹检索约会和会议。</span><span class="sxs-lookup"><span data-stu-id="cd5c6-105">You can retrieve appointments and meetings from a calendar folder by using the [CalendarFolder.FindAppointments](http://msdn.microsoft.com/en-us/library/dd636179%28v=exchg.80%29.aspx) EWS Managed API method or the [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) EWS operation.</span></span> 
  
## <a name="get-appointments-by-using-the-ews-managed-api"></a><span data-ttu-id="cd5c6-106">获取约会使用 EWS 托管 API</span><span class="sxs-lookup"><span data-stu-id="cd5c6-106">Get appointments by using the EWS Managed API</span></span>
<span data-ttu-id="cd5c6-107"><a name="bk_retrieveappsEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="cd5c6-107"></span></span>

<span data-ttu-id="cd5c6-108">下面的代码示例演示如何使用 EWS 托管 API 来检索位于指定的开始和结束时间之间的用户的约会。</span><span class="sxs-lookup"><span data-stu-id="cd5c6-108">The following code example shows how to use the EWS Managed API to retrieve a user's appointments that fall between a specified start and end time.</span></span>
  
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

<span data-ttu-id="cd5c6-109">下面是代码示例的输出。</span><span class="sxs-lookup"><span data-stu-id="cd5c6-109">The following is the output from the code example.</span></span>
  
<span data-ttu-id="cd5c6-110">您从 2013 年 8 日 21/到 2013-9 日 20 的日历的前五个约会是：</span><span class="sxs-lookup"><span data-stu-id="cd5c6-110">The first five appointments on your calendar from 8/21/2013 to 9/20/2013 are:</span></span> 
  
<span data-ttu-id="cd5c6-111">Subject: Contoso 开发人员团队会议开始： 2013 年 8 日 21/12:30:00 最终： 2013-8 日 21 1:00:00</span><span class="sxs-lookup"><span data-stu-id="cd5c6-111">Subject: Contoso devs team meeting Start: 8/21/2013 12:30:00 PM End: 8/21/2013 1:00:00 PM</span></span>
  
<span data-ttu-id="cd5c6-112">Subject： 每日状态会议开始： 2013-8 日 21 1:00:00 最终： 2013 年 8 日 21/2:00:00</span><span class="sxs-lookup"><span data-stu-id="cd5c6-112">Subject: Daily status meeting Start: 8/21/2013 1:00:00 PM End: 8/21/2013 2:00:00 PM</span></span>
  
<span data-ttu-id="cd5c6-113">Subject： 午餐与销售团队开始： 2013-8 日 21 2:30:00 最终： 2013 年 8 日 21/3:30:00</span><span class="sxs-lookup"><span data-stu-id="cd5c6-113">Subject: Lunch with sales team Start: 8/21/2013 2:30:00 PM End: 8/21/2013 3:30:00 PM</span></span>
  
<span data-ttu-id="cd5c6-114">主题： 在俱乐部开始网球： 2013-8 日 22 11:00:00 最终： 2013 年 8 日 22/12:00:00</span><span class="sxs-lookup"><span data-stu-id="cd5c6-114">Subject: Tennis at the club Start: 8/22/2013 11:00:00 AM End: 8/22/2013 12:00:00 PM</span></span>
  
<span data-ttu-id="cd5c6-115">Subject： 联机培训网络广播： 2013-8 日 22 2:00:00 最终： 2013 年 8 日 22/3:00:00</span><span class="sxs-lookup"><span data-stu-id="cd5c6-115">Subject: Online training webcast: 8/22/2013 2:00:00 PM End: 8/22/2013 3:00:00 PM</span></span>
## <a name="get-appointments-by-using-ews"></a><span data-ttu-id="cd5c6-116">通过使用 EWS 获取约会</span><span class="sxs-lookup"><span data-stu-id="cd5c6-116">Get appointments by using EWS</span></span>
<span data-ttu-id="cd5c6-117"><a name="bk_xml"> </a></span><span class="sxs-lookup"><span data-stu-id="cd5c6-117"></span></span>

<span data-ttu-id="cd5c6-118">以下 XML 显示了[GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx)操作请求返回[FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)操作文件夹 ID。</span><span class="sxs-lookup"><span data-stu-id="cd5c6-118">The following XML shows a [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) operation request to return a folder ID for the [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) operation.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
       xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
       xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="cd5c6-119">以下 XML 显示了**GetFolder**响应。</span><span class="sxs-lookup"><span data-stu-id="cd5c6-119">The following XML shows the **GetFolder** response.</span></span> <span data-ttu-id="cd5c6-120">请注意，以便于阅读缩短**文件夹 Id**和**更改密钥**属性。</span><span class="sxs-lookup"><span data-stu-id="cd5c6-120">Note that the **FolderID** and **ChangeKey** attributes are shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="731" MinorBuildNumber="10" Version="V2_3" 
 xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
 xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="cd5c6-121">以下 XML 显示了用于返回请求的约会**FindItem**请求。</span><span class="sxs-lookup"><span data-stu-id="cd5c6-121">The following XML shows the **FindItem** request used to return the requested appointments.</span></span> <span data-ttu-id="cd5c6-122">请注意，以便于阅读缩短**文件夹 Id**和**更改密钥**属性。</span><span class="sxs-lookup"><span data-stu-id="cd5c6-122">Note that the **FolderID** and **ChangeKey** attributes are shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
       xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
       xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="cd5c6-123">以下 XML 显示了**FindItem**响应。</span><span class="sxs-lookup"><span data-stu-id="cd5c6-123">The following XML shows the **FindItem** response.</span></span> <span data-ttu-id="cd5c6-124">请注意，以便于阅读缩短**ItemID**和**更改密钥**属性。</span><span class="sxs-lookup"><span data-stu-id="cd5c6-124">Note that the **ItemID** and **ChangeKey** attributes are shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="731" MinorBuildNumber="10" Version="V2_3" 
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

## <a name="recurring-meetings-and-the-calendar-view"></a><span data-ttu-id="cd5c6-125">定期会议和日历视图</span><span class="sxs-lookup"><span data-stu-id="cd5c6-125">Recurring meetings and the calendar view</span></span>
<span data-ttu-id="cd5c6-126"><a name="bk_recurring"> </a></span><span class="sxs-lookup"><span data-stu-id="cd5c6-126"></span></span>

<span data-ttu-id="cd5c6-127">因为定期系列和定期系列的例外发生次数不是实际的项目中邮箱，而不内部存储为附件定期主日历文件夹从邮箱中的其他文件夹稍有不同。</span><span class="sxs-lookup"><span data-stu-id="cd5c6-127">The calendar folder is a little different from other folders in a mailbox because occurrences in a recurring series and exceptions to a recurring series are not actual items in the mailbox, but rather are stored internally as attachments to a recurring master.</span></span> <span data-ttu-id="cd5c6-128">这意味着，虽然您可以创建 EWS 请求的返回值之间一**开始**和**结束**值使用 EWS 托管 API **FindItems**重载方法，如[ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)或 EWS [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)操作，EWS 不外观通过附件表中的每个日历项目，以查找例外和匹配项。</span><span class="sxs-lookup"><span data-stu-id="cd5c6-128">This means that although you can create an EWS request that returns values between a set of **start** and **end** values by using one of the EWS Managed API **FindItems** overload methods, such as [ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) or the EWS [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) operation, EWS would not look through the attachment table of every calendar item to find exceptions and occurrences.</span></span> 
  
<span data-ttu-id="cd5c6-129">相反，您确实要执行操作是有下面应用*Dataview*到的两个 SQL 表，联合使用[CalendarView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx)对象。</span><span class="sxs-lookup"><span data-stu-id="cd5c6-129">Instead, what you really want to do is something akin to applying a  *Dataview*  onto a union of two SQL tables, using a [CalendarView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx) object.</span></span> <span data-ttu-id="cd5c6-130">请注意，出于性能原因，我们建议您使用的[属性集](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx)属性以通过指示约会或会议要返回，以及所需的特定属性的数量限制的响应的大小。</span><span class="sxs-lookup"><span data-stu-id="cd5c6-130">Note that for performance reasons, we recommend that you use the [PropertySet](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) property to limit the size of the response by indicating the number of appointments or meetings you want returned, as well as the specific properties you want.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cd5c6-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cd5c6-131">See also</span></span>
<span data-ttu-id="cd5c6-132"><a name="bk_additional"> </a></span><span class="sxs-lookup"><span data-stu-id="cd5c6-132"></span></span>

- [<span data-ttu-id="cd5c6-133">Calendars and EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="cd5c6-133">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    
- [<span data-ttu-id="cd5c6-134">使用 Exchange 2013 中的 EWS 中创建约会和会议</span><span class="sxs-lookup"><span data-stu-id="cd5c6-134">Create appointments and meetings by using EWS in Exchange 2013</span></span>](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [<span data-ttu-id="cd5c6-135">在 Exchange 使用 EWS 更新约会和会议</span><span class="sxs-lookup"><span data-stu-id="cd5c6-135">Update appointments and meetings by using EWS in Exchange</span></span>](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="cd5c6-136">删除约会，并在 Exchange 使用 EWS 取消会议</span><span class="sxs-lookup"><span data-stu-id="cd5c6-136">Delete appointments and cancel meetings by using EWS in Exchange</span></span>](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="cd5c6-137">开发 Exchange Web 服务客户端</span><span class="sxs-lookup"><span data-stu-id="cd5c6-137">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    

