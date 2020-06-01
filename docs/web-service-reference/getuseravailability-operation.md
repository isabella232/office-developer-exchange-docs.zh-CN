---
title: GetUserAvailability 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetUserAvailability
api_type:
- schema
ms.assetid: 8da17226-5d3a-4525-9ffa-d83730f47bb1
description: 查找有关 GetUserAvailability EWS 操作的信息。
ms.openlocfilehash: b6d03c7da65e3f30f093b7e41448abcca2330a84
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458220"
---
# <a name="getuseravailability-operation"></a><span data-ttu-id="3d418-103">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="3d418-103">GetUserAvailability operation</span></span>

<span data-ttu-id="3d418-104">查找有关**GetUserAvailability** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="3d418-104">Find information about the **GetUserAvailability** EWS operation.</span></span> 
  
<span data-ttu-id="3d418-105">**GetUserAvailability**操作提供了有关一组用户、会议室和资源在指定时间段内的可用性的详细信息。</span><span class="sxs-lookup"><span data-stu-id="3d418-105">The **GetUserAvailability** operation provides detailed information about the availability of a set of users, rooms, and resources within a specified time period.</span></span> 
  
## <a name="using-the-getuseravailability-operation"></a><span data-ttu-id="3d418-106">使用 GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="3d418-106">Using the GetUserAvailability operation</span></span>

<span data-ttu-id="3d418-107">**GetUserAvailability**操作提供了特定的详细信息级别的当前用户可用性信息。</span><span class="sxs-lookup"><span data-stu-id="3d418-107">The **GetUserAvailability** operation provides current user availability information at a specified level of detail.</span></span> <span data-ttu-id="3d418-108">客户端应用程序（如 Outlook、Outlook Web Access、Outlook Mobile Access 和其他应用程序）使用 SMTP 地址来标识请求的用户信息。</span><span class="sxs-lookup"><span data-stu-id="3d418-108">Client applications such as Outlook, Outlook Web Access, Outlook Mobile Access, and others use SMTP addresses to identify the requested user information.</span></span> 
  
<span data-ttu-id="3d418-109">可用性服务展开通讯组列表，以检索列表中每个成员的忙/闲状态，前提是通讯组列表中的邮箱数小于100，这是**GetUserAvailability**操作可以请求的最大标识数。</span><span class="sxs-lookup"><span data-stu-id="3d418-109">The Availability service expands distribution lists to retrieve the free/busy status for each member of the list, as long as the number of mailboxes in the distribution list is less than 100, which is the maximum number of identities that the **GetUserAvailability** operation can request.</span></span> <span data-ttu-id="3d418-110">通讯组列表成员的忙/闲状态将合并为整个通讯组列表的一个忙/闲状态。</span><span class="sxs-lookup"><span data-stu-id="3d418-110">The free/busy statuses of the members of the distribution list are merged into a single free/busy status for the whole distribution list.</span></span> 
  
<span data-ttu-id="3d418-111">客户端应用程序请求指定可用性查询的时间段。</span><span class="sxs-lookup"><span data-stu-id="3d418-111">Client application requests specify the time period of the availability query.</span></span> <span data-ttu-id="3d418-112">请求的信息的默认时间段为42天。</span><span class="sxs-lookup"><span data-stu-id="3d418-112">The default time period for the requested information is 42 days.</span></span> <span data-ttu-id="3d418-113">如果用户的日历包含的约会或会议在指定的时间段内和该查询之外，则返回该约会。</span><span class="sxs-lookup"><span data-stu-id="3d418-113">If the user's calendar contains appointments or meetings that are both within and outside the defined time period for the query, the appointment is returned.</span></span> 
  
<span data-ttu-id="3d418-114">返回的约会和会议时间与请求会议的客户端应用程序位于相同的时区。</span><span class="sxs-lookup"><span data-stu-id="3d418-114">The appointment and meeting times that are returned are in the same time zone as the client application that is requesting the meeting.</span></span>
  
