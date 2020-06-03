---
title: ChangeHighlights
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f9bd7323-44db-4d2f-aaaa-94c2dfdeead6
description: ChangeHighlights 元素指定会议请求邮件的两个版本之间的变化。
ms.openlocfilehash: 6c78d2c96449ee41032859f90bf51d6e0faa92ae
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463277"
---
# <a name="changehighlights"></a><span data-ttu-id="7a9bf-103">ChangeHighlights</span><span class="sxs-lookup"><span data-stu-id="7a9bf-103">ChangeHighlights</span></span>

<span data-ttu-id="7a9bf-104">**ChangeHighlights**元素指定会议请求邮件的两个版本之间的变化。</span><span class="sxs-lookup"><span data-stu-id="7a9bf-104">The **ChangeHighlights** element specifies what has changed between two versions of a meeting request message.</span></span> 
  
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

 <span data-ttu-id="7a9bf-105">**ChangeHighlightsType**</span><span class="sxs-lookup"><span data-stu-id="7a9bf-105">**ChangeHighlightsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7a9bf-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7a9bf-106">Attributes and elements</span></span>

<span data-ttu-id="7a9bf-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7a9bf-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7a9bf-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="7a9bf-108">Attributes</span></span>

<span data-ttu-id="7a9bf-109">无。</span><span class="sxs-lookup"><span data-stu-id="7a9bf-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7a9bf-110">子元素</span><span class="sxs-lookup"><span data-stu-id="7a9bf-110">Child elements</span></span>

|<span data-ttu-id="7a9bf-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="7a9bf-111">**Element**</span></span>|<span data-ttu-id="7a9bf-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="7a9bf-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7a9bf-113">HasLocationChanged</span><span class="sxs-lookup"><span data-stu-id="7a9bf-113">HasLocationChanged</span></span>](haslocationchanged.md) <br/> |<span data-ttu-id="7a9bf-114">指定会议的 location 属性是否已更改。</span><span class="sxs-lookup"><span data-stu-id="7a9bf-114">Specifies whether the location property of a meeting has changed.</span></span>  <br/> |
|[<span data-ttu-id="7a9bf-115">Location</span><span class="sxs-lookup"><span data-stu-id="7a9bf-115">Location</span></span>](location.md) <br/> |<span data-ttu-id="7a9bf-116">代表会议或约会的位置。</span><span class="sxs-lookup"><span data-stu-id="7a9bf-116">Represents the location of a meeting or appointment.</span></span>  <br/> |
|[<span data-ttu-id="7a9bf-117">HasStartTimeChanged</span><span class="sxs-lookup"><span data-stu-id="7a9bf-117">HasStartTimeChanged</span></span>](hasstarttimechanged.md) <br/> |<span data-ttu-id="7a9bf-118">指定会议的开始时间是否已更改。</span><span class="sxs-lookup"><span data-stu-id="7a9bf-118">Specifies whether the start time for a meeting has changed.</span></span>  <br/> |
|[<span data-ttu-id="7a9bf-119">开始</span><span class="sxs-lookup"><span data-stu-id="7a9bf-119">Start</span></span>](start.md) <br/> |<span data-ttu-id="7a9bf-120">代表持续时间的开始日期。</span><span class="sxs-lookup"><span data-stu-id="7a9bf-120">Represents the start of a duration.</span></span>  <br/> |
|[<span data-ttu-id="7a9bf-121">HasEndTimeChanged</span><span class="sxs-lookup"><span data-stu-id="7a9bf-121">HasEndTimeChanged</span></span>](hasendtimechanged.md) <br/> |<span data-ttu-id="7a9bf-122">指定会议的结束时间是否已更改。</span><span class="sxs-lookup"><span data-stu-id="7a9bf-122">Specifies whether the end time for a meeting has changed.</span></span>  <br/> |
|[<span data-ttu-id="7a9bf-123">停止</span><span class="sxs-lookup"><span data-stu-id="7a9bf-123">End </span></span>](end-ex15websvcsotherref.md) <br/> |<span data-ttu-id="7a9bf-124">表示持续时间的结束。</span><span class="sxs-lookup"><span data-stu-id="7a9bf-124">Represents the end of a duration.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7a9bf-125">父元素</span><span class="sxs-lookup"><span data-stu-id="7a9bf-125">Parent elements</span></span>

|<span data-ttu-id="7a9bf-126">**元素**</span><span class="sxs-lookup"><span data-stu-id="7a9bf-126">**Element**</span></span>|<span data-ttu-id="7a9bf-127">**说明**</span><span class="sxs-lookup"><span data-stu-id="7a9bf-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7a9bf-128">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="7a9bf-128">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="7a9bf-129">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="7a9bf-129">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7a9bf-130">备注</span><span class="sxs-lookup"><span data-stu-id="7a9bf-130">Remarks</span></span>

<span data-ttu-id="7a9bf-131">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="7a9bf-131">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="7a9bf-132">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7a9bf-132">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7a9bf-133">元素信息</span><span class="sxs-lookup"><span data-stu-id="7a9bf-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7a9bf-134">命名空间</span><span class="sxs-lookup"><span data-stu-id="7a9bf-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7a9bf-135">架构名称</span><span class="sxs-lookup"><span data-stu-id="7a9bf-135">Schema Name</span></span>  <br/> |<span data-ttu-id="7a9bf-136">类型架构</span><span class="sxs-lookup"><span data-stu-id="7a9bf-136">Type schema</span></span>  <br/> |
|<span data-ttu-id="7a9bf-137">验证文件</span><span class="sxs-lookup"><span data-stu-id="7a9bf-137">Validation File</span></span>  <br/> |<span data-ttu-id="7a9bf-138">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="7a9bf-138">types.xsd</span></span>  <br/> |
|<span data-ttu-id="7a9bf-139">可以为空</span><span class="sxs-lookup"><span data-stu-id="7a9bf-139">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="7a9bf-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7a9bf-140">See also</span></span>



- [<span data-ttu-id="7a9bf-141">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="7a9bf-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

