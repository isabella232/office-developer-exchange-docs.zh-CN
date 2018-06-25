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
description: Rule 元素包含单一规则并代表用户的邮箱中的规则。
ms.openlocfilehash: b1f9f058213543633335db11f03729964baf98ad
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827259"
---
# <a name="rule-ruletype"></a><span data-ttu-id="63844-103">规则 (RuleType)</span><span class="sxs-lookup"><span data-stu-id="63844-103">Rule (RuleType)</span></span>

<span data-ttu-id="63844-104">**Rule**元素包含单一规则并代表用户的邮箱中的规则。</span><span class="sxs-lookup"><span data-stu-id="63844-104">The **Rule** element contains a single rule and represents a rule in a user's mailbox.</span></span> 
  
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

 <span data-ttu-id="63844-105">**RuleType**</span><span class="sxs-lookup"><span data-stu-id="63844-105">**RuleType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="63844-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="63844-106">Attributes and elements</span></span>

<span data-ttu-id="63844-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="63844-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="63844-108">属性</span><span class="sxs-lookup"><span data-stu-id="63844-108">Attributes</span></span>

<span data-ttu-id="63844-109">无。</span><span class="sxs-lookup"><span data-stu-id="63844-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="63844-110">子元素</span><span class="sxs-lookup"><span data-stu-id="63844-110">Child elements</span></span>