<span data-ttu-id="3d418-115">可用性服务处理每个客户端的请求。</span><span class="sxs-lookup"><span data-stu-id="3d418-115">The Availability service processes the request for each client.</span></span> <span data-ttu-id="3d418-116">服务展开所有定期约会，并返回请求客户端有权接收的日历详细信息的最大数量。</span><span class="sxs-lookup"><span data-stu-id="3d418-116">The service expands all the recurring appointments and returns the maximum number of calendar details that the requesting client has permission to receive.</span></span>
  
> [!NOTE]
> <span data-ttu-id="3d418-117">如果目标邮箱不可用或找不到，则会引发**MailRecipientNotFoundException**异常。</span><span class="sxs-lookup"><span data-stu-id="3d418-117">If the target mailbox is unavailable or cannot be found, a **MailRecipientNotFoundException** exception is thrown.</span></span> <span data-ttu-id="3d418-118">客户端收到一条错误消息，指出在 Active Directory 目录服务或 Active Directory 域服务（AD DS）中找不到邮件收件人。</span><span class="sxs-lookup"><span data-stu-id="3d418-118">The client receives an error message that states that the mail recipient is not found in the Active Directory directory service or Active Directory Domain Services (AD DS).</span></span> 
  
### <a name="getuseravailability-operation-soap-headers"></a><span data-ttu-id="3d418-119">GetUserAvailability 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="3d418-119">GetUserAvailability operation SOAP headers</span></span>

<span data-ttu-id="3d418-120">**GetUserAvailability**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="3d418-120">The **GetUserAvailability** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="3d418-121">**Header**</span><span class="sxs-lookup"><span data-stu-id="3d418-121">**Header**</span></span>|<span data-ttu-id="3d418-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="3d418-122">**Element**</span></span>|<span data-ttu-id="3d418-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="3d418-123">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3d418-124">**模拟**</span><span class="sxs-lookup"><span data-stu-id="3d418-124">**Impersonation**</span></span> <br/> |[<span data-ttu-id="3d418-125">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="3d418-125">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="3d418-126">标识客户端模拟的用户。</span><span class="sxs-lookup"><span data-stu-id="3d418-126">Identifies the user whom the client is impersonating.</span></span> <span data-ttu-id="3d418-127">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="3d418-127">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="3d418-128">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="3d418-128">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="3d418-129">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="3d418-129">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="3d418-130">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="3d418-130">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="3d418-131">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="3d418-131">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="3d418-132">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="3d418-132">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="3d418-133">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="3d418-133">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="3d418-134">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="3d418-134">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="3d418-135">此标头适用于响应。</span><span class="sxs-lookup"><span data-stu-id="3d418-135">This header is applicable to a response.</span></span>  <br/> |
|<span data-ttu-id="3d418-136">**TimeZoneContext**</span><span class="sxs-lookup"><span data-stu-id="3d418-136">**TimeZoneContext**</span></span> <br/> |[<span data-ttu-id="3d418-137">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="3d418-137">TimeZoneContext</span></span>](timezonecontext.md) <br/> |<span data-ttu-id="3d418-138">指定用于标识要用于来自服务器的所有响应的时区的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="3d418-138">Specifies a SOAP header that identifies the time zone to be used for all responses from the server.</span></span> <span data-ttu-id="3d418-139">从服务器返回的所有时间都将转换为指定的时区。</span><span class="sxs-lookup"><span data-stu-id="3d418-139">All times that are returned from the server will be converted to the specified time zone.</span></span> <span data-ttu-id="3d418-140">此标头适用于响应。</span><span class="sxs-lookup"><span data-stu-id="3d418-140">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getuseravailability-request-example-get-availability-information"></a><span data-ttu-id="3d418-141">GetUserAvailability 请求示例：获取可用性信息</span><span class="sxs-lookup"><span data-stu-id="3d418-141">GetUserAvailability request example: Get availability information</span></span>

