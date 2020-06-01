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
description: ConferenceType 元素描述使用日历项目执行的会议的类型。
ms.openlocfilehash: 482fc09d709e2b151b255107af59cb98de236aec
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463928"
---
# <a name="conferencetype"></a><span data-ttu-id="93a26-103">ConferenceType</span><span class="sxs-lookup"><span data-stu-id="93a26-103">ConferenceType</span></span>

<span data-ttu-id="93a26-104">**ConferenceType**元素描述使用日历项目执行的会议的类型。</span><span class="sxs-lookup"><span data-stu-id="93a26-104">The **ConferenceType** element describes the type of conferencing that is performed with a calendar item.</span></span> 
  
```xml
<ConferenceType/>
```

 <span data-ttu-id="93a26-105">**int**</span><span class="sxs-lookup"><span data-stu-id="93a26-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="93a26-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="93a26-106">Attributes and elements</span></span>

<span data-ttu-id="93a26-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="93a26-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="93a26-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="93a26-108">Attributes</span></span>

<span data-ttu-id="93a26-109">无。</span><span class="sxs-lookup"><span data-stu-id="93a26-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="93a26-110">子元素</span><span class="sxs-lookup"><span data-stu-id="93a26-110">Child elements</span></span>

<span data-ttu-id="93a26-111">无。</span><span class="sxs-lookup"><span data-stu-id="93a26-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="93a26-112">父元素</span><span class="sxs-lookup"><span data-stu-id="93a26-112">Parent elements</span></span>

|<span data-ttu-id="93a26-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="93a26-113">**Element**</span></span>|<span data-ttu-id="93a26-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="93a26-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="93a26-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="93a26-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="93a26-116">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="93a26-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="93a26-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="93a26-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="93a26-118">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="93a26-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="93a26-119">文本值</span><span class="sxs-lookup"><span data-stu-id="93a26-119">Text value</span></span>

<span data-ttu-id="93a26-120">如果使用此元素，则需要一个表示整数值的文本值。</span><span class="sxs-lookup"><span data-stu-id="93a26-120">A text value that represents an integer value is required if this element is used.</span></span> <span data-ttu-id="93a26-121">以下是此元素的可能值：</span><span class="sxs-lookup"><span data-stu-id="93a26-121">The following are the possible values for this element:</span></span>
  
- <span data-ttu-id="93a26-122">0 = NetMeeting</span><span class="sxs-lookup"><span data-stu-id="93a26-122">0 = NetMeeting</span></span>
    
- <span data-ttu-id="93a26-123">1 = NetShow</span><span class="sxs-lookup"><span data-stu-id="93a26-123">1 = NetShow</span></span>
    
- <span data-ttu-id="93a26-124">2 = 聊天</span><span class="sxs-lookup"><span data-stu-id="93a26-124">2 = Chat</span></span>
    
## <a name="remarks"></a><span data-ttu-id="93a26-125">备注</span><span class="sxs-lookup"><span data-stu-id="93a26-125">Remarks</span></span>

<span data-ttu-id="93a26-126">对于组织者的日历项目， **MeetingWorkspaceUrl**属性是可读写的。</span><span class="sxs-lookup"><span data-stu-id="93a26-126">The **MeetingWorkspaceUrl** property is read-writable for the organizer's calendar item.</span></span> <span data-ttu-id="93a26-127">对于会议请求和与会者的日历项目，它是只读的。</span><span class="sxs-lookup"><span data-stu-id="93a26-127">It is read-only for meeting requests and for attendee's calendar items.</span></span> 
  
<span data-ttu-id="93a26-128">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="93a26-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="93a26-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="93a26-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="93a26-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="93a26-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="93a26-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="93a26-131">Schema Name</span></span>  <br/> |<span data-ttu-id="93a26-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="93a26-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="93a26-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="93a26-133">Validation File</span></span>  <br/> |<span data-ttu-id="93a26-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="93a26-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="93a26-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="93a26-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="93a26-136">False</span><span class="sxs-lookup"><span data-stu-id="93a26-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="93a26-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="93a26-137">See also</span></span>



- [<span data-ttu-id="93a26-138">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="93a26-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

