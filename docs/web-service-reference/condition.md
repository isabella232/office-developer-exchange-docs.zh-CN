---
title: Condition
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Condition
api_type:
- schema
ms.assetid: 0790a3f2-cb31-4036-a757-7821aa0722cb
description: Condition 元素标识规则执行的操作部分必须满足的条件。
ms.openlocfilehash: d49f2984799b15c0499af59abecbb34abe15f7c3
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353558"
---
# <a name="condition"></a><span data-ttu-id="254f8-103">Condition</span><span class="sxs-lookup"><span data-stu-id="254f8-103">Condition</span></span>

<span data-ttu-id="254f8-104">**Condition**元素标识规则执行的操作部分必须满足的条件。</span><span class="sxs-lookup"><span data-stu-id="254f8-104">The **Condition** element identifies the condition that must be satisfied for the action part of the rule to be executed.</span></span> 
  
```xml
<Condition>
   <AllInternal/>
</Condition>
```

```xml
<Condition> 
    <SenderDepartments/> 
</Condition>
```

```xml
<Condition> 
    <True/> 
</Condition>
```

```xml
<Condition> 
    <Recipients/> 
</Condition>
```

```xml
<Condition> 
    <And/> 
</Condition>
```

<span data-ttu-id="254f8-105">**ProtectionRuleConditionType**</span><span class="sxs-lookup"><span data-stu-id="254f8-105">**ProtectionRuleConditionType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="254f8-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="254f8-106">Attributes and elements</span></span>

<span data-ttu-id="254f8-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="254f8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="254f8-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="254f8-108">Attributes</span></span>

<span data-ttu-id="254f8-109">无。</span><span class="sxs-lookup"><span data-stu-id="254f8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="254f8-110">子元素</span><span class="sxs-lookup"><span data-stu-id="254f8-110">Child elements</span></span>

|<span data-ttu-id="254f8-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="254f8-111">**Element**</span></span>|<span data-ttu-id="254f8-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="254f8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="254f8-113">AllInternal</span><span class="sxs-lookup"><span data-stu-id="254f8-113">AllInternal</span></span>](allinternal.md) <br/> |<span data-ttu-id="254f8-114">如果所有收件人的电子邮件的发件人的组织内部的计算结果为**true** 。</span><span class="sxs-lookup"><span data-stu-id="254f8-114">Evaluates to **true** if all recipients of an e-mail message are internal to the sender's organization.</span></span>  <br/> |
|[<span data-ttu-id="254f8-115">和 (ProtectionRuleAndType)</span><span class="sxs-lookup"><span data-stu-id="254f8-115">And (ProtectionRuleAndType)</span></span>](and-protectionruleandtype.md) <br/> |<span data-ttu-id="254f8-116">指定所有子元素都必须匹配以使值为 **true**。</span><span class="sxs-lookup"><span data-stu-id="254f8-116">Specifies that all child elements must match to evaluate to **true**.</span></span> <span data-ttu-id="254f8-117">指定必须有多个保护规则子条件。</span><span class="sxs-lookup"><span data-stu-id="254f8-117">Specifies that there must be more than one protection rule child condition.</span></span>  <br/> |
|[<span data-ttu-id="254f8-118">RecipientIs</span><span class="sxs-lookup"><span data-stu-id="254f8-118">RecipientIs</span></span>](recipientis.md) <br/> |<span data-ttu-id="254f8-119">指定任何收件人的电子邮件匹配的任何子[值 (ProtectionRuleValueType)](value-protectionrulevaluetype.md)元素中指定的收件人。</span><span class="sxs-lookup"><span data-stu-id="254f8-119">Specifies that any recipient of the e-mail message matches any of the specified recipients in the child [Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="254f8-120">SenderDepartments</span><span class="sxs-lookup"><span data-stu-id="254f8-120">SenderDepartments</span></span>](senderdepartments.md) <br/> |<span data-ttu-id="254f8-121">指定发件人的部门匹配任何子[值 (ProtectionRuleValueType)](value-protectionrulevaluetype.md)元素中指定的部门。</span><span class="sxs-lookup"><span data-stu-id="254f8-121">Specifies that the department of the sender matches any of the specified departments in the child [Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="254f8-122">True</span><span class="sxs-lookup"><span data-stu-id="254f8-122">True</span></span>](true.md) <br/> |<span data-ttu-id="254f8-123">指定始终匹配条件。</span><span class="sxs-lookup"><span data-stu-id="254f8-123">Specifies a condition that always matches.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="254f8-124">父元素</span><span class="sxs-lookup"><span data-stu-id="254f8-124">Parent elements</span></span>

|<span data-ttu-id="254f8-125">**元素**</span><span class="sxs-lookup"><span data-stu-id="254f8-125">**Element**</span></span>|<span data-ttu-id="254f8-126">**说明**</span><span class="sxs-lookup"><span data-stu-id="254f8-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="254f8-127">Rule</span><span class="sxs-lookup"><span data-stu-id="254f8-127">Rule</span></span>](rule.md) <br/> |<span data-ttu-id="254f8-128">包含单个保护规则。</span><span class="sxs-lookup"><span data-stu-id="254f8-128">Contains a single protection rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="254f8-129">文本值</span><span class="sxs-lookup"><span data-stu-id="254f8-129">Text value</span></span>

<span data-ttu-id="254f8-130">无。</span><span class="sxs-lookup"><span data-stu-id="254f8-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="254f8-131">说明</span><span class="sxs-lookup"><span data-stu-id="254f8-131">Remarks</span></span>

<span data-ttu-id="254f8-132">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="254f8-132">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="254f8-133">元素信息</span><span class="sxs-lookup"><span data-stu-id="254f8-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="254f8-134">命名空间</span><span class="sxs-lookup"><span data-stu-id="254f8-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="254f8-135">架构名称</span><span class="sxs-lookup"><span data-stu-id="254f8-135">Schema Name</span></span>  <br/> |<span data-ttu-id="254f8-136">类型架构</span><span class="sxs-lookup"><span data-stu-id="254f8-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="254f8-137">验证文件</span><span class="sxs-lookup"><span data-stu-id="254f8-137">Validation File</span></span>  <br/> |<span data-ttu-id="254f8-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="254f8-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="254f8-139">可以为空</span><span class="sxs-lookup"><span data-stu-id="254f8-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="254f8-140">False</span><span class="sxs-lookup"><span data-stu-id="254f8-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="254f8-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="254f8-141">See also</span></span>

- [<span data-ttu-id="254f8-142">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="254f8-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

