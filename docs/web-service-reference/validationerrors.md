---
title: ValidationErrors
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ValidationErrors
api_type:
- schema
ms.assetid: 009526aa-22e7-4f5c-be88-079175aa9122
description: ValidationErrors元素表示一个数组的规则上有一个错误的每个规则字段的验证错误。
ms.openlocfilehash: c95c8057ad2d16a314d33e3738553b495355fd76
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838497"
---
# <a name="validationerrors"></a><span data-ttu-id="6a4a0-103">ValidationErrors</span><span class="sxs-lookup"><span data-stu-id="6a4a0-103">ValidationErrors</span></span>

<span data-ttu-id="6a4a0-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **ValidationErrors**元素表示一个数组的规则上有一个错误的每个规则字段的验证错误。</span><span class="sxs-lookup"><span data-stu-id="6a4a0-104">The **ValidationErrors** element represents an array of rule validation errors on each rule field that has an error.</span></span> 
  
```XML
<VaidationErrors>
   <Error/>
</ValidationErrors>
```

 <span data-ttu-id="6a4a0-105">**ArrayOfRuleValidationErrorsType**</span><span class="sxs-lookup"><span data-stu-id="6a4a0-105">**ArrayOfRuleValidationErrorsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6a4a0-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6a4a0-106">Attributes and elements</span></span>

<span data-ttu-id="6a4a0-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6a4a0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6a4a0-108">属性</span><span class="sxs-lookup"><span data-stu-id="6a4a0-108">Attributes</span></span>

<span data-ttu-id="6a4a0-109">无。</span><span class="sxs-lookup"><span data-stu-id="6a4a0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6a4a0-110">子元素</span><span class="sxs-lookup"><span data-stu-id="6a4a0-110">Child elements</span></span>

|<span data-ttu-id="6a4a0-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="6a4a0-111">**Element**</span></span>|<span data-ttu-id="6a4a0-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="6a4a0-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6a4a0-113">Error</span><span class="sxs-lookup"><span data-stu-id="6a4a0-113">Error</span></span>](error.md) <br/> |<span data-ttu-id="6a4a0-114">表示在特定规则属性值、 谓词属性值或操作的属性值的单个验证错误</span><span class="sxs-lookup"><span data-stu-id="6a4a0-114">Represents a single validation error on a particular rule property value, predicate property value, or action property value</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6a4a0-115">父元素</span><span class="sxs-lookup"><span data-stu-id="6a4a0-115">Parent elements</span></span>

|<span data-ttu-id="6a4a0-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="6a4a0-116">**Element**</span></span>|<span data-ttu-id="6a4a0-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="6a4a0-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6a4a0-118">RuleOperationError</span><span class="sxs-lookup"><span data-stu-id="6a4a0-118">RuleOperationError</span></span>](ruleoperationerror.md) <br/> |<span data-ttu-id="6a4a0-119">表示一个规则操作错误。</span><span class="sxs-lookup"><span data-stu-id="6a4a0-119">Represents a rule operation error.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6a4a0-120">文本值</span><span class="sxs-lookup"><span data-stu-id="6a4a0-120">Text value</span></span>

<span data-ttu-id="6a4a0-121">无。</span><span class="sxs-lookup"><span data-stu-id="6a4a0-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6a4a0-122">备注</span><span class="sxs-lookup"><span data-stu-id="6a4a0-122">Remarks</span></span>

<span data-ttu-id="6a4a0-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="6a4a0-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6a4a0-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="6a4a0-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6a4a0-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="6a4a0-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6a4a0-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="6a4a0-126">Schema Name</span></span>  <br/> |<span data-ttu-id="6a4a0-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="6a4a0-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6a4a0-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="6a4a0-128">Validation File</span></span>  <br/> |<span data-ttu-id="6a4a0-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="6a4a0-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6a4a0-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="6a4a0-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="6a4a0-131">True</span><span class="sxs-lookup"><span data-stu-id="6a4a0-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6a4a0-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6a4a0-132">See also</span></span>



- [<span data-ttu-id="6a4a0-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="6a4a0-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
