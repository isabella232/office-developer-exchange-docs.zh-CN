---
title: 规则 (RuleType)
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
ms.assetid: 259a1f62-b235-4964-88bf-2d1f1c05a563
description: Rule 元素包含一个规则并表示用户邮箱中的规则。
ms.openlocfilehash: cdbd21df235a62a9e201e1eaae1d82a8ac10cdd2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/01/2020
ms.locfileid: "44465077"
---
# <a name="rule-ruletype"></a><span data-ttu-id="f26e7-103">规则 (RuleType)</span><span class="sxs-lookup"><span data-stu-id="f26e7-103">Rule (RuleType)</span></span>

<span data-ttu-id="f26e7-104">**Rule**元素包含一个规则并表示用户邮箱中的规则。</span><span class="sxs-lookup"><span data-stu-id="f26e7-104">The **Rule** element contains a single rule and represents a rule in a user's mailbox.</span></span> 
  
```XML
<Rule>
    <RuleId>
    <DisplayName>
    <Priority>
    <IsEnabled>
    <IsNotSupported>
    <IsInError>
    <Conditions>
    <Exceptions>
    <Actions>
</Rule>
```

 <span data-ttu-id="f26e7-105">**RuleType**</span><span class="sxs-lookup"><span data-stu-id="f26e7-105">**RuleType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f26e7-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f26e7-106">Attributes and elements</span></span>

<span data-ttu-id="f26e7-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f26e7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f26e7-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="f26e7-108">Attributes</span></span>

<span data-ttu-id="f26e7-109">无。</span><span class="sxs-lookup"><span data-stu-id="f26e7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f26e7-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f26e7-110">Child elements</span></span>

