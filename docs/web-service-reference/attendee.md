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
description: Attendee 元素均表示与会者和会议的资源。
ms.openlocfilehash: 60cb0839c2f6de69b833c11f4594d40c14cd8887
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753283"
---
# <a name="attendee"></a><span data-ttu-id="d864b-103">与会者</span><span class="sxs-lookup"><span data-stu-id="d864b-103">Attendee</span></span>

<span data-ttu-id="d864b-104">**Attendee**元素均表示与会者和会议的资源。</span><span class="sxs-lookup"><span data-stu-id="d864b-104">The **Attendee** element represents attendees and resources for a meeting.</span></span> 
  
```xml
<Attendee>
   <Mailbox/>
   <ResponseType/>
   <LastResponseTime/>
</Attendee>
```

 <span data-ttu-id="d864b-105">**AttendeeType**</span><span class="sxs-lookup"><span data-stu-id="d864b-105">**AttendeeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d864b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d864b-106">Attributes and elements</span></span>

<span data-ttu-id="d864b-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d864b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d864b-108">属性</span><span class="sxs-lookup"><span data-stu-id="d864b-108">Attributes</span></span>

<span data-ttu-id="d864b-109">无。</span><span class="sxs-lookup"><span data-stu-id="d864b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d864b-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d864b-110">Child elements</span></span>

|<span data-ttu-id="d864b-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="d864b-111">**Element**</span></span>|<span data-ttu-id="d864b-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="d864b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d864b-113">Mailbox</span><span class="sxs-lookup"><span data-stu-id="d864b-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="d864b-114">标识完全解析电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="d864b-114">Identifies a fully resolved e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="d864b-115">ResponseType</span><span class="sxs-lookup"><span data-stu-id="d864b-115">ResponseType</span></span>](responsetype.md) <br/> |<span data-ttu-id="d864b-116">代表收到会议的收件人响应的类型。</span><span class="sxs-lookup"><span data-stu-id="d864b-116">Represents the type of recipient response that is received for a meeting.</span></span> <span data-ttu-id="d864b-117">此属性才与会议组织者的日历项目相关。</span><span class="sxs-lookup"><span data-stu-id="d864b-117">This property is only relevant to a meeting organizer's calendar item.</span></span>  <br/> |
|[<span data-ttu-id="d864b-118">LastResponseTime</span><span class="sxs-lookup"><span data-stu-id="d864b-118">LastResponseTime</span></span>](lastresponsetime.md) <br/> |<span data-ttu-id="d864b-119">表示的日期和最新收到的响应的时间。</span><span class="sxs-lookup"><span data-stu-id="d864b-119">Represents the date and time of the latest response that is received.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d864b-120">父元素</span><span class="sxs-lookup"><span data-stu-id="d864b-120">Parent elements</span></span>

|<span data-ttu-id="d864b-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="d864b-121">**Element**</span></span>|<span data-ttu-id="d864b-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="d864b-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d864b-123">RequiredAttendees</span><span class="sxs-lookup"><span data-stu-id="d864b-123">RequiredAttendees</span></span>](requiredattendees.md) <br/> |<span data-ttu-id="d864b-124">代表需要参加会议的与会者。</span><span class="sxs-lookup"><span data-stu-id="d864b-124">Represents attendees that are required to attend a meeting.</span></span>  <br/> |
|[<span data-ttu-id="d864b-125">OptionalAttendees</span><span class="sxs-lookup"><span data-stu-id="d864b-125">OptionalAttendees</span></span>](optionalattendees.md) <br/> |<span data-ttu-id="d864b-126">表示无需参加会议的与会者。</span><span class="sxs-lookup"><span data-stu-id="d864b-126">Represents attendees that are not required to attend a meeting.</span></span>  <br/> |
|[<span data-ttu-id="d864b-127">资源</span><span class="sxs-lookup"><span data-stu-id="d864b-127">Resources</span></span>](resources.md) <br/> |<span data-ttu-id="d864b-128">表示会议的计划的资源。</span><span class="sxs-lookup"><span data-stu-id="d864b-128">Represents a scheduled resource for a meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d864b-129">备注</span><span class="sxs-lookup"><span data-stu-id="d864b-129">Remarks</span></span>

<span data-ttu-id="d864b-130">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d864b-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d864b-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="d864b-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d864b-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="d864b-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d864b-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="d864b-133">Schema name</span></span>  <br/> |<span data-ttu-id="d864b-134">类型架构</span><span class="sxs-lookup"><span data-stu-id="d864b-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="d864b-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="d864b-135">Validation file</span></span>  <br/> |<span data-ttu-id="d864b-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d864b-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d864b-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="d864b-137">Can be empty</span></span>  <br/> |<span data-ttu-id="d864b-138">False</span><span class="sxs-lookup"><span data-stu-id="d864b-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d864b-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d864b-139">See also</span></span>

- [<span data-ttu-id="d864b-140">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d864b-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

