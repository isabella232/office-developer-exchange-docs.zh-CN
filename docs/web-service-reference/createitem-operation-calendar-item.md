---
title: CreateItem operation，（日历项）
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
description: CreateItem operation，在 Exchange 存储中创建日历项目。
ms.openlocfilehash: c2174dd806b922e640ef7afcab32b98c67c65b41
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753659"
---
# <a name="createitem-operation-calendar-item"></a><span data-ttu-id="83a92-103">CreateItem operation，（日历项）</span><span class="sxs-lookup"><span data-stu-id="83a92-103">CreateItem operation (calendar item)</span></span>

<span data-ttu-id="83a92-104">CreateItem operation，在 Exchange 存储中创建日历项目。</span><span class="sxs-lookup"><span data-stu-id="83a92-104">The CreateItem operation creates calendar items in the Exchange store.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="83a92-105">备注</span><span class="sxs-lookup"><span data-stu-id="83a92-105">Remarks</span></span>

<span data-ttu-id="83a92-106">CreateItem 操作创建约会、 会议和会议请求。</span><span class="sxs-lookup"><span data-stu-id="83a92-106">The CreateItem operation creates appointments, meetings, and meeting requests.</span></span> <span data-ttu-id="83a92-107">如果与会者的情况下创建日历项目，则认为是约会。</span><span class="sxs-lookup"><span data-stu-id="83a92-107">If a calendar item is created without attendees, it is considered an appointment.</span></span> <span data-ttu-id="83a92-108">如果未指定与会者，则日历项目是会议。</span><span class="sxs-lookup"><span data-stu-id="83a92-108">If attendees are specified, the calendar item is a meeting.</span></span> <span data-ttu-id="83a92-109">使用 CreateItem 操作创建会议后，会议请求如果 SendMeetingInvitations 属性设置将发送会议请求自动发送到的标识的与会者。</span><span class="sxs-lookup"><span data-stu-id="83a92-109">When a meeting is created by using the CreateItem operation, meeting requests are automatically sent to the identified attendees if the SendMeetingInvitations attribute is set to send the meeting requests.</span></span>
  
## <a name="createitem-calendar-item-request-example"></a><span data-ttu-id="83a92-110">CreateItem （日历项） 请求示例</span><span class="sxs-lookup"><span data-stu-id="83a92-110">CreateItem (Calendar Item) request example</span></span>

### <a name="description"></a><span data-ttu-id="83a92-111">说明</span><span class="sxs-lookup"><span data-stu-id="83a92-111">Description</span></span>

<span data-ttu-id="83a92-112">CreateItem 请求的下面的示例演示如何创建与两个必需与会者的会议。</span><span class="sxs-lookup"><span data-stu-id="83a92-112">The following example of a CreateItem request shows how to create a meeting with two required attendees.</span></span> <span data-ttu-id="83a92-113">此请求将发送到两个与会者的会议请求。</span><span class="sxs-lookup"><span data-stu-id="83a92-113">This request will send the meeting requests to the two attendees.</span></span>
  
### <a name="code"></a><span data-ttu-id="83a92-114">代码</span><span class="sxs-lookup"><span data-stu-id="83a92-114">Code</span></span>

