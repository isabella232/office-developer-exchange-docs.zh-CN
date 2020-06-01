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
ms.openlocfilehash: b5e0105a1fdb1564b3115a4c3a8411019f725483
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/01/2020
ms.locfileid: "44464957"
---
# <a name="ruleoperationerror"></a><span data-ttu-id="18dda-103">RuleOperationError</span><span class="sxs-lookup"><span data-stu-id="18dda-103">RuleOperationError</span></span>

<span data-ttu-id="18dda-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **RuleOperationError**元素表示规则操作错误。</span><span class="sxs-lookup"><span data-stu-id="18dda-104">The **RuleOperationError** element represents a rule operation error.</span></span> 
  
```XML
<RuleOperationError>
    <OperationIndex/>
    <ValidationErrors/>
</RuleOperationError>
```

 <span data-ttu-id="18dda-105">**RuleOperationErrorType**</span><span class="sxs-lookup"><span data-stu-id="18dda-105">**RuleOperationErrorType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="18dda-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="18dda-106">Attributes and elements</span></span>

<span data-ttu-id="18dda-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="18dda-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="18dda-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="18dda-108">Attributes</span></span>

<span data-ttu-id="18dda-109">无。</span><span class="sxs-lookup"><span data-stu-id="18dda-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="18dda-110">子元素</span><span class="sxs-lookup"><span data-stu-id="18dda-110">Child elements</span></span>

|<span data-ttu-id="18dda-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="18dda-111">**Element**</span></span>|<span data-ttu-id="18dda-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="18dda-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="18dda-113">OperationIndex</span><span class="sxs-lookup"><span data-stu-id="18dda-113">OperationIndex</span></span>](operationindex.md) <br/> |<span data-ttu-id="18dda-114">指示导致规则操作错误的请求中的操作的索引。</span><span class="sxs-lookup"><span data-stu-id="18dda-114">Indicates the index of the operation in the request that caused the rule operation error.</span></span>  <br/> |
|[<span data-ttu-id="18dda-115">ValidationErrors</span><span class="sxs-lookup"><span data-stu-id="18dda-115">ValidationErrors</span></span>](validationerrors.md) <br/> |<span data-ttu-id="18dda-116">表示每个出错的规则字段上的规则验证错误数组。</span><span class="sxs-lookup"><span data-stu-id="18dda-116">Represents an array of rule validation errors on each rule field that has an error.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="18dda-117">父元素</span><span class="sxs-lookup"><span data-stu-id="18dda-117">Parent elements</span></span>

|<span data-ttu-id="18dda-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="18dda-118">**Element**</span></span>|<span data-ttu-id="18dda-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="18dda-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="18dda-120">RuleOperationErrors</span><span class="sxs-lookup"><span data-stu-id="18dda-120">RuleOperationErrors</span></span>](ruleoperationerrors.md) <br/> |<span data-ttu-id="18dda-121">表示每个出错的规则字段上的规则验证错误数组。</span><span class="sxs-lookup"><span data-stu-id="18dda-121">Represents an array of rule validation errors on each rule field that has an error.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="18dda-122">文本值</span><span class="sxs-lookup"><span data-stu-id="18dda-122">Text value</span></span>

<span data-ttu-id="18dda-123">无。</span><span class="sxs-lookup"><span data-stu-id="18dda-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="18dda-124">说明</span><span class="sxs-lookup"><span data-stu-id="18dda-124">Remarks</span></span>

<span data-ttu-id="18dda-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="18dda-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="18dda-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="18dda-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="18dda-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="18dda-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="18dda-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="18dda-128">Schema Name</span></span>  <br/> |<span data-ttu-id="18dda-129">消息架构</span><span class="sxs-lookup"><span data-stu-id="18dda-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="18dda-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="18dda-130">Validation File</span></span>  <br/> |<span data-ttu-id="18dda-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="18dda-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="18dda-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="18dda-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="18dda-133">True</span><span class="sxs-lookup"><span data-stu-id="18dda-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="18dda-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="18dda-134">See also</span></span>



- [<span data-ttu-id="18dda-135">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="18dda-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

