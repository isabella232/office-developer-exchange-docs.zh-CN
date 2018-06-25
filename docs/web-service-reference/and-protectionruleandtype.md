---
title: 和 (ProtectionRuleAndType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- And
api_type:
- schema
ms.assetid: 7fafd1c8-cd29-43a0-b383-f6595f934f48
description: And 元素指定所有子元素必须都匹配来计算结果为 true。
ms.openlocfilehash: 9e0128ee3fa2b6ffdc5975946694475afec53c25
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753147"
---
# <a name="and-protectionruleandtype"></a><span data-ttu-id="4c5bd-103">和 (ProtectionRuleAndType)</span><span class="sxs-lookup"><span data-stu-id="4c5bd-103">And (ProtectionRuleAndType)</span></span>

<span data-ttu-id="4c5bd-104">**和**元素指定的所有子元素必须都匹配计算结果为**true**。</span><span class="sxs-lookup"><span data-stu-id="4c5bd-104">The **And** element specifies that all child elements must match to evaluate to **true**.</span></span>
  
```xml
<And>
   <AllInternal/>
   <And/>
   <RecipientIs/>
   <SenderDepartments/>
   <True/>
</And>
```

 <span data-ttu-id="4c5bd-105">**ProtectionRuleAndType**</span><span class="sxs-lookup"><span data-stu-id="4c5bd-105">**ProtectionRuleAndType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4c5bd-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4c5bd-106">Attributes and elements</span></span>

<span data-ttu-id="4c5bd-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4c5bd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4c5bd-108">属性</span><span class="sxs-lookup"><span data-stu-id="4c5bd-108">Attributes</span></span>

<span data-ttu-id="4c5bd-109">无。</span><span class="sxs-lookup"><span data-stu-id="4c5bd-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4c5bd-110">子元素</span><span class="sxs-lookup"><span data-stu-id="4c5bd-110">Child elements</span></span>

|<span data-ttu-id="4c5bd-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="4c5bd-111">**Element**</span></span>|<span data-ttu-id="4c5bd-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="4c5bd-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4c5bd-113">AllInternal</span><span class="sxs-lookup"><span data-stu-id="4c5bd-113">AllInternal</span></span>](allinternal.md) <br/> |<span data-ttu-id="4c5bd-114">如果所有收件人的电子邮件的发件人的组织内部的计算结果为**true** 。</span><span class="sxs-lookup"><span data-stu-id="4c5bd-114">Evaluates to **true** if all recipients of an e-mail message are internal to the sender's organization.</span></span>  <br/> |
|<span data-ttu-id="4c5bd-115">**And**</span><span class="sxs-lookup"><span data-stu-id="4c5bd-115">**And**</span></span> <br/> |<span data-ttu-id="4c5bd-116">指定所有子元素都必须匹配以使值为 **true**。</span><span class="sxs-lookup"><span data-stu-id="4c5bd-116">Specifies that all child elements must match to evaluate to **true**.</span></span>  <br/> |
|[<span data-ttu-id="4c5bd-117">RecipientIs</span><span class="sxs-lookup"><span data-stu-id="4c5bd-117">RecipientIs</span></span>](recipientis.md) <br/> |<span data-ttu-id="4c5bd-118">指定任何收件人的电子邮件匹配的任何子[值 (ProtectionRuleValueType)](value-protectionrulevaluetype.md)元素中指定的收件人。</span><span class="sxs-lookup"><span data-stu-id="4c5bd-118">Specifies that any recipient of the e-mail message matches any of the specified recipients in the child [Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="4c5bd-119">SenderDepartments</span><span class="sxs-lookup"><span data-stu-id="4c5bd-119">SenderDepartments</span></span>](senderdepartments.md) <br/> |<span data-ttu-id="4c5bd-120">指定发件人的部门匹配任何子[值 (ProtectionRuleValueType)](value-protectionrulevaluetype.md)元素中指定的部门。</span><span class="sxs-lookup"><span data-stu-id="4c5bd-120">Specifies that the department of the sender matches any of the specified departments in the child [Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="4c5bd-121">True</span><span class="sxs-lookup"><span data-stu-id="4c5bd-121">True</span></span>](true.md) <br/> |<span data-ttu-id="4c5bd-122">指定始终匹配条件。</span><span class="sxs-lookup"><span data-stu-id="4c5bd-122">Specifies a condition that always matches.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4c5bd-123">父元素</span><span class="sxs-lookup"><span data-stu-id="4c5bd-123">Parent elements</span></span>

|<span data-ttu-id="4c5bd-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="4c5bd-124">**Element**</span></span>|<span data-ttu-id="4c5bd-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="4c5bd-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4c5bd-126">条件</span><span class="sxs-lookup"><span data-stu-id="4c5bd-126">Condition</span></span>](condition.md) <br/> |<span data-ttu-id="4c5bd-127">确定要执行该规则的操作部分必须满足的条件。</span><span class="sxs-lookup"><span data-stu-id="4c5bd-127">Identifies the condition that must be satisfied for the action part of the rule to be executed.</span></span>  <br/> |
|<span data-ttu-id="4c5bd-128">**And**</span><span class="sxs-lookup"><span data-stu-id="4c5bd-128">**And**</span></span> <br/> |<span data-ttu-id="4c5bd-129">指定所有子元素都必须匹配以使值为 **true**。</span><span class="sxs-lookup"><span data-stu-id="4c5bd-129">Specifies that all child elements must match to evaluate to **true**.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4c5bd-130">文本值</span><span class="sxs-lookup"><span data-stu-id="4c5bd-130">Text value</span></span>

<span data-ttu-id="4c5bd-131">无。</span><span class="sxs-lookup"><span data-stu-id="4c5bd-131">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4c5bd-132">备注</span><span class="sxs-lookup"><span data-stu-id="4c5bd-132">Remarks</span></span>

<span data-ttu-id="4c5bd-133">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4c5bd-133">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4c5bd-134">元素信息</span><span class="sxs-lookup"><span data-stu-id="4c5bd-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4c5bd-135">命名空间</span><span class="sxs-lookup"><span data-stu-id="4c5bd-135">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4c5bd-136">架构名称</span><span class="sxs-lookup"><span data-stu-id="4c5bd-136">Schema Name</span></span>  <br/> |<span data-ttu-id="4c5bd-137">类型架构</span><span class="sxs-lookup"><span data-stu-id="4c5bd-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="4c5bd-138">验证文件</span><span class="sxs-lookup"><span data-stu-id="4c5bd-138">Validation File</span></span>  <br/> |<span data-ttu-id="4c5bd-139">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4c5bd-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4c5bd-140">可以为空</span><span class="sxs-lookup"><span data-stu-id="4c5bd-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="4c5bd-141">False</span><span class="sxs-lookup"><span data-stu-id="4c5bd-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4c5bd-142">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4c5bd-142">See also</span></span>

- [<span data-ttu-id="4c5bd-143">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="4c5bd-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

