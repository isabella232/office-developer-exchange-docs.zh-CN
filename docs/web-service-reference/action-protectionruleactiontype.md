---
title: Action （ProtectionRuleActionType）
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
description: Action 元素标识当规则的条件部分匹配时，必须执行的操作。
ms.openlocfilehash: 220a6fea16abb9ea823ae6239537b8c121702589
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527507"
---
# <a name="action-protectionruleactiontype"></a><span data-ttu-id="7fca7-103">Action （ProtectionRuleActionType）</span><span class="sxs-lookup"><span data-stu-id="7fca7-103">Action (ProtectionRuleActionType)</span></span>

<span data-ttu-id="7fca7-104">**Action**元素标识当规则的条件部分匹配时，必须执行的操作。</span><span class="sxs-lookup"><span data-stu-id="7fca7-104">The **Action** element identifies what action must be executed if the condition part of the rule matches.</span></span> 
  
```xml
<Action Name="">
   <Argument/>
</Action>

```

 <span data-ttu-id="7fca7-105">**ProtectionRuleActionType**</span><span class="sxs-lookup"><span data-stu-id="7fca7-105">**ProtectionRuleActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7fca7-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7fca7-106">Attributes and elements</span></span>

<span data-ttu-id="7fca7-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7fca7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7fca7-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="7fca7-108">Attributes</span></span>

|<span data-ttu-id="7fca7-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="7fca7-109">**Attribute**</span></span>|<span data-ttu-id="7fca7-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="7fca7-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7fca7-111">**名称**</span><span class="sxs-lookup"><span data-stu-id="7fca7-111">**Name**</span></span> <br/> |<span data-ttu-id="7fca7-112">标识操作的名称。</span><span class="sxs-lookup"><span data-stu-id="7fca7-112">Identifies the name of the action.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7fca7-113">子元素</span><span class="sxs-lookup"><span data-stu-id="7fca7-113">Child elements</span></span>

|<span data-ttu-id="7fca7-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="7fca7-114">**Element**</span></span>|<span data-ttu-id="7fca7-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="7fca7-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7fca7-116">参数</span><span class="sxs-lookup"><span data-stu-id="7fca7-116">Argument</span></span>](argument.md) <br/> |<span data-ttu-id="7fca7-117">指定操作的参数。</span><span class="sxs-lookup"><span data-stu-id="7fca7-117">Specifies arguments to the action.</span></span> <span data-ttu-id="7fca7-118">如果指定的操作不需要指定参数，则不会出现此元素。</span><span class="sxs-lookup"><span data-stu-id="7fca7-118">This element will not occur if the specified action does not require arguments to be specified.</span></span> <span data-ttu-id="7fca7-119">如果操作需要一个或多个参数，则此元素可能出现一次或多次。</span><span class="sxs-lookup"><span data-stu-id="7fca7-119">This element can occur one or more times if an action requires one or more arguments.</span></span> <span data-ttu-id="7fca7-120">**RightsProtectMessage**操作将包含单个参数。</span><span class="sxs-lookup"><span data-stu-id="7fca7-120">The **RightsProtectMessage** action will contain a single argument.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7fca7-121">父元素</span><span class="sxs-lookup"><span data-stu-id="7fca7-121">Parent elements</span></span>

|<span data-ttu-id="7fca7-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="7fca7-122">**Element**</span></span>|<span data-ttu-id="7fca7-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="7fca7-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7fca7-124">Rule</span><span class="sxs-lookup"><span data-stu-id="7fca7-124">Rule</span></span>](rule.md) <br/> |<span data-ttu-id="7fca7-125">包含一个保护规则。</span><span class="sxs-lookup"><span data-stu-id="7fca7-125">Contains a single protection rule.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7fca7-126">说明</span><span class="sxs-lookup"><span data-stu-id="7fca7-126">Remarks</span></span>

<span data-ttu-id="7fca7-127">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7fca7-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7fca7-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="7fca7-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7fca7-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="7fca7-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7fca7-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="7fca7-130">Schema Name</span></span>  <br/> |<span data-ttu-id="7fca7-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="7fca7-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="7fca7-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="7fca7-132">Validation File</span></span>  <br/> |<span data-ttu-id="7fca7-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7fca7-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7fca7-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="7fca7-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="7fca7-135">False</span><span class="sxs-lookup"><span data-stu-id="7fca7-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7fca7-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7fca7-136">See also</span></span>

- [<span data-ttu-id="7fca7-137">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="7fca7-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

