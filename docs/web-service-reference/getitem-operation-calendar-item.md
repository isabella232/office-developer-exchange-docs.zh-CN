---
title: GetItem 操作 （日历项）
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
description: GetItem 操作获取从 Exchange 存储的日历项目。
ms.openlocfilehash: 69bce0f0cc7b5c986f9bf4767c3cd429a309e50d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754588"
---
# <a name="getitem-operation-calendar-item"></a><span data-ttu-id="085b6-103">GetItem 操作 （日历项）</span><span class="sxs-lookup"><span data-stu-id="085b6-103">GetItem operation (calendar item)</span></span>

<span data-ttu-id="085b6-104">GetItem 操作获取从 Exchange 存储的日历项目。</span><span class="sxs-lookup"><span data-stu-id="085b6-104">The GetItem operation gets calendar items from the Exchange store.</span></span>
  
## <a name="getitem-request-example"></a><span data-ttu-id="085b6-105">GetItem 请求示例</span><span class="sxs-lookup"><span data-stu-id="085b6-105">GetItem request example</span></span>

### <a name="description"></a><span data-ttu-id="085b6-106">说明</span><span class="sxs-lookup"><span data-stu-id="085b6-106">Description</span></span>

<span data-ttu-id="085b6-107">GetItem 请求的下面的示例演示如何以形成一个请求以获取的标识和项目的主题。</span><span class="sxs-lookup"><span data-stu-id="085b6-107">The following example of a GetItem request shows how to form a request to get the identity and subject of an item.</span></span>
  
### <a name="code"></a><span data-ttu-id="085b6-108">代码</span><span class="sxs-lookup"><span data-stu-id="085b6-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="request-elements"></a><span data-ttu-id="085b6-109">请求元素</span><span class="sxs-lookup"><span data-stu-id="085b6-109">Request elements</span></span>

<span data-ttu-id="085b6-110">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="085b6-110">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="085b6-111">GetItem</span><span class="sxs-lookup"><span data-stu-id="085b6-111">GetItem</span></span>](getitem.md)
    
- [<span data-ttu-id="085b6-112">ItemShape</span><span class="sxs-lookup"><span data-stu-id="085b6-112">ItemShape</span></span>](itemshape.md)
    
- [<span data-ttu-id="085b6-113">BaseShape</span><span class="sxs-lookup"><span data-stu-id="085b6-113">BaseShape</span></span>](baseshape.md)
    
- [<span data-ttu-id="085b6-114">AdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="085b6-114">AdditionalProperties</span></span>](additionalproperties.md)
    
- [<span data-ttu-id="085b6-115">FieldURI</span><span class="sxs-lookup"><span data-stu-id="085b6-115">FieldURI</span></span>](fielduri.md)
    
- [<span data-ttu-id="085b6-116">ItemIds</span><span class="sxs-lookup"><span data-stu-id="085b6-116">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="085b6-117">ItemId</span><span class="sxs-lookup"><span data-stu-id="085b6-117">ItemId</span></span>](itemid.md)
    
> [!NOTE]
> <span data-ttu-id="085b6-118">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="085b6-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
<span data-ttu-id="085b6-119">若要查找的请求邮件 GetItem 操作的其他选项，浏览的架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="085b6-119">To find other options for the request message of the GetItem operation, explore the schema hierarchy.</span></span> <span data-ttu-id="085b6-120">启动[GetItem](getitem.md)元素。</span><span class="sxs-lookup"><span data-stu-id="085b6-120">Start at the [GetItem](getitem.md) element.</span></span> 
  
## <a name="successful-getitem-response"></a><span data-ttu-id="085b6-121">成功的 GetItem 响应</span><span class="sxs-lookup"><span data-stu-id="085b6-121">Successful GetItem Response</span></span>

### <a name="description"></a><span data-ttu-id="085b6-122">说明</span><span class="sxs-lookup"><span data-stu-id="085b6-122">Description</span></span>

