---
title: FirstDayOfWeek
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FirstDayOfWeek
api_type:
- schema
ms.assetid: d6cf1bd3-a19b-4d5f-9e25-8e337a4939e0
description: FirstDayOfWeek 元素指定一周的第一天。
ms.openlocfilehash: 1b4aee8e1ce2548cd6b0047623b0bcda47ad316b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530970"
---
# <a name="firstdayofweek"></a><span data-ttu-id="a79f4-103">FirstDayOfWeek</span><span class="sxs-lookup"><span data-stu-id="a79f4-103">FirstDayOfWeek</span></span>

<span data-ttu-id="a79f4-104">**FirstDayOfWeek**元素指定一周的第一天。</span><span class="sxs-lookup"><span data-stu-id="a79f4-104">The **FirstDayOfWeek** element specifies the first day of the week.</span></span> 
  
```XML
<FirstDayOfWeek> Sunday | Monday | Tuesday | Wednesday | Thursday | Friday | Saturday</FirstDayOfWeek>
```

 <span data-ttu-id="a79f4-105">**DayOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="a79f4-105">**DayOfWeekType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a79f4-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a79f4-106">Attributes and elements</span></span>

<span data-ttu-id="a79f4-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a79f4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a79f4-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="a79f4-108">Attributes</span></span>

<span data-ttu-id="a79f4-109">无。</span><span class="sxs-lookup"><span data-stu-id="a79f4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a79f4-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a79f4-110">Child elements</span></span>

<span data-ttu-id="a79f4-111">无。</span><span class="sxs-lookup"><span data-stu-id="a79f4-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a79f4-112">父元素</span><span class="sxs-lookup"><span data-stu-id="a79f4-112">Parent elements</span></span>

|<span data-ttu-id="a79f4-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="a79f4-113">**Element**</span></span>|<span data-ttu-id="a79f4-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="a79f4-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a79f4-115">WeeklyRecurrence</span><span class="sxs-lookup"><span data-stu-id="a79f4-115">WeeklyRecurrence</span></span>](weeklyrecurrence.md) <br/> |<span data-ttu-id="a79f4-116">介绍每周定期模式。</span><span class="sxs-lookup"><span data-stu-id="a79f4-116">Describes a weekly recurrence pattern.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a79f4-117">文本值</span><span class="sxs-lookup"><span data-stu-id="a79f4-117">Text value</span></span>

<span data-ttu-id="a79f4-118">**FirstDayOfWeek**元素的文本值指示将星期中的哪一天用作一周的第一天。</span><span class="sxs-lookup"><span data-stu-id="a79f4-118">The text value of the **FirstDayOfWeek** element indicates which day of the week is used as the first day of the week.</span></span> <span data-ttu-id="a79f4-119">以下是可能的文本值：</span><span class="sxs-lookup"><span data-stu-id="a79f4-119">The following are the possible text values:</span></span> 
  
- <span data-ttu-id="a79f4-120">星期日</span><span class="sxs-lookup"><span data-stu-id="a79f4-120">Sunday</span></span>
    
- <span data-ttu-id="a79f4-121">星期一</span><span class="sxs-lookup"><span data-stu-id="a79f4-121">Monday</span></span>
    
- <span data-ttu-id="a79f4-122">星期二</span><span class="sxs-lookup"><span data-stu-id="a79f4-122">Tuesday</span></span>
    
- <span data-ttu-id="a79f4-123">星期三</span><span class="sxs-lookup"><span data-stu-id="a79f4-123">Wednesday</span></span>
    
- <span data-ttu-id="a79f4-124">星期四</span><span class="sxs-lookup"><span data-stu-id="a79f4-124">Thursday</span></span>
    
- <span data-ttu-id="a79f4-125">星期五</span><span class="sxs-lookup"><span data-stu-id="a79f4-125">Friday</span></span>
    
- <span data-ttu-id="a79f4-126">星期六</span><span class="sxs-lookup"><span data-stu-id="a79f4-126">Saturday</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a79f4-127">备注</span><span class="sxs-lookup"><span data-stu-id="a79f4-127">Remarks</span></span>

<span data-ttu-id="a79f4-128">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="a79f4-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a79f4-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="a79f4-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a79f4-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="a79f4-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a79f4-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="a79f4-131">Schema Name</span></span>  <br/> |<span data-ttu-id="a79f4-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="a79f4-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="a79f4-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="a79f4-133">Validation File</span></span>  <br/> |<span data-ttu-id="a79f4-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a79f4-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a79f4-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="a79f4-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="a79f4-136">False</span><span class="sxs-lookup"><span data-stu-id="a79f4-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a79f4-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a79f4-137">See also</span></span>



- [<span data-ttu-id="a79f4-138">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a79f4-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