<span data-ttu-id="3d418-142">下面的**GetUserAvailability**操作请求示例演示如何在太平洋时间时区中获取两个用户的详细可用性信息。</span><span class="sxs-lookup"><span data-stu-id="3d418-142">The following example of a **GetUserAvailability** operation request shows how to get detailed availability information for two users in the Pacific Time time zone.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetUserAvailabilityRequest xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <t:TimeZone xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
        <Bias>480</Bias>
        <StandardTime>
          <Bias>0</Bias>
          <Time>02:00:00</Time>
          <DayOrder>5</DayOrder>
          <Month>10</Month>
          <DayOfWeek>Sunday</DayOfWeek>
        </StandardTime>
        <DaylightTime>
          <Bias>-60</Bias>
          <Time>02:00:00</Time>
          <DayOrder>1</DayOrder>
          <Month>4</Month>
          <DayOfWeek>Sunday</DayOfWeek>
        </DaylightTime>
      </t:TimeZone>
      <MailboxDataArray>
        <t:MailboxData>
          <t:Email>
            <t:Address>user1@example.com</t:Address>
          </t:Email>
          <t:AttendeeType>Required</t:AttendeeType>
          <t:ExcludeConflicts>false</t:ExcludeConflicts>
        </t:MailboxData>
        <t:MailboxData>
          <t:Email>
            <t:Address>user2@example.com</t:Address>
          </t:Email>
          <t:AttendeeType>Required</t:AttendeeType>
          <t:ExcludeConflicts>false</t:ExcludeConflicts>
        </t:MailboxData>
      </MailboxDataArray>
      <t:FreeBusyViewOptions>
        <t:TimeWindow>
          <t:StartTime>2006-10-16T00:00:00</t:StartTime>
          <t:EndTime>2006-10-16T23:59:59</t:EndTime>
        </t:TimeWindow>
        <t:MergedFreeBusyIntervalInMinutes>60</t:MergedFreeBusyIntervalInMinutes>
        <t:RequestedView>DetailedMerged</t:RequestedView>
      </t:FreeBusyViewOptions>
    </GetUserAvailabilityRequest>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="3d418-143">有关使用[SuggestionsViewOptions](suggestionsviewoptions.md)元素检索建议的会议的详细信息，请参阅 EWS 虚拟目录中的架构。</span><span class="sxs-lookup"><span data-stu-id="3d418-143">For more information about retrieving suggested meetings by using the [SuggestionsViewOptions](suggestionsviewoptions.md) element, see the schema in the EWS virtual directory.</span></span> 
  
<span data-ttu-id="3d418-144">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="3d418-144">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="3d418-145">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="3d418-145">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
    
- [<span data-ttu-id="3d418-146">时区（可用性）</span><span class="sxs-lookup"><span data-stu-id="3d418-146">TimeZone (Availability)</span></span>](timezone-availability.md)
    
- [<span data-ttu-id="3d418-147">偏差（UTC）</span><span class="sxs-lookup"><span data-stu-id="3d418-147">Bias (UTC)</span></span>](bias-utc.md)
    
- [<span data-ttu-id="3d418-148">StandardTime</span><span class="sxs-lookup"><span data-stu-id="3d418-148">StandardTime</span></span>](standardtime.md)
    
- [<span data-ttu-id="3d418-149">偏置</span><span class="sxs-lookup"><span data-stu-id="3d418-149">Bias</span></span>](bias.md)
    
- [<span data-ttu-id="3d418-150">Time</span><span class="sxs-lookup"><span data-stu-id="3d418-150">Time</span></span>](time.md)
    
- [<span data-ttu-id="3d418-151">DayOrder</span><span class="sxs-lookup"><span data-stu-id="3d418-151">DayOrder</span></span>](dayorder.md)
    
- [<span data-ttu-id="3d418-152">Month</span><span class="sxs-lookup"><span data-stu-id="3d418-152">Month</span></span>](month.md)
    
- [<span data-ttu-id="3d418-153">DayOfWeek （时区）</span><span class="sxs-lookup"><span data-stu-id="3d418-153">DayOfWeek (TimeZone)</span></span>](dayofweek-timezone.md)
    
- [<span data-ttu-id="3d418-154">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="3d418-154">DaylightTime</span></span>](daylighttime.md)
    