<span data-ttu-id="085b6-123">下面的示例演示对 GetItem 请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="085b6-123">The following example shows a successful response to the GetItem request.</span></span> <span data-ttu-id="085b6-124">创建此响应该请求使用 IdOnly baseshape。</span><span class="sxs-lookup"><span data-stu-id="085b6-124">The request that created this response used the IdOnly baseshape.</span></span> <span data-ttu-id="085b6-125">本示例中，响应返回仅的项的 ID。</span><span class="sxs-lookup"><span data-stu-id="085b6-125">In this example, the response returns only the ID of the item.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="085b6-126">已缩短项目 ID 和更改密钥，以保留可读性。</span><span class="sxs-lookup"><span data-stu-id="085b6-126">The item ID and the change key have been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="085b6-127">代码</span><span class="sxs-lookup"><span data-stu-id="085b6-127">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                   xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                   xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="description"></a><span data-ttu-id="085b6-128">说明</span><span class="sxs-lookup"><span data-stu-id="085b6-128">Description</span></span>

<span data-ttu-id="085b6-129">下面的示例演示对 GetItem 请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="085b6-129">The following example shows a successful response to the GetItem request.</span></span> <span data-ttu-id="085b6-130">创建此响应该请求使用默认 baseshape。</span><span class="sxs-lookup"><span data-stu-id="085b6-130">The request that created this response used the Default baseshape.</span></span> <span data-ttu-id="085b6-131">本示例中，响应返回日历项目的默认形状。</span><span class="sxs-lookup"><span data-stu-id="085b6-131">In this example, the response returns the Default shape for a calendar item.</span></span>
  
> [!NOTE]
> <span data-ttu-id="085b6-132">已缩短项目 ID 和更改密钥，以保留可读性。</span><span class="sxs-lookup"><span data-stu-id="085b6-132">The item ID and the change key have been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="085b6-133">代码</span><span class="sxs-lookup"><span data-stu-id="085b6-133">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                     xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                     xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="description"></a><span data-ttu-id="085b6-134">说明</span><span class="sxs-lookup"><span data-stu-id="085b6-134">Description</span></span>

<span data-ttu-id="085b6-135">下面的示例演示对 GetItem 请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="085b6-135">The following example shows a successful response to the GetItem request.</span></span> <span data-ttu-id="085b6-136">创建此响应该请求使用 AllProperties baseshape。</span><span class="sxs-lookup"><span data-stu-id="085b6-136">The request that created this response used the AllProperties baseshape.</span></span> <span data-ttu-id="085b6-137">本示例中，响应返回日历项目的 AllProperties 形状。</span><span class="sxs-lookup"><span data-stu-id="085b6-137">In this example, the response returns the AllProperties shape for a calendar item.</span></span>
  
### <a name="code"></a><span data-ttu-id="085b6-138">代码</span><span class="sxs-lookup"><span data-stu-id="085b6-138">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                     xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                     xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="085b6-139">注释</span><span class="sxs-lookup"><span data-stu-id="085b6-139">Comments</span></span>

<span data-ttu-id="085b6-140">若要查找的响应消息 GetItem 操作的其他选项，浏览的架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="085b6-140">To find other options for the response message of the GetItem operation, explore the schema hierarchy.</span></span> <span data-ttu-id="085b6-141">启动[GetItemResponse](getitemresponse.md)元素。</span><span class="sxs-lookup"><span data-stu-id="085b6-141">Start at the [GetItemResponse](getitemresponse.md) element.</span></span> 
  
### <a name="successful-response-elements"></a><span data-ttu-id="085b6-142">成功响应元素</span><span class="sxs-lookup"><span data-stu-id="085b6-142">Successful response elements</span></span>

<span data-ttu-id="085b6-143">在响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="085b6-143">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="085b6-144">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="085b6-144">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="085b6-145">GetItemResponse</span><span class="sxs-lookup"><span data-stu-id="085b6-145">GetItemResponse</span></span>](getitemresponse.md)
    
- [<span data-ttu-id="085b6-146">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="085b6-146">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="085b6-147">GetItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="085b6-147">GetItemResponseMessage</span></span>](getitemresponsemessage.md)
    
