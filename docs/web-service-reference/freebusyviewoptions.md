---
title: FreeBusyViewOptions
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FreeBusyViewOptions
api_type:
- schema
ms.assetid: c07f3ddb-874b-4d30-a60e-7e5c7793bb6f
description: FreeBusyViewOptions 元素指定的响应中返回的忙/闲信息的类型。
ms.openlocfilehash: 703fc6a3625d24cf874a785600e13ee4505b506f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754431"
---
# <a name="freebusyviewoptions"></a><span data-ttu-id="1a2c2-103">FreeBusyViewOptions</span><span class="sxs-lookup"><span data-stu-id="1a2c2-103">FreeBusyViewOptions</span></span>

<span data-ttu-id="1a2c2-104">**FreeBusyViewOptions**元素指定的响应中返回的忙/闲信息的类型。</span><span class="sxs-lookup"><span data-stu-id="1a2c2-104">The **FreeBusyViewOptions** element specifies the type of free/busy information returned in the response.</span></span> 
  
[<span data-ttu-id="1a2c2-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="1a2c2-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="1a2c2-106">FreeBusyViewOptions</span><span class="sxs-lookup"><span data-stu-id="1a2c2-106">FreeBusyViewOptions</span></span>](freebusyviewoptions.md)
  
```xml
<FreeBusyViewOptions>
   <TimeWindow>...</TimeWindow>
   <MergedFreeBusyIntervalInMinutes>...</MergedFreeBusyIntervalInMinutes>
<RequestedView>...</RequestedView>
</FreeBusyViewOptions>

```

 <span data-ttu-id="1a2c2-107">**FreeBusyViewOptionsType**</span><span class="sxs-lookup"><span data-stu-id="1a2c2-107">**FreeBusyViewOptionsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1a2c2-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1a2c2-108">Attributes and elements</span></span>

<span data-ttu-id="1a2c2-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1a2c2-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1a2c2-110">属性</span><span class="sxs-lookup"><span data-stu-id="1a2c2-110">Attributes</span></span>

<span data-ttu-id="1a2c2-111">无。</span><span class="sxs-lookup"><span data-stu-id="1a2c2-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1a2c2-112">子元素</span><span class="sxs-lookup"><span data-stu-id="1a2c2-112">Child elements</span></span>

|<span data-ttu-id="1a2c2-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="1a2c2-113">**Element**</span></span>|<span data-ttu-id="1a2c2-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="1a2c2-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1a2c2-115">TimeWindow</span><span class="sxs-lookup"><span data-stu-id="1a2c2-115">TimeWindow</span></span>](timewindow.md) <br/> |<span data-ttu-id="1a2c2-116">标识查询的用户的可用性信息的时间跨度。</span><span class="sxs-lookup"><span data-stu-id="1a2c2-116">Identifies the time span queried for the user availability information.</span></span>  <br/> |
|[<span data-ttu-id="1a2c2-117">MergedFreeBusyIntervalInMinutes</span><span class="sxs-lookup"><span data-stu-id="1a2c2-117">MergedFreeBusyIntervalInMinutes</span></span>](mergedfreebusyintervalinminutes.md) <br/> |<span data-ttu-id="1a2c2-118">代表**FreeBusyMerged**视图中的两个连续插槽之间的时间差异。</span><span class="sxs-lookup"><span data-stu-id="1a2c2-118">Represents the time difference between two successive slots in the **FreeBusyMerged** view.</span></span>  <br/> |
|[<span data-ttu-id="1a2c2-119">RequestedView</span><span class="sxs-lookup"><span data-stu-id="1a2c2-119">RequestedView</span></span>](requestedview.md) <br/> |<span data-ttu-id="1a2c2-120">定义的客户端请求的日历信息的类型。</span><span class="sxs-lookup"><span data-stu-id="1a2c2-120">Defines the type of calendar information that a client requests.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1a2c2-121">父元素</span><span class="sxs-lookup"><span data-stu-id="1a2c2-121">Parent elements</span></span>

