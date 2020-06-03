---
title: GetItem 操作（日历项目）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetItem
api_type:
- schema
ms.assetid: a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8
description: GetItem 操作从 Exchange 存储中获取日历项目。
ms.openlocfilehash: 09fe92af12f03ce4cebd1e98f4e01c087ace64f9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460615"
---
# <a name="getitem-operation-calendar-item"></a><span data-ttu-id="e1d94-103">GetItem 操作（日历项目）</span><span class="sxs-lookup"><span data-stu-id="e1d94-103">GetItem operation (calendar item)</span></span>

<span data-ttu-id="e1d94-104">GetItem 操作从 Exchange 存储中获取日历项目。</span><span class="sxs-lookup"><span data-stu-id="e1d94-104">The GetItem operation gets calendar items from the Exchange store.</span></span>
  
## <a name="getitem-request-example"></a><span data-ttu-id="e1d94-105">GetItem 请求示例</span><span class="sxs-lookup"><span data-stu-id="e1d94-105">GetItem request example</span></span>

### <a name="description"></a><span data-ttu-id="e1d94-106">Description</span><span class="sxs-lookup"><span data-stu-id="e1d94-106">Description</span></span>

<span data-ttu-id="e1d94-107">以下示例的 GetItem 请求显示如何形成请求以获取项目的标识和主题。</span><span class="sxs-lookup"><span data-stu-id="e1d94-107">The following example of a GetItem request shows how to form a request to get the identity and subject of an item.</span></span>
  
### <a name="code"></a><span data-ttu-id="e1d94-108">代码</span><span class="sxs-lookup"><span data-stu-id="e1d94-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject"/>
        </t:AdditionalProperties>
      </ItemShape>
      <ItemIds>
        <t:ItemId Id="AsdD89=" ChangeKey="Jajs3=="/>
      </ItemIds>
    </GetItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="e1d94-109">Request 元素</span><span class="sxs-lookup"><span data-stu-id="e1d94-109">Request elements</span></span>

<span data-ttu-id="e1d94-110">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="e1d94-110">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="e1d94-111">GetItem</span><span class="sxs-lookup"><span data-stu-id="e1d94-111">GetItem</span></span>](getitem.md)
    
- [<span data-ttu-id="e1d94-112">ItemShape</span><span class="sxs-lookup"><span data-stu-id="e1d94-112">ItemShape</span></span>](itemshape.md)
    
- [<span data-ttu-id="e1d94-113">BaseShape</span><span class="sxs-lookup"><span data-stu-id="e1d94-113">BaseShape</span></span>](baseshape.md)
    
- [<span data-ttu-id="e1d94-114">AdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="e1d94-114">AdditionalProperties</span></span>](additionalproperties.md)
    
- [<span data-ttu-id="e1d94-115">FieldURI</span><span class="sxs-lookup"><span data-stu-id="e1d94-115">FieldURI</span></span>](fielduri.md)
    
- [<span data-ttu-id="e1d94-116">ItemIds</span><span class="sxs-lookup"><span data-stu-id="e1d94-116">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="e1d94-117">ItemId</span><span class="sxs-lookup"><span data-stu-id="e1d94-117">ItemId</span></span>](itemid.md)
    
> [!NOTE]
> <span data-ttu-id="e1d94-118">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e1d94-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
<span data-ttu-id="e1d94-119">若要查找 GetItem 操作的请求消息的其他选项，请浏览架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="e1d94-119">To find other options for the request message of the GetItem operation, explore the schema hierarchy.</span></span> <span data-ttu-id="e1d94-120">从[GetItem](getitem.md)元素开始。</span><span class="sxs-lookup"><span data-stu-id="e1d94-120">Start at the [GetItem](getitem.md) element.</span></span> 
  
## <a name="successful-getitem-response"></a><span data-ttu-id="e1d94-121">成功的 GetItem 响应</span><span class="sxs-lookup"><span data-stu-id="e1d94-121">Successful GetItem Response</span></span>

### <a name="description"></a><span data-ttu-id="e1d94-122">Description</span><span class="sxs-lookup"><span data-stu-id="e1d94-122">Description</span></span>