- [<span data-ttu-id="085b6-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="085b6-148">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="085b6-149">Items</span><span class="sxs-lookup"><span data-stu-id="085b6-149">Items</span></span>](items.md)
    
- [<span data-ttu-id="085b6-150">日历项目</span><span class="sxs-lookup"><span data-stu-id="085b6-150">CalendarItem</span></span>](calendaritem.md)
    
- [<span data-ttu-id="085b6-151">ItemId</span><span class="sxs-lookup"><span data-stu-id="085b6-151">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="085b6-152">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="085b6-152">ParentFolderId</span></span>](parentfolderid.md)
    
- [<span data-ttu-id="085b6-153">ItemClass</span><span class="sxs-lookup"><span data-stu-id="085b6-153">ItemClass</span></span>](itemclass.md)
    
- [<span data-ttu-id="085b6-154">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="085b6-154">Sensitivity</span></span>](sensitivity.md)
    
- [<span data-ttu-id="085b6-155">Body</span><span class="sxs-lookup"><span data-stu-id="085b6-155">Body</span></span>](body.md)
    
- [<span data-ttu-id="085b6-156">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="085b6-156">DateTimeReceived</span></span>](datetimereceived.md)
    
- [<span data-ttu-id="085b6-157">Size</span><span class="sxs-lookup"><span data-stu-id="085b6-157">Size</span></span>](size.md)
    
- [<span data-ttu-id="085b6-158">Importance</span><span class="sxs-lookup"><span data-stu-id="085b6-158">Importance</span></span>](importance.md)
    
- [<span data-ttu-id="085b6-159">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="085b6-159">IsSubmitted</span></span>](issubmitted.md)
    
- [<span data-ttu-id="085b6-160">IsDraft</span><span class="sxs-lookup"><span data-stu-id="085b6-160">IsDraft</span></span>](isdraft.md)
    
- [<span data-ttu-id="085b6-161">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="085b6-161">IsFromMe</span></span>](isfromme.md)
    
- [<span data-ttu-id="085b6-162">IsResend</span><span class="sxs-lookup"><span data-stu-id="085b6-162">IsResend</span></span>](isresend.md)
    
- [<span data-ttu-id="085b6-163">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="085b6-163">IsUnmodified</span></span>](isunmodified.md)
    
- [<span data-ttu-id="085b6-164">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="085b6-164">DateTimeSent</span></span>](datetimesent.md)
    
- [<span data-ttu-id="085b6-165">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="085b6-165">DateTimeCreated</span></span>](datetimecreated.md)
    
- [<span data-ttu-id="085b6-166">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="085b6-166">ResponseObjects</span></span>](responseobjects.md)
    
- [<span data-ttu-id="085b6-167">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="085b6-167">ForwardItem</span></span>](forwarditem.md)
    
- [<span data-ttu-id="085b6-168">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="085b6-168">ReminderDueBy</span></span>](reminderdueby.md)
    
- [<span data-ttu-id="085b6-169">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="085b6-169">ReminderIsSet</span></span>](reminderisset.md)
    
- [<span data-ttu-id="085b6-170">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="085b6-170">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md)
    
- [<span data-ttu-id="085b6-171">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="085b6-171">DisplayCc</span></span>](displaycc.md)
    
- [<span data-ttu-id="085b6-172">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="085b6-172">DisplayTo</span></span>](displayto.md)
    
- [<span data-ttu-id="085b6-173">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="085b6-173">HasAttachments</span></span>](hasattachments.md)
    
- [<span data-ttu-id="085b6-174">区域性</span><span class="sxs-lookup"><span data-stu-id="085b6-174">Culture</span></span>](culture.md)
    
- [<span data-ttu-id="085b6-175">Start</span><span class="sxs-lookup"><span data-stu-id="085b6-175">Start</span></span>](start.md)
    
- [<span data-ttu-id="085b6-176">结束</span><span class="sxs-lookup"><span data-stu-id="085b6-176">End </span></span>](end-ex15websvcsotherref.md)
    
- [<span data-ttu-id="085b6-177">IsAllDayEvent</span><span class="sxs-lookup"><span data-stu-id="085b6-177">IsAllDayEvent</span></span>](isalldayevent.md)
    
- [<span data-ttu-id="085b6-178">LegacyFreeBusyStatus</span><span class="sxs-lookup"><span data-stu-id="085b6-178">LegacyFreeBusyStatus</span></span>](legacyfreebusystatus.md)
    
- [<span data-ttu-id="085b6-179">IsMeeting</span><span class="sxs-lookup"><span data-stu-id="085b6-179">IsMeeting</span></span>](ismeeting.md)
    
- [<span data-ttu-id="085b6-180">IsCancelled</span><span class="sxs-lookup"><span data-stu-id="085b6-180">IsCancelled</span></span>](iscancelled.md)
    
- [<span data-ttu-id="085b6-181">IsRecurring</span><span class="sxs-lookup"><span data-stu-id="085b6-181">IsRecurring</span></span>](isrecurring.md)
    
- [<span data-ttu-id="085b6-182">MeetingRequestWasSent</span><span class="sxs-lookup"><span data-stu-id="085b6-182">MeetingRequestWasSent</span></span>](meetingrequestwassent.md)
    
- [<span data-ttu-id="085b6-183">CalendarItemType</span><span class="sxs-lookup"><span data-stu-id="085b6-183">CalendarItemType</span></span>](calendaritemtype.md)
    
- [<span data-ttu-id="085b6-184">MyResponseType</span><span class="sxs-lookup"><span data-stu-id="085b6-184">MyResponseType</span></span>](myresponsetype.md)
    
- [<span data-ttu-id="085b6-185">Organizer</span><span class="sxs-lookup"><span data-stu-id="085b6-185">Organizer</span></span>](organizer.md)
    
- [<span data-ttu-id="085b6-186">Mailbox</span><span class="sxs-lookup"><span data-stu-id="085b6-186">Mailbox</span></span>](mailbox.md)
    
- [<span data-ttu-id="085b6-187">名称 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="085b6-187">Name (EmailAddressType)</span></span>](name-emailaddresstype.md)
    
- [<span data-ttu-id="085b6-188">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="085b6-188">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
- [<span data-ttu-id="085b6-189">RoutingType (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="085b6-189">RoutingType (EmailAddressType)</span></span>](routingtype-emailaddresstype.md)
    
- [<span data-ttu-id="085b6-190">ConflictingMeetingCount</span><span class="sxs-lookup"><span data-stu-id="085b6-190">ConflictingMeetingCount</span></span>](conflictingmeetingcount.md)
    
- [<span data-ttu-id="085b6-191">AdjacentMeetingCount</span><span class="sxs-lookup"><span data-stu-id="085b6-191">AdjacentMeetingCount</span></span>](adjacentmeetingcount.md)
    
- [<span data-ttu-id="085b6-192">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="085b6-192">ConflictingMeetings</span></span>](conflictingmeetings.md)
    
- [<span data-ttu-id="085b6-193">位置</span><span class="sxs-lookup"><span data-stu-id="085b6-193">Location</span></span>](location.md)
    
- [<span data-ttu-id="085b6-194">持续时间 （项）</span><span class="sxs-lookup"><span data-stu-id="085b6-194">Duration (Items)</span></span>](duration-items.md)
    
- [<span data-ttu-id="085b6-195">TimeZone （项）</span><span class="sxs-lookup"><span data-stu-id="085b6-195">TimeZone (Item)</span></span>](timezone-item.md)
    
- [<span data-ttu-id="085b6-196">AppointmentSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="085b6-196">AppointmentSequenceNumber</span></span>](appointmentsequencenumber.md)
    
- [<span data-ttu-id="085b6-197">AppointmentState</span><span class="sxs-lookup"><span data-stu-id="085b6-197">AppointmentState</span></span>](appointmentstate.md)
    
## <a name="see-also"></a><span data-ttu-id="085b6-198">另请参阅</span><span class="sxs-lookup"><span data-stu-id="085b6-198">See also</span></span>



[<span data-ttu-id="085b6-199">GetItem 操作</span><span class="sxs-lookup"><span data-stu-id="085b6-199">GetItem operation</span></span>](getitem-operation.md)

