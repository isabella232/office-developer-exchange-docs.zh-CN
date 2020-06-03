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
description: Rule 元素包含一个保护规则。
ms.openlocfilehash: 6c18a2bd026893cd333bc7007203abf04a6f0be7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464999"
---
# <a name="rule"></a><span data-ttu-id="43a6d-103">Rule</span><span class="sxs-lookup"><span data-stu-id="43a6d-103">Rule</span></span>

<span data-ttu-id="43a6d-104">**Rule**元素包含一个保护规则。</span><span class="sxs-lookup"><span data-stu-id="43a6d-104">The **Rule** element contains a single protection rule.</span></span> 
  
```XML
<Rule Name="" UserOverridable=="" Priority="">
   <Condition/>
   <Action/>
</Rule>
```

 <span data-ttu-id="43a6d-105">**ProtectionRuleType**</span><span class="sxs-lookup"><span data-stu-id="43a6d-105">**ProtectionRuleType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="43a6d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="43a6d-106">Attributes and elements</span></span>

<span data-ttu-id="43a6d-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="43a6d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="43a6d-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="43a6d-108">Attributes</span></span>

|<span data-ttu-id="43a6d-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="43a6d-109">**Attribute**</span></span>|<span data-ttu-id="43a6d-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="43a6d-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="43a6d-111">**名称**</span><span class="sxs-lookup"><span data-stu-id="43a6d-111">**Name**</span></span> <br/> |<span data-ttu-id="43a6d-112">标识规则的名称。</span><span class="sxs-lookup"><span data-stu-id="43a6d-112">Identifies the name of the rule.</span></span> <span data-ttu-id="43a6d-113">一个必需的 string 类型的属性，最小长度为1。</span><span class="sxs-lookup"><span data-stu-id="43a6d-113">A required attribute of type string with a minimum length of 1.</span></span>  <br/> |
|<span data-ttu-id="43a6d-114">**UserOverridable**</span><span class="sxs-lookup"><span data-stu-id="43a6d-114">**UserOverridable**</span></span> <br/> |<span data-ttu-id="43a6d-115">指定规则是否是必需的。</span><span class="sxs-lookup"><span data-stu-id="43a6d-115">Specifies whether the rule is mandatory.</span></span> <span data-ttu-id="43a6d-116">如果规则是必需的，则此属性值必须为**false**。</span><span class="sxs-lookup"><span data-stu-id="43a6d-116">If the rule is mandatory, this attribute value must be **false**.</span></span> <span data-ttu-id="43a6d-117">一个 Boolean 类型的必需属性。</span><span class="sxs-lookup"><span data-stu-id="43a6d-117">A required attribute of type Boolean.</span></span>  <br/> |
|<span data-ttu-id="43a6d-118">**Priority**</span><span class="sxs-lookup"><span data-stu-id="43a6d-118">**Priority**</span></span> <br/> |<span data-ttu-id="43a6d-119">指定规则优先级。</span><span class="sxs-lookup"><span data-stu-id="43a6d-119">Specifies the rule priority.</span></span> <span data-ttu-id="43a6d-120">类型为 int 且最小值为1的必需属性。</span><span class="sxs-lookup"><span data-stu-id="43a6d-120">A required attribute of type int with a minimum value of 1.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="43a6d-121">子元素</span><span class="sxs-lookup"><span data-stu-id="43a6d-121">Child elements</span></span>

|<span data-ttu-id="43a6d-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="43a6d-122">**Element**</span></span>|<span data-ttu-id="43a6d-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="43a6d-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="43a6d-124">条件</span><span class="sxs-lookup"><span data-stu-id="43a6d-124">Condition</span></span>](condition.md) <br/> |<span data-ttu-id="43a6d-125">确定要执行该规则的操作部分必须满足的条件。</span><span class="sxs-lookup"><span data-stu-id="43a6d-125">Identifies the condition that must be satisfied for the action part of the rule to be executed.</span></span>  <br/> |
|[<span data-ttu-id="43a6d-126">Action （ProtectionRuleActionType）</span><span class="sxs-lookup"><span data-stu-id="43a6d-126">Action (ProtectionRuleActionType)</span></span>](action-protectionruleactiontype.md) <br/> |<span data-ttu-id="43a6d-127">确定当规则的条件部分匹配时，必须执行的操作。</span><span class="sxs-lookup"><span data-stu-id="43a6d-127">Identifies what action must be executed if the condition part of the rule matches.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="43a6d-128">父元素</span><span class="sxs-lookup"><span data-stu-id="43a6d-128">Parent elements</span></span>

|<span data-ttu-id="43a6d-129">**元素**</span><span class="sxs-lookup"><span data-stu-id="43a6d-129">**Element**</span></span>|<span data-ttu-id="43a6d-130">**说明**</span><span class="sxs-lookup"><span data-stu-id="43a6d-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="43a6d-131">原则</span><span class="sxs-lookup"><span data-stu-id="43a6d-131">Rules </span></span>](rules-ex15websvcsotherref.md) <br/> |<span data-ttu-id="43a6d-132">包含保护规则的数组。</span><span class="sxs-lookup"><span data-stu-id="43a6d-132">Contains an array of protection rules.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="43a6d-133">文本值</span><span class="sxs-lookup"><span data-stu-id="43a6d-133">Text value</span></span>

<span data-ttu-id="43a6d-134">无。</span><span class="sxs-lookup"><span data-stu-id="43a6d-134">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="43a6d-135">说明</span><span class="sxs-lookup"><span data-stu-id="43a6d-135">Remarks</span></span>

<span data-ttu-id="43a6d-136">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="43a6d-136">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="43a6d-137">元素信息</span><span class="sxs-lookup"><span data-stu-id="43a6d-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="43a6d-138">命名空间</span><span class="sxs-lookup"><span data-stu-id="43a6d-138">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="43a6d-139">架构名称</span><span class="sxs-lookup"><span data-stu-id="43a6d-139">Schema Name</span></span>  <br/> |<span data-ttu-id="43a6d-140">类型架构</span><span class="sxs-lookup"><span data-stu-id="43a6d-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="43a6d-141">验证文件</span><span class="sxs-lookup"><span data-stu-id="43a6d-141">Validation File</span></span>  <br/> |<span data-ttu-id="43a6d-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="43a6d-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="43a6d-143">可以为空</span><span class="sxs-lookup"><span data-stu-id="43a6d-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="43a6d-144">False</span><span class="sxs-lookup"><span data-stu-id="43a6d-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="43a6d-145">另请参阅</span><span class="sxs-lookup"><span data-stu-id="43a6d-145">See also</span></span>



- [<span data-ttu-id="43a6d-146">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="43a6d-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

