---
title: Rule
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Rule
api_type:
- schema
ms.assetid: c30f3851-bd56-4473-9106-dc85e9619486
description: Rule 元素包含单个保护规则。
ms.openlocfilehash: 9abbb70381c214211172d2d5ba1ed43ee4797f17
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827263"
---
# <a name="rule"></a><span data-ttu-id="a4c41-103">Rule</span><span class="sxs-lookup"><span data-stu-id="a4c41-103">Rule</span></span>

<span data-ttu-id="a4c41-104">**Rule**元素包含单个保护规则。</span><span class="sxs-lookup"><span data-stu-id="a4c41-104">The **Rule** element contains a single protection rule.</span></span> 
  
```XML
<Rule Name="" UserOverridable=="" Priority="">
   <Condition/>
   <Action/>
</Rule>
```

 <span data-ttu-id="a4c41-105">**ProtectionRuleType**</span><span class="sxs-lookup"><span data-stu-id="a4c41-105">**ProtectionRuleType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a4c41-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a4c41-106">Attributes and elements</span></span>

<span data-ttu-id="a4c41-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a4c41-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a4c41-108">属性</span><span class="sxs-lookup"><span data-stu-id="a4c41-108">Attributes</span></span>

|<span data-ttu-id="a4c41-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="a4c41-109">**Attribute**</span></span>|<span data-ttu-id="a4c41-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="a4c41-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a4c41-111">**名称**</span><span class="sxs-lookup"><span data-stu-id="a4c41-111">**Name**</span></span> <br/> |<span data-ttu-id="a4c41-112">标识该规则的名称。</span><span class="sxs-lookup"><span data-stu-id="a4c41-112">Identifies the name of the rule.</span></span> <span data-ttu-id="a4c41-113">Required 的属性字符串类型的最小长度为 1。</span><span class="sxs-lookup"><span data-stu-id="a4c41-113">A required attribute of type string with a minimum length of 1.</span></span>  <br/> |
|<span data-ttu-id="a4c41-114">**UserOverridable**</span><span class="sxs-lookup"><span data-stu-id="a4c41-114">**UserOverridable**</span></span> <br/> |<span data-ttu-id="a4c41-115">指定是否强制规则。</span><span class="sxs-lookup"><span data-stu-id="a4c41-115">Specifies whether the rule is mandatory.</span></span> <span data-ttu-id="a4c41-116">如果规则是必需的此属性的值必须是**false**。</span><span class="sxs-lookup"><span data-stu-id="a4c41-116">If the rule is mandatory, this attribute value must be **false**.</span></span> <span data-ttu-id="a4c41-117">布尔类型所需的属性。</span><span class="sxs-lookup"><span data-stu-id="a4c41-117">A required attribute of type Boolean.</span></span>  <br/> |
|<span data-ttu-id="a4c41-118">**Priority**</span><span class="sxs-lookup"><span data-stu-id="a4c41-118">**Priority**</span></span> <br/> |<span data-ttu-id="a4c41-119">指定规则的优先级。</span><span class="sxs-lookup"><span data-stu-id="a4c41-119">Specifies the rule priority.</span></span> <span data-ttu-id="a4c41-120">Int 类型的最小值为 1 必需的属性。</span><span class="sxs-lookup"><span data-stu-id="a4c41-120">A required attribute of type int with a minimum value of 1.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a4c41-121">子元素</span><span class="sxs-lookup"><span data-stu-id="a4c41-121">Child elements</span></span>

|<span data-ttu-id="a4c41-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="a4c41-122">**Element**</span></span>|<span data-ttu-id="a4c41-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="a4c41-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a4c41-124">条件</span><span class="sxs-lookup"><span data-stu-id="a4c41-124">Condition</span></span>](condition.md) <br/> |<span data-ttu-id="a4c41-125">确定要执行该规则的操作部分必须满足的条件。</span><span class="sxs-lookup"><span data-stu-id="a4c41-125">Identifies the condition that must be satisfied for the action part of the rule to be executed.</span></span>  <br/> |
|[<span data-ttu-id="a4c41-126">操作 (ProtectionRuleActionType)</span><span class="sxs-lookup"><span data-stu-id="a4c41-126">Action (ProtectionRuleActionType)</span></span>](action-protectionruleactiontype.md) <br/> |<span data-ttu-id="a4c41-127">标识必须执行哪些操作，如果该规则的条件部分匹配。</span><span class="sxs-lookup"><span data-stu-id="a4c41-127">Identifies what action must be executed if the condition part of the rule matches.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a4c41-128">父元素</span><span class="sxs-lookup"><span data-stu-id="a4c41-128">Parent elements</span></span>

|<span data-ttu-id="a4c41-129">**元素**</span><span class="sxs-lookup"><span data-stu-id="a4c41-129">**Element**</span></span>|<span data-ttu-id="a4c41-130">**说明**</span><span class="sxs-lookup"><span data-stu-id="a4c41-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a4c41-131">规则</span><span class="sxs-lookup"><span data-stu-id="a4c41-131">Rules </span></span>](rules-ex15websvcsotherref.md) <br/> |<span data-ttu-id="a4c41-132">包含数组保护规则。</span><span class="sxs-lookup"><span data-stu-id="a4c41-132">Contains an array of protection rules.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a4c41-133">文本值</span><span class="sxs-lookup"><span data-stu-id="a4c41-133">Text value</span></span>

<span data-ttu-id="a4c41-134">无。</span><span class="sxs-lookup"><span data-stu-id="a4c41-134">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a4c41-135">备注</span><span class="sxs-lookup"><span data-stu-id="a4c41-135">Remarks</span></span>

<span data-ttu-id="a4c41-136">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a4c41-136">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a4c41-137">元素信息</span><span class="sxs-lookup"><span data-stu-id="a4c41-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a4c41-138">命名空间</span><span class="sxs-lookup"><span data-stu-id="a4c41-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a4c41-139">架构名称</span><span class="sxs-lookup"><span data-stu-id="a4c41-139">Schema Name</span></span>  <br/> |<span data-ttu-id="a4c41-140">类型架构</span><span class="sxs-lookup"><span data-stu-id="a4c41-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="a4c41-141">验证文件</span><span class="sxs-lookup"><span data-stu-id="a4c41-141">Validation File</span></span>  <br/> |<span data-ttu-id="a4c41-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a4c41-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a4c41-143">可以为空</span><span class="sxs-lookup"><span data-stu-id="a4c41-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="a4c41-144">False</span><span class="sxs-lookup"><span data-stu-id="a4c41-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a4c41-145">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a4c41-145">See also</span></span>



- [<span data-ttu-id="a4c41-146">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a4c41-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

