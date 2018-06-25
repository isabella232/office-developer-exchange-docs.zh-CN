---
title: SetRuleOperation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SetRuleOperation
api_type:
- schema
ms.assetid: 2106a85b-58fe-49be-b71d-4ca6aa66e060
description: SetRuleOperation 元素均表示更新现有规则的操作。
ms.openlocfilehash: 9c956394d14c510e8dcc95110ef1874ea7010be0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827451"
---
# <a name="setruleoperation"></a><span data-ttu-id="b77f8-103">SetRuleOperation</span><span class="sxs-lookup"><span data-stu-id="b77f8-103">SetRuleOperation</span></span>

<span data-ttu-id="b77f8-104">**SetRuleOperation**元素均表示更新现有规则的操作。</span><span class="sxs-lookup"><span data-stu-id="b77f8-104">The **SetRuleOperation** element represents an operation to update an existing rule.</span></span> 
  
[<span data-ttu-id="b77f8-105">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="b77f8-105">UpdateInboxRules</span></span>](updateinboxrules.md)
  
[<span data-ttu-id="b77f8-106">操作</span><span class="sxs-lookup"><span data-stu-id="b77f8-106">Operations</span></span>](operations.md)
  
```XML
<SetRuleOperation>
    <Rule/>
</SetRuleOperation>
```

 <span data-ttu-id="b77f8-107">**SetRuleOperationType**</span><span class="sxs-lookup"><span data-stu-id="b77f8-107">**SetRuleOperationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b77f8-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b77f8-108">Attributes and elements</span></span>

<span data-ttu-id="b77f8-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b77f8-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b77f8-110">属性</span><span class="sxs-lookup"><span data-stu-id="b77f8-110">Attributes</span></span>

<span data-ttu-id="b77f8-111">无。</span><span class="sxs-lookup"><span data-stu-id="b77f8-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b77f8-112">子元素</span><span class="sxs-lookup"><span data-stu-id="b77f8-112">Child elements</span></span>

|<span data-ttu-id="b77f8-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="b77f8-113">**Element**</span></span>|<span data-ttu-id="b77f8-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="b77f8-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b77f8-115">规则 (RuleType)</span><span class="sxs-lookup"><span data-stu-id="b77f8-115">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="b77f8-116">代表用户的邮箱中的规则。</span><span class="sxs-lookup"><span data-stu-id="b77f8-116">Represents a rule in a user's mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b77f8-117">父元素</span><span class="sxs-lookup"><span data-stu-id="b77f8-117">Parent elements</span></span>

|<span data-ttu-id="b77f8-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="b77f8-118">**Element**</span></span>|<span data-ttu-id="b77f8-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="b77f8-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b77f8-120">操作</span><span class="sxs-lookup"><span data-stu-id="b77f8-120">Operations</span></span>](operations.md) <br/> |<span data-ttu-id="b77f8-121">包含规则的操作，可以在收件箱的一个数组。</span><span class="sxs-lookup"><span data-stu-id="b77f8-121">Contains an array of rule operations that can be performed on an Inbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b77f8-122">文本值</span><span class="sxs-lookup"><span data-stu-id="b77f8-122">Text value</span></span>

<span data-ttu-id="b77f8-123">无。</span><span class="sxs-lookup"><span data-stu-id="b77f8-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b77f8-124">备注</span><span class="sxs-lookup"><span data-stu-id="b77f8-124">Remarks</span></span>

<span data-ttu-id="b77f8-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b77f8-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b77f8-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="b77f8-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b77f8-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="b77f8-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b77f8-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="b77f8-128">Schema Name</span></span>  <br/> |<span data-ttu-id="b77f8-129">类型架构</span><span class="sxs-lookup"><span data-stu-id="b77f8-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="b77f8-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="b77f8-130">Validation File</span></span>  <br/> |<span data-ttu-id="b77f8-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b77f8-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b77f8-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="b77f8-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="b77f8-133">False</span><span class="sxs-lookup"><span data-stu-id="b77f8-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b77f8-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b77f8-134">See also</span></span>



[<span data-ttu-id="b77f8-135">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="b77f8-135">UpdateInboxRules</span></span>](updateinboxrules.md)
  
[<span data-ttu-id="b77f8-136">DeleteRuleOperation</span><span class="sxs-lookup"><span data-stu-id="b77f8-136">DeleteRuleOperation</span></span>](deleteruleoperation.md)
  
[<span data-ttu-id="b77f8-137">CreateRuleOperation</span><span class="sxs-lookup"><span data-stu-id="b77f8-137">CreateRuleOperation</span></span>](createruleoperation.md)


- [<span data-ttu-id="b77f8-138">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b77f8-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

