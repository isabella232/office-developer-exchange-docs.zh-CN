---
title: OptionalAttendees
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OptionalAttendees
api_type:
- schema
ms.assetid: e7c80c4d-3794-45e9-986f-6a8a687df0a4
description: OptionalAttendees 元素表示无需参加会议的与会者。
ms.openlocfilehash: 9eeff7151042f26fe5b00b43ec16a27946680a9f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468171"
---
# <a name="optionalattendees"></a><span data-ttu-id="5411f-103">OptionalAttendees</span><span class="sxs-lookup"><span data-stu-id="5411f-103">OptionalAttendees</span></span>

<span data-ttu-id="5411f-104">**OptionalAttendees**元素表示无需参加会议的与会者。</span><span class="sxs-lookup"><span data-stu-id="5411f-104">The **OptionalAttendees** element represents attendees who are not required to attend a meeting.</span></span> 
  
```xml
<OptionalAttendees>
   <Attendee/>
</OptionalAttendees>
```

 <span data-ttu-id="5411f-105">**NonEmptyArrayOfAttendeesType**</span><span class="sxs-lookup"><span data-stu-id="5411f-105">**NonEmptyArrayOfAttendeesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5411f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5411f-106">Attributes and elements</span></span>

<span data-ttu-id="5411f-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5411f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5411f-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="5411f-108">Attributes</span></span>

<span data-ttu-id="5411f-109">无。</span><span class="sxs-lookup"><span data-stu-id="5411f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5411f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="5411f-110">Child elements</span></span>

|<span data-ttu-id="5411f-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="5411f-111">**Element**</span></span>|<span data-ttu-id="5411f-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="5411f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5411f-113">与会者</span><span class="sxs-lookup"><span data-stu-id="5411f-113">Attendee</span></span>](attendee.md) <br/> |<span data-ttu-id="5411f-114">表示会议的与会者和资源。</span><span class="sxs-lookup"><span data-stu-id="5411f-114">Represents attendees and resources for a meeting.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5411f-115">父元素</span><span class="sxs-lookup"><span data-stu-id="5411f-115">Parent elements</span></span>

|<span data-ttu-id="5411f-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="5411f-116">**Element**</span></span>|<span data-ttu-id="5411f-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="5411f-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5411f-118">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="5411f-118">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="5411f-119">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="5411f-119">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="5411f-120">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="5411f-120">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="5411f-121">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="5411f-121">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5411f-122">说明</span><span class="sxs-lookup"><span data-stu-id="5411f-122">Remarks</span></span>

<span data-ttu-id="5411f-123">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="5411f-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5411f-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="5411f-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5411f-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="5411f-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5411f-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="5411f-126">Schema name</span></span>  <br/> |<span data-ttu-id="5411f-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="5411f-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="5411f-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="5411f-128">Validation file</span></span>  <br/> |<span data-ttu-id="5411f-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5411f-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5411f-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="5411f-130">Can be empty</span></span>  <br/> |<span data-ttu-id="5411f-131">False</span><span class="sxs-lookup"><span data-stu-id="5411f-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5411f-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5411f-132">See also</span></span>



- [<span data-ttu-id="5411f-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="5411f-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