<span data-ttu-id="e1d94-123">下面的示例演示对 GetItem 请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="e1d94-123">The following example shows a successful response to the GetItem request.</span></span> <span data-ttu-id="e1d94-124">创建此响应的请求使用 IdOnly baseshape。</span><span class="sxs-lookup"><span data-stu-id="e1d94-124">The request that created this response used the IdOnly baseshape.</span></span> <span data-ttu-id="e1d94-125">在此示例中，响应仅返回项目的 ID。</span><span class="sxs-lookup"><span data-stu-id="e1d94-125">In this example, the response returns only the ID of the item.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e1d94-126">项目 ID 和更改密钥已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="e1d94-126">The item ID and the change key have been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="e1d94-127">代码</span><span class="sxs-lookup"><span data-stu-id="e1d94-127">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                   xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                   xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:CalendarItem>
              <t:ItemId Id="ASUAd" ChangeKey="otlIqB=="/>
            </t:CalendarItem>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </GetItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="description"></a><span data-ttu-id="e1d94-128">说明</span><span class="sxs-lookup"><span data-stu-id="e1d94-128">Description</span></span>

<span data-ttu-id="e1d94-129">下面的示例演示对 GetItem 请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="e1d94-129">The following example shows a successful response to the GetItem request.</span></span> <span data-ttu-id="e1d94-130">创建此响应的请求使用默认 baseshape。</span><span class="sxs-lookup"><span data-stu-id="e1d94-130">The request that created this response used the Default baseshape.</span></span> <span data-ttu-id="e1d94-131">在此示例中，响应返回日历项目的默认形状。</span><span class="sxs-lookup"><span data-stu-id="e1d94-131">In this example, the response returns the Default shape for a calendar item.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e1d94-132">项目 ID 和更改密钥已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="e1d94-132">The item ID and the change key have been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="e1d94-133">代码</span><span class="sxs-lookup"><span data-stu-id="e1d94-133">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                     xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                     xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:CalendarItem>
              <t:ItemId Id="ASUAdTB" ChangeKey="otlIqBwrt=="/>
              <t:ResponseObjects>
                <t:ForwardItem/>
              </t:ResponseObjects>
              <t:Start>2006-06-16T00:30:00Z</t:Start>
              <t:End>2006-06-16T01:00:00Z</t:End>
              <t:LegacyFreeBusyStatus>Busy</t:LegacyFreeBusyStatus>
              <t:CalendarItemType>Single</t:CalendarItemType>
              <t:Organizer>
                <t:Mailbox>
                  <t:Name>Bob</t:Name>
                  <t:EmailAddress>someone@example.com</t:EmailAddress>
                  <t:RoutingType>SMTP</t:RoutingType>
                </t:Mailbox>
              </t:Organizer>
            </t:CalendarItem>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </GetItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="description"></a><span data-ttu-id="e1d94-134">说明</span><span class="sxs-lookup"><span data-stu-id="e1d94-134">Description</span></span>

<span data-ttu-id="e1d94-135">下面的示例演示对 GetItem 请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="e1d94-135">The following example shows a successful response to the GetItem request.</span></span> <span data-ttu-id="e1d94-136">创建此响应的请求使用 AllProperties baseshape。</span><span class="sxs-lookup"><span data-stu-id="e1d94-136">The request that created this response used the AllProperties baseshape.</span></span> <span data-ttu-id="e1d94-137">在此示例中，响应返回日历项目的 AllProperties 形状。</span><span class="sxs-lookup"><span data-stu-id="e1d94-137">In this example, the response returns the AllProperties shape for a calendar item.</span></span>
  