|<span data-ttu-id="f26e7-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="f26e7-111">**Element**</span></span>|<span data-ttu-id="f26e7-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="f26e7-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f26e7-113">RuleId</span><span class="sxs-lookup"><span data-stu-id="f26e7-113">RuleId</span></span>](ruleid.md) <br/> |<span data-ttu-id="f26e7-114">指定规则标识符。</span><span class="sxs-lookup"><span data-stu-id="f26e7-114">Specifies the rule identifier.</span></span>  <br/> |
|[<span data-ttu-id="f26e7-115">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="f26e7-115">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="f26e7-116">包含规则的显示名称。</span><span class="sxs-lookup"><span data-stu-id="f26e7-116">Contains the display name of a rule.</span></span>  <br/> |
|[<span data-ttu-id="f26e7-117">Priority</span><span class="sxs-lookup"><span data-stu-id="f26e7-117">Priority</span></span>](priority.md) <br/> |<span data-ttu-id="f26e7-118">指示规则的运行顺序。</span><span class="sxs-lookup"><span data-stu-id="f26e7-118">Indicates the order in which a rule is to be run.</span></span>  <br/> |
|[<span data-ttu-id="f26e7-119">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="f26e7-119">IsEnabled</span></span>](isenabled.md) <br/> |<span data-ttu-id="f26e7-120">指示是否已启用该规则。</span><span class="sxs-lookup"><span data-stu-id="f26e7-120">Indicates whether the rule is enabled.</span></span>  <br/> |
|[<span data-ttu-id="f26e7-121">IsNotSupported</span><span class="sxs-lookup"><span data-stu-id="f26e7-121">IsNotSupported</span></span>](isnotsupported.md) <br/> |<span data-ttu-id="f26e7-122">指示是否不能使用托管代码 Api 修改规则。</span><span class="sxs-lookup"><span data-stu-id="f26e7-122">Indicates whether the rule cannot be modified with the managed code APIs.</span></span>  <br/> |
|[<span data-ttu-id="f26e7-123">IsInError</span><span class="sxs-lookup"><span data-stu-id="f26e7-123">IsInError</span></span>](isinerror.md) <br/> |<span data-ttu-id="f26e7-124">指示规则是否处于错误状态。</span><span class="sxs-lookup"><span data-stu-id="f26e7-124">Indicates whether the rule is in an error condition.</span></span>  <br/> |
|[<span data-ttu-id="f26e7-125">条件</span><span class="sxs-lookup"><span data-stu-id="f26e7-125">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="f26e7-126">标识在满足时将触发规则的规则操作的条件。</span><span class="sxs-lookup"><span data-stu-id="f26e7-126">Identifies the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="f26e7-127">异常</span><span class="sxs-lookup"><span data-stu-id="f26e7-127">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="f26e7-128">标识代表收件箱规则的所有可用的规则例外条件的例外。</span><span class="sxs-lookup"><span data-stu-id="f26e7-128">Identifies the exceptions that represent all the available rule exception conditions for the inbox rule.</span></span>  <br/> |
|[<span data-ttu-id="f26e7-129">Actions</span><span class="sxs-lookup"><span data-stu-id="f26e7-129">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="f26e7-130">表示在满足条件时对邮件执行的操作。</span><span class="sxs-lookup"><span data-stu-id="f26e7-130">Represents the actions to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f26e7-131">父元素</span><span class="sxs-lookup"><span data-stu-id="f26e7-131">Parent elements</span></span>

|<span data-ttu-id="f26e7-132">**元素**</span><span class="sxs-lookup"><span data-stu-id="f26e7-132">**Element**</span></span>|<span data-ttu-id="f26e7-133">**说明**</span><span class="sxs-lookup"><span data-stu-id="f26e7-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f26e7-134">CreateRuleOperation</span><span class="sxs-lookup"><span data-stu-id="f26e7-134">CreateRuleOperation</span></span>](createruleoperation.md) <br/> |<span data-ttu-id="f26e7-135">表示一个用于创建新规则的操作。</span><span class="sxs-lookup"><span data-stu-id="f26e7-135">Represents an operation to create a new rule.</span></span>  <br/> |
|[<span data-ttu-id="f26e7-136">InboxRules</span><span class="sxs-lookup"><span data-stu-id="f26e7-136">InboxRules</span></span>](inboxrules.md) <br/> |<span data-ttu-id="f26e7-137">表示用户邮箱中的一组规则。</span><span class="sxs-lookup"><span data-stu-id="f26e7-137">Represents an array of rules in the user's mailbox.</span></span>  <br/> |
|[<span data-ttu-id="f26e7-138">SetRuleOperation</span><span class="sxs-lookup"><span data-stu-id="f26e7-138">SetRuleOperation</span></span>](setruleoperation.md) <br/> |<span data-ttu-id="f26e7-139">表示用于更新现有规则的操作。</span><span class="sxs-lookup"><span data-stu-id="f26e7-139">Represents an operation to update an existing rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f26e7-140">文本值</span><span class="sxs-lookup"><span data-stu-id="f26e7-140">Text value</span></span>

<span data-ttu-id="f26e7-141">无。</span><span class="sxs-lookup"><span data-stu-id="f26e7-141">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f26e7-142">说明</span><span class="sxs-lookup"><span data-stu-id="f26e7-142">Remarks</span></span>

<span data-ttu-id="f26e7-143">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f26e7-143">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f26e7-144">元素信息</span><span class="sxs-lookup"><span data-stu-id="f26e7-144">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f26e7-145">命名空间</span><span class="sxs-lookup"><span data-stu-id="f26e7-145">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f26e7-146">架构名称</span><span class="sxs-lookup"><span data-stu-id="f26e7-146">Schema Name</span></span>  <br/> |<span data-ttu-id="f26e7-147">类型架构</span><span class="sxs-lookup"><span data-stu-id="f26e7-147">Types schema</span></span>  <br/> |
|<span data-ttu-id="f26e7-148">验证文件</span><span class="sxs-lookup"><span data-stu-id="f26e7-148">Validation File</span></span>  <br/> |<span data-ttu-id="f26e7-149">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f26e7-149">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f26e7-150">可以为空</span><span class="sxs-lookup"><span data-stu-id="f26e7-150">Can be Empty</span></span>  <br/> |<span data-ttu-id="f26e7-151">True</span><span class="sxs-lookup"><span data-stu-id="f26e7-151">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f26e7-152">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f26e7-152">See also</span></span>



[<span data-ttu-id="f26e7-153">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="f26e7-153">UpdateInboxRules</span></span>](updateinboxrules.md)
  
[<span data-ttu-id="f26e7-154">SetRuleOperation</span><span class="sxs-lookup"><span data-stu-id="f26e7-154">SetRuleOperation</span></span>](setruleoperation.md)
  
[<span data-ttu-id="f26e7-155">CreateRuleOperation</span><span class="sxs-lookup"><span data-stu-id="f26e7-155">CreateRuleOperation</span></span>](createruleoperation.md)


- [<span data-ttu-id="f26e7-156">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f26e7-156">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

