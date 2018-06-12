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
description: GetUserAvailabilityRequest 元素包含用于获取用户的可用性信息的参数。 这是根元素。
ms.openlocfilehash: 5440f739b09bfbe27ad97cba99c08756686594f7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825683"
---
# <a name="getuseravailabilityrequest"></a><span data-ttu-id="5c975-104">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="5c975-104">GetUserAvailabilityRequest</span></span>

<span data-ttu-id="5c975-105">**GetUserAvailabilityRequest**元素包含用于获取用户的可用性信息的参数。</span><span class="sxs-lookup"><span data-stu-id="5c975-105">The **GetUserAvailabilityRequest** element contains the arguments used to obtain user availability information.</span></span> <span data-ttu-id="5c975-106">这是根元素。</span><span class="sxs-lookup"><span data-stu-id="5c975-106">This is a root element.</span></span> 
  
```xml
<GetUserAvailabilityRequest>
   <TimeZone>...</TimeZone>
   <MailboxDataArray>...</MailboxDataArray>
   <FreeBusyViewOptions>...</FreeBusyViewOptions>
   <SuggestionsViewOptions>...</SuggestionsViewOptions>
</GetUserAvailabilityRequest>
```

 <span data-ttu-id="5c975-107">**GetUserAvailabilityRequestType**</span><span class="sxs-lookup"><span data-stu-id="5c975-107">**GetUserAvailabilityRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5c975-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5c975-108">Attributes and elements</span></span>

<span data-ttu-id="5c975-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5c975-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5c975-110">属性</span><span class="sxs-lookup"><span data-stu-id="5c975-110">Attributes</span></span>

<span data-ttu-id="5c975-111">无。</span><span class="sxs-lookup"><span data-stu-id="5c975-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5c975-112">子元素</span><span class="sxs-lookup"><span data-stu-id="5c975-112">Child elements</span></span>

|<span data-ttu-id="5c975-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="5c975-113">**Element**</span></span>|<span data-ttu-id="5c975-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="5c975-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5c975-115">TimeZone （可用性）</span><span class="sxs-lookup"><span data-stu-id="5c975-115">TimeZone (Availability)</span></span>](timezone-availability.md) <br/> |<span data-ttu-id="5c975-116">包含标识时区信息的元素。</span><span class="sxs-lookup"><span data-stu-id="5c975-116">Contains elements that identify time zone information.</span></span> <span data-ttu-id="5c975-117">此元素还包含有关标准时间和夏时制之间的转换的信息。</span><span class="sxs-lookup"><span data-stu-id="5c975-117">This element also contains information about the transition between standard time and daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="5c975-118">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="5c975-118">MailboxDataArray</span></span>](mailboxdataarray.md) <br/> |<span data-ttu-id="5c975-119">包含要查询的可用性信息的邮箱列表。</span><span class="sxs-lookup"><span data-stu-id="5c975-119">Contains a list of mailboxes to query for availability information.</span></span>  <br/> |
|[<span data-ttu-id="5c975-120">FreeBusyViewOptions</span><span class="sxs-lookup"><span data-stu-id="5c975-120">FreeBusyViewOptions</span></span>](freebusyviewoptions.md) <br/> |<span data-ttu-id="5c975-121">指定响应中返回的忙/闲信息的类型。</span><span class="sxs-lookup"><span data-stu-id="5c975-121">Specifies the type of free/busy information returned in the response.</span></span>  <br/> |
|[<span data-ttu-id="5c975-122">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="5c975-122">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md) <br/> |<span data-ttu-id="5c975-123">包含选项的获取会议建议信息。</span><span class="sxs-lookup"><span data-stu-id="5c975-123">Contains the options for obtaining meeting suggestion information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5c975-124">父元素</span><span class="sxs-lookup"><span data-stu-id="5c975-124">Parent elements</span></span>

<span data-ttu-id="5c975-125">无。</span><span class="sxs-lookup"><span data-stu-id="5c975-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5c975-126">备注</span><span class="sxs-lookup"><span data-stu-id="5c975-126">Remarks</span></span>

<span data-ttu-id="5c975-127">描述此元素的架构位于运行 Microsoft Exchange Server 2007 的安装了客户端访问服务器角色的计算机的 /EWS/ 目录中。</span><span class="sxs-lookup"><span data-stu-id="5c975-127">The schema that describes this element is located in the /EWS/ directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="5c975-128">示例</span><span class="sxs-lookup"><span data-stu-id="5c975-128">Example</span></span>

<span data-ttu-id="5c975-129">下面的示例演示忙/闲信息的请求。</span><span class="sxs-lookup"><span data-stu-id="5c975-129">The following example shows a request for free/busy information.</span></span>
  
```
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetUserAvailabilityRequest xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <TimeZone xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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
        <MailboxData xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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
      <FreeBusyViewOptions xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="element-information"></a><span data-ttu-id="5c975-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="5c975-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5c975-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="5c975-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5c975-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="5c975-132">Schema Name</span></span>  <br/> |<span data-ttu-id="5c975-133">消息架构</span><span class="sxs-lookup"><span data-stu-id="5c975-133">Messages schema</span></span>  <br/> |
|<span data-ttu-id="5c975-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="5c975-134">Validation File</span></span>  <br/> |<span data-ttu-id="5c975-135">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="5c975-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5c975-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="5c975-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="5c975-137">False</span><span class="sxs-lookup"><span data-stu-id="5c975-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5c975-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5c975-138">See also</span></span>



[<span data-ttu-id="5c975-139">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="5c975-139">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="5c975-140">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="5c975-140">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="5c975-141">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="5c975-141">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

