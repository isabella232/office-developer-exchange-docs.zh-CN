---
title: TransitionsGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TransitionsGroup
api_type:
- schema
ms.assetid: 19d56080-546a-4d53-929e-363d56186759
description: TransitionsGroup 元素表示时区转换的数组。
ms.openlocfilehash: 9f08dec048d410dadab9580e7886b2499d943176
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467415"
---
# <a name="transitionsgroup"></a><span data-ttu-id="d326c-103">TransitionsGroup</span><span class="sxs-lookup"><span data-stu-id="d326c-103">TransitionsGroup</span></span>

<span data-ttu-id="d326c-104">**TransitionsGroup**元素表示时区转换的数组。</span><span class="sxs-lookup"><span data-stu-id="d326c-104">The **TransitionsGroup** element represents an array of time zone transitions.</span></span> 
  
```xml
<TransitionsGroup Id="">
   <AbsoluteDateTransition/>
   <RecurringDayTransition/>
   <RecurringDateTransition/>
</TransitionsGroup>
```

 <span data-ttu-id="d326c-105">**ArrayOfTransitionsType**</span><span class="sxs-lookup"><span data-stu-id="d326c-105">**ArrayOfTransitionsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d326c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d326c-106">Attributes and elements</span></span>

<span data-ttu-id="d326c-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d326c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d326c-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="d326c-108">Attributes</span></span>

|<span data-ttu-id="d326c-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="d326c-109">**Attribute**</span></span>|<span data-ttu-id="d326c-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="d326c-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d326c-111">Id</span><span class="sxs-lookup"><span data-stu-id="d326c-111">Id</span></span>  <br/> |<span data-ttu-id="d326c-112">一个 string 值，它代表转换组的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="d326c-112">A string value that represents the unique identifier of the transitions group.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d326c-113">子元素</span><span class="sxs-lookup"><span data-stu-id="d326c-113">Child elements</span></span>

|<span data-ttu-id="d326c-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="d326c-114">**Element**</span></span>|<span data-ttu-id="d326c-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="d326c-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d326c-116">AbsoluteDateTransition</span><span class="sxs-lookup"><span data-stu-id="d326c-116">AbsoluteDateTransition</span></span>](absolutedatetransition.md) <br/> |<span data-ttu-id="d326c-117">表示在特定日期和特定时间发生的时区转换。</span><span class="sxs-lookup"><span data-stu-id="d326c-117">Represents a time zone transition that occurs on a specific date and at a specific time.</span></span>  <br/> |
|[<span data-ttu-id="d326c-118">RecurringDayTransition</span><span class="sxs-lookup"><span data-stu-id="d326c-118">RecurringDayTransition</span></span>](recurringdaytransition.md) <br/> |<span data-ttu-id="d326c-119">表示时区转换发生在每年的同一天。</span><span class="sxs-lookup"><span data-stu-id="d326c-119">Represents a time zone transition that occurs on the same day each year.</span></span>  <br/> |
|[<span data-ttu-id="d326c-120">RecurringDateTransition</span><span class="sxs-lookup"><span data-stu-id="d326c-120">RecurringDateTransition</span></span>](recurringdatetransition.md) <br/> |<span data-ttu-id="d326c-121">表示在指定的一年中的某一天发生的时区转换。</span><span class="sxs-lookup"><span data-stu-id="d326c-121">Represents a time zone transition that occurs on a specified day of the year.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d326c-122">父元素</span><span class="sxs-lookup"><span data-stu-id="d326c-122">Parent elements</span></span>

|<span data-ttu-id="d326c-123">**元素**</span><span class="sxs-lookup"><span data-stu-id="d326c-123">**Element**</span></span>|<span data-ttu-id="d326c-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="d326c-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d326c-125">TransitionsGroups</span><span class="sxs-lookup"><span data-stu-id="d326c-125">TransitionsGroups</span></span>](transitionsgroups.md) <br/> |<span data-ttu-id="d326c-126">表示时区转换组的数组。</span><span class="sxs-lookup"><span data-stu-id="d326c-126">Represents an array of time zone transition groups.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d326c-127">备注</span><span class="sxs-lookup"><span data-stu-id="d326c-127">Remarks</span></span>

<span data-ttu-id="d326c-128">描述此元素的架构位于运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d326c-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d326c-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="d326c-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d326c-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="d326c-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d326c-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="d326c-131">Schema Name</span></span>  <br/> |<span data-ttu-id="d326c-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="d326c-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="d326c-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="d326c-133">Validation File</span></span>  <br/> |<span data-ttu-id="d326c-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d326c-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d326c-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="d326c-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="d326c-136">False</span><span class="sxs-lookup"><span data-stu-id="d326c-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d326c-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d326c-137">See also</span></span>



- [<span data-ttu-id="d326c-138">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d326c-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

