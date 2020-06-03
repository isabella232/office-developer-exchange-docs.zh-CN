---
title: GetUserAvailabilityResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetUserAvailabilityResponse
api_type:
- schema
ms.assetid: 6999510a-d60e-43da-8964-57b5fb3e9d11
description: GetUserAvailabilityResponse 元素是根元素，其中包含用于定义用户可用性信息或建议的会议时间信息的属性。
ms.openlocfilehash: ceb24bc8b31a7d7313add213c26bef5efd3c89ae
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458213"
---
# <a name="getuseravailabilityresponse"></a><span data-ttu-id="9a3ef-103">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="9a3ef-103">GetUserAvailabilityResponse</span></span>

<span data-ttu-id="9a3ef-104">**GetUserAvailabilityResponse**元素是根元素，其中包含用于定义用户可用性信息或建议的会议时间信息的属性。</span><span class="sxs-lookup"><span data-stu-id="9a3ef-104">The **GetUserAvailabilityResponse** element is the root element that contains the properties that define user availability information or suggested meeting time information.</span></span> 
  
```xml
<GetUserAvailabilityResponse>
   <FreeBusyResponseArray>...</FreeBusyResponseArray>
   <SuggestionsResponse>...</SuggestionsResponse>
</GetUserAvailabilityResponse>
```

 <span data-ttu-id="9a3ef-105">**GetUserAvailabilityResponseType**</span><span class="sxs-lookup"><span data-stu-id="9a3ef-105">**GetUserAvailabilityResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9a3ef-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9a3ef-106">Attributes and elements</span></span>

<span data-ttu-id="9a3ef-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9a3ef-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9a3ef-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="9a3ef-108">Attributes</span></span>

<span data-ttu-id="9a3ef-109">无。</span><span class="sxs-lookup"><span data-stu-id="9a3ef-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9a3ef-110">子元素</span><span class="sxs-lookup"><span data-stu-id="9a3ef-110">Child elements</span></span>

|<span data-ttu-id="9a3ef-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="9a3ef-111">**Element**</span></span>|<span data-ttu-id="9a3ef-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="9a3ef-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9a3ef-113">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="9a3ef-113">FreeBusyResponseArray</span></span>](freebusyresponsearray.md) <br/> |<span data-ttu-id="9a3ef-114">包含请求的用户的可用性信息和响应状态。</span><span class="sxs-lookup"><span data-stu-id="9a3ef-114">Contains the requested users' availability information and the response status.</span></span>  <br/> |
|[<span data-ttu-id="9a3ef-115">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="9a3ef-115">SuggestionsResponse</span></span>](suggestionsresponse.md) <br/> |<span data-ttu-id="9a3ef-116">包含请求的会议建议的响应状态信息和建议数据。</span><span class="sxs-lookup"><span data-stu-id="9a3ef-116">Contains response status information and suggestion data for requested meeting suggestions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9a3ef-117">父元素</span><span class="sxs-lookup"><span data-stu-id="9a3ef-117">Parent elements</span></span>

<span data-ttu-id="9a3ef-118">无。</span><span class="sxs-lookup"><span data-stu-id="9a3ef-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9a3ef-119">说明</span><span class="sxs-lookup"><span data-stu-id="9a3ef-119">Remarks</span></span>

<span data-ttu-id="9a3ef-120">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9a3ef-120">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="9a3ef-121">示例</span><span class="sxs-lookup"><span data-stu-id="9a3ef-121">Example</span></span>

<span data-ttu-id="9a3ef-122">以下示例的 GetUserAvailability 响应显示对 GetUserAvailability 请求的响应。</span><span class="sxs-lookup"><span data-stu-id="9a3ef-122">The following example of a GetUserAvailability response shows a response to a GetUserAvailability request.</span></span>
  
```
<?xml version="1.0" encoding="utf-8" ?>
<GetUserAvailabilityResponse xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
                             xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <FreeBusyResponseArray xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
    <FreeBusyResponse>
      <ResponseMessage ResponseClass="Success">
        <Path select="/m:GetUserAvailabilityRequest/MailboxDataArray[0]" />
      </ResponseMessage>
      <FreeBusyView>
        <FreeBusyViewType xmlns="https://schemas.microsoft.com/exchange/services/2006/types">Detailed</FreeBusyViewType>
        <CalendarEventArray xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <CalendarEvent>
            <StartTime>2006-02-28T19:00:00-08:00</StartTime>
            <EndTime>2006-02-28T23:30:00-08:00</EndTime>
            <BusyType>OOF</BusyType>
            <IsPrivate>false</IsPrivate>
            <CalendarEventDetails>
              <ID>00000</ID>
              <Subject>Exercise</Subject>
              <Location>the gym</Location>
              <IsMeeting>false</IsMeeting>
              <IsRecurring>false</IsRecurring>
              <IsException>false</IsException>
              <IsReminderSet>true</IsReminderSet>
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
  </FreeBusyResponseArray>
</GetUserAvailabilityResponse>
```

<span data-ttu-id="9a3ef-123">[ID](id.md)元素内容被缩短以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="9a3ef-123">The [ID](id.md) element contents were shortened to preserve readability.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="9a3ef-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="9a3ef-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9a3ef-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="9a3ef-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9a3ef-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="9a3ef-126">Schema Name</span></span>  <br/> |<span data-ttu-id="9a3ef-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="9a3ef-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9a3ef-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="9a3ef-128">Validation File</span></span>  <br/> |<span data-ttu-id="9a3ef-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9a3ef-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9a3ef-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="9a3ef-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="9a3ef-131">False</span><span class="sxs-lookup"><span data-stu-id="9a3ef-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9a3ef-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9a3ef-132">See also</span></span>



[<span data-ttu-id="9a3ef-133">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="9a3ef-133">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)


[<span data-ttu-id="9a3ef-134">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="9a3ef-134">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

