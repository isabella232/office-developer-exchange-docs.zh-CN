---
title: MeetingWorkspaceUrl
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MeetingWorkspaceUrl
api_type:
- schema
ms.assetid: 0ca942fe-8f57-4065-93ad-65790f9a04c3
description: MeetingWorkspaceUrl 元素包含日历项目中包含的会议工作区的 URL。 "会议工作区" 是用于规划会议和跟踪结果的共享网站。
ms.openlocfilehash: cd4396e590ab1471278bd44b9a4e0009fe326eaf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466281"
---
# <a name="meetingworkspaceurl"></a><span data-ttu-id="fc771-104">MeetingWorkspaceUrl</span><span class="sxs-lookup"><span data-stu-id="fc771-104">MeetingWorkspaceUrl</span></span>

<span data-ttu-id="fc771-105">**MeetingWorkspaceUrl**元素包含日历项目中包含的会议工作区的 URL。</span><span class="sxs-lookup"><span data-stu-id="fc771-105">The **MeetingWorkspaceUrl** element contains the URL for the meeting workspace that is included in the calendar item.</span></span> <span data-ttu-id="fc771-106">"会议工作区" 是用于规划会议和跟踪结果的共享网站。</span><span class="sxs-lookup"><span data-stu-id="fc771-106">A meeting workspace is a shared Web site for planning the meeting and tracking the results.</span></span> 
  
```xml
<MeetingWorkspaceUrl/>
```

 <span data-ttu-id="fc771-107">**string**</span><span class="sxs-lookup"><span data-stu-id="fc771-107">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fc771-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fc771-108">Attributes and elements</span></span>

<span data-ttu-id="fc771-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fc771-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fc771-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="fc771-110">Attributes</span></span>

<span data-ttu-id="fc771-111">无。</span><span class="sxs-lookup"><span data-stu-id="fc771-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fc771-112">子元素</span><span class="sxs-lookup"><span data-stu-id="fc771-112">Child elements</span></span>

<span data-ttu-id="fc771-113">无。</span><span class="sxs-lookup"><span data-stu-id="fc771-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fc771-114">父元素</span><span class="sxs-lookup"><span data-stu-id="fc771-114">Parent elements</span></span>

|<span data-ttu-id="fc771-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="fc771-115">**Element**</span></span>|<span data-ttu-id="fc771-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="fc771-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fc771-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="fc771-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="fc771-118">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="fc771-118">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="fc771-119">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="fc771-119">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="fc771-120">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="fc771-120">Represents an Exchange calendar item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fc771-121">文本值</span><span class="sxs-lookup"><span data-stu-id="fc771-121">Text value</span></span>

<span data-ttu-id="fc771-122">如果使用此元素，则需要一个表示 URL 的文本值。</span><span class="sxs-lookup"><span data-stu-id="fc771-122">A text value that represents a URL is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fc771-123">备注</span><span class="sxs-lookup"><span data-stu-id="fc771-123">Remarks</span></span>

<span data-ttu-id="fc771-124">对于组织者的日历项目，MeetingWorkspaceUrl 属性是可读写的。</span><span class="sxs-lookup"><span data-stu-id="fc771-124">The MeetingWorkspaceUrl property is read-writable for the organizer's calendar item.</span></span> <span data-ttu-id="fc771-125">对于会议请求和与会者的日历项目，它是只读的。</span><span class="sxs-lookup"><span data-stu-id="fc771-125">It is read-only for meeting requests and for attendees' calendar items.</span></span>
  
<span data-ttu-id="fc771-126">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="fc771-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fc771-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="fc771-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fc771-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="fc771-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fc771-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="fc771-129">Schema name</span></span>  <br/> |<span data-ttu-id="fc771-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="fc771-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="fc771-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="fc771-131">Validation file</span></span>  <br/> |<span data-ttu-id="fc771-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fc771-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fc771-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="fc771-133">Can be empty</span></span>  <br/> |<span data-ttu-id="fc771-134">False</span><span class="sxs-lookup"><span data-stu-id="fc771-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fc771-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fc771-135">See also</span></span>



- [<span data-ttu-id="fc771-136">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="fc771-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

