---
title: RecurrenceId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RecurrenceId
api_type:
- schema
ms.assetid: 9ef3569d-ee56-4b22-b008-609fb3337da7
description: RecurrenceId 元素用于标识定期日历项目的特定实例。
ms.openlocfilehash: 078bec85e1ca1530137f9935365d7dd3e530ea34
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827005"
---
# <a name="recurrenceid"></a><span data-ttu-id="947be-103">RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="947be-103">RecurrenceId</span></span>

<span data-ttu-id="947be-104">**RecurrenceId**元素用于标识定期日历项目的特定实例。</span><span class="sxs-lookup"><span data-stu-id="947be-104">The **RecurrenceId** element is used to identify a specific instance of a recurring calendar item.</span></span> 
  
```xml
<RecurrenceId/>
```

 <span data-ttu-id="947be-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="947be-105">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="947be-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="947be-106">Attributes and elements</span></span>

<span data-ttu-id="947be-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="947be-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="947be-108">属性</span><span class="sxs-lookup"><span data-stu-id="947be-108">Attributes</span></span>

<span data-ttu-id="947be-109">无。</span><span class="sxs-lookup"><span data-stu-id="947be-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="947be-110">子元素</span><span class="sxs-lookup"><span data-stu-id="947be-110">Child elements</span></span>

<span data-ttu-id="947be-111">无。</span><span class="sxs-lookup"><span data-stu-id="947be-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="947be-112">父元素</span><span class="sxs-lookup"><span data-stu-id="947be-112">Parent elements</span></span>

|<span data-ttu-id="947be-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="947be-113">**Element**</span></span>|<span data-ttu-id="947be-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="947be-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="947be-115">日历项目</span><span class="sxs-lookup"><span data-stu-id="947be-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="947be-116">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="947be-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="947be-117">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="947be-117">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="947be-118">表示会议消息。</span><span class="sxs-lookup"><span data-stu-id="947be-118">Represents a meeting message.</span></span>  <br/> |
|[<span data-ttu-id="947be-119">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="947be-119">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="947be-120">表示一个会议请求。</span><span class="sxs-lookup"><span data-stu-id="947be-120">Represents a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="947be-121">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="947be-121">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="947be-122">代表会议响应。</span><span class="sxs-lookup"><span data-stu-id="947be-122">Represents a meeting response.</span></span>  <br/> |
|[<span data-ttu-id="947be-123">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="947be-123">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="947be-124">表示会议取消。</span><span class="sxs-lookup"><span data-stu-id="947be-124">Represents a meeting cancellation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="947be-125">文本值</span><span class="sxs-lookup"><span data-stu-id="947be-125">Text value</span></span>

<span data-ttu-id="947be-126">文本值表示标识日历匹配项的日期/时间值。</span><span class="sxs-lookup"><span data-stu-id="947be-126">The text value represents a date/time value that identifies a calendar occurrence.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="947be-127">备注</span><span class="sxs-lookup"><span data-stu-id="947be-127">Remarks</span></span>

<span data-ttu-id="947be-128">此属性与[UID](uid.md)属性用于确定定期日历项目的特定实例。</span><span class="sxs-lookup"><span data-stu-id="947be-128">This property is used with the [UID](uid.md) property to identify a specific instance of a recurring calendar item.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="947be-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="947be-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="947be-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="947be-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="947be-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="947be-131">Schema Name</span></span>  <br/> |<span data-ttu-id="947be-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="947be-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="947be-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="947be-133">Validation File</span></span>  <br/> |<span data-ttu-id="947be-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="947be-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="947be-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="947be-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="947be-136">False</span><span class="sxs-lookup"><span data-stu-id="947be-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="947be-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="947be-137">See also</span></span>



- [<span data-ttu-id="947be-138">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="947be-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