|<span data-ttu-id="1a2c2-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="1a2c2-122">**Element**</span></span>|<span data-ttu-id="1a2c2-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="1a2c2-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1a2c2-124">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="1a2c2-124">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md) <br/> |<span data-ttu-id="1a2c2-125">包含用于获取用户的可用性信息的参数。</span><span class="sxs-lookup"><span data-stu-id="1a2c2-125">Contains the arguments used to obtain user availability information.</span></span> <span data-ttu-id="1a2c2-126">这是根元素。</span><span class="sxs-lookup"><span data-stu-id="1a2c2-126">This is a root element.</span></span>  <br/> <span data-ttu-id="1a2c2-127">以下是此元素的 XPath:</span><span class="sxs-lookup"><span data-stu-id="1a2c2-127">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1a2c2-128">备注</span><span class="sxs-lookup"><span data-stu-id="1a2c2-128">Remarks</span></span>

<span data-ttu-id="1a2c2-129">此元素不需要，并且如果使用可以只发生一次。</span><span class="sxs-lookup"><span data-stu-id="1a2c2-129">This element is not required and can only occur once if used.</span></span> <span data-ttu-id="1a2c2-130">如果[SuggestionsViewOptions](suggestionsviewoptions.md)元素的值不为 null，则此值可以是 null。</span><span class="sxs-lookup"><span data-stu-id="1a2c2-130">This value can be null if the value of the [SuggestionsViewOptions](suggestionsviewoptions.md) element is not null.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1a2c2-131">描述此元素的架构位于运行 Microsoft® Exchange Server 2007 的安装了客户端访问服务器角色的计算机的 /epi/ 目录中。</span><span class="sxs-lookup"><span data-stu-id="1a2c2-131">The schema that describes this element is located in the /epi/ directory of the computer that is running Microsoft® Exchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="example"></a><span data-ttu-id="1a2c2-132">示例</span><span class="sxs-lookup"><span data-stu-id="1a2c2-132">Example</span></span>

<span data-ttu-id="1a2c2-133">下面的示例获取会议和 60 分钟的间隔中的忙/闲流的列表。</span><span class="sxs-lookup"><span data-stu-id="1a2c2-133">The following example obtains a list of meetings and a free/busy stream in 60-minute intervals.</span></span>
  
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
            <Address>someone@ExServer.example.com</Address>
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
          <EndTime>2006-02-25T23:59:59</EndTime>
        </TimeWindow>
        <MergedFreeBusyIntervalInMinutes>60</MergedFreeBusyIntervalInMinutes>
        <RequestedView>FreeBusyMerged</RequestedView>
      </FreeBusyViewOptions>
    </GetUserAvailabilityRequest>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a><span data-ttu-id="1a2c2-134">元素信息</span><span class="sxs-lookup"><span data-stu-id="1a2c2-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1a2c2-135">命名空间</span><span class="sxs-lookup"><span data-stu-id="1a2c2-135">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1a2c2-136">架构名称</span><span class="sxs-lookup"><span data-stu-id="1a2c2-136">Schema Name</span></span>  <br/> |<span data-ttu-id="1a2c2-137">类型架构</span><span class="sxs-lookup"><span data-stu-id="1a2c2-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="1a2c2-138">验证文件</span><span class="sxs-lookup"><span data-stu-id="1a2c2-138">Validation File</span></span>  <br/> |<span data-ttu-id="1a2c2-139">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1a2c2-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1a2c2-140">可以为空</span><span class="sxs-lookup"><span data-stu-id="1a2c2-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="1a2c2-141">False</span><span class="sxs-lookup"><span data-stu-id="1a2c2-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1a2c2-142">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1a2c2-142">See also</span></span>



[<span data-ttu-id="1a2c2-143">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="1a2c2-143">GetUserAvailability operation</span></span>](getuseravailability-operation.md)


[<span data-ttu-id="1a2c2-144">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="1a2c2-144">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