### <a name="code"></a><span data-ttu-id="e1d94-138">代码</span><span class="sxs-lookup"><span data-stu-id="e1d94-138">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                     xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                     xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:CalendarItem>
              <t:ItemId Id="ASUAdT" ChangeKey="otlIqB=="/>
              <t:ParentFolderId Id="ASUAdT=="/>
              <t:ItemClass>IPM.Appointment</t:ItemClass>
              <t:Sensitivity>Normal</t:Sensitivity>
              <t:Body BodyType="Text"/>
              <t:DateTimeReceived>2006-06-16T00:12:41Z</t:DateTimeReceived>
              <t:Size>374</t:Size>
              <t:Importance>Normal</t:Importance>
              <t:IsSubmitted>false</t:IsSubmitted>
              <t:IsDraft>false</t:IsDraft>
              <t:IsFromMe>false</t:IsFromMe>
              <t:IsResend>false</t:IsResend>
              <t:IsUnmodified>false</t:IsUnmodified>
              <t:DateTimeSent>2006-06-16T00:12:41Z</t:DateTimeSent>
              <t:DateTimeCreated>2006-06-16T00:12:41Z</t:DateTimeCreated>
              <t:ResponseObjects>
                <t:ForwardItem/>
              </t:ResponseObjects>
              <t:ReminderDueBy>2006-06-16T00:30:00Z</t:ReminderDueBy>
              <t:ReminderIsSet>true</t:ReminderIsSet>
              <t:ReminderMinutesBeforeStart>15</t:ReminderMinutesBeforeStart>
              <t:DisplayCc/>
              <t:DisplayTo/>
              <t:HasAttachments>false</t:HasAttachments>
              <t:Culture>en-US</t:Culture>
              <t:Start>2006-06-16T00:30:00Z</t:Start>
              <t:End>2006-06-16T01:00:00Z</t:End>
              <t:IsAllDayEvent>false</t:IsAllDayEvent>
              <t:LegacyFreeBusyStatus>Busy</t:LegacyFreeBusyStatus>
              <t:IsMeeting>false</t:IsMeeting>
              <t:IsCancelled>false</t:IsCancelled>
              <t:IsRecurring>false</t:IsRecurring>
              <t:MeetingRequestWasSent>false</t:MeetingRequestWasSent>
              <t:CalendarItemType>Single</t:CalendarItemType>
              <t:MyResponseType>Organizer</t:MyResponseType>
              <t:Organizer>
                <t:Mailbox>
                  <t:Name>Bob</t:Name>
                  <t:EmailAddress>someone@example.com</t:EmailAddress>
                  <t:RoutingType>SMTP</t:RoutingType>
                </t:Mailbox>
              </t:Organizer>
              <t:ConflictingMeetingCount>2</t:ConflictingMeetingCount>
              <t:AdjacentMeetingCount>0</t:AdjacentMeetingCount>
              <t:ConflictingMeetings>
                <t:CalendarItem>
                  <t:ItemId Id="ASUAdTB" ChangeKey="otlIqBwr=="/>
                  <t:Subject/>
                  <t:Start>2006-06-16T00:30:00Z</t:Start>
                  <t:End>2006-06-16T01:00:00Z</t:End>
                  <t:LegacyFreeBusyStatus>Busy</t:LegacyFreeBusyStatus>
                  <t:Location/>
                </t:CalendarItem>
                <t:CalendarItem>
                  <t:ItemId Id="ASUAd" ChangeKey="otlIqBw=="/>
                  <t:Subject/>
                  <t:Start>2006-06-16T00:30:00Z</t:Start>
                  <t:End>2006-06-16T01:00:00Z</t:End>
                  <t:LegacyFreeBusyStatus>Busy</t:LegacyFreeBusyStatus>
                  <t:Location/>
                </t:CalendarItem>
              </t:ConflictingMeetings>
              <t:Duration>PT30M</t:Duration>
              <t:TimeZone>Pacific Standard Time</t:TimeZone>
              <t:AppointmentSequenceNumber>0</t:AppointmentSequenceNumber>
              <t:AppointmentState>0</t:AppointmentState>
            </t:CalendarItem>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </GetItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="e1d94-139">备注</span><span class="sxs-lookup"><span data-stu-id="e1d94-139">Comments</span></span>

<span data-ttu-id="e1d94-140">若要查找 GetItem 操作的响应邮件的其他选项，请浏览架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="e1d94-140">To find other options for the response message of the GetItem operation, explore the schema hierarchy.</span></span> <span data-ttu-id="e1d94-141">从[GetItemResponse](getitemresponse.md)元素开始。</span><span class="sxs-lookup"><span data-stu-id="e1d94-141">Start at the [GetItemResponse](getitemresponse.md) element.</span></span> 
  
### <a name="successful-response-elements"></a><span data-ttu-id="e1d94-142">成功的响应元素</span><span class="sxs-lookup"><span data-stu-id="e1d94-142">Successful response elements</span></span>

<span data-ttu-id="e1d94-143">响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="e1d94-143">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="e1d94-144">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="e1d94-144">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="e1d94-145">GetItemResponse</span><span class="sxs-lookup"><span data-stu-id="e1d94-145">GetItemResponse</span></span>](getitemresponse.md)
    
