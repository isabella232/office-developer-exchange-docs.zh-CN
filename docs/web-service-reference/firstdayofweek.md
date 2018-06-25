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
ms.openlocfilehash: 99858d17213d077ce7c51ad1c746588f2f3939a7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754370"
---
# <a name="firstdayofweek"></a><span data-ttu-id="ae718-103">FirstDayOfWeek</span><span class="sxs-lookup"><span data-stu-id="ae718-103">FirstDayOfWeek</span></span>

<span data-ttu-id="ae718-104">**FirstDayOfWeek**元素指定一周的第一天。</span><span class="sxs-lookup"><span data-stu-id="ae718-104">The **FirstDayOfWeek** element specifies the first day of the week.</span></span> 
  
```XML
<FirstDayOfWeek> Sunday | Monday | Tuesday | Wednesday | Thursday | Friday | Saturday</FirstDayOfWeek>
```

 <span data-ttu-id="ae718-105">**DayOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="ae718-105">**DayOfWeekType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ae718-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ae718-106">Attributes and elements</span></span>

<span data-ttu-id="ae718-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ae718-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ae718-108">属性</span><span class="sxs-lookup"><span data-stu-id="ae718-108">Attributes</span></span>

<span data-ttu-id="ae718-109">无。</span><span class="sxs-lookup"><span data-stu-id="ae718-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ae718-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ae718-110">Child elements</span></span>

<span data-ttu-id="ae718-111">无。</span><span class="sxs-lookup"><span data-stu-id="ae718-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ae718-112">父元素</span><span class="sxs-lookup"><span data-stu-id="ae718-112">Parent elements</span></span>

|<span data-ttu-id="ae718-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="ae718-113">**Element**</span></span>|<span data-ttu-id="ae718-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="ae718-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ae718-115">WeeklyRecurrence</span><span class="sxs-lookup"><span data-stu-id="ae718-115">WeeklyRecurrence</span></span>](weeklyrecurrence.md) <br/> |<span data-ttu-id="ae718-116">介绍每周定期模式。</span><span class="sxs-lookup"><span data-stu-id="ae718-116">Describes a weekly recurrence pattern.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ae718-117">文本值</span><span class="sxs-lookup"><span data-stu-id="ae718-117">Text value</span></span>

<span data-ttu-id="ae718-118">**FirstDayOfWeek**元素的文本值指示一周的哪一天用作一周的第一天。</span><span class="sxs-lookup"><span data-stu-id="ae718-118">The text value of the **FirstDayOfWeek** element indicates which day of the week is used as the first day of the week.</span></span> <span data-ttu-id="ae718-119">以下是可能的文本值：</span><span class="sxs-lookup"><span data-stu-id="ae718-119">The following are the possible text values:</span></span> 
  
- <span data-ttu-id="ae718-120">星期日</span><span class="sxs-lookup"><span data-stu-id="ae718-120">Sunday</span></span>
    
- <span data-ttu-id="ae718-121">周一</span><span class="sxs-lookup"><span data-stu-id="ae718-121">Monday</span></span>
    
- <span data-ttu-id="ae718-122">周二</span><span class="sxs-lookup"><span data-stu-id="ae718-122">Tuesday</span></span>
    
- <span data-ttu-id="ae718-123">周三</span><span class="sxs-lookup"><span data-stu-id="ae718-123">Wednesday</span></span>
    
- <span data-ttu-id="ae718-124">周四</span><span class="sxs-lookup"><span data-stu-id="ae718-124">Thursday</span></span>
    
- <span data-ttu-id="ae718-125">周五</span><span class="sxs-lookup"><span data-stu-id="ae718-125">Friday</span></span>
    
- <span data-ttu-id="ae718-126">周六</span><span class="sxs-lookup"><span data-stu-id="ae718-126">Saturday</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ae718-127">备注</span><span class="sxs-lookup"><span data-stu-id="ae718-127">Remarks</span></span>

<span data-ttu-id="ae718-128">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="ae718-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ae718-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="ae718-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ae718-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="ae718-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ae718-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="ae718-131">Schema Name</span></span>  <br/> |<span data-ttu-id="ae718-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="ae718-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="ae718-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="ae718-133">Validation File</span></span>  <br/> |<span data-ttu-id="ae718-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ae718-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ae718-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="ae718-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="ae718-136">False</span><span class="sxs-lookup"><span data-stu-id="ae718-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ae718-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ae718-137">See also</span></span>



- [<span data-ttu-id="ae718-138">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="ae718-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