|<span data-ttu-id="63844-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="63844-111">**Element**</span></span>|<span data-ttu-id="63844-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="63844-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="63844-113">规则 Id</span><span class="sxs-lookup"><span data-stu-id="63844-113">RuleId</span></span>](ruleid.md) <br/> |<span data-ttu-id="63844-114">指定规则标识符。</span><span class="sxs-lookup"><span data-stu-id="63844-114">Specifies the rule identifier.</span></span>  <br/> |
|[<span data-ttu-id="63844-115">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="63844-115">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="63844-116">包含规则的显示名称。</span><span class="sxs-lookup"><span data-stu-id="63844-116">Contains the display name of a rule.</span></span>  <br/> |
|[<span data-ttu-id="63844-117">Priority</span><span class="sxs-lookup"><span data-stu-id="63844-117">Priority</span></span>](priority.md) <br/> |<span data-ttu-id="63844-118">指示是用来运行规则的顺序。</span><span class="sxs-lookup"><span data-stu-id="63844-118">Indicates the order in which a rule is to be run.</span></span>  <br/> |
|[<span data-ttu-id="63844-119">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="63844-119">IsEnabled</span></span>](isenabled.md) <br/> |<span data-ttu-id="63844-120">指示是否启用规则。</span><span class="sxs-lookup"><span data-stu-id="63844-120">Indicates whether the rule is enabled.</span></span>  <br/> |
|[<span data-ttu-id="63844-121">IsNotSupported</span><span class="sxs-lookup"><span data-stu-id="63844-121">IsNotSupported</span></span>](isnotsupported.md) <br/> |<span data-ttu-id="63844-122">指示是否无法使用 Api 的托管代码修改该规则。</span><span class="sxs-lookup"><span data-stu-id="63844-122">Indicates whether the rule cannot be modified with the managed code APIs.</span></span>  <br/> |
|[<span data-ttu-id="63844-123">IsInError</span><span class="sxs-lookup"><span data-stu-id="63844-123">IsInError</span></span>](isinerror.md) <br/> |<span data-ttu-id="63844-124">指示规则是否处于错误状态。</span><span class="sxs-lookup"><span data-stu-id="63844-124">Indicates whether the rule is in an error condition.</span></span>  <br/> |
|[<span data-ttu-id="63844-125">条件</span><span class="sxs-lookup"><span data-stu-id="63844-125">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="63844-126">标识条件，履行时, 将触发规则的规则操作。</span><span class="sxs-lookup"><span data-stu-id="63844-126">Identifies the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="63844-127">异常</span><span class="sxs-lookup"><span data-stu-id="63844-127">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="63844-128">标识表示收件箱规则的所有可用规则例外条件的例外。</span><span class="sxs-lookup"><span data-stu-id="63844-128">Identifies the exceptions that represent all the available rule exception conditions for the inbox rule.</span></span>  <br/> |
|[<span data-ttu-id="63844-129">Actions</span><span class="sxs-lookup"><span data-stu-id="63844-129">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="63844-130">表示当满足条件时要采取的上一条消息的操作。</span><span class="sxs-lookup"><span data-stu-id="63844-130">Represents the actions to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="63844-131">父元素</span><span class="sxs-lookup"><span data-stu-id="63844-131">Parent elements</span></span>

|<span data-ttu-id="63844-132">**元素**</span><span class="sxs-lookup"><span data-stu-id="63844-132">**Element**</span></span>|<span data-ttu-id="63844-133">**说明**</span><span class="sxs-lookup"><span data-stu-id="63844-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="63844-134">CreateRuleOperation</span><span class="sxs-lookup"><span data-stu-id="63844-134">CreateRuleOperation</span></span>](createruleoperation.md) <br/> |<span data-ttu-id="63844-135">代表要创建新的规则操作。</span><span class="sxs-lookup"><span data-stu-id="63844-135">Represents an operation to create a new rule.</span></span>  <br/> |
|[<span data-ttu-id="63844-136">InboxRules</span><span class="sxs-lookup"><span data-stu-id="63844-136">InboxRules</span></span>](inboxrules.md) <br/> |<span data-ttu-id="63844-137">代表规则在用户的邮箱中的数组。</span><span class="sxs-lookup"><span data-stu-id="63844-137">Represents an array of rules in the user's mailbox.</span></span>  <br/> |
|[<span data-ttu-id="63844-138">SetRuleOperation</span><span class="sxs-lookup"><span data-stu-id="63844-138">SetRuleOperation</span></span>](setruleoperation.md) <br/> |<span data-ttu-id="63844-139">代表要更新现有规则的操作。</span><span class="sxs-lookup"><span data-stu-id="63844-139">Represents an operation to update an existing rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="63844-140">文本值</span><span class="sxs-lookup"><span data-stu-id="63844-140">Text value</span></span>

<span data-ttu-id="63844-141">无。</span><span class="sxs-lookup"><span data-stu-id="63844-141">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="63844-142">备注</span><span class="sxs-lookup"><span data-stu-id="63844-142">Remarks</span></span>

<span data-ttu-id="63844-143">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="63844-143">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="63844-144">元素信息</span><span class="sxs-lookup"><span data-stu-id="63844-144">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="63844-145">命名空间</span><span class="sxs-lookup"><span data-stu-id="63844-145">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="63844-146">架构名称</span><span class="sxs-lookup"><span data-stu-id="63844-146">Schema Name</span></span>  <br/> |<span data-ttu-id="63844-147">类型架构</span><span class="sxs-lookup"><span data-stu-id="63844-147">Types schema</span></span>  <br/> |
|<span data-ttu-id="63844-148">验证文件</span><span class="sxs-lookup"><span data-stu-id="63844-148">Validation File</span></span>  <br/> |<span data-ttu-id="63844-149">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="63844-149">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="63844-150">可以为空</span><span class="sxs-lookup"><span data-stu-id="63844-150">Can be Empty</span></span>  <br/> |<span data-ttu-id="63844-151">True</span><span class="sxs-lookup"><span data-stu-id="63844-151">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="63844-152">另请参阅</span><span class="sxs-lookup"><span data-stu-id="63844-152">See also</span></span>



[<span data-ttu-id="63844-153">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="63844-153">UpdateInboxRules</span></span>](updateinboxrules.md)
  
[<span data-ttu-id="63844-154">SetRuleOperation</span><span class="sxs-lookup"><span data-stu-id="63844-154">SetRuleOperation</span></span>](setruleoperation.md)
  
[<span data-ttu-id="63844-155">CreateRuleOperation</span><span class="sxs-lookup"><span data-stu-id="63844-155">CreateRuleOperation</span></span>](createruleoperation.md)


- [<span data-ttu-id="63844-156">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="63844-156">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

