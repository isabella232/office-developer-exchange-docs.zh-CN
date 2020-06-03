---
title: 错误
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0bb00cee-c66b-4f34-b99d-355458f5e83b
description: ErrorCode 元素表示一个规则验证错误代码，该代码描述对每个规则谓词或操作的验证失败的情况。
ms.openlocfilehash: 6432aeee786d74a9afcb346cb66765f9001257de
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460076"
---
# <a name="errorcode"></a><span data-ttu-id="6f86e-103">错误</span><span class="sxs-lookup"><span data-stu-id="6f86e-103">ErrorCode</span></span>

<span data-ttu-id="6f86e-104">**ErrorCode**元素表示一个规则验证错误代码，该代码描述对每个规则谓词或操作的验证失败的情况。</span><span class="sxs-lookup"><span data-stu-id="6f86e-104">The **ErrorCode** element represents a rule validation error code that describes what failed validation for each rule predicate or action.</span></span> 
  
```XML
<ErrorCode/>
```

 <span data-ttu-id="6f86e-105">**RuleValidationErrorCodeType**</span><span class="sxs-lookup"><span data-stu-id="6f86e-105">**RuleValidationErrorCodeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6f86e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6f86e-106">Attributes and elements</span></span>

<span data-ttu-id="6f86e-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6f86e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6f86e-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="6f86e-108">Attributes</span></span>

<span data-ttu-id="6f86e-109">无。</span><span class="sxs-lookup"><span data-stu-id="6f86e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6f86e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="6f86e-110">Child elements</span></span>

<span data-ttu-id="6f86e-111">无。</span><span class="sxs-lookup"><span data-stu-id="6f86e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6f86e-112">父元素</span><span class="sxs-lookup"><span data-stu-id="6f86e-112">Parent elements</span></span>

|<span data-ttu-id="6f86e-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="6f86e-113">**Element**</span></span>|<span data-ttu-id="6f86e-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="6f86e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6f86e-115">Error</span><span class="sxs-lookup"><span data-stu-id="6f86e-115">Error</span></span>](error.md) <br/> |<span data-ttu-id="6f86e-116">表示特定规则属性值、谓词属性值或 action 属性值上的单个验证错误。</span><span class="sxs-lookup"><span data-stu-id="6f86e-116">Represents a single validation error on a particular rule property value, predicate property value, or action property value.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6f86e-117">文本值</span><span class="sxs-lookup"><span data-stu-id="6f86e-117">Text value</span></span>

<span data-ttu-id="6f86e-118">此元素的文本值被限制为以下字符串之一：</span><span class="sxs-lookup"><span data-stu-id="6f86e-118">The text value for this element is restricted to one of the following strings:</span></span>
  
- <span data-ttu-id="6f86e-119">ADOperationFailure</span><span class="sxs-lookup"><span data-stu-id="6f86e-119">ADOperationFailure</span></span>
    
- <span data-ttu-id="6f86e-120">ConnectedAccountNotFound</span><span class="sxs-lookup"><span data-stu-id="6f86e-120">ConnectedAccountNotFound</span></span>
    
- <span data-ttu-id="6f86e-121">CreateWithRuleId</span><span class="sxs-lookup"><span data-stu-id="6f86e-121">CreateWithRuleId</span></span>
    
- <span data-ttu-id="6f86e-122">EmptyValueFound</span><span class="sxs-lookup"><span data-stu-id="6f86e-122">EmptyValueFound</span></span>
    
- <span data-ttu-id="6f86e-123">DuplicatedPriority</span><span class="sxs-lookup"><span data-stu-id="6f86e-123">DuplicatedPriority</span></span>
    
- <span data-ttu-id="6f86e-124">DuplicatedOperationOnTheSameRule</span><span class="sxs-lookup"><span data-stu-id="6f86e-124">DuplicatedOperationOnTheSameRule</span></span>
    
- <span data-ttu-id="6f86e-125">FolderDoesNotExist</span><span class="sxs-lookup"><span data-stu-id="6f86e-125">FolderDoesNotExist</span></span>
    
- <span data-ttu-id="6f86e-126">InvalidAddress</span><span class="sxs-lookup"><span data-stu-id="6f86e-126">InvalidAddress</span></span>
    
