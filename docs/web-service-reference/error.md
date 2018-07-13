---
title: 错误
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Error
api_type:
- schema
ms.assetid: b1f54673-578a-496b-99f5-0fde2c669278
description: Error 元素表示特定规则属性值、谓词属性值或操作属性值上的单一验证错误。
ms.openlocfilehash: adb2de56b7610aa92b5bf5b8d43ac22f35021b64
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754147"
---
# <a name="error"></a><span data-ttu-id="bb08e-103">错误</span><span class="sxs-lookup"><span data-stu-id="bb08e-103">Error</span></span>

<span data-ttu-id="bb08e-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **Error** 元素表示特定规则属性值、谓词属性值或操作属性值上的单一验证错误。</span><span class="sxs-lookup"><span data-stu-id="bb08e-104">The **Error** element represents a single validation error on a particular rule property value, predicate property value, or action property value.</span></span> 
  
```XML
<Error>
   <FieldUri/>
   <ErrorCode/>
   <ErrorMessage/>
   <FieldValue/>
</Error>
```

 <span data-ttu-id="bb08e-105">**RuleValidationErrorType**</span><span class="sxs-lookup"><span data-stu-id="bb08e-105">**RuleValidationErrorType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bb08e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="bb08e-106">Attributes and elements</span></span>

<span data-ttu-id="bb08e-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="bb08e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bb08e-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="bb08e-108">Attributes</span></span>

<span data-ttu-id="bb08e-109">无。</span><span class="sxs-lookup"><span data-stu-id="bb08e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bb08e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="bb08e-110">Child elements</span></span>

|<span data-ttu-id="bb08e-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="bb08e-111">**Element**</span></span>|<span data-ttu-id="bb08e-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="bb08e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bb08e-113">FieldUri (规则)</span><span class="sxs-lookup"><span data-stu-id="bb08e-113">FieldUri (Rule)</span></span>](fielduri-rule.md) <br/> |<span data-ttu-id="bb08e-114">指定指向导致验证错误的规则字段的 URI。</span><span class="sxs-lookup"><span data-stu-id="bb08e-114">Specifies the URI to the rule field that caused the validation error.</span></span>  <br/> |
|[<span data-ttu-id="bb08e-115">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="bb08e-115">errorCode</span></span>](errorcode.md) <br/> |<span data-ttu-id="bb08e-116">表示规则验证错误代码，该代码描述是什么造成了每个规则谓词或操作验证失败。</span><span class="sxs-lookup"><span data-stu-id="bb08e-116">Represents a rule validation error code that describes what failed validation for each rule predicate or action.</span></span>  <br/> |
|[<span data-ttu-id="bb08e-117">ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="bb08e-117">Error.message</span></span>](errormessage.md) <br/> |<span data-ttu-id="bb08e-118">表示验证错误的原因。</span><span class="sxs-lookup"><span data-stu-id="bb08e-118">Represents the reason for the validation error.</span></span>  <br/> |
|[<span data-ttu-id="bb08e-119">FieldValue</span><span class="sxs-lookup"><span data-stu-id="bb08e-119">fieldValue</span></span>](fieldvalue.md) <br/> |<span data-ttu-id="bb08e-120">表示导致验证错误的字段值。</span><span class="sxs-lookup"><span data-stu-id="bb08e-120">Represents the value of the field that caused the validation error.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bb08e-121">父元素</span><span class="sxs-lookup"><span data-stu-id="bb08e-121">Parent elements</span></span>

|<span data-ttu-id="bb08e-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="bb08e-122">**Element**</span></span>|<span data-ttu-id="bb08e-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="bb08e-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bb08e-124">ValidationErrors</span><span class="sxs-lookup"><span data-stu-id="bb08e-124">validationErrors</span></span>](validationerrors.md) <br/> |<span data-ttu-id="bb08e-125">表示每个出错的规则字段上的规则验证错误数组。</span><span class="sxs-lookup"><span data-stu-id="bb08e-125">Represents an array of rule validation errors on each rule field that has an error.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="bb08e-126">文本值</span><span class="sxs-lookup"><span data-stu-id="bb08e-126">Text value</span></span>

<span data-ttu-id="bb08e-127">无。</span><span class="sxs-lookup"><span data-stu-id="bb08e-127">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bb08e-128">说明</span><span class="sxs-lookup"><span data-stu-id="bb08e-128">Remarks</span></span>

<span data-ttu-id="bb08e-129">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="bb08e-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bb08e-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="bb08e-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bb08e-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="bb08e-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="bb08e-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="bb08e-132">Schema Name</span></span>  <br/> |<span data-ttu-id="bb08e-133">消息架构</span><span class="sxs-lookup"><span data-stu-id="bb08e-133">Messages schema</span></span>  <br/> |
|<span data-ttu-id="bb08e-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="bb08e-134">Validation File</span></span>  <br/> |<span data-ttu-id="bb08e-135">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="bb08e-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="bb08e-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="bb08e-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="bb08e-137">True</span><span class="sxs-lookup"><span data-stu-id="bb08e-137">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bb08e-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bb08e-138">See also</span></span>



- [<span data-ttu-id="bb08e-139">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="bb08e-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

