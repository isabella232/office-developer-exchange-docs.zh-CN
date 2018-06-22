---
title: ConflictingMeetingCount
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConflictingMeetingCount
api_type:
- schema
ms.assetid: 11f4d93a-b514-4a27-8d19-f4f0a35a185e
description: ConflictingMeetingCount 元素均表示与日历项目发生冲突的会议数。
ms.openlocfilehash: ace800982c284cf65ff22d92c711197ee5ee1d06
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753478"
---
# <a name="conflictingmeetingcount"></a><span data-ttu-id="3364e-103">ConflictingMeetingCount</span><span class="sxs-lookup"><span data-stu-id="3364e-103">ConflictingMeetingCount</span></span>

<span data-ttu-id="3364e-104">**ConflictingMeetingCount**元素均表示与日历项目发生冲突的会议数。</span><span class="sxs-lookup"><span data-stu-id="3364e-104">The **ConflictingMeetingCount** element represents the number of meetings that conflict with the calendar item.</span></span> 
  
```xml
<ConflictingMeetingCount/>
```

 <span data-ttu-id="3364e-105">**int**</span><span class="sxs-lookup"><span data-stu-id="3364e-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3364e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="3364e-106">Attributes and elements</span></span>

<span data-ttu-id="3364e-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3364e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3364e-108">属性</span><span class="sxs-lookup"><span data-stu-id="3364e-108">Attributes</span></span>

<span data-ttu-id="3364e-109">无。</span><span class="sxs-lookup"><span data-stu-id="3364e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3364e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="3364e-110">Child elements</span></span>

<span data-ttu-id="3364e-111">无。</span><span class="sxs-lookup"><span data-stu-id="3364e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3364e-112">父元素</span><span class="sxs-lookup"><span data-stu-id="3364e-112">Parent elements</span></span>

|<span data-ttu-id="3364e-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="3364e-113">**Element**</span></span>|<span data-ttu-id="3364e-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="3364e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3364e-115">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="3364e-115">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="3364e-116">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="3364e-116">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3364e-117">日历项目</span><span class="sxs-lookup"><span data-stu-id="3364e-117">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="3364e-118">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="3364e-118">Represents an Exchange calendar item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3364e-119">文本值</span><span class="sxs-lookup"><span data-stu-id="3364e-119">Text value</span></span>

<span data-ttu-id="3364e-120">文本值表示一个整数。</span><span class="sxs-lookup"><span data-stu-id="3364e-120">The text value represents an integer.</span></span> <span data-ttu-id="3364e-121">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="3364e-121">This property is read-only.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3364e-122">备注</span><span class="sxs-lookup"><span data-stu-id="3364e-122">Remarks</span></span>

<span data-ttu-id="3364e-123">日历项被视为发生时，至少在部件中，为相同的日历文件夹中的另一个日历项同时冲突。</span><span class="sxs-lookup"><span data-stu-id="3364e-123">A calendar item is considered conflicting if it occurs, at least in part, at the same time as another calendar item in the same calendar folder.</span></span> <span data-ttu-id="3364e-124">如果日历项目 noncalendar 文件夹中，将与默认的日历文件夹中的日历项目进行比较。</span><span class="sxs-lookup"><span data-stu-id="3364e-124">If a calendar item is in a noncalendar folder, it is compared with calendar items in the default calendar folder.</span></span> <span data-ttu-id="3364e-125">与默认的日历文件夹中的日历项目，会议请求进行比较。</span><span class="sxs-lookup"><span data-stu-id="3364e-125">Meeting requests are compared with calendar items in the default calendar folder.</span></span>
  
<span data-ttu-id="3364e-126">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="3364e-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3364e-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="3364e-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3364e-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="3364e-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3364e-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="3364e-129">Schema name</span></span>  <br/> |<span data-ttu-id="3364e-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="3364e-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="3364e-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="3364e-131">Validation file</span></span>  <br/> |<span data-ttu-id="3364e-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3364e-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3364e-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="3364e-133">Can be empty</span></span>  <br/> |<span data-ttu-id="3364e-134">False</span><span class="sxs-lookup"><span data-stu-id="3364e-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3364e-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3364e-135">See also</span></span>



- [<span data-ttu-id="3364e-136">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="3364e-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