- [<span data-ttu-id="3d418-155">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="3d418-155">MailboxDataArray</span></span>](mailboxdataarray.md)
    
- [<span data-ttu-id="3d418-156">MailboxData</span><span class="sxs-lookup"><span data-stu-id="3d418-156">MailboxData</span></span>](mailboxdata.md)
    
- [<span data-ttu-id="3d418-157">电子邮件（EmailAddressType）</span><span class="sxs-lookup"><span data-stu-id="3d418-157">Email (EmailAddressType)</span></span>](email-emailaddresstype.md)
    
- [<span data-ttu-id="3d418-158">Address （string）</span><span class="sxs-lookup"><span data-stu-id="3d418-158">Address (string)</span></span>](address-string.md)
    
- [<span data-ttu-id="3d418-159">AttendeeType</span><span class="sxs-lookup"><span data-stu-id="3d418-159">AttendeeType</span></span>](attendeetype.md)
    
- [<span data-ttu-id="3d418-160">ExcludeConflicts</span><span class="sxs-lookup"><span data-stu-id="3d418-160">ExcludeConflicts</span></span>](excludeconflicts.md)
    
- [<span data-ttu-id="3d418-161">FreeBusyViewOptions</span><span class="sxs-lookup"><span data-stu-id="3d418-161">FreeBusyViewOptions</span></span>](freebusyviewoptions.md)
    
- [<span data-ttu-id="3d418-162">TimeWindow</span><span class="sxs-lookup"><span data-stu-id="3d418-162">TimeWindow</span></span>](timewindow.md)
    
- [<span data-ttu-id="3d418-163">StartTime</span><span class="sxs-lookup"><span data-stu-id="3d418-163">StartTime</span></span>](starttime.md)
    
- [<span data-ttu-id="3d418-164">EndTime</span><span class="sxs-lookup"><span data-stu-id="3d418-164">EndTime</span></span>](endtime.md)
    
## <a name="successful-getuseravailability-operation-response"></a><span data-ttu-id="3d418-165">成功的 GetUserAvailability 操作响应</span><span class="sxs-lookup"><span data-stu-id="3d418-165">Successful GetUserAvailability operation response</span></span>

