---
title: StartDate （重复）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StartDate
api_type:
- schema
ms.assetid: bd65ac06-b3ac-4c9b-9568-3e4dc94378e7
description: StartDate 元素均表示一个周期性任务或日历项的开始日期。
ms.openlocfilehash: 6a38e63bbcf010ab6dca8f66440a2b0a559cf88d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827551"
---
# <a name="startdate-recurrence"></a><span data-ttu-id="a89a8-103">StartDate （重复）</span><span class="sxs-lookup"><span data-stu-id="a89a8-103">StartDate (Recurrence)</span></span>

<span data-ttu-id="a89a8-104">**StartDate**元素均表示一个周期性任务或日历项的开始日期。</span><span class="sxs-lookup"><span data-stu-id="a89a8-104">The **StartDate** element represents the start date of a recurring task or calendar item.</span></span> 
  
```xml
<StartDate/>
```

<span data-ttu-id="a89a8-105">**日期**</span><span class="sxs-lookup"><span data-stu-id="a89a8-105">**Date**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="a89a8-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a89a8-106">Attributes and elements</span></span>

<span data-ttu-id="a89a8-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a89a8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a89a8-108">属性</span><span class="sxs-lookup"><span data-stu-id="a89a8-108">Attributes</span></span>

<span data-ttu-id="a89a8-109">无。</span><span class="sxs-lookup"><span data-stu-id="a89a8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a89a8-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a89a8-110">Child elements</span></span>

<span data-ttu-id="a89a8-111">无。</span><span class="sxs-lookup"><span data-stu-id="a89a8-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a89a8-112">父元素</span><span class="sxs-lookup"><span data-stu-id="a89a8-112">Parent elements</span></span>

|<span data-ttu-id="a89a8-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="a89a8-113">**Element**</span></span>|<span data-ttu-id="a89a8-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="a89a8-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a89a8-115">EndDateRecurrence</span><span class="sxs-lookup"><span data-stu-id="a89a8-115">EndDateRecurrence</span></span>](enddaterecurrence.md) <br/> |<span data-ttu-id="a89a8-116">介绍的开始日期和结束日期的项目定期模式。</span><span class="sxs-lookup"><span data-stu-id="a89a8-116">Describes the start date and the end date of an item recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="a89a8-117">NoEndRecurrence</span><span class="sxs-lookup"><span data-stu-id="a89a8-117">NoEndRecurrence</span></span>](noendrecurrence.md) <br/> |<span data-ttu-id="a89a8-118">介绍没有定义的结束日期项目定期模式的开始日期。</span><span class="sxs-lookup"><span data-stu-id="a89a8-118">Describes the start date of an item recurrence pattern that does not have a defined end date.</span></span>  <br/> |
|[<span data-ttu-id="a89a8-119">NumberedRecurrence</span><span class="sxs-lookup"><span data-stu-id="a89a8-119">NumberedRecurrence</span></span>](numberedrecurrence.md) <br/> |<span data-ttu-id="a89a8-120">介绍的开始日期和定期项目的次数。</span><span class="sxs-lookup"><span data-stu-id="a89a8-120">Describes the start date and the number of occurrences of a recurring item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a89a8-121">文本值</span><span class="sxs-lookup"><span data-stu-id="a89a8-121">Text value</span></span>

<span data-ttu-id="a89a8-122">如果使用此元素，则需要表示日期的文本值。</span><span class="sxs-lookup"><span data-stu-id="a89a8-122">A text value that represents a date is required if this element is used.</span></span> <span data-ttu-id="a89a8-123">值不能小于 Apr，1，该值表示自 1601年 00:00:00。</span><span class="sxs-lookup"><span data-stu-id="a89a8-123">The value cannot be less than Apr, 1, 1601 00:00:00.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a89a8-124">备注</span><span class="sxs-lookup"><span data-stu-id="a89a8-124">Remarks</span></span>

<span data-ttu-id="a89a8-125">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a89a8-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a89a8-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="a89a8-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a89a8-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="a89a8-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a89a8-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="a89a8-128">Schema name</span></span>  <br/> |<span data-ttu-id="a89a8-129">类型架构</span><span class="sxs-lookup"><span data-stu-id="a89a8-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="a89a8-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="a89a8-130">Validation file</span></span>  <br/> |<span data-ttu-id="a89a8-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a89a8-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a89a8-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="a89a8-132">Can be empty</span></span>  <br/> |<span data-ttu-id="a89a8-133">False</span><span class="sxs-lookup"><span data-stu-id="a89a8-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a89a8-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a89a8-134">See also</span></span>

- [<span data-ttu-id="a89a8-135">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a89a8-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

