---
title: DeleteRuleOperation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteRuleOperation
api_type:
- schema
ms.assetid: c5e251af-f795-43cc-baaf-95d84475677c
description: DeleteRuleOperation 元素包含要删除现有的收件箱规则操作。
ms.openlocfilehash: 3410361e0b896fb0ef01c1873c9f8b0ac99afe58
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753819"
---
# <a name="deleteruleoperation"></a><span data-ttu-id="b461d-103">DeleteRuleOperation</span><span class="sxs-lookup"><span data-stu-id="b461d-103">DeleteRuleOperation</span></span>

<span data-ttu-id="b461d-104">**DeleteRuleOperation**元素包含要删除现有的收件箱规则操作。</span><span class="sxs-lookup"><span data-stu-id="b461d-104">The **DeleteRuleOperation** element contains an operation to delete an existing Inbox rule.</span></span> 
  
- [<span data-ttu-id="b461d-105">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="b461d-105">UpdateInboxRules</span></span>](updateinboxrules.md)
- [<span data-ttu-id="b461d-106">操作</span><span class="sxs-lookup"><span data-stu-id="b461d-106">Operations</span></span>](operations.md)
  
```XML
<DeleteRuleOperation>
    <RuleId/>
</DeleteRuleOperation>
```

 <span data-ttu-id="b461d-107">**DeleteRuleOperationType**</span><span class="sxs-lookup"><span data-stu-id="b461d-107">**DeleteRuleOperationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b461d-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b461d-108">Attributes and elements</span></span>

<span data-ttu-id="b461d-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b461d-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b461d-110">属性</span><span class="sxs-lookup"><span data-stu-id="b461d-110">Attributes</span></span>

<span data-ttu-id="b461d-111">无。</span><span class="sxs-lookup"><span data-stu-id="b461d-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b461d-112">子元素</span><span class="sxs-lookup"><span data-stu-id="b461d-112">Child elements</span></span>

|<span data-ttu-id="b461d-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="b461d-113">**Element**</span></span>|<span data-ttu-id="b461d-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="b461d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b461d-115">规则 Id</span><span class="sxs-lookup"><span data-stu-id="b461d-115">RuleId</span></span>](ruleid.md) <br/> |<span data-ttu-id="b461d-116">指定要删除的规则的标识符。</span><span class="sxs-lookup"><span data-stu-id="b461d-116">Specifies the identifier of the rule to delete.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b461d-117">父元素</span><span class="sxs-lookup"><span data-stu-id="b461d-117">Parent elements</span></span>

|<span data-ttu-id="b461d-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="b461d-118">**Element**</span></span>|<span data-ttu-id="b461d-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="b461d-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b461d-120">操作</span><span class="sxs-lookup"><span data-stu-id="b461d-120">Operations</span></span>](operations.md) <br/> |<span data-ttu-id="b461d-121">包含规则的操作，可以在收件箱的一个数组。</span><span class="sxs-lookup"><span data-stu-id="b461d-121">Contains an array of rule operations that can be performed on an Inbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b461d-122">文本值</span><span class="sxs-lookup"><span data-stu-id="b461d-122">Text value</span></span>

<span data-ttu-id="b461d-123">无。</span><span class="sxs-lookup"><span data-stu-id="b461d-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b461d-124">备注</span><span class="sxs-lookup"><span data-stu-id="b461d-124">Remarks</span></span>

<span data-ttu-id="b461d-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b461d-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b461d-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="b461d-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b461d-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="b461d-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b461d-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="b461d-128">Schema Name</span></span>  <br/> |<span data-ttu-id="b461d-129">类型架构</span><span class="sxs-lookup"><span data-stu-id="b461d-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="b461d-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="b461d-130">Validation File</span></span>  <br/> |<span data-ttu-id="b461d-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b461d-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b461d-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="b461d-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="b461d-133">False</span><span class="sxs-lookup"><span data-stu-id="b461d-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b461d-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b461d-134">See also</span></span>

- [<span data-ttu-id="b461d-135">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="b461d-135">UpdateInboxRules</span></span>](updateinboxrules.md) 
- [<span data-ttu-id="b461d-136">SetRuleOperation</span><span class="sxs-lookup"><span data-stu-id="b461d-136">SetRuleOperation</span></span>](setruleoperation.md) 
- [<span data-ttu-id="b461d-137">CreateRuleOperation</span><span class="sxs-lookup"><span data-stu-id="b461d-137">CreateRuleOperation</span></span>](createruleoperation.md)
- [<span data-ttu-id="b461d-138">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b461d-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

