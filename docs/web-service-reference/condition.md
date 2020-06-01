---
title: 条件
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
description: Condition 元素标识要执行的规则的操作部分必须满足的条件。
ms.openlocfilehash: 2aea11197f072a4dbe21292bb47075d6f273d31b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463221"
---
# <a name="condition"></a><span data-ttu-id="06220-103">条件</span><span class="sxs-lookup"><span data-stu-id="06220-103">Condition</span></span>

<span data-ttu-id="06220-104">**Condition**元素标识要执行的规则的操作部分必须满足的条件。</span><span class="sxs-lookup"><span data-stu-id="06220-104">The **Condition** element identifies the condition that must be satisfied for the action part of the rule to be executed.</span></span> 
  
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

<span data-ttu-id="06220-105">**ProtectionRuleConditionType**</span><span class="sxs-lookup"><span data-stu-id="06220-105">**ProtectionRuleConditionType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="06220-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="06220-106">Attributes and elements</span></span>

<span data-ttu-id="06220-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="06220-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="06220-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="06220-108">Attributes</span></span>

<span data-ttu-id="06220-109">无。</span><span class="sxs-lookup"><span data-stu-id="06220-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="06220-110">子元素</span><span class="sxs-lookup"><span data-stu-id="06220-110">Child elements</span></span>

|<span data-ttu-id="06220-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="06220-111">**Element**</span></span>|<span data-ttu-id="06220-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="06220-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="06220-113">AllInternal</span><span class="sxs-lookup"><span data-stu-id="06220-113">AllInternal</span></span>](allinternal.md) <br/> |<span data-ttu-id="06220-114">如果电子邮件的所有收件人均为发件人的组织内部，则计算结果为**true** 。</span><span class="sxs-lookup"><span data-stu-id="06220-114">Evaluates to **true** if all recipients of an e-mail message are internal to the sender's organization.</span></span>  <br/> |
|[<span data-ttu-id="06220-115">和 (ProtectionRuleAndType)</span><span class="sxs-lookup"><span data-stu-id="06220-115">And (ProtectionRuleAndType)</span></span>](and-protectionruleandtype.md) <br/> |<span data-ttu-id="06220-116">指定所有子元素都必须匹配以使值为 **true**。</span><span class="sxs-lookup"><span data-stu-id="06220-116">Specifies that all child elements must match to evaluate to **true**.</span></span> <span data-ttu-id="06220-117">指定必须存在不止一个 "保护规则" 子条件。</span><span class="sxs-lookup"><span data-stu-id="06220-117">Specifies that there must be more than one protection rule child condition.</span></span>  <br/> |
|[<span data-ttu-id="06220-118">收件人是</span><span class="sxs-lookup"><span data-stu-id="06220-118">RecipientIs</span></span>](recipientis.md) <br/> |<span data-ttu-id="06220-119">指定电子邮件的任何收件人与子[值（ProtectionRuleValueType）](value-protectionrulevaluetype.md)元素中的任何指定收件人相匹配。</span><span class="sxs-lookup"><span data-stu-id="06220-119">Specifies that any recipient of the e-mail message matches any of the specified recipients in the child [Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="06220-120">SenderDepartments</span><span class="sxs-lookup"><span data-stu-id="06220-120">SenderDepartments</span></span>](senderdepartments.md) <br/> |<span data-ttu-id="06220-121">指定发件人的部门与子[值（ProtectionRuleValueType）](value-protectionrulevaluetype.md)元素中的任何指定的部门相匹配。</span><span class="sxs-lookup"><span data-stu-id="06220-121">Specifies that the department of the sender matches any of the specified departments in the child [Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="06220-122">True</span><span class="sxs-lookup"><span data-stu-id="06220-122">True</span></span>](true.md) <br/> |<span data-ttu-id="06220-123">指定始终匹配的条件。</span><span class="sxs-lookup"><span data-stu-id="06220-123">Specifies a condition that always matches.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="06220-124">父元素</span><span class="sxs-lookup"><span data-stu-id="06220-124">Parent elements</span></span>

|<span data-ttu-id="06220-125">**元素**</span><span class="sxs-lookup"><span data-stu-id="06220-125">**Element**</span></span>|<span data-ttu-id="06220-126">**说明**</span><span class="sxs-lookup"><span data-stu-id="06220-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="06220-127">Rule</span><span class="sxs-lookup"><span data-stu-id="06220-127">Rule</span></span>](rule.md) <br/> |<span data-ttu-id="06220-128">包含一个保护规则。</span><span class="sxs-lookup"><span data-stu-id="06220-128">Contains a single protection rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="06220-129">文本值</span><span class="sxs-lookup"><span data-stu-id="06220-129">Text value</span></span>

<span data-ttu-id="06220-130">无。</span><span class="sxs-lookup"><span data-stu-id="06220-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="06220-131">说明</span><span class="sxs-lookup"><span data-stu-id="06220-131">Remarks</span></span>

<span data-ttu-id="06220-132">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="06220-132">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="06220-133">元素信息</span><span class="sxs-lookup"><span data-stu-id="06220-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="06220-134">命名空间</span><span class="sxs-lookup"><span data-stu-id="06220-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="06220-135">架构名称</span><span class="sxs-lookup"><span data-stu-id="06220-135">Schema Name</span></span>  <br/> |<span data-ttu-id="06220-136">类型架构</span><span class="sxs-lookup"><span data-stu-id="06220-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="06220-137">验证文件</span><span class="sxs-lookup"><span data-stu-id="06220-137">Validation File</span></span>  <br/> |<span data-ttu-id="06220-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="06220-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="06220-139">可以为空</span><span class="sxs-lookup"><span data-stu-id="06220-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="06220-140">False</span><span class="sxs-lookup"><span data-stu-id="06220-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="06220-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="06220-141">See also</span></span>

- [<span data-ttu-id="06220-142">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="06220-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

