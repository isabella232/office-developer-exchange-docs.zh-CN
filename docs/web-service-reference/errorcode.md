---
title: 错误代码
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0bb00cee-c66b-4f34-b99d-355458f5e83b
description: ErrorCode 元素均表示描述什么失败规则验证错误代码为每个规则谓词或操作的验证。
ms.openlocfilehash: ed8e2fa72b0eb007925742e6d194f3a391b3f3cb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754152"
---
# <a name="errorcode"></a><span data-ttu-id="9a254-103">错误代码</span><span class="sxs-lookup"><span data-stu-id="9a254-103">ErrorCode</span></span>

<span data-ttu-id="9a254-104">**ErrorCode**元素均表示描述什么失败规则验证错误代码为每个规则谓词或操作的验证。</span><span class="sxs-lookup"><span data-stu-id="9a254-104">The **ErrorCode** element represents a rule validation error code that describes what failed validation for each rule predicate or action.</span></span> 
  
```XML
<ErrorCode/>
```

 <span data-ttu-id="9a254-105">**RuleValidationErrorCodeType**</span><span class="sxs-lookup"><span data-stu-id="9a254-105">**RuleValidationErrorCodeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9a254-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9a254-106">Attributes and elements</span></span>

<span data-ttu-id="9a254-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9a254-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9a254-108">属性</span><span class="sxs-lookup"><span data-stu-id="9a254-108">Attributes</span></span>

<span data-ttu-id="9a254-109">无。</span><span class="sxs-lookup"><span data-stu-id="9a254-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9a254-110">子元素</span><span class="sxs-lookup"><span data-stu-id="9a254-110">Child elements</span></span>

<span data-ttu-id="9a254-111">无。</span><span class="sxs-lookup"><span data-stu-id="9a254-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9a254-112">父元素</span><span class="sxs-lookup"><span data-stu-id="9a254-112">Parent elements</span></span>

|<span data-ttu-id="9a254-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="9a254-113">**Element**</span></span>|<span data-ttu-id="9a254-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="9a254-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9a254-115">Error</span><span class="sxs-lookup"><span data-stu-id="9a254-115">Error</span></span>](error.md) <br/> |<span data-ttu-id="9a254-116">代表对特定规则属性值、 谓词属性值或 action 属性值的单个验证错误。</span><span class="sxs-lookup"><span data-stu-id="9a254-116">Represents a single validation error on a particular rule property value, predicate property value, or action property value.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9a254-117">文本值</span><span class="sxs-lookup"><span data-stu-id="9a254-117">Text value</span></span>

<span data-ttu-id="9a254-118">此元素的文本值仅限于以下字符串之一：</span><span class="sxs-lookup"><span data-stu-id="9a254-118">The text value for this element is restricted to one of the following strings:</span></span>
  
- <span data-ttu-id="9a254-119">ADOperationFailure</span><span class="sxs-lookup"><span data-stu-id="9a254-119">ADOperationFailure</span></span>
    
- <span data-ttu-id="9a254-120">ConnectedAccountNotFound</span><span class="sxs-lookup"><span data-stu-id="9a254-120">ConnectedAccountNotFound</span></span>
    
- <span data-ttu-id="9a254-121">CreateWithRuleId</span><span class="sxs-lookup"><span data-stu-id="9a254-121">CreateWithRuleId</span></span>
    
- <span data-ttu-id="9a254-122">EmptyValueFound</span><span class="sxs-lookup"><span data-stu-id="9a254-122">EmptyValueFound</span></span>
    
- <span data-ttu-id="9a254-123">DuplicatedPriority</span><span class="sxs-lookup"><span data-stu-id="9a254-123">DuplicatedPriority</span></span>
    
- <span data-ttu-id="9a254-124">DuplicatedOperationOnTheSameRule</span><span class="sxs-lookup"><span data-stu-id="9a254-124">DuplicatedOperationOnTheSameRule</span></span>
    
- <span data-ttu-id="9a254-125">FolderDoesNotExist</span><span class="sxs-lookup"><span data-stu-id="9a254-125">FolderDoesNotExist</span></span>
    
