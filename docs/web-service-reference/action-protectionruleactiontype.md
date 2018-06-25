---
title: 操作 (ProtectionRuleActionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Action
api_type:
- schema
ms.assetid: ca090dec-e2c5-49c8-a057-8d1f2409147f
description: Action 元素标识如果规则的条件部分匹配，则必须执行哪些操作。
ms.openlocfilehash: 8f699e698d3159c5ff2636da506542da3b218251
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754272"
---
# <a name="action-protectionruleactiontype"></a><span data-ttu-id="72e1e-103">操作 (ProtectionRuleActionType)</span><span class="sxs-lookup"><span data-stu-id="72e1e-103">Action (ProtectionRuleActionType)</span></span>

<span data-ttu-id="72e1e-104">**Action**元素标识如果规则的条件部分匹配，则必须执行哪些操作。</span><span class="sxs-lookup"><span data-stu-id="72e1e-104">The **Action** element identifies what action must be executed if the condition part of the rule matches.</span></span> 
  
```xml
<Action Name="">
   <Argument/>
</Action>

```

 <span data-ttu-id="72e1e-105">**ProtectionRuleActionType**</span><span class="sxs-lookup"><span data-stu-id="72e1e-105">**ProtectionRuleActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="72e1e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="72e1e-106">Attributes and elements</span></span>

<span data-ttu-id="72e1e-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="72e1e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="72e1e-108">属性</span><span class="sxs-lookup"><span data-stu-id="72e1e-108">Attributes</span></span>

|<span data-ttu-id="72e1e-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="72e1e-109">**Attribute**</span></span>|<span data-ttu-id="72e1e-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="72e1e-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="72e1e-111">**名称**</span><span class="sxs-lookup"><span data-stu-id="72e1e-111">**Name**</span></span> <br/> |<span data-ttu-id="72e1e-112">标识的操作的名称。</span><span class="sxs-lookup"><span data-stu-id="72e1e-112">Identifies the name of the action.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="72e1e-113">子元素</span><span class="sxs-lookup"><span data-stu-id="72e1e-113">Child elements</span></span>

|<span data-ttu-id="72e1e-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="72e1e-114">**Element**</span></span>|<span data-ttu-id="72e1e-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="72e1e-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="72e1e-116">参数</span><span class="sxs-lookup"><span data-stu-id="72e1e-116">Argument</span></span>](argument.md) <br/> |<span data-ttu-id="72e1e-117">指定为操作的参数。</span><span class="sxs-lookup"><span data-stu-id="72e1e-117">Specifies arguments to the action.</span></span> <span data-ttu-id="72e1e-118">如果指定的操作不需要指定参数，则不会发生此元素。</span><span class="sxs-lookup"><span data-stu-id="72e1e-118">This element will not occur if the specified action does not require arguments to be specified.</span></span> <span data-ttu-id="72e1e-119">如果操作需要一个或多个参数，此元素会出现一个或多个时间。</span><span class="sxs-lookup"><span data-stu-id="72e1e-119">This element can occur one or more times if an action requires one or more arguments.</span></span> <span data-ttu-id="72e1e-120">**RightsProtectMessage**操作将包含单个参数。</span><span class="sxs-lookup"><span data-stu-id="72e1e-120">The **RightsProtectMessage** action will contain a single argument.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="72e1e-121">父元素</span><span class="sxs-lookup"><span data-stu-id="72e1e-121">Parent elements</span></span>

|<span data-ttu-id="72e1e-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="72e1e-122">**Element**</span></span>|<span data-ttu-id="72e1e-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="72e1e-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="72e1e-124">Rule</span><span class="sxs-lookup"><span data-stu-id="72e1e-124">Rule</span></span>](rule.md) <br/> |<span data-ttu-id="72e1e-125">包含单个保护规则。</span><span class="sxs-lookup"><span data-stu-id="72e1e-125">Contains a single protection rule.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="72e1e-126">备注</span><span class="sxs-lookup"><span data-stu-id="72e1e-126">Remarks</span></span>

<span data-ttu-id="72e1e-127">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="72e1e-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="72e1e-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="72e1e-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="72e1e-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="72e1e-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="72e1e-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="72e1e-130">Schema Name</span></span>  <br/> |<span data-ttu-id="72e1e-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="72e1e-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="72e1e-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="72e1e-132">Validation File</span></span>  <br/> |<span data-ttu-id="72e1e-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="72e1e-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="72e1e-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="72e1e-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="72e1e-135">False</span><span class="sxs-lookup"><span data-stu-id="72e1e-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="72e1e-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="72e1e-136">See also</span></span>

- [<span data-ttu-id="72e1e-137">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="72e1e-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

