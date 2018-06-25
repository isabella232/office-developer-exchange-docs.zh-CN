---
title: 参数
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Argument
api_type:
- schema
ms.assetid: 15b0bfb8-2448-4ceb-aeac-965115e0fb72
description: 实参元素指定为操作的参数。
ms.openlocfilehash: ed4e46a8d9897516e9c96bf3930f7d488bc06714
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753264"
---
# <a name="argument"></a><span data-ttu-id="af189-103">参数</span><span class="sxs-lookup"><span data-stu-id="af189-103">Argument</span></span>

<span data-ttu-id="af189-104">**实参**元素指定为操作的参数。</span><span class="sxs-lookup"><span data-stu-id="af189-104">The **Argument** element specifies arguments to the action.</span></span> 
  
```xml
<Argument Value=""/>
```

 <span data-ttu-id="af189-105">**ProtectionRuleArgumentType**</span><span class="sxs-lookup"><span data-stu-id="af189-105">**ProtectionRuleArgumentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="af189-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="af189-106">Attributes and elements</span></span>

<span data-ttu-id="af189-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="af189-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="af189-108">属性</span><span class="sxs-lookup"><span data-stu-id="af189-108">Attributes</span></span>

|<span data-ttu-id="af189-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="af189-109">**Attribute**</span></span>|<span data-ttu-id="af189-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="af189-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="af189-111">**Value**</span><span class="sxs-lookup"><span data-stu-id="af189-111">**Value**</span></span> <br/> |<span data-ttu-id="af189-112">一个表示保护规则的操作部分的参数的值的非空字符串值。</span><span class="sxs-lookup"><span data-stu-id="af189-112">A non-empty string value that represents the value of an argument to the action part of a protection rule.</span></span> <span data-ttu-id="af189-113">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="af189-113">This attribute is required.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="af189-114">子元素</span><span class="sxs-lookup"><span data-stu-id="af189-114">Child elements</span></span>

<span data-ttu-id="af189-115">无。</span><span class="sxs-lookup"><span data-stu-id="af189-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="af189-116">父元素</span><span class="sxs-lookup"><span data-stu-id="af189-116">Parent elements</span></span>

|<span data-ttu-id="af189-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="af189-117">**Element**</span></span>|<span data-ttu-id="af189-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="af189-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="af189-119">操作 (ProtectionRuleActionType)</span><span class="sxs-lookup"><span data-stu-id="af189-119">Action (ProtectionRuleActionType)</span></span>](action-protectionruleactiontype.md) <br/> |<span data-ttu-id="af189-120">标识必须执行哪些操作，如果该规则的条件部分匹配。</span><span class="sxs-lookup"><span data-stu-id="af189-120">Identifies what action must be executed if the condition part of the rule matches.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="af189-121">文本值</span><span class="sxs-lookup"><span data-stu-id="af189-121">Text value</span></span>

<span data-ttu-id="af189-122">无。</span><span class="sxs-lookup"><span data-stu-id="af189-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="af189-123">备注</span><span class="sxs-lookup"><span data-stu-id="af189-123">Remarks</span></span>

<span data-ttu-id="af189-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="af189-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="af189-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="af189-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="af189-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="af189-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="af189-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="af189-127">Schema Name</span></span>  <br/> |<span data-ttu-id="af189-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="af189-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="af189-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="af189-129">Validation File</span></span>  <br/> |<span data-ttu-id="af189-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="af189-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="af189-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="af189-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="af189-132">False</span><span class="sxs-lookup"><span data-stu-id="af189-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="af189-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="af189-133">See also</span></span>

- [<span data-ttu-id="af189-134">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="af189-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

