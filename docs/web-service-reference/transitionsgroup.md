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
description: TransitionsGroup 元素均表示一个数组所在的时区转换。
ms.openlocfilehash: e5991ad7f73a1694e0d4abadd8d252acc04970e5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838286"
---
# <a name="transitionsgroup"></a><span data-ttu-id="02255-103">TransitionsGroup</span><span class="sxs-lookup"><span data-stu-id="02255-103">TransitionsGroup</span></span>

<span data-ttu-id="02255-104">**TransitionsGroup**元素均表示一个数组所在的时区转换。</span><span class="sxs-lookup"><span data-stu-id="02255-104">The **TransitionsGroup** element represents an array of time zone transitions.</span></span> 
  
```xml
<TransitionsGroup Id="">
   <AbsoluteDateTransition/>
   <RecurringDayTransition/>
   <RecurringDateTransition/>
</TransitionsGroup>
```

 <span data-ttu-id="02255-105">**ArrayOfTransitionsType**</span><span class="sxs-lookup"><span data-stu-id="02255-105">**ArrayOfTransitionsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="02255-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="02255-106">Attributes and elements</span></span>

<span data-ttu-id="02255-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="02255-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="02255-108">属性</span><span class="sxs-lookup"><span data-stu-id="02255-108">Attributes</span></span>

|<span data-ttu-id="02255-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="02255-109">**Attribute**</span></span>|<span data-ttu-id="02255-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="02255-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="02255-111">Id</span><span class="sxs-lookup"><span data-stu-id="02255-111">Id</span></span>  <br/> |<span data-ttu-id="02255-112">一个字符串值，表示转换组的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="02255-112">A string value that represents the unique identifier of the transitions group.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="02255-113">子元素</span><span class="sxs-lookup"><span data-stu-id="02255-113">Child elements</span></span>

|<span data-ttu-id="02255-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="02255-114">**Element**</span></span>|<span data-ttu-id="02255-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="02255-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="02255-116">AbsoluteDateTransition</span><span class="sxs-lookup"><span data-stu-id="02255-116">AbsoluteDateTransition</span></span>](absolutedatetransition.md) <br/> |<span data-ttu-id="02255-117">代表在特定日期和在特定时间发生的时区转换。</span><span class="sxs-lookup"><span data-stu-id="02255-117">Represents a time zone transition that occurs on a specific date and at a specific time.</span></span>  <br/> |
|[<span data-ttu-id="02255-118">RecurringDayTransition</span><span class="sxs-lookup"><span data-stu-id="02255-118">RecurringDayTransition</span></span>](recurringdaytransition.md) <br/> |<span data-ttu-id="02255-119">表示时区转换发生在每年的同一天。</span><span class="sxs-lookup"><span data-stu-id="02255-119">Represents a time zone transition that occurs on the same day each year.</span></span>  <br/> |
|[<span data-ttu-id="02255-120">RecurringDateTransition</span><span class="sxs-lookup"><span data-stu-id="02255-120">RecurringDateTransition</span></span>](recurringdatetransition.md) <br/> |<span data-ttu-id="02255-121">表示在一年中的指定日期发生所在的时区转换。</span><span class="sxs-lookup"><span data-stu-id="02255-121">Represents a time zone transition that occurs on a specified day of the year.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="02255-122">父元素</span><span class="sxs-lookup"><span data-stu-id="02255-122">Parent elements</span></span>

|<span data-ttu-id="02255-123">**元素**</span><span class="sxs-lookup"><span data-stu-id="02255-123">**Element**</span></span>|<span data-ttu-id="02255-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="02255-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="02255-125">TransitionsGroups</span><span class="sxs-lookup"><span data-stu-id="02255-125">TransitionsGroups</span></span>](transitionsgroups.md) <br/> |<span data-ttu-id="02255-126">代表所在的时区转换组的数组。</span><span class="sxs-lookup"><span data-stu-id="02255-126">Represents an array of time zone transition groups.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="02255-127">注解</span><span class="sxs-lookup"><span data-stu-id="02255-127">Remarks</span></span>

<span data-ttu-id="02255-128">描述此元素的架构位于运行 Microsoft Exchange Server 已安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="02255-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="02255-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="02255-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="02255-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="02255-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="02255-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="02255-131">Schema Name</span></span>  <br/> |<span data-ttu-id="02255-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="02255-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="02255-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="02255-133">Validation File</span></span>  <br/> |<span data-ttu-id="02255-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="02255-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="02255-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="02255-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="02255-136">False</span><span class="sxs-lookup"><span data-stu-id="02255-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="02255-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="02255-137">See also</span></span>



- [<span data-ttu-id="02255-138">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="02255-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