```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                SendMeetingInvitations="SendToAllAndSaveCopy" >
      <SavedItemFolderId>
        <t:DistinguishedFolderId Id="calendar"/>
      </SavedItemFolderId>
      <Items>
        <t:CalendarItem xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="comments"></a><span data-ttu-id="83a92-115">注释</span><span class="sxs-lookup"><span data-stu-id="83a92-115">Comments</span></span>

<span data-ttu-id="83a92-116">有关如何响应会议请求的示例，请参阅[CreateItem operation，（会议请求）](createitem-operation-meeting-request.md)这一主题。</span><span class="sxs-lookup"><span data-stu-id="83a92-116">For an example of how to respond to a meeting request, see the [CreateItem operation (meeting request)](createitem-operation-meeting-request.md) topic.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="83a92-117">请求元素</span><span class="sxs-lookup"><span data-stu-id="83a92-117">Request elements</span></span>

<span data-ttu-id="83a92-118">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="83a92-118">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="83a92-119">CreateItem</span><span class="sxs-lookup"><span data-stu-id="83a92-119">CreateItem</span></span>](createitem.md)
    
- [<span data-ttu-id="83a92-120">SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="83a92-120">SavedItemFolderId</span></span>](saveditemfolderid.md)
    
- [<span data-ttu-id="83a92-121">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="83a92-121">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="83a92-122">项目 (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="83a92-122">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
- [<span data-ttu-id="83a92-123">日历项目</span><span class="sxs-lookup"><span data-stu-id="83a92-123">CalendarItem</span></span>](calendaritem.md)
    
- [<span data-ttu-id="83a92-124">Subject</span><span class="sxs-lookup"><span data-stu-id="83a92-124">Subject</span></span>](subject.md)
    
- [<span data-ttu-id="83a92-125">Body</span><span class="sxs-lookup"><span data-stu-id="83a92-125">Body</span></span>](body.md)
    
- [<span data-ttu-id="83a92-126">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="83a92-126">ReminderIsSet</span></span>](reminderisset.md)
    
- [<span data-ttu-id="83a92-127">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="83a92-127">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md)
    
- [<span data-ttu-id="83a92-128">Start</span><span class="sxs-lookup"><span data-stu-id="83a92-128">Start</span></span>](start.md)
    
- [<span data-ttu-id="83a92-129">结束</span><span class="sxs-lookup"><span data-stu-id="83a92-129">End </span></span>](end-ex15websvcsotherref.md)
    
- [<span data-ttu-id="83a92-130">IsAllDayEvent</span><span class="sxs-lookup"><span data-stu-id="83a92-130">IsAllDayEvent</span></span>](isalldayevent.md)
    
- [<span data-ttu-id="83a92-131">LegacyFreeBusyStatus</span><span class="sxs-lookup"><span data-stu-id="83a92-131">LegacyFreeBusyStatus</span></span>](legacyfreebusystatus.md)
    
- [<span data-ttu-id="83a92-132">位置</span><span class="sxs-lookup"><span data-stu-id="83a92-132">Location</span></span>](location.md)
    
- [<span data-ttu-id="83a92-133">RequiredAttendees</span><span class="sxs-lookup"><span data-stu-id="83a92-133">RequiredAttendees</span></span>](requiredattendees.md)
    
- [<span data-ttu-id="83a92-134">参与者</span><span class="sxs-lookup"><span data-stu-id="83a92-134">Attendee</span></span>](attendee.md)
    
- [<span data-ttu-id="83a92-135">Mailbox</span><span class="sxs-lookup"><span data-stu-id="83a92-135">Mailbox</span></span>](mailbox.md)
    
- [<span data-ttu-id="83a92-136">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="83a92-136">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
## <a name="successful-createitem-calendar-item-response"></a><span data-ttu-id="83a92-137">成功 CreateItem （日历项） 响应</span><span class="sxs-lookup"><span data-stu-id="83a92-137">Successful CreateItem (Calendar Item) Response</span></span>

### <a name="description"></a><span data-ttu-id="83a92-138">说明</span><span class="sxs-lookup"><span data-stu-id="83a92-138">Description</span></span>

<span data-ttu-id="83a92-139">下面的示例演示对 CreateItem 请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="83a92-139">The following example shows a successful response to the CreateItem request.</span></span>
  
### <a name="code"></a><span data-ttu-id="83a92-140">代码</span><span class="sxs-lookup"><span data-stu-id="83a92-140">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CreateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="83a92-141">注释</span><span class="sxs-lookup"><span data-stu-id="83a92-141">Comments</span></span>

<span data-ttu-id="83a92-142">[ItemId](itemid.md)元素的**Id**和**更改密钥**属性具有已缩短要保留可读性。</span><span class="sxs-lookup"><span data-stu-id="83a92-142">The [ItemId](itemid.md) element **Id** and **ChangeKey** attributes have been shortened to preserve readability.</span></span> 
  
### <a name="successful-response-elements"></a><span data-ttu-id="83a92-143">成功响应元素</span><span class="sxs-lookup"><span data-stu-id="83a92-143">Successful response elements</span></span>

<span data-ttu-id="83a92-144">在响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="83a92-144">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="83a92-145">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="83a92-145">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="83a92-146">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="83a92-146">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="83a92-147">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="83a92-147">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="83a92-148">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="83a92-148">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="83a92-149">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="83a92-149">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="83a92-150">Items</span><span class="sxs-lookup"><span data-stu-id="83a92-150">Items</span></span>](items.md)
    
- [<span data-ttu-id="83a92-151">日历项目</span><span class="sxs-lookup"><span data-stu-id="83a92-151">CalendarItem</span></span>](calendaritem.md)
    
- [<span data-ttu-id="83a92-152">ItemId</span><span class="sxs-lookup"><span data-stu-id="83a92-152">ItemId</span></span>](itemid.md)
    
## <a name="see-also"></a><span data-ttu-id="83a92-153">另请参阅</span><span class="sxs-lookup"><span data-stu-id="83a92-153">See also</span></span>



[<span data-ttu-id="83a92-154">CreateItem 操作</span><span class="sxs-lookup"><span data-stu-id="83a92-154">CreateItem operation</span></span>](createitem-operation.md)

