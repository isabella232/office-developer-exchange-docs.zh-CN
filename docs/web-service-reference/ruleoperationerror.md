---
title: RuleOperationError
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RuleOperationError
api_type:
- schema
ms.assetid: b447e610-d37c-40d3-9158-aa108a9f248e
description: RuleOperationError元素表示规则操作错误。
ms.openlocfilehash: ff42addea0f55b13794e2c910d4d865ad0b17bc3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827265"
---
# <a name="ruleoperationerror"></a><span data-ttu-id="0e6a8-103">RuleOperationError</span><span class="sxs-lookup"><span data-stu-id="0e6a8-103">RuleOperationError</span></span>

<span data-ttu-id="0e6a8-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **RuleOperationError**元素表示规则操作错误。</span><span class="sxs-lookup"><span data-stu-id="0e6a8-104">The **RuleOperationError** element represents a rule operation error.</span></span> 
  
```XML
<RuleOperationError>
    <OperationIndex/>
    <ValidationErrors/>
</RuleOperationError>
```

 <span data-ttu-id="0e6a8-105">**RuleOperationErrorType**</span><span class="sxs-lookup"><span data-stu-id="0e6a8-105">**RuleOperationErrorType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0e6a8-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0e6a8-106">Attributes and elements</span></span>

<span data-ttu-id="0e6a8-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0e6a8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0e6a8-108">属性</span><span class="sxs-lookup"><span data-stu-id="0e6a8-108">Attributes</span></span>

<span data-ttu-id="0e6a8-109">无。</span><span class="sxs-lookup"><span data-stu-id="0e6a8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0e6a8-110">子元素</span><span class="sxs-lookup"><span data-stu-id="0e6a8-110">Child elements</span></span>

|<span data-ttu-id="0e6a8-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="0e6a8-111">**Element**</span></span>|<span data-ttu-id="0e6a8-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="0e6a8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0e6a8-113">OperationIndex</span><span class="sxs-lookup"><span data-stu-id="0e6a8-113">OperationIndex</span></span>](operationindex.md) <br/> |<span data-ttu-id="0e6a8-114">指示导致规则操作错误的请求中的操作的索引。</span><span class="sxs-lookup"><span data-stu-id="0e6a8-114">Indicates the index of the operation in the request that caused the rule operation error.</span></span>  <br/> |
|[<span data-ttu-id="0e6a8-115">ValidationErrors</span><span class="sxs-lookup"><span data-stu-id="0e6a8-115">ValidationErrors</span></span>](validationerrors.md) <br/> |<span data-ttu-id="0e6a8-116">表示一个数组的规则上有一个错误的每个规则字段的验证错误。</span><span class="sxs-lookup"><span data-stu-id="0e6a8-116">Represents an array of rule validation errors on each rule field that has an error.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0e6a8-117">父元素</span><span class="sxs-lookup"><span data-stu-id="0e6a8-117">Parent elements</span></span>

|<span data-ttu-id="0e6a8-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="0e6a8-118">**Element**</span></span>|<span data-ttu-id="0e6a8-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="0e6a8-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0e6a8-120">RuleOperationErrors</span><span class="sxs-lookup"><span data-stu-id="0e6a8-120">RuleOperationErrors</span></span>](ruleoperationerrors.md) <br/> |<span data-ttu-id="0e6a8-121">表示一个数组的规则上有一个错误的每个规则字段的验证错误。</span><span class="sxs-lookup"><span data-stu-id="0e6a8-121">Represents an array of rule validation errors on each rule field that has an error.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0e6a8-122">文本值</span><span class="sxs-lookup"><span data-stu-id="0e6a8-122">Text value</span></span>

<span data-ttu-id="0e6a8-123">无。</span><span class="sxs-lookup"><span data-stu-id="0e6a8-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0e6a8-124">备注</span><span class="sxs-lookup"><span data-stu-id="0e6a8-124">Remarks</span></span>

<span data-ttu-id="0e6a8-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0e6a8-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0e6a8-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="0e6a8-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0e6a8-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="0e6a8-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0e6a8-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="0e6a8-128">Schema Name</span></span>  <br/> |<span data-ttu-id="0e6a8-129">消息架构</span><span class="sxs-lookup"><span data-stu-id="0e6a8-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0e6a8-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="0e6a8-130">Validation File</span></span>  <br/> |<span data-ttu-id="0e6a8-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0e6a8-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0e6a8-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="0e6a8-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="0e6a8-133">True</span><span class="sxs-lookup"><span data-stu-id="0e6a8-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0e6a8-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0e6a8-134">See also</span></span>



- [<span data-ttu-id="0e6a8-135">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="0e6a8-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