- [<span data-ttu-id="e1d94-146">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e1d94-146">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="e1d94-147">GetItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e1d94-147">GetItemResponseMessage</span></span>](getitemresponsemessage.md)
    
- [<span data-ttu-id="e1d94-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e1d94-148">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="e1d94-149">Items</span><span class="sxs-lookup"><span data-stu-id="e1d94-149">Items</span></span>](items.md)
    
- [<span data-ttu-id="e1d94-150">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="e1d94-150">CalendarItem</span></span>](calendaritem.md)
    
- [<span data-ttu-id="e1d94-151">ItemId</span><span class="sxs-lookup"><span data-stu-id="e1d94-151">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="e1d94-152">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="e1d94-152">ParentFolderId</span></span>](parentfolderid.md)
    
- [<span data-ttu-id="e1d94-153">ItemClass</span><span class="sxs-lookup"><span data-stu-id="e1d94-153">ItemClass</span></span>](itemclass.md)
    
- [<span data-ttu-id="e1d94-154">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="e1d94-154">Sensitivity</span></span>](sensitivity.md)
    
- [<span data-ttu-id="e1d94-155">Body</span><span class="sxs-lookup"><span data-stu-id="e1d94-155">Body</span></span>](body.md)
    
- [<span data-ttu-id="e1d94-156">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="e1d94-156">DateTimeReceived</span></span>](datetimereceived.md)
    
- [<span data-ttu-id="e1d94-157">大小</span><span class="sxs-lookup"><span data-stu-id="e1d94-157">Size</span></span>](size.md)
    
- [<span data-ttu-id="e1d94-158">Importance</span><span class="sxs-lookup"><span data-stu-id="e1d94-158">Importance</span></span>](importance.md)
    
- [<span data-ttu-id="e1d94-159">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="e1d94-159">IsSubmitted</span></span>](issubmitted.md)
    
- [<span data-ttu-id="e1d94-160">IsDraft</span><span class="sxs-lookup"><span data-stu-id="e1d94-160">IsDraft</span></span>](isdraft.md)
    
- [<span data-ttu-id="e1d94-161">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="e1d94-161">IsFromMe</span></span>](isfromme.md)
    
- [<span data-ttu-id="e1d94-162">IsResend</span><span class="sxs-lookup"><span data-stu-id="e1d94-162">IsResend</span></span>](isresend.md)
    
- [<span data-ttu-id="e1d94-163">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="e1d94-163">IsUnmodified</span></span>](isunmodified.md)
    
- [<span data-ttu-id="e1d94-164">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="e1d94-164">DateTimeSent</span></span>](datetimesent.md)
    
- [<span data-ttu-id="e1d94-165">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="e1d94-165">DateTimeCreated</span></span>](datetimecreated.md)
    
- [<span data-ttu-id="e1d94-166">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="e1d94-166">ResponseObjects</span></span>](responseobjects.md)
    
- [<span data-ttu-id="e1d94-167">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="e1d94-167">ForwardItem</span></span>](forwarditem.md)
    
- [<span data-ttu-id="e1d94-168">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="e1d94-168">ReminderDueBy</span></span>](reminderdueby.md)
    
- [<span data-ttu-id="e1d94-169">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="e1d94-169">ReminderIsSet</span></span>](reminderisset.md)
    
- [<span data-ttu-id="e1d94-170">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="e1d94-170">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md)
    
- [<span data-ttu-id="e1d94-171">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="e1d94-171">DisplayCc</span></span>](displaycc.md)
    
- [<span data-ttu-id="e1d94-172">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="e1d94-172">DisplayTo</span></span>](displayto.md)
    
- [<span data-ttu-id="e1d94-173">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="e1d94-173">HasAttachments</span></span>](hasattachments.md)
    
- [<span data-ttu-id="e1d94-174">Culture</span><span class="sxs-lookup"><span data-stu-id="e1d94-174">Culture</span></span>](culture.md)
    
- [<span data-ttu-id="e1d94-175">开始</span><span class="sxs-lookup"><span data-stu-id="e1d94-175">Start</span></span>](start.md)
    
- [<span data-ttu-id="e1d94-176">停止</span><span class="sxs-lookup"><span data-stu-id="e1d94-176">End </span></span>](end-ex15websvcsotherref.md)
    
