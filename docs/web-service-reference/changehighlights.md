---
title: ChangeHighlights
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f9bd7323-44db-4d2f-aaaa-94c2dfdeead6
description: 元素指定会议的两种版本之间的更改 ChangeHighlights 请求消息。
ms.openlocfilehash: 5fe7aa95f60ae95f1af24e8f7a0463ad49716f65
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753443"
---
# <a name="changehighlights"></a><span data-ttu-id="07837-103">ChangeHighlights</span><span class="sxs-lookup"><span data-stu-id="07837-103">ChangeHighlights</span></span>

<span data-ttu-id="07837-104">**ChangeHighlights**元素指定会议的两种版本之间的更改请求消息。</span><span class="sxs-lookup"><span data-stu-id="07837-104">The **ChangeHighlights** element specifies what has changed between two versions of a meeting request message.</span></span> 
  
```XML
<ChangeHighlights>
    <HasLocationChanged></HasLocationChanged>
    <Location></Location>
    <HasStartTimeChanged></HasStartTimeChanged>
    <Start></Start>
    <HasEndTimeChanged></HasEndTimeChanged>
    <End></End>
</ChangeHighlights>
```

 <span data-ttu-id="07837-105">**ChangeHighlightsType**</span><span class="sxs-lookup"><span data-stu-id="07837-105">**ChangeHighlightsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="07837-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="07837-106">Attributes and elements</span></span>

<span data-ttu-id="07837-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="07837-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="07837-108">属性</span><span class="sxs-lookup"><span data-stu-id="07837-108">Attributes</span></span>

<span data-ttu-id="07837-109">无。</span><span class="sxs-lookup"><span data-stu-id="07837-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="07837-110">子元素</span><span class="sxs-lookup"><span data-stu-id="07837-110">Child elements</span></span>

|<span data-ttu-id="07837-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="07837-111">**Element**</span></span>|<span data-ttu-id="07837-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="07837-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="07837-113">HasLocationChanged</span><span class="sxs-lookup"><span data-stu-id="07837-113">HasLocationChanged</span></span>](haslocationchanged.md) <br/> |<span data-ttu-id="07837-114">指定会议的 location 属性是否已更改。</span><span class="sxs-lookup"><span data-stu-id="07837-114">Specifies whether the location property of a meeting has changed.</span></span>  <br/> |
|[<span data-ttu-id="07837-115">位置</span><span class="sxs-lookup"><span data-stu-id="07837-115">Location</span></span>](location.md) <br/> |<span data-ttu-id="07837-116">表示会议或约会的位置。</span><span class="sxs-lookup"><span data-stu-id="07837-116">Represents the location of a meeting or appointment.</span></span>  <br/> |
|[<span data-ttu-id="07837-117">HasStartTimeChanged</span><span class="sxs-lookup"><span data-stu-id="07837-117">HasStartTimeChanged</span></span>](hasstarttimechanged.md) <br/> |<span data-ttu-id="07837-118">指定是否已更改会议的开始时间。</span><span class="sxs-lookup"><span data-stu-id="07837-118">Specifies whether the start time for a meeting has changed.</span></span>  <br/> |
|[<span data-ttu-id="07837-119">Start</span><span class="sxs-lookup"><span data-stu-id="07837-119">Start</span></span>](start.md) <br/> |<span data-ttu-id="07837-120">表示持续时间的开始。</span><span class="sxs-lookup"><span data-stu-id="07837-120">Represents the start of a duration.</span></span>  <br/> |
|[<span data-ttu-id="07837-121">HasEndTimeChanged</span><span class="sxs-lookup"><span data-stu-id="07837-121">HasEndTimeChanged</span></span>](hasendtimechanged.md) <br/> |<span data-ttu-id="07837-122">指定是否已更改为会议的结束时间。</span><span class="sxs-lookup"><span data-stu-id="07837-122">Specifies whether the end time for a meeting has changed.</span></span>  <br/> |
|[<span data-ttu-id="07837-123">结束</span><span class="sxs-lookup"><span data-stu-id="07837-123">End </span></span>](end-ex15websvcsotherref.md) <br/> |<span data-ttu-id="07837-124">代表工期的结束。</span><span class="sxs-lookup"><span data-stu-id="07837-124">Represents the end of a duration.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="07837-125">父元素</span><span class="sxs-lookup"><span data-stu-id="07837-125">Parent elements</span></span>

|<span data-ttu-id="07837-126">**元素**</span><span class="sxs-lookup"><span data-stu-id="07837-126">**Element**</span></span>|<span data-ttu-id="07837-127">**说明**</span><span class="sxs-lookup"><span data-stu-id="07837-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="07837-128">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="07837-128">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="07837-129">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="07837-129">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="07837-130">备注</span><span class="sxs-lookup"><span data-stu-id="07837-130">Remarks</span></span>

<span data-ttu-id="07837-131">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="07837-131">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="07837-132">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="07837-132">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="07837-133">元素信息</span><span class="sxs-lookup"><span data-stu-id="07837-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="07837-134">命名空间</span><span class="sxs-lookup"><span data-stu-id="07837-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="07837-135">架构名称</span><span class="sxs-lookup"><span data-stu-id="07837-135">Schema Name</span></span>  <br/> |<span data-ttu-id="07837-136">类型架构</span><span class="sxs-lookup"><span data-stu-id="07837-136">Type schema</span></span>  <br/> |
|<span data-ttu-id="07837-137">验证文件</span><span class="sxs-lookup"><span data-stu-id="07837-137">Validation File</span></span>  <br/> |<span data-ttu-id="07837-138">types.xsd</span><span class="sxs-lookup"><span data-stu-id="07837-138">types.xsd</span></span>  <br/> |
|<span data-ttu-id="07837-139">可以为空</span><span class="sxs-lookup"><span data-stu-id="07837-139">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="07837-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="07837-140">See also</span></span>



- [<span data-ttu-id="07837-141">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="07837-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

