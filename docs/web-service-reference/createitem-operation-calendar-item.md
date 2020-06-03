---
title: CreateItem 操作（日历项目）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateItem
api_type:
- schema
ms.assetid: aa4a7c94-f668-4bd2-8079-c855f6ab17e1
description: CreateItem 操作在 Exchange 存储中创建日历项目。
ms.openlocfilehash: 535edf9fe567bc3063a5b853f01d604ea4c7eb95
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457499"
---
# <a name="createitem-operation-calendar-item"></a><span data-ttu-id="a4932-103">CreateItem 操作（日历项目）</span><span class="sxs-lookup"><span data-stu-id="a4932-103">CreateItem operation (calendar item)</span></span>

<span data-ttu-id="a4932-104">CreateItem 操作在 Exchange 存储中创建日历项目。</span><span class="sxs-lookup"><span data-stu-id="a4932-104">The CreateItem operation creates calendar items in the Exchange store.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a4932-105">备注</span><span class="sxs-lookup"><span data-stu-id="a4932-105">Remarks</span></span>

<span data-ttu-id="a4932-106">CreateItem 操作创建约会、会议和会议请求。</span><span class="sxs-lookup"><span data-stu-id="a4932-106">The CreateItem operation creates appointments, meetings, and meeting requests.</span></span> <span data-ttu-id="a4932-107">如果日历项目是在没有与会者的情况下创建的，则会将其视为约会。</span><span class="sxs-lookup"><span data-stu-id="a4932-107">If a calendar item is created without attendees, it is considered an appointment.</span></span> <span data-ttu-id="a4932-108">如果指定了与会者，则日历项目是会议。</span><span class="sxs-lookup"><span data-stu-id="a4932-108">If attendees are specified, the calendar item is a meeting.</span></span> <span data-ttu-id="a4932-109">使用 CreateItem 操作创建会议时，如果 SendMeetingInvitations 属性设置为发送会议请求，则会自动向已标识的与会者发送会议请求。</span><span class="sxs-lookup"><span data-stu-id="a4932-109">When a meeting is created by using the CreateItem operation, meeting requests are automatically sent to the identified attendees if the SendMeetingInvitations attribute is set to send the meeting requests.</span></span>
  
## <a name="createitem-calendar-item-request-example"></a><span data-ttu-id="a4932-110">CreateItem （日历项目）请求示例</span><span class="sxs-lookup"><span data-stu-id="a4932-110">CreateItem (Calendar Item) request example</span></span>

### <a name="description"></a><span data-ttu-id="a4932-111">Description</span><span class="sxs-lookup"><span data-stu-id="a4932-111">Description</span></span>

<span data-ttu-id="a4932-112">以下示例的 CreateItem 请求显示了如何使用两个必需的与会者创建会议。</span><span class="sxs-lookup"><span data-stu-id="a4932-112">The following example of a CreateItem request shows how to create a meeting with two required attendees.</span></span> <span data-ttu-id="a4932-113">此请求会将会议请求发送给两个与会者。</span><span class="sxs-lookup"><span data-stu-id="a4932-113">This request will send the meeting requests to the two attendees.</span></span>
  
### <a name="code"></a><span data-ttu-id="a4932-114">代码</span><span class="sxs-lookup"><span data-stu-id="a4932-114">Code</span></span>

