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
description: ConflictingMeetingCount 元素表示与日历项目相冲突的会议数。
ms.openlocfilehash: d53245e1b5d1f0182b28b15bf55ba9742bbb2a07
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463858"
---
# <a name="conflictingmeetingcount"></a><span data-ttu-id="e0bc2-103">ConflictingMeetingCount</span><span class="sxs-lookup"><span data-stu-id="e0bc2-103">ConflictingMeetingCount</span></span>

<span data-ttu-id="e0bc2-104">**ConflictingMeetingCount**元素表示与日历项目相冲突的会议数。</span><span class="sxs-lookup"><span data-stu-id="e0bc2-104">The **ConflictingMeetingCount** element represents the number of meetings that conflict with the calendar item.</span></span> 
  
```xml
<ConflictingMeetingCount/>
```

 <span data-ttu-id="e0bc2-105">**int**</span><span class="sxs-lookup"><span data-stu-id="e0bc2-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e0bc2-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e0bc2-106">Attributes and elements</span></span>

<span data-ttu-id="e0bc2-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e0bc2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e0bc2-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="e0bc2-108">Attributes</span></span>

<span data-ttu-id="e0bc2-109">无。</span><span class="sxs-lookup"><span data-stu-id="e0bc2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e0bc2-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e0bc2-110">Child elements</span></span>

<span data-ttu-id="e0bc2-111">无。</span><span class="sxs-lookup"><span data-stu-id="e0bc2-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e0bc2-112">父元素</span><span class="sxs-lookup"><span data-stu-id="e0bc2-112">Parent elements</span></span>

|<span data-ttu-id="e0bc2-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="e0bc2-113">**Element**</span></span>|<span data-ttu-id="e0bc2-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="e0bc2-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e0bc2-115">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="e0bc2-115">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="e0bc2-116">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="e0bc2-116">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e0bc2-117">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="e0bc2-117">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="e0bc2-118">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="e0bc2-118">Represents an Exchange calendar item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e0bc2-119">文本值</span><span class="sxs-lookup"><span data-stu-id="e0bc2-119">Text value</span></span>

<span data-ttu-id="e0bc2-120">文本值表示一个整数。</span><span class="sxs-lookup"><span data-stu-id="e0bc2-120">The text value represents an integer.</span></span> <span data-ttu-id="e0bc2-121">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="e0bc2-121">This property is read-only.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e0bc2-122">备注</span><span class="sxs-lookup"><span data-stu-id="e0bc2-122">Remarks</span></span>

<span data-ttu-id="e0bc2-123">如果日历项目至少发生在同一日历文件夹中的其他日历项目，则被视为冲突。</span><span class="sxs-lookup"><span data-stu-id="e0bc2-123">A calendar item is considered conflicting if it occurs, at least in part, at the same time as another calendar item in the same calendar folder.</span></span> <span data-ttu-id="e0bc2-124">如果日历项目位于 noncalendar 文件夹中，则会与默认 "日历" 文件夹中的 "日历" 项目进行比较。</span><span class="sxs-lookup"><span data-stu-id="e0bc2-124">If a calendar item is in a noncalendar folder, it is compared with calendar items in the default calendar folder.</span></span> <span data-ttu-id="e0bc2-125">会议请求将与默认 "日历" 文件夹中的日历项目进行比较。</span><span class="sxs-lookup"><span data-stu-id="e0bc2-125">Meeting requests are compared with calendar items in the default calendar folder.</span></span>
  
<span data-ttu-id="e0bc2-126">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e0bc2-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e0bc2-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="e0bc2-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e0bc2-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="e0bc2-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e0bc2-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="e0bc2-129">Schema name</span></span>  <br/> |<span data-ttu-id="e0bc2-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="e0bc2-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="e0bc2-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="e0bc2-131">Validation file</span></span>  <br/> |<span data-ttu-id="e0bc2-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e0bc2-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e0bc2-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="e0bc2-133">Can be empty</span></span>  <br/> |<span data-ttu-id="e0bc2-134">False</span><span class="sxs-lookup"><span data-stu-id="e0bc2-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e0bc2-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e0bc2-135">See also</span></span>



- [<span data-ttu-id="e0bc2-136">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e0bc2-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

