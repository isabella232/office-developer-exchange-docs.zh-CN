---
title: 值 (ProtectionRuleValueType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Value
api_type:
- schema
ms.assetid: b039bd6e-2198-47cf-9c78-a5e8b9d51c98
description: Value 元素标识单个收件人或发件人部门。
ms.openlocfilehash: 6173f94dcfb83eafd62e35f185a5e8c669d50f6c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838511"
---
# <a name="value-protectionrulevaluetype"></a><span data-ttu-id="997e5-103">值 (ProtectionRuleValueType)</span><span class="sxs-lookup"><span data-stu-id="997e5-103">Value (ProtectionRuleValueType)</span></span>

<span data-ttu-id="997e5-104">**Value**元素标识单个收件人或发件人部门。</span><span class="sxs-lookup"><span data-stu-id="997e5-104">The **Value** element identifies a single recipient or sender department.</span></span> 
  
```XML
<Value/>
```

<span data-ttu-id="997e5-105">**ProtectionRuleValueType**</span><span class="sxs-lookup"><span data-stu-id="997e5-105">**ProtectionRuleValueType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="997e5-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="997e5-106">Attributes and elements</span></span>

<span data-ttu-id="997e5-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="997e5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="997e5-108">属性</span><span class="sxs-lookup"><span data-stu-id="997e5-108">Attributes</span></span>

<span data-ttu-id="997e5-109">无。</span><span class="sxs-lookup"><span data-stu-id="997e5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="997e5-110">子元素</span><span class="sxs-lookup"><span data-stu-id="997e5-110">Child elements</span></span>

<span data-ttu-id="997e5-111">无。</span><span class="sxs-lookup"><span data-stu-id="997e5-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="997e5-112">父元素</span><span class="sxs-lookup"><span data-stu-id="997e5-112">Parent elements</span></span>

|<span data-ttu-id="997e5-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="997e5-113">**Element**</span></span>|<span data-ttu-id="997e5-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="997e5-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="997e5-115">RecipientIs</span><span class="sxs-lookup"><span data-stu-id="997e5-115">RecipientIs</span></span>](recipientis.md) <br/> |<span data-ttu-id="997e5-116">指定任何收件人的电子邮件匹配的任何子**值**元素中指定的收件人。</span><span class="sxs-lookup"><span data-stu-id="997e5-116">Specifies that any recipient of the email message matches any of the specified recipients in the child **Value** elements.</span></span>  <br/> |
|[<span data-ttu-id="997e5-117">SenderDepartments</span><span class="sxs-lookup"><span data-stu-id="997e5-117">SenderDepartments</span></span>](senderdepartments.md) <br/> |<span data-ttu-id="997e5-118">指定发件人的部门匹配任何子**值**元素中指定的部门。</span><span class="sxs-lookup"><span data-stu-id="997e5-118">Specifies that the department of the sender matches any of the specified departments in the child **Value** elements.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="997e5-119">文本值</span><span class="sxs-lookup"><span data-stu-id="997e5-119">Text value</span></span>

<span data-ttu-id="997e5-120">此元素必须包含一个非空字符串值。</span><span class="sxs-lookup"><span data-stu-id="997e5-120">This element must contain a nonempty string value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="997e5-121">备注</span><span class="sxs-lookup"><span data-stu-id="997e5-121">Remarks</span></span>

<span data-ttu-id="997e5-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="997e5-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="997e5-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="997e5-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="997e5-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="997e5-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="997e5-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="997e5-125">Schema Name</span></span>  <br/> |<span data-ttu-id="997e5-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="997e5-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="997e5-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="997e5-127">Validation File</span></span>  <br/> |<span data-ttu-id="997e5-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="997e5-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="997e5-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="997e5-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="997e5-130">False</span><span class="sxs-lookup"><span data-stu-id="997e5-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="997e5-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="997e5-131">See also</span></span>

- [<span data-ttu-id="997e5-132">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="997e5-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

