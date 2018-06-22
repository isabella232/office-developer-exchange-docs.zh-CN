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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753147"
---
# <a name="and-protectionruleandtype"></a><span data-ttu-id="92201-103">和 (ProtectionRuleAndType)</span><span class="sxs-lookup"><span data-stu-id="92201-103">And (ProtectionRuleAndType)</span></span>

<span data-ttu-id="92201-104">**和**元素指定的所有子元素必须都匹配计算结果为**true**。</span><span class="sxs-lookup"><span data-stu-id="92201-104">The **And** element specifies that all child elements must match to evaluate to **true**.</span></span>
  
```xml
<And>
   <AllInternal/>
   <And/>
   <RecipientIs/>
   <SenderDepartments/>
   <True/>
</And>
```

 <span data-ttu-id="92201-105">**ProtectionRuleAndType**</span><span class="sxs-lookup"><span data-stu-id="92201-105">**ProtectionRuleAndType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="92201-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="92201-106">Attributes and elements</span></span>

<span data-ttu-id="92201-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="92201-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="92201-108">属性</span><span class="sxs-lookup"><span data-stu-id="92201-108">Attributes</span></span>

<span data-ttu-id="92201-109">无。</span><span class="sxs-lookup"><span data-stu-id="92201-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="92201-110">子元素</span><span class="sxs-lookup"><span data-stu-id="92201-110">Child elements</span></span>

|<span data-ttu-id="92201-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="92201-111">**Element**</span></span>|<span data-ttu-id="92201-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="92201-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="92201-113">AllInternal</span><span class="sxs-lookup"><span data-stu-id="92201-113">AllInternal</span></span>](allinternal.md) <br/> |<span data-ttu-id="92201-114">如果所有收件人的电子邮件的发件人的组织内部的计算结果为**true** 。</span><span class="sxs-lookup"><span data-stu-id="92201-114">Evaluates to **true** if all recipients of an e-mail message are internal to the sender's organization.</span></span>  <br/> |
|<span data-ttu-id="92201-115">**And**</span><span class="sxs-lookup"><span data-stu-id="92201-115">**And**</span></span> <br/> |<span data-ttu-id="92201-116">指定所有子元素都必须匹配以使值为 **true**。</span><span class="sxs-lookup"><span data-stu-id="92201-116">Specifies that all child elements must match to evaluate to **true**.</span></span>  <br/> |
|[<span data-ttu-id="92201-117">RecipientIs</span><span class="sxs-lookup"><span data-stu-id="92201-117">RecipientIs</span></span>](recipientis.md) <br/> |<span data-ttu-id="92201-118">指定任何收件人的电子邮件匹配的任何子[值 (ProtectionRuleValueType)](value-protectionrulevaluetype.md)元素中指定的收件人。</span><span class="sxs-lookup"><span data-stu-id="92201-118">Specifies that any recipient of the e-mail message matches any of the specified recipients in the child [Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="92201-119">SenderDepartments</span><span class="sxs-lookup"><span data-stu-id="92201-119">SenderDepartments</span></span>](senderdepartments.md) <br/> |<span data-ttu-id="92201-120">指定发件人的部门匹配任何子[值 (ProtectionRuleValueType)](value-protectionrulevaluetype.md)元素中指定的部门。</span><span class="sxs-lookup"><span data-stu-id="92201-120">Specifies that the department of the sender matches any of the specified departments in the child [Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="92201-121">True</span><span class="sxs-lookup"><span data-stu-id="92201-121">True</span></span>](true.md) <br/> |<span data-ttu-id="92201-122">指定始终匹配条件。</span><span class="sxs-lookup"><span data-stu-id="92201-122">Specifies a condition that always matches.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="92201-123">父元素</span><span class="sxs-lookup"><span data-stu-id="92201-123">Parent elements</span></span>

|<span data-ttu-id="92201-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="92201-124">**Element**</span></span>|<span data-ttu-id="92201-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="92201-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="92201-126">条件</span><span class="sxs-lookup"><span data-stu-id="92201-126">Condition</span></span>](condition.md) <br/> |<span data-ttu-id="92201-127">确定要执行该规则的操作部分必须满足的条件。</span><span class="sxs-lookup"><span data-stu-id="92201-127">Identifies the condition that must be satisfied for the action part of the rule to be executed.</span></span>  <br/> |
|<span data-ttu-id="92201-128">**And**</span><span class="sxs-lookup"><span data-stu-id="92201-128">**And**</span></span> <br/> |<span data-ttu-id="92201-129">指定所有子元素都必须匹配以使值为 **true**。</span><span class="sxs-lookup"><span data-stu-id="92201-129">Specifies that all child elements must match to evaluate to **true**.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="92201-130">文本值</span><span class="sxs-lookup"><span data-stu-id="92201-130">Text value</span></span>

<span data-ttu-id="92201-131">无。</span><span class="sxs-lookup"><span data-stu-id="92201-131">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="92201-132">备注</span><span class="sxs-lookup"><span data-stu-id="92201-132">Remarks</span></span>

<span data-ttu-id="92201-133">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="92201-133">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="92201-134">元素信息</span><span class="sxs-lookup"><span data-stu-id="92201-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="92201-135">命名空间</span><span class="sxs-lookup"><span data-stu-id="92201-135">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="92201-136">架构名称</span><span class="sxs-lookup"><span data-stu-id="92201-136">Schema Name</span></span>  <br/> |<span data-ttu-id="92201-137">类型架构</span><span class="sxs-lookup"><span data-stu-id="92201-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="92201-138">验证文件</span><span class="sxs-lookup"><span data-stu-id="92201-138">Validation File</span></span>  <br/> |<span data-ttu-id="92201-139">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="92201-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="92201-140">可以为空</span><span class="sxs-lookup"><span data-stu-id="92201-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="92201-141">False</span><span class="sxs-lookup"><span data-stu-id="92201-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="92201-142">另请参阅</span><span class="sxs-lookup"><span data-stu-id="92201-142">See also</span></span>

- [<span data-ttu-id="92201-143">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="92201-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

