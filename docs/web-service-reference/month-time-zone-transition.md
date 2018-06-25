---
title: 每月 （所在的时区转换）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Month
api_type:
- schema
ms.assetid: 5e6aac75-366d-43d0-8ccb-956285474662
description: Month 元素表示所在的时区转换发生的月份。
ms.openlocfilehash: 887bd750b9cad1e28e6f7603c7b3289da8f8dc07
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826483"
---
# <a name="month-time-zone-transition"></a><span data-ttu-id="2b5bd-103">每月 （所在的时区转换）</span><span class="sxs-lookup"><span data-stu-id="2b5bd-103">Month (Time Zone Transition)</span></span>

<span data-ttu-id="2b5bd-104">**Month**元素表示所在的时区转换发生的月份。</span><span class="sxs-lookup"><span data-stu-id="2b5bd-104">The **Month** element represents the month in which the time zone transition occurs.</span></span> 
  
```xml
<Month/>
```

 <span data-ttu-id="2b5bd-105">**int**</span><span class="sxs-lookup"><span data-stu-id="2b5bd-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2b5bd-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2b5bd-106">Attributes and elements</span></span>

<span data-ttu-id="2b5bd-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2b5bd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2b5bd-108">属性</span><span class="sxs-lookup"><span data-stu-id="2b5bd-108">Attributes</span></span>

<span data-ttu-id="2b5bd-109">无。</span><span class="sxs-lookup"><span data-stu-id="2b5bd-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2b5bd-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2b5bd-110">Child elements</span></span>

<span data-ttu-id="2b5bd-111">无。</span><span class="sxs-lookup"><span data-stu-id="2b5bd-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2b5bd-112">父元素</span><span class="sxs-lookup"><span data-stu-id="2b5bd-112">Parent elements</span></span>

|<span data-ttu-id="2b5bd-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="2b5bd-113">**Element**</span></span>|<span data-ttu-id="2b5bd-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="2b5bd-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2b5bd-115">RecurringDateTransition</span><span class="sxs-lookup"><span data-stu-id="2b5bd-115">RecurringDateTransition</span></span>](recurringdatetransition.md) <br/> |<span data-ttu-id="2b5bd-116">表示每年的特定日期发生的时区转换。</span><span class="sxs-lookup"><span data-stu-id="2b5bd-116">Represents a time zone transition that occurs on a specific date each year.</span></span>  <br/> |
|[<span data-ttu-id="2b5bd-117">RecurringDayTransition</span><span class="sxs-lookup"><span data-stu-id="2b5bd-117">RecurringDayTransition</span></span>](recurringdaytransition.md) <br/> |<span data-ttu-id="2b5bd-118">表示时区转换发生在每年的同一天。</span><span class="sxs-lookup"><span data-stu-id="2b5bd-118">Represents a time zone transition that occurs on the same day each year.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2b5bd-119">文本值</span><span class="sxs-lookup"><span data-stu-id="2b5bd-119">Text value</span></span>

<span data-ttu-id="2b5bd-120">文本值为整数表示时区转换发生的月份。</span><span class="sxs-lookup"><span data-stu-id="2b5bd-120">The text value is an integer that represents the month in which the time zone transition occurs.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2b5bd-121">注解</span><span class="sxs-lookup"><span data-stu-id="2b5bd-121">Remarks</span></span>

<span data-ttu-id="2b5bd-122">描述此元素的架构位于运行 Microsoft Exchange Server 已安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2b5bd-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2b5bd-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="2b5bd-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2b5bd-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="2b5bd-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2b5bd-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="2b5bd-125">Schema Name</span></span>  <br/> |<span data-ttu-id="2b5bd-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="2b5bd-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="2b5bd-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="2b5bd-127">Validation File</span></span>  <br/> |<span data-ttu-id="2b5bd-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2b5bd-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2b5bd-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="2b5bd-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="2b5bd-130">False</span><span class="sxs-lookup"><span data-stu-id="2b5bd-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2b5bd-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2b5bd-131">See also</span></span>



- [<span data-ttu-id="2b5bd-132">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2b5bd-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