<span data-ttu-id="3d418-166">下面的示例演示对**GetUserAvailability**操作请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="3d418-166">The following example shows a successful response to the **GetUserAvailability** operation request.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3d418-167">日历事件标识符已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="3d418-167">The calendar event identifiers have been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="665" MinorBuildNumber="7" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetUserAvailabilityResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <FreeBusyResponseArray>
        <FreeBusyResponse>
          <ResponseMessage ResponseClass="Success">
            <ResponseCode>NoError</ResponseCode>
          </ResponseMessage>
          <FreeBusyView>
            <FreeBusyViewType xmlns="https://schemas.microsoft.com/exchange/services/2006/types">DetailedMerged</FreeBusyViewType>
            <MergedFreeBusy xmlns="https://schemas.microsoft.com/exchange/services/2006/types">000002220220000000000000</MergedFreeBusy>
            <CalendarEventArray xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
              <CalendarEvent>
                <StartTime>2006-10-16T06:00:00-07:00</StartTime>
                <EndTime>2006-10-16T06:30:00-07:00</EndTime>
                <BusyType>Busy</BusyType>
                <CalendarEventDetails>
                  <ID>14B6414B0</ID>
                  <Subject>Meet with Contoso Account Executives</Subject>
                  <Location />
                  <IsMeeting>false</IsMeeting>
                  <IsRecurring>false</IsRecurring>
                  <IsException>false</IsException>
                  <IsReminderSet>false</IsReminderSet>
                  <IsPrivate>false</IsPrivate>
                </CalendarEventDetails>
              </CalendarEvent>
              <CalendarEvent>
                <StartTime>2006-10-16T07:00:00-07:00</StartTime>
                <EndTime>2006-10-16T08:00:00-07:00</EndTime>
                <BusyType>Busy</BusyType>
                <CalendarEventDetails>
                  <ID>E14B6414B0B</ID>
                  <Subject>Pick up my groceries</Subject>
                  <Location />
                  <IsMeeting>false</IsMeeting>
                  <IsRecurring>false</IsRecurring>
                  <IsException>false</IsException>
                  <IsReminderSet>false</IsReminderSet>
                  <IsPrivate>false</IsPrivate>
                </CalendarEventDetails>
              </CalendarEvent>
              <CalendarEvent>
                <StartTime>2006-10-16T09:40:00-07:00</StartTime>
                <EndTime>2006-10-16T10:10:00-07:00</EndTime>
                <BusyType>Busy</BusyType>
                <CalendarEventDetails>
                  <ID>14B6414B0B1</ID>
                  <Subject>Meet with doctor</Subject>
                  <Location>Kirkland</Location>
                  <IsMeeting>false</IsMeeting>
                  <IsRecurring>false</IsRecurring>
                  <IsException>false</IsException>
                  <IsReminderSet>false</IsReminderSet>
                  <IsPrivate>false</IsPrivate>
                </CalendarEventDetails>
              </CalendarEvent>
            </CalendarEventArray>
            <WorkingHours xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
              <TimeZone>
                <Bias>480</Bias>
                <StandardTime>
                  <Bias>0</Bias>
                  <Time>02:00:00</Time>
                  <DayOrder>5</DayOrder>
                  <Month>10</Month>
                  <DayOfWeek>Sunday</DayOfWeek>
                </StandardTime>
                <DaylightTime>
                  <Bias>-60</Bias>
                  <Time>02:00:00</Time>
                  <DayOrder>1</DayOrder>
                  <Month>4</Month>
                  <DayOfWeek>Sunday</DayOfWeek>
                </DaylightTime>
              </TimeZone>
              <WorkingPeriodArray>
                <WorkingPeriod>
                  <DayOfWeek>Monday Tuesday Wednesday Thursday Friday</DayOfWeek>
                  <StartTimeInMinutes>480</StartTimeInMinutes>
                  <EndTimeInMinutes>1020</EndTimeInMinutes>
                </WorkingPeriod>
              </WorkingPeriodArray>
            </WorkingHours>
          </FreeBusyView>
        </FreeBusyResponse>
        <FreeBusyResponse>
          <ResponseMessage ResponseClass="Success">
            <ResponseCode>NoError</ResponseCode>
          </ResponseMessage>
          <FreeBusyView>
            <FreeBusyViewType xmlns="https://schemas.microsoft.com/exchange/services/2006/types">FreeBusyMerged</FreeBusyViewType>
            <MergedFreeBusy xmlns="https://schemas.microsoft.com/exchange/services/2006/types">000000001100000000000000</MergedFreeBusy>
            <CalendarEventArray xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
              <CalendarEvent>
                <StartTime>2006-10-16T09:00:00-07:00</StartTime>
                <EndTime>2006-10-16T10:00:00-07:00</EndTime>
                <BusyType>Tentative</BusyType>
              </CalendarEvent>
            </CalendarEventArray>
            <WorkingHours xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
              <TimeZone>
                <Bias>480</Bias>
                <StandardTime>
                  <Bias>0</Bias>
                  <Time>02:00:00</Time>
                  <DayOrder>5</DayOrder>
                  <Month>10</Month>
                  <DayOfWeek>Sunday</DayOfWeek>
                </StandardTime>
                <DaylightTime>
                  <Bias>-60</Bias>
                  <Time>02:00:00</Time>
                  <DayOrder>1</DayOrder>
                  <Month>4</Month>
                  <DayOfWeek>Sunday</DayOfWeek>
                </DaylightTime>
              </TimeZone>
              <WorkingPeriodArray>
                <WorkingPeriod>
                  <DayOfWeek>Monday Tuesday Wednesday Thursday Friday</DayOfWeek>
                  <StartTimeInMinutes>480</StartTimeInMinutes>
                  <EndTimeInMinutes>1020</EndTimeInMinutes>
                </WorkingPeriod>
              </WorkingPeriodArray>
            </WorkingHours>
          </FreeBusyView>
        </FreeBusyResponse>
      </FreeBusyResponseArray>
    </GetUserAvailabilityResponse>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="3d418-168">每个用户的可用性信息显示在一个唯一的[FreeBusyResponse](freebusyresponse.md)元素中。</span><span class="sxs-lookup"><span data-stu-id="3d418-168">The availability information for each user appears in a unique [FreeBusyResponse](freebusyresponse.md) element.</span></span> <span data-ttu-id="3d418-169">**GetUserAvailability**操作请求中的用户顺序决定了响应中每个用户的可用性数据的顺序。</span><span class="sxs-lookup"><span data-stu-id="3d418-169">The order of users in the **GetUserAvailability** operation request determines the order of availability data for each user in the response.</span></span> 
  
