---
title: GetUserAvailabilityRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetUserAvailabilityRequest
api_type:
- schema
ms.assetid: 7906711b-80a1-42ae-8b33-26eeac036a5a
description: GetUserAvailabilityRequest 元素包含用于获取用户可用性信息的参数。 这是一个根元素。
ms.openlocfilehash: 6c2e2c5452b6379171e49cf6aea2d437152ecb9b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459116"
---
# <a name="getuseravailabilityrequest"></a><span data-ttu-id="dbcb1-104">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="dbcb1-104">GetUserAvailabilityRequest</span></span>

<span data-ttu-id="dbcb1-105">**GetUserAvailabilityRequest**元素包含用于获取用户可用性信息的参数。</span><span class="sxs-lookup"><span data-stu-id="dbcb1-105">The **GetUserAvailabilityRequest** element contains the arguments used to obtain user availability information.</span></span> <span data-ttu-id="dbcb1-106">这是一个根元素。</span><span class="sxs-lookup"><span data-stu-id="dbcb1-106">This is a root element.</span></span> 
  
```xml
<GetUserAvailabilityRequest>
   <TimeZone>...</TimeZone>
   <MailboxDataArray>...</MailboxDataArray>
   <FreeBusyViewOptions>...</FreeBusyViewOptions>
   <SuggestionsViewOptions>...</SuggestionsViewOptions>
</GetUserAvailabilityRequest>
```

 <span data-ttu-id="dbcb1-107">**GetUserAvailabilityRequestType**</span><span class="sxs-lookup"><span data-stu-id="dbcb1-107">**GetUserAvailabilityRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dbcb1-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="dbcb1-108">Attributes and elements</span></span>

<span data-ttu-id="dbcb1-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="dbcb1-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dbcb1-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="dbcb1-110">Attributes</span></span>

<span data-ttu-id="dbcb1-111">无。</span><span class="sxs-lookup"><span data-stu-id="dbcb1-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dbcb1-112">子元素</span><span class="sxs-lookup"><span data-stu-id="dbcb1-112">Child elements</span></span>

|<span data-ttu-id="dbcb1-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="dbcb1-113">**Element**</span></span>|<span data-ttu-id="dbcb1-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="dbcb1-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dbcb1-115">时区（可用性）</span><span class="sxs-lookup"><span data-stu-id="dbcb1-115">TimeZone (Availability)</span></span>](timezone-availability.md) <br/> |<span data-ttu-id="dbcb1-116">包含标识时区信息的元素。</span><span class="sxs-lookup"><span data-stu-id="dbcb1-116">Contains elements that identify time zone information.</span></span> <span data-ttu-id="dbcb1-117">此元素还包含有关标准时间和夏时制之间转换的信息。</span><span class="sxs-lookup"><span data-stu-id="dbcb1-117">This element also contains information about the transition between standard time and daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="dbcb1-118">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="dbcb1-118">MailboxDataArray</span></span>](mailboxdataarray.md) <br/> |<span data-ttu-id="dbcb1-119">包含要查询可用性信息的邮箱的列表。</span><span class="sxs-lookup"><span data-stu-id="dbcb1-119">Contains a list of mailboxes to query for availability information.</span></span>  <br/> |
|[<span data-ttu-id="dbcb1-120">FreeBusyViewOptions</span><span class="sxs-lookup"><span data-stu-id="dbcb1-120">FreeBusyViewOptions</span></span>](freebusyviewoptions.md) <br/> |<span data-ttu-id="dbcb1-121">指定响应中返回的忙/闲信息的类型。</span><span class="sxs-lookup"><span data-stu-id="dbcb1-121">Specifies the type of free/busy information returned in the response.</span></span>  <br/> |
|[<span data-ttu-id="dbcb1-122">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="dbcb1-122">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md) <br/> |<span data-ttu-id="dbcb1-123">包含用于获取会议建议信息的选项。</span><span class="sxs-lookup"><span data-stu-id="dbcb1-123">Contains the options for obtaining meeting suggestion information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="dbcb1-124">父元素</span><span class="sxs-lookup"><span data-stu-id="dbcb1-124">Parent elements</span></span>

<span data-ttu-id="dbcb1-125">无。</span><span class="sxs-lookup"><span data-stu-id="dbcb1-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dbcb1-126">说明</span><span class="sxs-lookup"><span data-stu-id="dbcb1-126">Remarks</span></span>

<span data-ttu-id="dbcb1-127">描述此元素的架构位于运行 Microsoft Exchange Server 2007 且安装了客户端访问服务器角色的计算机的/EWS/目录中。</span><span class="sxs-lookup"><span data-stu-id="dbcb1-127">The schema that describes this element is located in the /EWS/ directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="dbcb1-128">示例</span><span class="sxs-lookup"><span data-stu-id="dbcb1-128">Example</span></span>

<span data-ttu-id="dbcb1-129">以下示例显示忙/闲信息的请求。</span><span class="sxs-lookup"><span data-stu-id="dbcb1-129">The following example shows a request for free/busy information.</span></span>
  
```
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetUserAvailabilityRequest xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <TimeZone xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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
      <MailboxDataArray>
        <MailboxData xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <Email>
            <Name></Name>
            <Address>someone@exchangeserver.example.com</Address>
            <RoutingType>SMTP</RoutingType>
          </Email>
          <AttendeeType>Organizer</AttendeeType>
          <ExcludeConflicts>false</ExcludeConflicts>
          <ExcludeNonWorkingHours>false</ExcludeNonWorkingHours>
        </MailboxData>
      </MailboxDataArray>
      <FreeBusyViewOptions xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
        <TimeWindow>
          <StartTime>2006-02-06T00:00:00</StartTime>
          <EndTime>2006-02-30T23:59:59</EndTime>
        </TimeWindow>
        <MergedFreeBusyIntervalInMinutes>60</MergedFreeBusyIntervalInMinutes>
        <RequestedView>FreeBusyMerged</RequestedView>
      </FreeBusyViewOptions>
    </GetUserAvailabilityRequest>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a><span data-ttu-id="dbcb1-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="dbcb1-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dbcb1-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="dbcb1-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="dbcb1-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="dbcb1-132">Schema Name</span></span>  <br/> |<span data-ttu-id="dbcb1-133">消息架构</span><span class="sxs-lookup"><span data-stu-id="dbcb1-133">Messages schema</span></span>  <br/> |
|<span data-ttu-id="dbcb1-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="dbcb1-134">Validation File</span></span>  <br/> |<span data-ttu-id="dbcb1-135">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="dbcb1-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="dbcb1-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="dbcb1-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="dbcb1-137">False</span><span class="sxs-lookup"><span data-stu-id="dbcb1-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dbcb1-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="dbcb1-138">See also</span></span>



[<span data-ttu-id="dbcb1-139">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="dbcb1-139">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="dbcb1-140">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="dbcb1-140">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="dbcb1-141">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="dbcb1-141">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

