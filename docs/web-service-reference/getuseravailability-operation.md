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
description: 查找信息 GetUserAvailability EWS 操作。
ms.openlocfilehash: 41246fe22bfb7444cd4aa7b1d4651d475dd9231c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825686"
---
# <a name="getuseravailability-operation"></a><span data-ttu-id="796e3-103">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="796e3-103">GetUserAvailability operation</span></span>

<span data-ttu-id="796e3-104">查找有关**GetUserAvailability** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="796e3-104">Find information about the **GetUserAvailability** EWS operation.</span></span> 
  
<span data-ttu-id="796e3-105">**GetUserAvailability**操作提供有关详细的信息的可用性的一组用户、 聊天室和资源中指定的时间段。</span><span class="sxs-lookup"><span data-stu-id="796e3-105">The **GetUserAvailability** operation provides detailed information about the availability of a set of users, rooms, and resources within a specified time period.</span></span> 
  
## <a name="using-the-getuseravailability-operation"></a><span data-ttu-id="796e3-106">使用 GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="796e3-106">Using the GetUserAvailability operation</span></span>

<span data-ttu-id="796e3-107">**GetUserAvailability**操作提供在指定级别的详细信息的当前用户的可用性信息。</span><span class="sxs-lookup"><span data-stu-id="796e3-107">The **GetUserAvailability** operation provides current user availability information at a specified level of detail.</span></span> <span data-ttu-id="796e3-108">客户端应用程序，如 Outlook、 Outlook Web Access、 Outlook Mobile Access 和其他人使用的 SMTP 地址来标识的请求的用户信息。</span><span class="sxs-lookup"><span data-stu-id="796e3-108">Client applications such as Outlook, Outlook Web Access, Outlook Mobile Access, and others use SMTP addresses to identify the requested user information.</span></span> 
  
<span data-ttu-id="796e3-109">可用性服务展开通讯组列表的列表中，每个成员检索忙/闲状态，只要通讯组列表中的邮箱数为少于 100，即标识的最大数量的**GetUserAvailability**操作可以请求。</span><span class="sxs-lookup"><span data-stu-id="796e3-109">The Availability service expands distribution lists to retrieve the free/busy status for each member of the list, as long as the number of mailboxes in the distribution list is less than 100, which is the maximum number of identities that the **GetUserAvailability** operation can request.</span></span> <span data-ttu-id="796e3-110">通讯组列表的成员的忙/闲状态已合并到单个的忙/闲状态的整个通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="796e3-110">The free/busy statuses of the members of the distribution list are merged into a single free/busy status for the whole distribution list.</span></span> 
  
<span data-ttu-id="796e3-111">客户端应用程序请求指定可用性查询的时间的段。</span><span class="sxs-lookup"><span data-stu-id="796e3-111">Client application requests specify the time period of the availability query.</span></span> <span data-ttu-id="796e3-112">默认的请求信息的时间段为 42 天。</span><span class="sxs-lookup"><span data-stu-id="796e3-112">The default time period for the requested information is 42 days.</span></span> <span data-ttu-id="796e3-113">如果用户的日历包含约会或会议的内部和外部查询的定义的时间段，则返回约会。</span><span class="sxs-lookup"><span data-stu-id="796e3-113">If the user's calendar contains appointments or meetings that are both within and outside the defined time period for the query, the appointment is returned.</span></span> 
  
<span data-ttu-id="796e3-114">返回约会和会议时间是在会议请求的客户端应用程序相同的时区。</span><span class="sxs-lookup"><span data-stu-id="796e3-114">The appointment and meeting times that are returned are in the same time zone as the client application that is requesting the meeting.</span></span>
  
<span data-ttu-id="796e3-115">可用性服务处理的每个客户端的请求。</span><span class="sxs-lookup"><span data-stu-id="796e3-115">The Availability service processes the request for each client.</span></span> <span data-ttu-id="796e3-116">服务展开所有的定期约会，并返回请求的客户端有权接收的日历详细信息的最大数量。</span><span class="sxs-lookup"><span data-stu-id="796e3-116">The service expands all the recurring appointments and returns the maximum number of calendar details that the requesting client has permission to receive.</span></span>
  