- <span data-ttu-id="6f86e-127">InvalidDateRange</span><span class="sxs-lookup"><span data-stu-id="6f86e-127">InvalidDateRange</span></span>
    
- <span data-ttu-id="6f86e-128">InvalidFolderId</span><span class="sxs-lookup"><span data-stu-id="6f86e-128">InvalidFolderId</span></span>
    
- <span data-ttu-id="6f86e-129">InvalidSizeRange</span><span class="sxs-lookup"><span data-stu-id="6f86e-129">InvalidSizeRange</span></span>
    
- <span data-ttu-id="6f86e-130">InvalidValue</span><span class="sxs-lookup"><span data-stu-id="6f86e-130">InvalidValue</span></span>
    
- <span data-ttu-id="6f86e-131">MessageClassificationNotFound</span><span class="sxs-lookup"><span data-stu-id="6f86e-131">MessageClassificationNotFound</span></span>
    
- <span data-ttu-id="6f86e-132">MissingAction</span><span class="sxs-lookup"><span data-stu-id="6f86e-132">MissingAction</span></span>
    
- <span data-ttu-id="6f86e-133">MissingParameter</span><span class="sxs-lookup"><span data-stu-id="6f86e-133">MissingParameter</span></span>
    
- <span data-ttu-id="6f86e-134">MissingRangeValue</span><span class="sxs-lookup"><span data-stu-id="6f86e-134">MissingRangeValue</span></span>
    
- <span data-ttu-id="6f86e-135">NotSettable</span><span class="sxs-lookup"><span data-stu-id="6f86e-135">NotSettable</span></span>
    
- <span data-ttu-id="6f86e-136">RecipientDoesNotExist</span><span class="sxs-lookup"><span data-stu-id="6f86e-136">RecipientDoesNotExist</span></span>
    
- <span data-ttu-id="6f86e-137">RuleNotFound</span><span class="sxs-lookup"><span data-stu-id="6f86e-137">RuleNotFound</span></span>
    
- <span data-ttu-id="6f86e-138">SizeLessThanZero</span><span class="sxs-lookup"><span data-stu-id="6f86e-138">SizeLessThanZero</span></span>
    
- <span data-ttu-id="6f86e-139">StringValueTooBig</span><span class="sxs-lookup"><span data-stu-id="6f86e-139">StringValueTooBig</span></span>
    
- <span data-ttu-id="6f86e-140">UnsupportedAddress</span><span class="sxs-lookup"><span data-stu-id="6f86e-140">UnsupportedAddress</span></span>
    
- <span data-ttu-id="6f86e-141">UnexpectedError</span><span class="sxs-lookup"><span data-stu-id="6f86e-141">UnexpectedError</span></span>
    
- <span data-ttu-id="6f86e-142">UnsupportedRule</span><span class="sxs-lookup"><span data-stu-id="6f86e-142">UnsupportedRule</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6f86e-143">说明</span><span class="sxs-lookup"><span data-stu-id="6f86e-143">Remarks</span></span>

<span data-ttu-id="6f86e-144">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="6f86e-144">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6f86e-145">元素信息</span><span class="sxs-lookup"><span data-stu-id="6f86e-145">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6f86e-146">命名空间</span><span class="sxs-lookup"><span data-stu-id="6f86e-146">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6f86e-147">架构名称</span><span class="sxs-lookup"><span data-stu-id="6f86e-147">Schema Name</span></span>  <br/> |<span data-ttu-id="6f86e-148">消息架构</span><span class="sxs-lookup"><span data-stu-id="6f86e-148">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6f86e-149">验证文件</span><span class="sxs-lookup"><span data-stu-id="6f86e-149">Validation File</span></span>  <br/> |<span data-ttu-id="6f86e-150">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="6f86e-150">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6f86e-151">可以为空</span><span class="sxs-lookup"><span data-stu-id="6f86e-151">Can be Empty</span></span>  <br/> |<span data-ttu-id="6f86e-152">False</span><span class="sxs-lookup"><span data-stu-id="6f86e-152">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6f86e-153">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6f86e-153">See also</span></span>



- [<span data-ttu-id="6f86e-154">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="6f86e-154">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