- [<span data-ttu-id="e1d94-177">IsAllDayEvent</span><span class="sxs-lookup"><span data-stu-id="e1d94-177">IsAllDayEvent</span></span>](isalldayevent.md)
    
- [<span data-ttu-id="e1d94-178">LegacyFreeBusyStatus</span><span class="sxs-lookup"><span data-stu-id="e1d94-178">LegacyFreeBusyStatus</span></span>](legacyfreebusystatus.md)
    
- [<span data-ttu-id="e1d94-179">IsMeeting</span><span class="sxs-lookup"><span data-stu-id="e1d94-179">IsMeeting</span></span>](ismeeting.md)
    
- [<span data-ttu-id="e1d94-180">IsCancelled</span><span class="sxs-lookup"><span data-stu-id="e1d94-180">IsCancelled</span></span>](iscancelled.md)
    
- [<span data-ttu-id="e1d94-181">IsRecurring</span><span class="sxs-lookup"><span data-stu-id="e1d94-181">IsRecurring</span></span>](isrecurring.md)
    
- [<span data-ttu-id="e1d94-182">MeetingRequestWasSent</span><span class="sxs-lookup"><span data-stu-id="e1d94-182">MeetingRequestWasSent</span></span>](meetingrequestwassent.md)
    
- [<span data-ttu-id="e1d94-183">CalendarItemType</span><span class="sxs-lookup"><span data-stu-id="e1d94-183">CalendarItemType</span></span>](calendaritemtype.md)
    
- [<span data-ttu-id="e1d94-184">MyResponseType</span><span class="sxs-lookup"><span data-stu-id="e1d94-184">MyResponseType</span></span>](myresponsetype.md)
    
- [<span data-ttu-id="e1d94-185">Organizer</span><span class="sxs-lookup"><span data-stu-id="e1d94-185">Organizer</span></span>](organizer.md)
    
- [<span data-ttu-id="e1d94-186">邮箱</span><span class="sxs-lookup"><span data-stu-id="e1d94-186">Mailbox</span></span>](mailbox.md)
    
- [<span data-ttu-id="e1d94-187">名称 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="e1d94-187">Name (EmailAddressType)</span></span>](name-emailaddresstype.md)
    
- [<span data-ttu-id="e1d94-188">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="e1d94-188">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
- [<span data-ttu-id="e1d94-189">RoutingType （EmailAddressType）</span><span class="sxs-lookup"><span data-stu-id="e1d94-189">RoutingType (EmailAddressType)</span></span>](routingtype-emailaddresstype.md)
    
- [<span data-ttu-id="e1d94-190">ConflictingMeetingCount</span><span class="sxs-lookup"><span data-stu-id="e1d94-190">ConflictingMeetingCount</span></span>](conflictingmeetingcount.md)
    
- [<span data-ttu-id="e1d94-191">AdjacentMeetingCount</span><span class="sxs-lookup"><span data-stu-id="e1d94-191">AdjacentMeetingCount</span></span>](adjacentmeetingcount.md)
    
- [<span data-ttu-id="e1d94-192">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="e1d94-192">ConflictingMeetings</span></span>](conflictingmeetings.md)
    
- [<span data-ttu-id="e1d94-193">Location</span><span class="sxs-lookup"><span data-stu-id="e1d94-193">Location</span></span>](location.md)
    
- [<span data-ttu-id="e1d94-194">持续时间（项目）</span><span class="sxs-lookup"><span data-stu-id="e1d94-194">Duration (Items)</span></span>](duration-items.md)
    
- [<span data-ttu-id="e1d94-195">时区（项目）</span><span class="sxs-lookup"><span data-stu-id="e1d94-195">TimeZone (Item)</span></span>](timezone-item.md)
    
- [<span data-ttu-id="e1d94-196">AppointmentSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="e1d94-196">AppointmentSequenceNumber</span></span>](appointmentsequencenumber.md)
    
- [<span data-ttu-id="e1d94-197">AppointmentState</span><span class="sxs-lookup"><span data-stu-id="e1d94-197">AppointmentState</span></span>](appointmentstate.md)
    
## <a name="see-also"></a><span data-ttu-id="e1d94-198">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e1d94-198">See also</span></span>



[<span data-ttu-id="e1d94-199">GetItem 操作</span><span class="sxs-lookup"><span data-stu-id="e1d94-199">GetItem operation</span></span>](getitem-operation.md)