```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                SendMeetingInvitations="SendToAllAndSaveCopy" >
      <SavedItemFolderId>
        <t:DistinguishedFolderId Id="calendar"/>
      </SavedItemFolderId>
      <Items>
        <t:CalendarItem xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <Subject>Planning Meeting</Subject>
          <Body BodyType="Text">Plan the agenda for next week's meeting.</Body>
          <ReminderIsSet>true</ReminderIsSet>
          <ReminderMinutesBeforeStart>60</ReminderMinutesBeforeStart>
          <Start>2006-11-02T14:00:00</Start>
          <End>2006-11-02T15:00:00</End>
          <IsAllDayEvent>false</IsAllDayEvent>
          <LegacyFreeBusyStatus>Busy</LegacyFreeBusyStatus>
          <Location>Conference Room 721</Location>
          <RequiredAttendees>
            <Attendee>
              <Mailbox>
                <EmailAddress>User1@example.com</EmailAddress>
              </Mailbox>
            </Attendee>
            <Attendee>
              <Mailbox>
                <EmailAddress>User2@example.com</EmailAddress>
              </Mailbox>
            </Attendee>
          </RequiredAttendees>
        </t:CalendarItem>
      </Items>
    </CreateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="a4932-115">备注</span><span class="sxs-lookup"><span data-stu-id="a4932-115">Comments</span></span>

<span data-ttu-id="a4932-116">有关如何响应会议请求的示例，请参阅[CreateItem 操作（会议请求）](createitem-operation-meeting-request.md)主题。</span><span class="sxs-lookup"><span data-stu-id="a4932-116">For an example of how to respond to a meeting request, see the [CreateItem operation (meeting request)](createitem-operation-meeting-request.md) topic.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="a4932-117">Request 元素</span><span class="sxs-lookup"><span data-stu-id="a4932-117">Request elements</span></span>

<span data-ttu-id="a4932-118">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="a4932-118">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="a4932-119">CreateItem</span><span class="sxs-lookup"><span data-stu-id="a4932-119">CreateItem</span></span>](createitem.md)
    
- [<span data-ttu-id="a4932-120">SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="a4932-120">SavedItemFolderId</span></span>](saveditemfolderid.md)
    
- [<span data-ttu-id="a4932-121">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="a4932-121">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="a4932-122">项目（NonEmptyArrayOfAllItemsType）</span><span class="sxs-lookup"><span data-stu-id="a4932-122">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
- [<span data-ttu-id="a4932-123">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="a4932-123">CalendarItem</span></span>](calendaritem.md)
    
- [<span data-ttu-id="a4932-124">主题</span><span class="sxs-lookup"><span data-stu-id="a4932-124">Subject</span></span>](subject.md)
    
- [<span data-ttu-id="a4932-125">Body</span><span class="sxs-lookup"><span data-stu-id="a4932-125">Body</span></span>](body.md)
    
- [<span data-ttu-id="a4932-126">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="a4932-126">ReminderIsSet</span></span>](reminderisset.md)
    
- [<span data-ttu-id="a4932-127">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="a4932-127">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md)
    
- [<span data-ttu-id="a4932-128">开始</span><span class="sxs-lookup"><span data-stu-id="a4932-128">Start</span></span>](start.md)
    
- [<span data-ttu-id="a4932-129">停止</span><span class="sxs-lookup"><span data-stu-id="a4932-129">End </span></span>](end-ex15websvcsotherref.md)
    
- [<span data-ttu-id="a4932-130">IsAllDayEvent</span><span class="sxs-lookup"><span data-stu-id="a4932-130">IsAllDayEvent</span></span>](isalldayevent.md)
    
- [<span data-ttu-id="a4932-131">LegacyFreeBusyStatus</span><span class="sxs-lookup"><span data-stu-id="a4932-131">LegacyFreeBusyStatus</span></span>](legacyfreebusystatus.md)
    
- [<span data-ttu-id="a4932-132">Location</span><span class="sxs-lookup"><span data-stu-id="a4932-132">Location</span></span>](location.md)
    
- [<span data-ttu-id="a4932-133">RequiredAttendees</span><span class="sxs-lookup"><span data-stu-id="a4932-133">RequiredAttendees</span></span>](requiredattendees.md)
    
- [<span data-ttu-id="a4932-134">与会者</span><span class="sxs-lookup"><span data-stu-id="a4932-134">Attendee</span></span>](attendee.md)
    
- [<span data-ttu-id="a4932-135">邮箱</span><span class="sxs-lookup"><span data-stu-id="a4932-135">Mailbox</span></span>](mailbox.md)
    
- [<span data-ttu-id="a4932-136">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="a4932-136">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
## <a name="successful-createitem-calendar-item-response"></a><span data-ttu-id="a4932-137">成功的 CreateItem （日历项目）响应</span><span class="sxs-lookup"><span data-stu-id="a4932-137">Successful CreateItem (Calendar Item) Response</span></span>

### <a name="description"></a><span data-ttu-id="a4932-138">Description</span><span class="sxs-lookup"><span data-stu-id="a4932-138">Description</span></span>

<span data-ttu-id="a4932-139">下面的示例演示对 CreateItem 请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="a4932-139">The following example shows a successful response to the CreateItem request.</span></span>
  
### <a name="code"></a><span data-ttu-id="a4932-140">代码</span><span class="sxs-lookup"><span data-stu-id="a4932-140">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:CalendarItem>
              <t:ItemId Id="AAAlAFV" ChangeKey="DwAAABYA" />
            </t:CalendarItem>
          </m:Items>
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </CreateItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="a4932-141">备注</span><span class="sxs-lookup"><span data-stu-id="a4932-141">Comments</span></span>

<span data-ttu-id="a4932-142">[ItemId](itemid.md)元素**Id**和**ChangeKey**属性已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="a4932-142">The [ItemId](itemid.md) element **Id** and **ChangeKey** attributes have been shortened to preserve readability.</span></span> 
  
### <a name="successful-response-elements"></a><span data-ttu-id="a4932-143">成功的响应元素</span><span class="sxs-lookup"><span data-stu-id="a4932-143">Successful response elements</span></span>

<span data-ttu-id="a4932-144">响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="a4932-144">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="a4932-145">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="a4932-145">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="a4932-146">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="a4932-146">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="a4932-147">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="a4932-147">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="a4932-148">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a4932-148">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="a4932-149">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="a4932-149">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="a4932-150">Items</span><span class="sxs-lookup"><span data-stu-id="a4932-150">Items</span></span>](items.md)
    
- [<span data-ttu-id="a4932-151">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="a4932-151">CalendarItem</span></span>](calendaritem.md)
    
- [<span data-ttu-id="a4932-152">ItemId</span><span class="sxs-lookup"><span data-stu-id="a4932-152">ItemId</span></span>](itemid.md)
    
## <a name="see-also"></a><span data-ttu-id="a4932-153">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a4932-153">See also</span></span>



[<span data-ttu-id="a4932-154">CreateItem 操作</span><span class="sxs-lookup"><span data-stu-id="a4932-154">CreateItem operation</span></span>](createitem-operation.md)

