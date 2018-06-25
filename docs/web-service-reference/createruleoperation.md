---
title: CreateRuleOperation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateRuleOperation
api_type:
- schema
ms.assetid: e9f70726-db08-4089-839e-a41007d0a473
description: CreateRuleOperation 元素均表示要创建新的收件箱规则操作。
ms.openlocfilehash: c531f222ffe886e6ef53a99609cfa27e84fd6107
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753680"
---
# <a name="createruleoperation"></a><span data-ttu-id="086d5-103">CreateRuleOperation</span><span class="sxs-lookup"><span data-stu-id="086d5-103">CreateRuleOperation</span></span>

<span data-ttu-id="086d5-104">**CreateRuleOperation**元素均表示要创建新的收件箱规则操作。</span><span class="sxs-lookup"><span data-stu-id="086d5-104">The **CreateRuleOperation** element represents an operation to create a new Inbox rule.</span></span> 
  
[<span data-ttu-id="086d5-105">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="086d5-105">UpdateInboxRules</span></span>](updateinboxrules.md)
  
[<span data-ttu-id="086d5-106">操作</span><span class="sxs-lookup"><span data-stu-id="086d5-106">Operations</span></span>](operations.md)
  
```xml
<CreateRuleOperation>
    <Rule/>
</CreateRuleOperation>
```

 <span data-ttu-id="086d5-107">**CreateRuleOperationType**</span><span class="sxs-lookup"><span data-stu-id="086d5-107">**CreateRuleOperationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="086d5-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="086d5-108">Attributes and elements</span></span>

<span data-ttu-id="086d5-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="086d5-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="086d5-110">属性</span><span class="sxs-lookup"><span data-stu-id="086d5-110">Attributes</span></span>

<span data-ttu-id="086d5-111">无。</span><span class="sxs-lookup"><span data-stu-id="086d5-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="086d5-112">子元素</span><span class="sxs-lookup"><span data-stu-id="086d5-112">Child elements</span></span>

|<span data-ttu-id="086d5-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="086d5-113">**Element**</span></span>|<span data-ttu-id="086d5-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="086d5-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="086d5-115">规则 (RuleType)</span><span class="sxs-lookup"><span data-stu-id="086d5-115">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="086d5-116">表示用户的邮箱中创建的规则。</span><span class="sxs-lookup"><span data-stu-id="086d5-116">Represents a rule to be created in a user's mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="086d5-117">父元素</span><span class="sxs-lookup"><span data-stu-id="086d5-117">Parent elements</span></span>

|<span data-ttu-id="086d5-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="086d5-118">**Element**</span></span>|<span data-ttu-id="086d5-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="086d5-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="086d5-120">操作</span><span class="sxs-lookup"><span data-stu-id="086d5-120">Operations</span></span>](operations.md) <br/> |<span data-ttu-id="086d5-121">包含可在收件箱中执行的操作。</span><span class="sxs-lookup"><span data-stu-id="086d5-121">Contains the operations that can be performed on an Inbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="086d5-122">文本值</span><span class="sxs-lookup"><span data-stu-id="086d5-122">Text value</span></span>

<span data-ttu-id="086d5-123">无。</span><span class="sxs-lookup"><span data-stu-id="086d5-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="086d5-124">备注</span><span class="sxs-lookup"><span data-stu-id="086d5-124">Remarks</span></span>

<span data-ttu-id="086d5-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="086d5-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="086d5-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="086d5-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="086d5-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="086d5-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="086d5-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="086d5-128">Schema Name</span></span>  <br/> |<span data-ttu-id="086d5-129">类型架构</span><span class="sxs-lookup"><span data-stu-id="086d5-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="086d5-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="086d5-130">Validation File</span></span>  <br/> |<span data-ttu-id="086d5-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="086d5-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="086d5-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="086d5-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="086d5-133">False</span><span class="sxs-lookup"><span data-stu-id="086d5-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="086d5-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="086d5-134">See also</span></span>



[<span data-ttu-id="086d5-135">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="086d5-135">UpdateInboxRules</span></span>](updateinboxrules.md)
  
[<span data-ttu-id="086d5-136">SetRuleOperation</span><span class="sxs-lookup"><span data-stu-id="086d5-136">SetRuleOperation</span></span>](setruleoperation.md)
  
[<span data-ttu-id="086d5-137">DeleteRuleOperation</span><span class="sxs-lookup"><span data-stu-id="086d5-137">DeleteRuleOperation</span></span>](deleteruleoperation.md)


- [<span data-ttu-id="086d5-138">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="086d5-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

