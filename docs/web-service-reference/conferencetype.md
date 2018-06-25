---
title: ConferenceType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConferenceType
api_type:
- schema
ms.assetid: 6bcf6c18-2695-44b1-aabe-dadc52b2633a
description: ConferenceType 元素描述使用日历项目执行的会议类型。
ms.openlocfilehash: d312420606c5e1914fe321ae7c7c512f0833199c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753474"
---
# <a name="conferencetype"></a><span data-ttu-id="18099-103">ConferenceType</span><span class="sxs-lookup"><span data-stu-id="18099-103">ConferenceType</span></span>

<span data-ttu-id="18099-104">**ConferenceType**元素描述使用日历项目执行的会议类型。</span><span class="sxs-lookup"><span data-stu-id="18099-104">The **ConferenceType** element describes the type of conferencing that is performed with a calendar item.</span></span> 
  
```xml
<ConferenceType/>
```

 <span data-ttu-id="18099-105">**int**</span><span class="sxs-lookup"><span data-stu-id="18099-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="18099-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="18099-106">Attributes and elements</span></span>

<span data-ttu-id="18099-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="18099-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="18099-108">属性</span><span class="sxs-lookup"><span data-stu-id="18099-108">Attributes</span></span>

<span data-ttu-id="18099-109">无。</span><span class="sxs-lookup"><span data-stu-id="18099-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="18099-110">子元素</span><span class="sxs-lookup"><span data-stu-id="18099-110">Child elements</span></span>

<span data-ttu-id="18099-111">无。</span><span class="sxs-lookup"><span data-stu-id="18099-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="18099-112">父元素</span><span class="sxs-lookup"><span data-stu-id="18099-112">Parent elements</span></span>

|<span data-ttu-id="18099-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="18099-113">**Element**</span></span>|<span data-ttu-id="18099-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="18099-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="18099-115">日历项目</span><span class="sxs-lookup"><span data-stu-id="18099-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="18099-116">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="18099-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="18099-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="18099-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="18099-118">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="18099-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="18099-119">文本值</span><span class="sxs-lookup"><span data-stu-id="18099-119">Text value</span></span>

<span data-ttu-id="18099-120">如果使用此元素，则需要一个文本值，它代表一个整数值。</span><span class="sxs-lookup"><span data-stu-id="18099-120">A text value that represents an integer value is required if this element is used.</span></span> <span data-ttu-id="18099-121">此元素的可能值如下：</span><span class="sxs-lookup"><span data-stu-id="18099-121">The following are the possible values for this element:</span></span>
  
- <span data-ttu-id="18099-122">0 = NetMeeting</span><span class="sxs-lookup"><span data-stu-id="18099-122">0 = NetMeeting</span></span>
    
- <span data-ttu-id="18099-123">1 = NetShow</span><span class="sxs-lookup"><span data-stu-id="18099-123">1 = NetShow</span></span>
    
- <span data-ttu-id="18099-124">2 = 聊天</span><span class="sxs-lookup"><span data-stu-id="18099-124">2 = Chat</span></span>
    
## <a name="remarks"></a><span data-ttu-id="18099-125">注解</span><span class="sxs-lookup"><span data-stu-id="18099-125">Remarks</span></span>

<span data-ttu-id="18099-126">**MeetingWorkspaceUrl**属性为读写的组织者的日历项目。</span><span class="sxs-lookup"><span data-stu-id="18099-126">The **MeetingWorkspaceUrl** property is read-writable for the organizer's calendar item.</span></span> <span data-ttu-id="18099-127">它是只读的会议请求和与会者的日历项目。</span><span class="sxs-lookup"><span data-stu-id="18099-127">It is read-only for meeting requests and for attendee's calendar items.</span></span> 
  
<span data-ttu-id="18099-128">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="18099-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="18099-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="18099-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="18099-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="18099-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="18099-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="18099-131">Schema Name</span></span>  <br/> |<span data-ttu-id="18099-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="18099-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="18099-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="18099-133">Validation File</span></span>  <br/> |<span data-ttu-id="18099-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="18099-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="18099-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="18099-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="18099-136">False</span><span class="sxs-lookup"><span data-stu-id="18099-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="18099-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="18099-137">See also</span></span>



- [<span data-ttu-id="18099-138">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="18099-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

