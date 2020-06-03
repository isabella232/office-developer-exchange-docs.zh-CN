---
title: RuleOperationErrors
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f15c7b9e-a670-4a11-bb62-2a298c91f142
description: RuleOperationErrors元素表示一个数组的规则上有一个错误的每个规则字段的验证错误。
ms.openlocfilehash: d547155f3cbf9eedd0f9bfac7bf3768b3630b50e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464950"
---
# <a name="ruleoperationerrors"></a><span data-ttu-id="d802f-103">RuleOperationErrors</span><span class="sxs-lookup"><span data-stu-id="d802f-103">RuleOperationErrors</span></span>

<span data-ttu-id="d802f-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **RuleOperationErrors**元素表示一个数组的规则上有一个错误的每个规则字段的验证错误。</span><span class="sxs-lookup"><span data-stu-id="d802f-104">The **RuleOperationErrors** element represents an array of rule validation errors on each rule field that has an error.</span></span> 
  
[<span data-ttu-id="d802f-105">UpdateInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="d802f-105">UpdateInboxRulesResponse</span></span>](updateinboxrulesresponse.md)
  
[<span data-ttu-id="d802f-106">RuleOperationErrors</span><span class="sxs-lookup"><span data-stu-id="d802f-106">RuleOperationErrors</span></span>](ruleoperationerrors.md)
  
```XML
<RuleOperationErrors>
    <RuleOperationError>
</RuleOperationErrors>
```

 <span data-ttu-id="d802f-107">**ArrayOfRuleOperationErrorsType**</span><span class="sxs-lookup"><span data-stu-id="d802f-107">**ArrayOfRuleOperationErrorsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d802f-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d802f-108">Attributes and elements</span></span>

<span data-ttu-id="d802f-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d802f-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d802f-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="d802f-110">Attributes</span></span>

<span data-ttu-id="d802f-111">无。</span><span class="sxs-lookup"><span data-stu-id="d802f-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d802f-112">子元素</span><span class="sxs-lookup"><span data-stu-id="d802f-112">Child elements</span></span>

|<span data-ttu-id="d802f-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="d802f-113">**Element**</span></span>|<span data-ttu-id="d802f-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="d802f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d802f-115">RuleOperationError</span><span class="sxs-lookup"><span data-stu-id="d802f-115">RuleOperationError</span></span>](ruleoperationerror.md) <br/> |<span data-ttu-id="d802f-116">表示一个规则操作错误。</span><span class="sxs-lookup"><span data-stu-id="d802f-116">Represents a rule operation error.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d802f-117">父元素</span><span class="sxs-lookup"><span data-stu-id="d802f-117">Parent elements</span></span>

|<span data-ttu-id="d802f-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="d802f-118">**Element**</span></span>|<span data-ttu-id="d802f-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="d802f-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d802f-120">UpdateInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="d802f-120">UpdateInboxRulesResponse</span></span>](updateinboxrulesresponse.md) <br/> |<span data-ttu-id="d802f-121">定义一个[UpdateInboxRules](updateinboxrules.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="d802f-121">Defines a response to an [UpdateInboxRules](updateinboxrules.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d802f-122">文本值</span><span class="sxs-lookup"><span data-stu-id="d802f-122">Text value</span></span>

<span data-ttu-id="d802f-123">无。</span><span class="sxs-lookup"><span data-stu-id="d802f-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d802f-124">说明</span><span class="sxs-lookup"><span data-stu-id="d802f-124">Remarks</span></span>

<span data-ttu-id="d802f-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d802f-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d802f-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="d802f-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d802f-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="d802f-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d802f-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="d802f-128">Schema name</span></span>  <br/> |<span data-ttu-id="d802f-129">消息架构</span><span class="sxs-lookup"><span data-stu-id="d802f-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d802f-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="d802f-130">Validation file</span></span>  <br/> |<span data-ttu-id="d802f-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d802f-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d802f-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="d802f-132">Can be empty</span></span>  <br/> |<span data-ttu-id="d802f-133">True</span><span class="sxs-lookup"><span data-stu-id="d802f-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d802f-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d802f-134">See also</span></span>



[<span data-ttu-id="d802f-135">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="d802f-135">UpdateInboxRules</span></span>](updateinboxrules.md)


- [<span data-ttu-id="d802f-136">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d802f-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