- <span data-ttu-id="9a254-126">InvalidAddress</span><span class="sxs-lookup"><span data-stu-id="9a254-126">InvalidAddress</span></span>
    
- <span data-ttu-id="9a254-127">InvalidDateRange</span><span class="sxs-lookup"><span data-stu-id="9a254-127">InvalidDateRange</span></span>
    
- <span data-ttu-id="9a254-128">InvalidFolderId</span><span class="sxs-lookup"><span data-stu-id="9a254-128">InvalidFolderId</span></span>
    
- <span data-ttu-id="9a254-129">InvalidSizeRange</span><span class="sxs-lookup"><span data-stu-id="9a254-129">InvalidSizeRange</span></span>
    
- <span data-ttu-id="9a254-130">InvalidValue</span><span class="sxs-lookup"><span data-stu-id="9a254-130">InvalidValue</span></span>
    
- <span data-ttu-id="9a254-131">MessageClassificationNotFound</span><span class="sxs-lookup"><span data-stu-id="9a254-131">MessageClassificationNotFound</span></span>
    
- <span data-ttu-id="9a254-132">MissingAction</span><span class="sxs-lookup"><span data-stu-id="9a254-132">MissingAction</span></span>
    
- <span data-ttu-id="9a254-133">MissingParameter</span><span class="sxs-lookup"><span data-stu-id="9a254-133">MissingParameter</span></span>
    
- <span data-ttu-id="9a254-134">MissingRangeValue</span><span class="sxs-lookup"><span data-stu-id="9a254-134">MissingRangeValue</span></span>
    
- <span data-ttu-id="9a254-135">NotSettable</span><span class="sxs-lookup"><span data-stu-id="9a254-135">NotSettable</span></span>
    
- <span data-ttu-id="9a254-136">RecipientDoesNotExist</span><span class="sxs-lookup"><span data-stu-id="9a254-136">RecipientDoesNotExist</span></span>
    
- <span data-ttu-id="9a254-137">RuleNotFound</span><span class="sxs-lookup"><span data-stu-id="9a254-137">RuleNotFound</span></span>
    
- <span data-ttu-id="9a254-138">SizeLessThanZero</span><span class="sxs-lookup"><span data-stu-id="9a254-138">SizeLessThanZero</span></span>
    
- <span data-ttu-id="9a254-139">StringValueTooBig</span><span class="sxs-lookup"><span data-stu-id="9a254-139">StringValueTooBig</span></span>
    
- <span data-ttu-id="9a254-140">UnsupportedAddress</span><span class="sxs-lookup"><span data-stu-id="9a254-140">UnsupportedAddress</span></span>
    
- <span data-ttu-id="9a254-141">UnexpectedError</span><span class="sxs-lookup"><span data-stu-id="9a254-141">UnexpectedError</span></span>
    
- <span data-ttu-id="9a254-142">UnsupportedRule</span><span class="sxs-lookup"><span data-stu-id="9a254-142">UnsupportedRule</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9a254-143">备注</span><span class="sxs-lookup"><span data-stu-id="9a254-143">Remarks</span></span>

<span data-ttu-id="9a254-144">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9a254-144">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9a254-145">元素信息</span><span class="sxs-lookup"><span data-stu-id="9a254-145">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9a254-146">命名空间</span><span class="sxs-lookup"><span data-stu-id="9a254-146">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9a254-147">架构名称</span><span class="sxs-lookup"><span data-stu-id="9a254-147">Schema Name</span></span>  <br/> |<span data-ttu-id="9a254-148">消息架构</span><span class="sxs-lookup"><span data-stu-id="9a254-148">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9a254-149">验证文件</span><span class="sxs-lookup"><span data-stu-id="9a254-149">Validation File</span></span>  <br/> |<span data-ttu-id="9a254-150">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9a254-150">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9a254-151">可以为空</span><span class="sxs-lookup"><span data-stu-id="9a254-151">Can be Empty</span></span>  <br/> |<span data-ttu-id="9a254-152">False</span><span class="sxs-lookup"><span data-stu-id="9a254-152">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9a254-153">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9a254-153">See also</span></span>



- [<span data-ttu-id="9a254-154">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="9a254-154">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

