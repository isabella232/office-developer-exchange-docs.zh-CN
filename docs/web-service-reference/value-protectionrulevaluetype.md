---
title: Value （ProtectionRuleValueType）
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
ms.openlocfilehash: 908ea451800abc343fb6e4d4a4ed98d57223bd23
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465238"
---
# <a name="value-protectionrulevaluetype"></a><span data-ttu-id="21672-103">Value （ProtectionRuleValueType）</span><span class="sxs-lookup"><span data-stu-id="21672-103">Value (ProtectionRuleValueType)</span></span>

<span data-ttu-id="21672-104">**Value**元素标识单个收件人或发件人部门。</span><span class="sxs-lookup"><span data-stu-id="21672-104">The **Value** element identifies a single recipient or sender department.</span></span> 
  
```XML
<Value/>
```

<span data-ttu-id="21672-105">**ProtectionRuleValueType**</span><span class="sxs-lookup"><span data-stu-id="21672-105">**ProtectionRuleValueType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="21672-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="21672-106">Attributes and elements</span></span>

<span data-ttu-id="21672-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="21672-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="21672-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="21672-108">Attributes</span></span>

<span data-ttu-id="21672-109">无。</span><span class="sxs-lookup"><span data-stu-id="21672-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="21672-110">子元素</span><span class="sxs-lookup"><span data-stu-id="21672-110">Child elements</span></span>

<span data-ttu-id="21672-111">无。</span><span class="sxs-lookup"><span data-stu-id="21672-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="21672-112">父元素</span><span class="sxs-lookup"><span data-stu-id="21672-112">Parent elements</span></span>

|<span data-ttu-id="21672-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="21672-113">**Element**</span></span>|<span data-ttu-id="21672-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="21672-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="21672-115">收件人是</span><span class="sxs-lookup"><span data-stu-id="21672-115">RecipientIs</span></span>](recipientis.md) <br/> |<span data-ttu-id="21672-116">指定电子邮件的任何收件人与子**值**元素中的任何指定收件人相匹配。</span><span class="sxs-lookup"><span data-stu-id="21672-116">Specifies that any recipient of the email message matches any of the specified recipients in the child **Value** elements.</span></span>  <br/> |
|[<span data-ttu-id="21672-117">SenderDepartments</span><span class="sxs-lookup"><span data-stu-id="21672-117">SenderDepartments</span></span>](senderdepartments.md) <br/> |<span data-ttu-id="21672-118">指定发件人的部门与子**值**元素中的任何指定的部门相匹配。</span><span class="sxs-lookup"><span data-stu-id="21672-118">Specifies that the department of the sender matches any of the specified departments in the child **Value** elements.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="21672-119">文本值</span><span class="sxs-lookup"><span data-stu-id="21672-119">Text value</span></span>

<span data-ttu-id="21672-120">此元素必须包含非空的字符串值。</span><span class="sxs-lookup"><span data-stu-id="21672-120">This element must contain a nonempty string value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="21672-121">说明</span><span class="sxs-lookup"><span data-stu-id="21672-121">Remarks</span></span>

<span data-ttu-id="21672-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="21672-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="21672-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="21672-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="21672-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="21672-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="21672-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="21672-125">Schema Name</span></span>  <br/> |<span data-ttu-id="21672-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="21672-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="21672-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="21672-127">Validation File</span></span>  <br/> |<span data-ttu-id="21672-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="21672-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="21672-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="21672-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="21672-130">False</span><span class="sxs-lookup"><span data-stu-id="21672-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="21672-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="21672-131">See also</span></span>

- [<span data-ttu-id="21672-132">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="21672-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

