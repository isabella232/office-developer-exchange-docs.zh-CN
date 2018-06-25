---
title: WithinDateRange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- WithinDateRange
api_type:
- schema
ms.assetid: 226aeb15-016f-45ca-992a-c137ba09ca08
description: WithinDateRange 元素指定在其中传入消息必须已收到的条件或例外的顺序应用中的日期范围。
ms.openlocfilehash: d85ef91c581008c2aafb06b1900c4514aebacd65
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838561"
---
# <a name="withindaterange"></a><span data-ttu-id="065c4-103">WithinDateRange</span><span class="sxs-lookup"><span data-stu-id="065c4-103">WithinDateRange</span></span>

<span data-ttu-id="065c4-104">**WithinDateRange**元素指定在其中传入消息必须已收到的条件或例外的顺序应用中的日期范围。</span><span class="sxs-lookup"><span data-stu-id="065c4-104">The **WithinDateRange** element specifies the date range within which incoming messages have to have been received in order for the condition or exception to apply.</span></span> 
  
```XML
<WithinDateRange>
     <StartDateTime/>
     <EndDateTime/>
</WithinDateRange>
```

 <span data-ttu-id="065c4-105">**RulePredicateDateRangeType**</span><span class="sxs-lookup"><span data-stu-id="065c4-105">**RulePredicateDateRangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="065c4-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="065c4-106">Attributes and elements</span></span>

<span data-ttu-id="065c4-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="065c4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="065c4-108">属性</span><span class="sxs-lookup"><span data-stu-id="065c4-108">Attributes</span></span>

<span data-ttu-id="065c4-109">无。</span><span class="sxs-lookup"><span data-stu-id="065c4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="065c4-110">子元素</span><span class="sxs-lookup"><span data-stu-id="065c4-110">Child elements</span></span>

|<span data-ttu-id="065c4-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="065c4-111">**Element**</span></span>|<span data-ttu-id="065c4-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="065c4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="065c4-113">开始日期时间</span><span class="sxs-lookup"><span data-stu-id="065c4-113">StartDateTime</span></span>](startdatetime.md) <br/> |<span data-ttu-id="065c4-114">指定时间段的规则，并指示的规则条件得到满足后此值。</span><span class="sxs-lookup"><span data-stu-id="065c4-114">Specifies the rule time period and indicates that the rule condition is met after this value.</span></span>  <br/> |
|[<span data-ttu-id="065c4-115">EndDateTime</span><span class="sxs-lookup"><span data-stu-id="065c4-115">EndDateTime</span></span>](enddatetime.md) <br/> |<span data-ttu-id="065c4-116">指定时间段的规则，并指示的规则条件得到满足此值之前。</span><span class="sxs-lookup"><span data-stu-id="065c4-116">Specifies the rule time period and indicates that the rule condition is met before this value.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="065c4-117">父元素</span><span class="sxs-lookup"><span data-stu-id="065c4-117">Parent elements</span></span>

|<span data-ttu-id="065c4-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="065c4-118">**Element**</span></span>|<span data-ttu-id="065c4-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="065c4-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="065c4-120">条件</span><span class="sxs-lookup"><span data-stu-id="065c4-120">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="065c4-121">表示履行时将触发规则的规则操作的条件。</span><span class="sxs-lookup"><span data-stu-id="065c4-121">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="065c4-122">异常</span><span class="sxs-lookup"><span data-stu-id="065c4-122">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="065c4-123">代表收件箱规则的所有可用规则例外条件。</span><span class="sxs-lookup"><span data-stu-id="065c4-123">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="065c4-124">文本值</span><span class="sxs-lookup"><span data-stu-id="065c4-124">Text value</span></span>

<span data-ttu-id="065c4-125">无。</span><span class="sxs-lookup"><span data-stu-id="065c4-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="065c4-126">备注</span><span class="sxs-lookup"><span data-stu-id="065c4-126">Remarks</span></span>

<span data-ttu-id="065c4-127">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="065c4-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="065c4-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="065c4-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="065c4-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="065c4-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="065c4-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="065c4-130">Schema Name</span></span>  <br/> |<span data-ttu-id="065c4-131">消息架构</span><span class="sxs-lookup"><span data-stu-id="065c4-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="065c4-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="065c4-132">Validation File</span></span>  <br/> |<span data-ttu-id="065c4-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="065c4-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="065c4-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="065c4-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="065c4-135">True</span><span class="sxs-lookup"><span data-stu-id="065c4-135">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="065c4-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="065c4-136">See also</span></span>



- [<span data-ttu-id="065c4-137">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="065c4-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

