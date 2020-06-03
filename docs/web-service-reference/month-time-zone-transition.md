---
title: Month （时区转换）
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
description: Month 元素表示发生时区转换的月份。
ms.openlocfilehash: 1fa32ea355cc3fe826f9c34b2fd147a0d8201673
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467737"
---
# <a name="month-time-zone-transition"></a><span data-ttu-id="75958-103">Month （时区转换）</span><span class="sxs-lookup"><span data-stu-id="75958-103">Month (Time Zone Transition)</span></span>

<span data-ttu-id="75958-104">**Month**元素表示发生时区转换的月份。</span><span class="sxs-lookup"><span data-stu-id="75958-104">The **Month** element represents the month in which the time zone transition occurs.</span></span> 
  
```xml
<Month/>
```

 <span data-ttu-id="75958-105">**int**</span><span class="sxs-lookup"><span data-stu-id="75958-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="75958-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="75958-106">Attributes and elements</span></span>

<span data-ttu-id="75958-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="75958-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="75958-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="75958-108">Attributes</span></span>

<span data-ttu-id="75958-109">无。</span><span class="sxs-lookup"><span data-stu-id="75958-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="75958-110">子元素</span><span class="sxs-lookup"><span data-stu-id="75958-110">Child elements</span></span>

<span data-ttu-id="75958-111">无。</span><span class="sxs-lookup"><span data-stu-id="75958-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="75958-112">父元素</span><span class="sxs-lookup"><span data-stu-id="75958-112">Parent elements</span></span>

|<span data-ttu-id="75958-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="75958-113">**Element**</span></span>|<span data-ttu-id="75958-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="75958-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="75958-115">RecurringDateTransition</span><span class="sxs-lookup"><span data-stu-id="75958-115">RecurringDateTransition</span></span>](recurringdatetransition.md) <br/> |<span data-ttu-id="75958-116">表示每年的特定日期发生的时区转换。</span><span class="sxs-lookup"><span data-stu-id="75958-116">Represents a time zone transition that occurs on a specific date each year.</span></span>  <br/> |
|[<span data-ttu-id="75958-117">RecurringDayTransition</span><span class="sxs-lookup"><span data-stu-id="75958-117">RecurringDayTransition</span></span>](recurringdaytransition.md) <br/> |<span data-ttu-id="75958-118">表示时区转换发生在每年的同一天。</span><span class="sxs-lookup"><span data-stu-id="75958-118">Represents a time zone transition that occurs on the same day each year.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="75958-119">文本值</span><span class="sxs-lookup"><span data-stu-id="75958-119">Text value</span></span>

<span data-ttu-id="75958-120">Text 值是一个整数，表示发生时区转换的月份。</span><span class="sxs-lookup"><span data-stu-id="75958-120">The text value is an integer that represents the month in which the time zone transition occurs.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="75958-121">备注</span><span class="sxs-lookup"><span data-stu-id="75958-121">Remarks</span></span>

<span data-ttu-id="75958-122">描述此元素的架构位于运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="75958-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="75958-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="75958-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="75958-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="75958-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="75958-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="75958-125">Schema Name</span></span>  <br/> |<span data-ttu-id="75958-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="75958-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="75958-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="75958-127">Validation File</span></span>  <br/> |<span data-ttu-id="75958-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="75958-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="75958-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="75958-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="75958-130">False</span><span class="sxs-lookup"><span data-stu-id="75958-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="75958-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="75958-131">See also</span></span>



- [<span data-ttu-id="75958-132">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="75958-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

