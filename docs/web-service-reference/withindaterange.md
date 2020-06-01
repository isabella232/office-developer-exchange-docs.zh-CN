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
description: WithinDateRange 元素指定要在其中接收传入邮件的日期范围，以便条件或例外情况适用。
ms.openlocfilehash: ef5fb15b64ee4f7060f907818c4ebd4367ced5e7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461847"
---
# <a name="withindaterange"></a><span data-ttu-id="b4174-103">WithinDateRange</span><span class="sxs-lookup"><span data-stu-id="b4174-103">WithinDateRange</span></span>

<span data-ttu-id="b4174-104">**WithinDateRange**元素指定要在其中接收传入邮件的日期范围，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="b4174-104">The **WithinDateRange** element specifies the date range within which incoming messages have to have been received in order for the condition or exception to apply.</span></span> 
  
```XML
<WithinDateRange>
     <StartDateTime/>
     <EndDateTime/>
</WithinDateRange>
```

 <span data-ttu-id="b4174-105">**RulePredicateDateRangeType**</span><span class="sxs-lookup"><span data-stu-id="b4174-105">**RulePredicateDateRangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b4174-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b4174-106">Attributes and elements</span></span>

<span data-ttu-id="b4174-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b4174-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b4174-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="b4174-108">Attributes</span></span>

<span data-ttu-id="b4174-109">无。</span><span class="sxs-lookup"><span data-stu-id="b4174-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b4174-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b4174-110">Child elements</span></span>

|<span data-ttu-id="b4174-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="b4174-111">**Element**</span></span>|<span data-ttu-id="b4174-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="b4174-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b4174-113">StartDateTime</span><span class="sxs-lookup"><span data-stu-id="b4174-113">StartDateTime</span></span>](startdatetime.md) <br/> |<span data-ttu-id="b4174-114">指定规则时间段，并指示在此值之后满足规则条件。</span><span class="sxs-lookup"><span data-stu-id="b4174-114">Specifies the rule time period and indicates that the rule condition is met after this value.</span></span>  <br/> |
|[<span data-ttu-id="b4174-115">EndDateTime</span><span class="sxs-lookup"><span data-stu-id="b4174-115">EndDateTime</span></span>](enddatetime.md) <br/> |<span data-ttu-id="b4174-116">指定规则时间段，并指示在此值之前满足规则条件。</span><span class="sxs-lookup"><span data-stu-id="b4174-116">Specifies the rule time period and indicates that the rule condition is met before this value.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b4174-117">父元素</span><span class="sxs-lookup"><span data-stu-id="b4174-117">Parent elements</span></span>

|<span data-ttu-id="b4174-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="b4174-118">**Element**</span></span>|<span data-ttu-id="b4174-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="b4174-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b4174-120">条件</span><span class="sxs-lookup"><span data-stu-id="b4174-120">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="b4174-121">表示履行时将触发规则的规则操作的条件。</span><span class="sxs-lookup"><span data-stu-id="b4174-121">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="b4174-122">异常</span><span class="sxs-lookup"><span data-stu-id="b4174-122">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="b4174-123">代表收件箱规则的所有可用的规则例外条件。</span><span class="sxs-lookup"><span data-stu-id="b4174-123">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b4174-124">文本值</span><span class="sxs-lookup"><span data-stu-id="b4174-124">Text value</span></span>

<span data-ttu-id="b4174-125">无。</span><span class="sxs-lookup"><span data-stu-id="b4174-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b4174-126">说明</span><span class="sxs-lookup"><span data-stu-id="b4174-126">Remarks</span></span>

<span data-ttu-id="b4174-127">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b4174-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b4174-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="b4174-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b4174-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="b4174-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b4174-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="b4174-130">Schema Name</span></span>  <br/> |<span data-ttu-id="b4174-131">消息架构</span><span class="sxs-lookup"><span data-stu-id="b4174-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b4174-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="b4174-132">Validation File</span></span>  <br/> |<span data-ttu-id="b4174-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b4174-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b4174-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="b4174-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="b4174-135">True</span><span class="sxs-lookup"><span data-stu-id="b4174-135">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b4174-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b4174-136">See also</span></span>



- [<span data-ttu-id="b4174-137">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b4174-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

