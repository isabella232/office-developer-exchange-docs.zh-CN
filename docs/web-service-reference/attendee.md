---
title: 与会者
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Attendee
api_type:
- schema
ms.assetid: 393c3d7e-7416-458a-b976-270b88eaaa03
description: "\"与会者\" 元素表示会议的与会者和资源。"
ms.openlocfilehash: f376e59b27017e0a9d27692cb1a4ae759cd1af0e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457646"
---
# <a name="attendee"></a><span data-ttu-id="a3ed5-103">与会者</span><span class="sxs-lookup"><span data-stu-id="a3ed5-103">Attendee</span></span>

<span data-ttu-id="a3ed5-104">"**与会者**" 元素表示会议的与会者和资源。</span><span class="sxs-lookup"><span data-stu-id="a3ed5-104">The **Attendee** element represents attendees and resources for a meeting.</span></span> 
  
```xml
<Attendee>
   <Mailbox/>
   <ResponseType/>
   <LastResponseTime/>
</Attendee>
```

 <span data-ttu-id="a3ed5-105">**AttendeeType**</span><span class="sxs-lookup"><span data-stu-id="a3ed5-105">**AttendeeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a3ed5-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a3ed5-106">Attributes and elements</span></span>

<span data-ttu-id="a3ed5-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a3ed5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a3ed5-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="a3ed5-108">Attributes</span></span>

<span data-ttu-id="a3ed5-109">无。</span><span class="sxs-lookup"><span data-stu-id="a3ed5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a3ed5-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a3ed5-110">Child elements</span></span>

|<span data-ttu-id="a3ed5-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="a3ed5-111">**Element**</span></span>|<span data-ttu-id="a3ed5-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="a3ed5-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a3ed5-113">Mailbox</span><span class="sxs-lookup"><span data-stu-id="a3ed5-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="a3ed5-114">标识完全解析的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="a3ed5-114">Identifies a fully resolved e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="a3ed5-115">ResponseType</span><span class="sxs-lookup"><span data-stu-id="a3ed5-115">ResponseType</span></span>](responsetype.md) <br/> |<span data-ttu-id="a3ed5-116">表示接收会议的收件人响应的类型。</span><span class="sxs-lookup"><span data-stu-id="a3ed5-116">Represents the type of recipient response that is received for a meeting.</span></span> <span data-ttu-id="a3ed5-117">此属性仅与会议组织者的日历项目相关。</span><span class="sxs-lookup"><span data-stu-id="a3ed5-117">This property is only relevant to a meeting organizer's calendar item.</span></span>  <br/> |
|[<span data-ttu-id="a3ed5-118">LastResponseTime</span><span class="sxs-lookup"><span data-stu-id="a3ed5-118">LastResponseTime</span></span>](lastresponsetime.md) <br/> |<span data-ttu-id="a3ed5-119">表示收到的最新响应的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="a3ed5-119">Represents the date and time of the latest response that is received.</span></span>  <br/> |
|[<span data-ttu-id="a3ed5-120">ProposedStart</span><span class="sxs-lookup"><span data-stu-id="a3ed5-120">ProposedStart</span></span>](proposedstart-attendeetype.md) <br/> |<span data-ttu-id="a3ed5-121">表示与会者为会议建议的开始时间。</span><span class="sxs-lookup"><span data-stu-id="a3ed5-121">Represents an attendee's proposed start time for a meeting.</span></span> <br/> |
|[<span data-ttu-id="a3ed5-122">ProposedEnd</span><span class="sxs-lookup"><span data-stu-id="a3ed5-122">ProposedEnd</span></span>](proposedend-attendeetype.md) <br/> |<span data-ttu-id="a3ed5-123">表示与会者为会议建议的结束时间。</span><span class="sxs-lookup"><span data-stu-id="a3ed5-123">Represents an attendee's proposed end time for a meeting.</span></span> <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a3ed5-124">父元素</span><span class="sxs-lookup"><span data-stu-id="a3ed5-124">Parent elements</span></span>

|<span data-ttu-id="a3ed5-125">**元素**</span><span class="sxs-lookup"><span data-stu-id="a3ed5-125">**Element**</span></span>|<span data-ttu-id="a3ed5-126">**说明**</span><span class="sxs-lookup"><span data-stu-id="a3ed5-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a3ed5-127">RequiredAttendees</span><span class="sxs-lookup"><span data-stu-id="a3ed5-127">RequiredAttendees</span></span>](requiredattendees.md) <br/> |<span data-ttu-id="a3ed5-128">表示参加会议所需的与会者。</span><span class="sxs-lookup"><span data-stu-id="a3ed5-128">Represents attendees that are required to attend a meeting.</span></span>  <br/> |
|[<span data-ttu-id="a3ed5-129">OptionalAttendees</span><span class="sxs-lookup"><span data-stu-id="a3ed5-129">OptionalAttendees</span></span>](optionalattendees.md) <br/> |<span data-ttu-id="a3ed5-130">表示参加会议不需要的与会者。</span><span class="sxs-lookup"><span data-stu-id="a3ed5-130">Represents attendees that are not required to attend a meeting.</span></span>  <br/> |
|[<span data-ttu-id="a3ed5-131">资源</span><span class="sxs-lookup"><span data-stu-id="a3ed5-131">Resources</span></span>](resources.md) <br/> |<span data-ttu-id="a3ed5-132">表示会议的计划资源。</span><span class="sxs-lookup"><span data-stu-id="a3ed5-132">Represents a scheduled resource for a meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a3ed5-133">说明</span><span class="sxs-lookup"><span data-stu-id="a3ed5-133">Remarks</span></span>

<span data-ttu-id="a3ed5-134">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a3ed5-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a3ed5-135">元素信息</span><span class="sxs-lookup"><span data-stu-id="a3ed5-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a3ed5-136">命名空间</span><span class="sxs-lookup"><span data-stu-id="a3ed5-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a3ed5-137">架构名称</span><span class="sxs-lookup"><span data-stu-id="a3ed5-137">Schema name</span></span>  <br/> |<span data-ttu-id="a3ed5-138">类型架构</span><span class="sxs-lookup"><span data-stu-id="a3ed5-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="a3ed5-139">验证文件</span><span class="sxs-lookup"><span data-stu-id="a3ed5-139">Validation file</span></span>  <br/> |<span data-ttu-id="a3ed5-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a3ed5-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a3ed5-141">可以为空</span><span class="sxs-lookup"><span data-stu-id="a3ed5-141">Can be empty</span></span>  <br/> |<span data-ttu-id="a3ed5-142">False</span><span class="sxs-lookup"><span data-stu-id="a3ed5-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a3ed5-143">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a3ed5-143">See also</span></span>

- [<span data-ttu-id="a3ed5-144">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a3ed5-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