<span data-ttu-id="3d418-170">如果在查询中定义的时间段内的约会数大于管理员指定的最大数目，则会向客户端返回一个错误。</span><span class="sxs-lookup"><span data-stu-id="3d418-170">An error will be returned to the client if the number of appointments in the time period that is defined in the query is greater than the administrator-specified maximum number.</span></span> <span data-ttu-id="3d418-171">默认最大约会数为10000单个实例和展开的定期项目。</span><span class="sxs-lookup"><span data-stu-id="3d418-171">The default maximum number of appointments is 10,000 single instances and expanded recurrence items.</span></span> <span data-ttu-id="3d418-172">此属性只能由管理员配置。</span><span class="sxs-lookup"><span data-stu-id="3d418-172">This property can be configured only by an administrator.</span></span>
  
<span data-ttu-id="3d418-173">响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="3d418-173">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="3d418-174">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="3d418-174">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="3d418-175">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="3d418-175">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
    
- [<span data-ttu-id="3d418-176">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="3d418-176">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
    
- [<span data-ttu-id="3d418-177">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="3d418-177">FreeBusyResponse</span></span>](freebusyresponse.md)
    
- [<span data-ttu-id="3d418-178">ResponseMessage</span><span class="sxs-lookup"><span data-stu-id="3d418-178">ResponseMessage</span></span>](responsemessage.md)
    
- [<span data-ttu-id="3d418-179">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="3d418-179">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="3d418-180">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="3d418-180">FreeBusyView</span></span>](freebusyview.md)
    
- [<span data-ttu-id="3d418-181">FreeBusyViewType</span><span class="sxs-lookup"><span data-stu-id="3d418-181">FreeBusyViewType</span></span>](freebusyviewtype.md)
    
- [<span data-ttu-id="3d418-182">MergedFreeBusy</span><span class="sxs-lookup"><span data-stu-id="3d418-182">MergedFreeBusy</span></span>](mergedfreebusy.md)
    
- [<span data-ttu-id="3d418-183">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="3d418-183">CalendarEventArray</span></span>](calendareventarray.md)
    
- [<span data-ttu-id="3d418-184">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="3d418-184">CalendarEvent</span></span>](calendarevent.md)
    
- [<span data-ttu-id="3d418-185">StartTime</span><span class="sxs-lookup"><span data-stu-id="3d418-185">StartTime</span></span>](starttime.md)
    
- [<span data-ttu-id="3d418-186">EndTime</span><span class="sxs-lookup"><span data-stu-id="3d418-186">EndTime</span></span>](endtime.md)
    
- [<span data-ttu-id="3d418-187">BusyType</span><span class="sxs-lookup"><span data-stu-id="3d418-187">BusyType</span></span>](busytype.md)
    
- [<span data-ttu-id="3d418-188">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="3d418-188">CalendarEventDetails</span></span>](calendareventdetails.md)
    
- [<span data-ttu-id="3d418-189">ID</span><span class="sxs-lookup"><span data-stu-id="3d418-189">ID</span></span>](id.md)
    
- [<span data-ttu-id="3d418-190">Subject （CalendarEventDetails）</span><span class="sxs-lookup"><span data-stu-id="3d418-190">Subject (CalendarEventDetails)</span></span>](subject-calendareventdetails.md)
    
- [<span data-ttu-id="3d418-191">Location （CalendarEventDetails）</span><span class="sxs-lookup"><span data-stu-id="3d418-191">Location (CalendarEventDetails)</span></span>](location-calendareventdetails.md)
    
- [<span data-ttu-id="3d418-192">IsMeeting (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="3d418-192">IsMeeting (CalendarEventDetails)</span></span>](ismeeting-calendareventdetails.md)
    
- [<span data-ttu-id="3d418-193">IsRecurring （CalendarEventDetails）</span><span class="sxs-lookup"><span data-stu-id="3d418-193">IsRecurring (CalendarEventDetails)</span></span>](isrecurring-calendareventdetails.md)
    
- [<span data-ttu-id="3d418-194">IsException</span><span class="sxs-lookup"><span data-stu-id="3d418-194">IsException</span></span>](isexception.md)
    
- [<span data-ttu-id="3d418-195">IsReminderSet</span><span class="sxs-lookup"><span data-stu-id="3d418-195">IsReminderSet</span></span>](isreminderset.md)
    
- [<span data-ttu-id="3d418-196">IsPrivate</span><span class="sxs-lookup"><span data-stu-id="3d418-196">IsPrivate</span></span>](isprivate.md)
    
- [<span data-ttu-id="3d418-197">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="3d418-197">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md)
    
- [<span data-ttu-id="3d418-198">时区（可用性）</span><span class="sxs-lookup"><span data-stu-id="3d418-198">TimeZone (Availability)</span></span>](timezone-availability.md)
    
- [<span data-ttu-id="3d418-199">偏差（UTC）</span><span class="sxs-lookup"><span data-stu-id="3d418-199">Bias (UTC)</span></span>](bias-utc.md)
    
- [<span data-ttu-id="3d418-200">StandardTime</span><span class="sxs-lookup"><span data-stu-id="3d418-200">StandardTime</span></span>](standardtime.md)
    
- [<span data-ttu-id="3d418-201">偏置</span><span class="sxs-lookup"><span data-stu-id="3d418-201">Bias</span></span>](bias.md)
    
- [<span data-ttu-id="3d418-202">Time</span><span class="sxs-lookup"><span data-stu-id="3d418-202">Time</span></span>](time.md)
    
- [<span data-ttu-id="3d418-203">DayOrder</span><span class="sxs-lookup"><span data-stu-id="3d418-203">DayOrder</span></span>](dayorder.md)
    
- [<span data-ttu-id="3d418-204">Month</span><span class="sxs-lookup"><span data-stu-id="3d418-204">Month</span></span>](month.md)
    
- [<span data-ttu-id="3d418-205">DayOfWeek （时区）</span><span class="sxs-lookup"><span data-stu-id="3d418-205">DayOfWeek (TimeZone)</span></span>](dayofweek-timezone.md)
    
- [<span data-ttu-id="3d418-206">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="3d418-206">DaylightTime</span></span>](daylighttime.md)
    
- [<span data-ttu-id="3d418-207">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="3d418-207">WorkingPeriodArray</span></span>](workingperiodarray.md)
    
- [<span data-ttu-id="3d418-208">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="3d418-208">WorkingPeriod</span></span>](workingperiod.md)
    
- [<span data-ttu-id="3d418-209">DayOfWeek （WorkingPeriod）</span><span class="sxs-lookup"><span data-stu-id="3d418-209">DayOfWeek (WorkingPeriod)</span></span>](dayofweek-workingperiod.md)
    
- [<span data-ttu-id="3d418-210">StartTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="3d418-210">StartTimeInMinutes</span></span>](starttimeinminutes.md)
    
- [<span data-ttu-id="3d418-211">EndTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="3d418-211">EndTimeInMinutes</span></span>](endtimeinminutes.md)
    
## <a name="see-also"></a><span data-ttu-id="3d418-212">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3d418-212">See also</span></span>

- [<span data-ttu-id="3d418-213">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="3d418-213">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="3d418-214">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="3d418-214">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)
    