> [!NOTE]
> <span data-ttu-id="796e3-117">如果目标邮箱不可用或找不到，则会**MailRecipientNotFoundException**异常。</span><span class="sxs-lookup"><span data-stu-id="796e3-117">If the target mailbox is unavailable or cannot be found, a **MailRecipientNotFoundException** exception is thrown.</span></span> <span data-ttu-id="796e3-118">客户端收到错误消息，指出的 Active Directory 目录服务或 Active Directory 域服务 (AD DS) 中未找到邮件收件人。</span><span class="sxs-lookup"><span data-stu-id="796e3-118">The client receives an error message that states that the mail recipient is not found in the Active Directory directory service or Active Directory Domain Services (AD DS).</span></span> 
  
### <a name="getuseravailability-operation-soap-headers"></a><span data-ttu-id="796e3-119">GetUserAvailability 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="796e3-119">GetUserAvailability operation SOAP headers</span></span>

<span data-ttu-id="796e3-120">**GetUserAvailability**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="796e3-120">The **GetUserAvailability** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="796e3-121">**Header**</span><span class="sxs-lookup"><span data-stu-id="796e3-121">**Header**</span></span>|<span data-ttu-id="796e3-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="796e3-122">**Element**</span></span>|<span data-ttu-id="796e3-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="796e3-123">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="796e3-124">**模拟**</span><span class="sxs-lookup"><span data-stu-id="796e3-124">**Impersonation**</span></span> <br/> |[<span data-ttu-id="796e3-125">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="796e3-125">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="796e3-126">标识模拟客户端的用户。</span><span class="sxs-lookup"><span data-stu-id="796e3-126">Identifies the user whom the client is impersonating.</span></span> <span data-ttu-id="796e3-127">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="796e3-127">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="796e3-128">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="796e3-128">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="796e3-129">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="796e3-129">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="796e3-130">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="796e3-130">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="796e3-131">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="796e3-131">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="796e3-132">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="796e3-132">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="796e3-133">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="796e3-133">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="796e3-134">标识响应该请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="796e3-134">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="796e3-135">适用于响应此标头。</span><span class="sxs-lookup"><span data-stu-id="796e3-135">This header is applicable to a response.</span></span>  <br/> |
|<span data-ttu-id="796e3-136">**TimeZoneContext**</span><span class="sxs-lookup"><span data-stu-id="796e3-136">**TimeZoneContext**</span></span> <br/> |[<span data-ttu-id="796e3-137">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="796e3-137">TimeZoneContext</span></span>](timezonecontext.md) <br/> |<span data-ttu-id="796e3-138">指定确定要用于来自服务器的所有响应的时区的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="796e3-138">Specifies a SOAP header that identifies the time zone to be used for all responses from the server.</span></span> <span data-ttu-id="796e3-139">从服务器返回的所有时间将都转换为指定的时区。</span><span class="sxs-lookup"><span data-stu-id="796e3-139">All times that are returned from the server will be converted to the specified time zone.</span></span> <span data-ttu-id="796e3-140">适用于响应此标头。</span><span class="sxs-lookup"><span data-stu-id="796e3-140">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getuseravailability-request-example-get-availability-information"></a><span data-ttu-id="796e3-141">GetUserAvailability 请求示例： 获取可用性信息</span><span class="sxs-lookup"><span data-stu-id="796e3-141">GetUserAvailability request example: Get availability information</span></span>

<span data-ttu-id="796e3-142">**GetUserAvailability**操作请求的下面的示例演示如何获取太平洋时区时间中的两个用户的详细的可用性信息。</span><span class="sxs-lookup"><span data-stu-id="796e3-142">The following example of a **GetUserAvailability** operation request shows how to get detailed availability information for two users in the Pacific Time time zone.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetUserAvailabilityRequest xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <t:TimeZone xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="796e3-143">有关使用[SuggestionsViewOptions](suggestionsviewoptions.md)元素检索建议的会议的详细信息，请参阅 EWS 虚拟目录中的架构。</span><span class="sxs-lookup"><span data-stu-id="796e3-143">For more information about retrieving suggested meetings by using the [SuggestionsViewOptions](suggestionsviewoptions.md) element, see the schema in the EWS virtual directory.</span></span> 
  
<span data-ttu-id="796e3-144">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="796e3-144">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="796e3-145">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="796e3-145">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
    
- [<span data-ttu-id="796e3-146">TimeZone （可用性）</span><span class="sxs-lookup"><span data-stu-id="796e3-146">TimeZone (Availability)</span></span>](timezone-availability.md)
    
- [<span data-ttu-id="796e3-147">斜线 (UTC)</span><span class="sxs-lookup"><span data-stu-id="796e3-147">Bias (UTC)</span></span>](bias-utc.md)
    
- [<span data-ttu-id="796e3-148">StandardTime</span><span class="sxs-lookup"><span data-stu-id="796e3-148">StandardTime</span></span>](standardtime.md)
    
- [<span data-ttu-id="796e3-149">Bias</span><span class="sxs-lookup"><span data-stu-id="796e3-149">Bias</span></span>](bias.md)
    
- [<span data-ttu-id="796e3-150">Time</span><span class="sxs-lookup"><span data-stu-id="796e3-150">Time</span></span>](time.md)
    
- [<span data-ttu-id="796e3-151">DayOrder</span><span class="sxs-lookup"><span data-stu-id="796e3-151">DayOrder</span></span>](dayorder.md)
    
- [<span data-ttu-id="796e3-152">month</span><span class="sxs-lookup"><span data-stu-id="796e3-152">Month</span></span>](month.md)
    
- [<span data-ttu-id="796e3-153">DayOfWeek (TimeZone)</span><span class="sxs-lookup"><span data-stu-id="796e3-153">DayOfWeek (TimeZone)</span></span>](dayofweek-timezone.md)
    
- [<span data-ttu-id="796e3-154">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="796e3-154">DaylightTime</span></span>](daylighttime.md)
    
- [<span data-ttu-id="796e3-155">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="796e3-155">MailboxDataArray</span></span>](mailboxdataarray.md)
    
- [<span data-ttu-id="796e3-156">MailboxData</span><span class="sxs-lookup"><span data-stu-id="796e3-156">MailboxData</span></span>](mailboxdata.md)
    
- [<span data-ttu-id="796e3-157">电子邮件 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="796e3-157">Email (EmailAddressType)</span></span>](email-emailaddresstype.md)
    
- [<span data-ttu-id="796e3-158">地址 （字符串）</span><span class="sxs-lookup"><span data-stu-id="796e3-158">Address (string)</span></span>](address-string.md)
    
- [<span data-ttu-id="796e3-159">AttendeeType</span><span class="sxs-lookup"><span data-stu-id="796e3-159">AttendeeType</span></span>](attendeetype.md)
    
- [<span data-ttu-id="796e3-160">ExcludeConflicts</span><span class="sxs-lookup"><span data-stu-id="796e3-160">ExcludeConflicts</span></span>](excludeconflicts.md)
    
- [<span data-ttu-id="796e3-161">FreeBusyViewOptions</span><span class="sxs-lookup"><span data-stu-id="796e3-161">FreeBusyViewOptions</span></span>](freebusyviewoptions.md)
    
- [<span data-ttu-id="796e3-162">TimeWindow</span><span class="sxs-lookup"><span data-stu-id="796e3-162">TimeWindow</span></span>](timewindow.md)
    
- [<span data-ttu-id="796e3-163">StartTime</span><span class="sxs-lookup"><span data-stu-id="796e3-163">StartTime</span></span>](starttime.md)
    
- [<span data-ttu-id="796e3-164">结束时间</span><span class="sxs-lookup"><span data-stu-id="796e3-164">EndTime</span></span>](endtime.md)
    
## <a name="successful-getuseravailability-operation-response"></a><span data-ttu-id="796e3-165">成功 GetUserAvailability 操作响应</span><span class="sxs-lookup"><span data-stu-id="796e3-165">Successful GetUserAvailability operation response</span></span>

<span data-ttu-id="796e3-166">下面的示例显示**GetUserAvailability**操作请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="796e3-166">The following example shows a successful response to the **GetUserAvailability** operation request.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="796e3-167">日历事件标识符具有已缩短要保留可读性。</span><span class="sxs-lookup"><span data-stu-id="796e3-167">The calendar event identifiers have been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="665" MinorBuildNumber="7" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetUserAvailabilityResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <FreeBusyResponseArray>
        <FreeBusyResponse>
          <ResponseMessage ResponseClass="Success">
            <ResponseCode>NoError</ResponseCode>
          </ResponseMessage>
          <FreeBusyView>
            <FreeBusyViewType xmlns="http://schemas.microsoft.com/exchange/services/2006/types">DetailedMerged</FreeBusyViewType>
            <MergedFreeBusy xmlns="http://schemas.microsoft.com/exchange/services/2006/types">000002220220000000000000</MergedFreeBusy>
            <CalendarEventArray xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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
            <WorkingHours xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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
            <FreeBusyViewType xmlns="http://schemas.microsoft.com/exchange/services/2006/types">FreeBusyMerged</FreeBusyViewType>
            <MergedFreeBusy xmlns="http://schemas.microsoft.com/exchange/services/2006/types">000000001100000000000000</MergedFreeBusy>
            <CalendarEventArray xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
              <CalendarEvent>
                <StartTime>2006-10-16T09:00:00-07:00</StartTime>
                <EndTime>2006-10-16T10:00:00-07:00</EndTime>
                <BusyType>Tentative</BusyType>
              </CalendarEvent>
            </CalendarEventArray>
            <WorkingHours xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="796e3-168">唯一[FreeBusyResponse](freebusyresponse.md)元素中将显示每个用户的可用性信息。</span><span class="sxs-lookup"><span data-stu-id="796e3-168">The availability information for each user appears in a unique [FreeBusyResponse](freebusyresponse.md) element.</span></span> <span data-ttu-id="796e3-169">**GetUserAvailability**操作请求中的用户的顺序确定在响应中的每个用户的可用性数据的顺序。</span><span class="sxs-lookup"><span data-stu-id="796e3-169">The order of users in the **GetUserAvailability** operation request determines the order of availability data for each user in the response.</span></span> 
  
<span data-ttu-id="796e3-170">如果在查询中定义的时间段中的约会数大于管理员指定的最大数目，将向客户端返回错误。</span><span class="sxs-lookup"><span data-stu-id="796e3-170">An error will be returned to the client if the number of appointments in the time period that is defined in the query is greater than the administrator-specified maximum number.</span></span> <span data-ttu-id="796e3-171">默认最大数目约会是 10,000 的单个实例，扩展重复项。</span><span class="sxs-lookup"><span data-stu-id="796e3-171">The default maximum number of appointments is 10,000 single instances and expanded recurrence items.</span></span> <span data-ttu-id="796e3-172">仅由管理员可以配置此属性。</span><span class="sxs-lookup"><span data-stu-id="796e3-172">This property can be configured only by an administrator.</span></span>
  
<span data-ttu-id="796e3-173">在响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="796e3-173">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="796e3-174">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="796e3-174">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="796e3-175">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="796e3-175">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
    
- [<span data-ttu-id="796e3-176">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="796e3-176">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
    
- [<span data-ttu-id="796e3-177">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="796e3-177">FreeBusyResponse</span></span>](freebusyresponse.md)
    
- [<span data-ttu-id="796e3-178">ResponseMessage</span><span class="sxs-lookup"><span data-stu-id="796e3-178">ResponseMessage</span></span>](responsemessage.md)
    
- [<span data-ttu-id="796e3-179">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="796e3-179">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="796e3-180">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="796e3-180">FreeBusyView</span></span>](freebusyview.md)
    
- [<span data-ttu-id="796e3-181">FreeBusyViewType</span><span class="sxs-lookup"><span data-stu-id="796e3-181">FreeBusyViewType</span></span>](freebusyviewtype.md)
    
- [<span data-ttu-id="796e3-182">MergedFreeBusy</span><span class="sxs-lookup"><span data-stu-id="796e3-182">MergedFreeBusy</span></span>](mergedfreebusy.md)
    
- [<span data-ttu-id="796e3-183">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="796e3-183">CalendarEventArray</span></span>](calendareventarray.md)
    
- [<span data-ttu-id="796e3-184">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="796e3-184">CalendarEvent</span></span>](calendarevent.md)
    
- [<span data-ttu-id="796e3-185">StartTime</span><span class="sxs-lookup"><span data-stu-id="796e3-185">StartTime</span></span>](starttime.md)
    
- [<span data-ttu-id="796e3-186">结束时间</span><span class="sxs-lookup"><span data-stu-id="796e3-186">EndTime</span></span>](endtime.md)
    
- [<span data-ttu-id="796e3-187">BusyType</span><span class="sxs-lookup"><span data-stu-id="796e3-187">BusyType</span></span>](busytype.md)
    
- [<span data-ttu-id="796e3-188">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="796e3-188">CalendarEventDetails</span></span>](calendareventdetails.md)
    
- [<span data-ttu-id="796e3-189">标识</span><span class="sxs-lookup"><span data-stu-id="796e3-189">ID</span></span>](id.md)
    
- [<span data-ttu-id="796e3-190">主题 (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="796e3-190">Subject (CalendarEventDetails)</span></span>](subject-calendareventdetails.md)
    
- [<span data-ttu-id="796e3-191">位置 (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="796e3-191">Location (CalendarEventDetails)</span></span>](location-calendareventdetails.md)
    
- [<span data-ttu-id="796e3-192">IsMeeting (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="796e3-192">IsMeeting (CalendarEventDetails)</span></span>](ismeeting-calendareventdetails.md)
    
- [<span data-ttu-id="796e3-193">IsRecurring (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="796e3-193">IsRecurring (CalendarEventDetails)</span></span>](isrecurring-calendareventdetails.md)
    
- [<span data-ttu-id="796e3-194">IsException</span><span class="sxs-lookup"><span data-stu-id="796e3-194">IsException</span></span>](isexception.md)
    
- [<span data-ttu-id="796e3-195">IsReminderSet</span><span class="sxs-lookup"><span data-stu-id="796e3-195">IsReminderSet</span></span>](isreminderset.md)
    
- [<span data-ttu-id="796e3-196">IsPrivate</span><span class="sxs-lookup"><span data-stu-id="796e3-196">IsPrivate</span></span>](isprivate.md)
    
- [<span data-ttu-id="796e3-197">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="796e3-197">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md)
    
- [<span data-ttu-id="796e3-198">TimeZone （可用性）</span><span class="sxs-lookup"><span data-stu-id="796e3-198">TimeZone (Availability)</span></span>](timezone-availability.md)
    
- [<span data-ttu-id="796e3-199">斜线 (UTC)</span><span class="sxs-lookup"><span data-stu-id="796e3-199">Bias (UTC)</span></span>](bias-utc.md)
    
- [<span data-ttu-id="796e3-200">StandardTime</span><span class="sxs-lookup"><span data-stu-id="796e3-200">StandardTime</span></span>](standardtime.md)
    
- [<span data-ttu-id="796e3-201">Bias</span><span class="sxs-lookup"><span data-stu-id="796e3-201">Bias</span></span>](bias.md)
    
- [<span data-ttu-id="796e3-202">Time</span><span class="sxs-lookup"><span data-stu-id="796e3-202">Time</span></span>](time.md)
    
- [<span data-ttu-id="796e3-203">DayOrder</span><span class="sxs-lookup"><span data-stu-id="796e3-203">DayOrder</span></span>](dayorder.md)
    
- [<span data-ttu-id="796e3-204">month</span><span class="sxs-lookup"><span data-stu-id="796e3-204">Month</span></span>](month.md)
    
- [<span data-ttu-id="796e3-205">DayOfWeek (TimeZone)</span><span class="sxs-lookup"><span data-stu-id="796e3-205">DayOfWeek (TimeZone)</span></span>](dayofweek-timezone.md)
    
- [<span data-ttu-id="796e3-206">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="796e3-206">DaylightTime</span></span>](daylighttime.md)
    
- [<span data-ttu-id="796e3-207">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="796e3-207">WorkingPeriodArray</span></span>](workingperiodarray.md)
    
- [<span data-ttu-id="796e3-208">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="796e3-208">WorkingPeriod</span></span>](workingperiod.md)
    
- [<span data-ttu-id="796e3-209">DayOfWeek (WorkingPeriod)</span><span class="sxs-lookup"><span data-stu-id="796e3-209">DayOfWeek (WorkingPeriod)</span></span>](dayofweek-workingperiod.md)
    
- [<span data-ttu-id="796e3-210">StartTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="796e3-210">StartTimeInMinutes</span></span>](starttimeinminutes.md)
    
- [<span data-ttu-id="796e3-211">EndTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="796e3-211">EndTimeInMinutes</span></span>](endtimeinminutes.md)
    
## <a name="see-also"></a><span data-ttu-id="796e3-212">另请参阅</span><span class="sxs-lookup"><span data-stu-id="796e3-212">See also</span></span>

- [<span data-ttu-id="796e3-213">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="796e3-213">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="796e3-214">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="796e3-214">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)
    

