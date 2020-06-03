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
description: 和元素指定所有子元素都必须匹配以求值为 true。
ms.openlocfilehash: ba898ccd77518971afaf713d1c7c7955f46465d5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464733"
---
# <a name="and-protectionruleandtype"></a><span data-ttu-id="2b3ed-103">和 (ProtectionRuleAndType)</span><span class="sxs-lookup"><span data-stu-id="2b3ed-103">And (ProtectionRuleAndType)</span></span>

<span data-ttu-id="2b3ed-104">**和**元素指定所有子元素都必须匹配以求值为**true**。</span><span class="sxs-lookup"><span data-stu-id="2b3ed-104">The **And** element specifies that all child elements must match to evaluate to **true**.</span></span>
  
```xml
<And>
   <AllInternal/>
   <And/>
   <RecipientIs/>
   <SenderDepartments/>
   <True/>
</And>
```

 <span data-ttu-id="2b3ed-105">**ProtectionRuleAndType**</span><span class="sxs-lookup"><span data-stu-id="2b3ed-105">**ProtectionRuleAndType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2b3ed-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2b3ed-106">Attributes and elements</span></span>

<span data-ttu-id="2b3ed-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2b3ed-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2b3ed-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="2b3ed-108">Attributes</span></span>

<span data-ttu-id="2b3ed-109">无。</span><span class="sxs-lookup"><span data-stu-id="2b3ed-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2b3ed-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2b3ed-110">Child elements</span></span>

|<span data-ttu-id="2b3ed-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="2b3ed-111">**Element**</span></span>|<span data-ttu-id="2b3ed-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="2b3ed-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2b3ed-113">AllInternal</span><span class="sxs-lookup"><span data-stu-id="2b3ed-113">AllInternal</span></span>](allinternal.md) <br/> |<span data-ttu-id="2b3ed-114">如果电子邮件的所有收件人均为发件人的组织内部，则计算结果为**true** 。</span><span class="sxs-lookup"><span data-stu-id="2b3ed-114">Evaluates to **true** if all recipients of an e-mail message are internal to the sender's organization.</span></span>  <br/> |
|<span data-ttu-id="2b3ed-115">**And**</span><span class="sxs-lookup"><span data-stu-id="2b3ed-115">**And**</span></span> <br/> |<span data-ttu-id="2b3ed-116">指定所有子元素都必须匹配以使值为 **true**。</span><span class="sxs-lookup"><span data-stu-id="2b3ed-116">Specifies that all child elements must match to evaluate to **true**.</span></span>  <br/> |
|[<span data-ttu-id="2b3ed-117">收件人是</span><span class="sxs-lookup"><span data-stu-id="2b3ed-117">RecipientIs</span></span>](recipientis.md) <br/> |<span data-ttu-id="2b3ed-118">指定电子邮件的任何收件人与子[值（ProtectionRuleValueType）](value-protectionrulevaluetype.md)元素中的任何指定收件人相匹配。</span><span class="sxs-lookup"><span data-stu-id="2b3ed-118">Specifies that any recipient of the e-mail message matches any of the specified recipients in the child [Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="2b3ed-119">SenderDepartments</span><span class="sxs-lookup"><span data-stu-id="2b3ed-119">SenderDepartments</span></span>](senderdepartments.md) <br/> |<span data-ttu-id="2b3ed-120">指定发件人的部门与子[值（ProtectionRuleValueType）](value-protectionrulevaluetype.md)元素中的任何指定的部门相匹配。</span><span class="sxs-lookup"><span data-stu-id="2b3ed-120">Specifies that the department of the sender matches any of the specified departments in the child [Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="2b3ed-121">True</span><span class="sxs-lookup"><span data-stu-id="2b3ed-121">True</span></span>](true.md) <br/> |<span data-ttu-id="2b3ed-122">指定始终匹配的条件。</span><span class="sxs-lookup"><span data-stu-id="2b3ed-122">Specifies a condition that always matches.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2b3ed-123">父元素</span><span class="sxs-lookup"><span data-stu-id="2b3ed-123">Parent elements</span></span>

|<span data-ttu-id="2b3ed-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="2b3ed-124">**Element**</span></span>|<span data-ttu-id="2b3ed-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="2b3ed-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2b3ed-126">条件</span><span class="sxs-lookup"><span data-stu-id="2b3ed-126">Condition</span></span>](condition.md) <br/> |<span data-ttu-id="2b3ed-127">确定要执行该规则的操作部分必须满足的条件。</span><span class="sxs-lookup"><span data-stu-id="2b3ed-127">Identifies the condition that must be satisfied for the action part of the rule to be executed.</span></span>  <br/> |
|<span data-ttu-id="2b3ed-128">**And**</span><span class="sxs-lookup"><span data-stu-id="2b3ed-128">**And**</span></span> <br/> |<span data-ttu-id="2b3ed-129">指定所有子元素都必须匹配以使值为 **true**。</span><span class="sxs-lookup"><span data-stu-id="2b3ed-129">Specifies that all child elements must match to evaluate to **true**.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2b3ed-130">文本值</span><span class="sxs-lookup"><span data-stu-id="2b3ed-130">Text value</span></span>

<span data-ttu-id="2b3ed-131">无。</span><span class="sxs-lookup"><span data-stu-id="2b3ed-131">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2b3ed-132">说明</span><span class="sxs-lookup"><span data-stu-id="2b3ed-132">Remarks</span></span>

<span data-ttu-id="2b3ed-133">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2b3ed-133">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2b3ed-134">元素信息</span><span class="sxs-lookup"><span data-stu-id="2b3ed-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2b3ed-135">命名空间</span><span class="sxs-lookup"><span data-stu-id="2b3ed-135">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2b3ed-136">架构名称</span><span class="sxs-lookup"><span data-stu-id="2b3ed-136">Schema Name</span></span>  <br/> |<span data-ttu-id="2b3ed-137">类型架构</span><span class="sxs-lookup"><span data-stu-id="2b3ed-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="2b3ed-138">验证文件</span><span class="sxs-lookup"><span data-stu-id="2b3ed-138">Validation File</span></span>  <br/> |<span data-ttu-id="2b3ed-139">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2b3ed-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2b3ed-140">可以为空</span><span class="sxs-lookup"><span data-stu-id="2b3ed-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="2b3ed-141">False</span><span class="sxs-lookup"><span data-stu-id="2b3ed-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2b3ed-142">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2b3ed-142">See also</span></span>

- [<span data-ttu-id="2b3ed-143">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2b3ed-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

