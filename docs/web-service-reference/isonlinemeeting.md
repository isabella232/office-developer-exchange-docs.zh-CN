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
description: IsOnlineMeeting 元素指示会议是否处于联机状态。
ms.openlocfilehash: d2d60c8a51ad7e03c33b57709d9173e79d162268
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460398"
---
# <a name="isonlinemeeting"></a><span data-ttu-id="fe901-103">IsOnlineMeeting</span><span class="sxs-lookup"><span data-stu-id="fe901-103">IsOnlineMeeting</span></span>

<span data-ttu-id="fe901-104">**IsOnlineMeeting**元素指示会议是否处于联机状态。</span><span class="sxs-lookup"><span data-stu-id="fe901-104">The **IsOnlineMeeting** element indicates whether the meeting is online.</span></span> 
  
```xml
<IsOnlineMeeting/>
```

 <span data-ttu-id="fe901-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="fe901-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fe901-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fe901-106">Attributes and elements</span></span>

<span data-ttu-id="fe901-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fe901-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fe901-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="fe901-108">Attributes</span></span>

<span data-ttu-id="fe901-109">无。</span><span class="sxs-lookup"><span data-stu-id="fe901-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fe901-110">子元素</span><span class="sxs-lookup"><span data-stu-id="fe901-110">Child elements</span></span>

<span data-ttu-id="fe901-111">无。</span><span class="sxs-lookup"><span data-stu-id="fe901-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fe901-112">父元素</span><span class="sxs-lookup"><span data-stu-id="fe901-112">Parent elements</span></span>

|<span data-ttu-id="fe901-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="fe901-113">**Element**</span></span>|<span data-ttu-id="fe901-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="fe901-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fe901-115">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="fe901-115">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="fe901-116">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="fe901-116">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="fe901-117">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="fe901-117">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="fe901-118">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="fe901-118">Represents an Exchange calendar item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fe901-119">文本值</span><span class="sxs-lookup"><span data-stu-id="fe901-119">Text value</span></span>

<span data-ttu-id="fe901-120">如果使用此元素，则需要一个表示布尔值的文本值。</span><span class="sxs-lookup"><span data-stu-id="fe901-120">A text value that represents a Boolean value is required if this element is used.</span></span> <span data-ttu-id="fe901-121">值**为 true**表示会议处于联机状态。</span><span class="sxs-lookup"><span data-stu-id="fe901-121">A value of **true** indicates that the meeting is online.</span></span> <span data-ttu-id="fe901-122">**如果值为 false** ，则表示会议不在线。</span><span class="sxs-lookup"><span data-stu-id="fe901-122">A value of **false** indicates that the meeting is not online.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fe901-123">备注</span><span class="sxs-lookup"><span data-stu-id="fe901-123">Remarks</span></span>

<span data-ttu-id="fe901-124">对于组织者的日历项目，IsOnlineMeeting 属性是可读写的。</span><span class="sxs-lookup"><span data-stu-id="fe901-124">The IsOnlineMeeting property is read-writable for the organizer's calendar item.</span></span> <span data-ttu-id="fe901-125">对于会议请求和与会者的日历项目，它是只读的。</span><span class="sxs-lookup"><span data-stu-id="fe901-125">It is read-only for meeting requests and for attendees' calendar items.</span></span>
  
<span data-ttu-id="fe901-126">描述此元素的架构位于运行 MicrosoftExchange 2007 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="fe901-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fe901-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="fe901-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fe901-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="fe901-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fe901-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="fe901-129">Schema name</span></span>  <br/> |<span data-ttu-id="fe901-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="fe901-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="fe901-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="fe901-131">Validation file</span></span>  <br/> |<span data-ttu-id="fe901-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fe901-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fe901-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="fe901-133">Can be empty</span></span>  <br/> |<span data-ttu-id="fe901-134">False</span><span class="sxs-lookup"><span data-stu-id="fe901-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fe901-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fe901-135">See also</span></span>



- [<span data-ttu-id="fe901-136">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="fe901-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

