---
title: RequiredAttendees
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RequiredAttendees
api_type:
- schema
ms.assetid: 422f8d44-b0eb-49ca-af0f-0e22b54c78d2
description: RequiredAttendees 元素表示参加会议所需的与会者。
ms.openlocfilehash: a67800687f24dc323c3d80e4166ca9dd34dfc4fc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468290"
---
# <a name="requiredattendees"></a><span data-ttu-id="c4026-103">RequiredAttendees</span><span class="sxs-lookup"><span data-stu-id="c4026-103">RequiredAttendees</span></span>

<span data-ttu-id="c4026-104">**RequiredAttendees**元素表示参加会议所需的与会者。</span><span class="sxs-lookup"><span data-stu-id="c4026-104">The **RequiredAttendees** element represents attendees that are required to attend a meeting.</span></span> 
  
```xml
<RequiredAttendees>
   <Attendee/>
</RequiredAttendees>
```

 <span data-ttu-id="c4026-105">**NonEmptyArrayOfAttendeesType**</span><span class="sxs-lookup"><span data-stu-id="c4026-105">**NonEmptyArrayOfAttendeesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c4026-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c4026-106">Attributes and elements</span></span>

<span data-ttu-id="c4026-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c4026-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c4026-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="c4026-108">Attributes</span></span>

<span data-ttu-id="c4026-109">无。</span><span class="sxs-lookup"><span data-stu-id="c4026-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c4026-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c4026-110">Child elements</span></span>

|<span data-ttu-id="c4026-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="c4026-111">**Element**</span></span>|<span data-ttu-id="c4026-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="c4026-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c4026-113">与会者</span><span class="sxs-lookup"><span data-stu-id="c4026-113">Attendee</span></span>](attendee.md) <br/> |<span data-ttu-id="c4026-114">表示会议的与会者和资源。</span><span class="sxs-lookup"><span data-stu-id="c4026-114">Represents attendees and resources for a meeting.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c4026-115">父元素</span><span class="sxs-lookup"><span data-stu-id="c4026-115">Parent elements</span></span>

|<span data-ttu-id="c4026-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="c4026-116">**Element**</span></span>|<span data-ttu-id="c4026-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="c4026-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c4026-118">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="c4026-118">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="c4026-119">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="c4026-119">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="c4026-120">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="c4026-120">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="c4026-121">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="c4026-121">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c4026-122">说明</span><span class="sxs-lookup"><span data-stu-id="c4026-122">Remarks</span></span>

<span data-ttu-id="c4026-123">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c4026-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c4026-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="c4026-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c4026-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="c4026-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c4026-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="c4026-126">Schema name</span></span>  <br/> |<span data-ttu-id="c4026-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="c4026-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="c4026-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="c4026-128">Validation file</span></span>  <br/> |<span data-ttu-id="c4026-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c4026-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c4026-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="c4026-130">Can be empty</span></span>  <br/> |<span data-ttu-id="c4026-131">False</span><span class="sxs-lookup"><span data-stu-id="c4026-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c4026-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c4026-132">See also</span></span>



- [<span data-ttu-id="c4026-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c4026-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

