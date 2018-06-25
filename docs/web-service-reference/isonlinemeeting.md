---
title: IsOnlineMeeting
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsOnlineMeeting
api_type:
- schema
ms.assetid: c29df676-0f3a-4694-a42f-522c6d16872f
description: IsOnlineMeeting 元素指示是否联机会议。
ms.openlocfilehash: 5a56b0b9828d6f6bec83fc0ad0f8f9579b471a72
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826061"
---
# <a name="isonlinemeeting"></a><span data-ttu-id="ce093-103">IsOnlineMeeting</span><span class="sxs-lookup"><span data-stu-id="ce093-103">IsOnlineMeeting</span></span>

<span data-ttu-id="ce093-104">**IsOnlineMeeting**元素指示是否联机会议。</span><span class="sxs-lookup"><span data-stu-id="ce093-104">The **IsOnlineMeeting** element indicates whether the meeting is online.</span></span> 
  
```xml
<IsOnlineMeeting/>
```

 <span data-ttu-id="ce093-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="ce093-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ce093-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ce093-106">Attributes and elements</span></span>

<span data-ttu-id="ce093-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ce093-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ce093-108">属性</span><span class="sxs-lookup"><span data-stu-id="ce093-108">Attributes</span></span>

<span data-ttu-id="ce093-109">无。</span><span class="sxs-lookup"><span data-stu-id="ce093-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ce093-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ce093-110">Child elements</span></span>

<span data-ttu-id="ce093-111">无。</span><span class="sxs-lookup"><span data-stu-id="ce093-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ce093-112">父元素</span><span class="sxs-lookup"><span data-stu-id="ce093-112">Parent elements</span></span>

|<span data-ttu-id="ce093-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="ce093-113">**Element**</span></span>|<span data-ttu-id="ce093-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="ce093-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ce093-115">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="ce093-115">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="ce093-116">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="ce093-116">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ce093-117">日历项目</span><span class="sxs-lookup"><span data-stu-id="ce093-117">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="ce093-118">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="ce093-118">Represents an Exchange calendar item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ce093-119">文本值</span><span class="sxs-lookup"><span data-stu-id="ce093-119">Text value</span></span>

<span data-ttu-id="ce093-120">如果使用此元素，则需要一个文本值，它代表一个布尔值。</span><span class="sxs-lookup"><span data-stu-id="ce093-120">A text value that represents a Boolean value is required if this element is used.</span></span> <span data-ttu-id="ce093-121">值为**true**指示会议处于联机状态。</span><span class="sxs-lookup"><span data-stu-id="ce093-121">A value of **true** indicates that the meeting is online.</span></span> <span data-ttu-id="ce093-122">如果值为**false**指示会议未处于联机状态。</span><span class="sxs-lookup"><span data-stu-id="ce093-122">A value of **false** indicates that the meeting is not online.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ce093-123">注解</span><span class="sxs-lookup"><span data-stu-id="ce093-123">Remarks</span></span>

<span data-ttu-id="ce093-124">读写的组织者的日历项目的 IsOnlineMeeting 属性。</span><span class="sxs-lookup"><span data-stu-id="ce093-124">The IsOnlineMeeting property is read-writable for the organizer's calendar item.</span></span> <span data-ttu-id="ce093-125">它是只读的会议请求和与会者的日历项目。</span><span class="sxs-lookup"><span data-stu-id="ce093-125">It is read-only for meeting requests and for attendees' calendar items.</span></span>
  
<span data-ttu-id="ce093-126">描述此元素的架构位于运行 MicrosoftExchange 2007 已安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ce093-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ce093-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="ce093-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ce093-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="ce093-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ce093-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="ce093-129">Schema name</span></span>  <br/> |<span data-ttu-id="ce093-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="ce093-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="ce093-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="ce093-131">Validation file</span></span>  <br/> |<span data-ttu-id="ce093-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ce093-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ce093-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="ce093-133">Can be empty</span></span>  <br/> |<span data-ttu-id="ce093-134">False</span><span class="sxs-lookup"><span data-stu-id="ce093-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ce093-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ce093-135">See also</span></span>



- [<span data-ttu-id="ce093-136">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="ce093-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

