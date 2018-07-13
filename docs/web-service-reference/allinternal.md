---
title: AllInternal
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AllInternal
api_type:
- schema
ms.assetid: b7e5072f-5d9f-4ee0-b58b-4d75d878ea1c
description: 如果电子邮件的所有收件人均为发件人组织的内部人员，AllInternal 元素的值为 true。
ms.openlocfilehash: 0ffd4178e711e3117497eed682e3fd3e0594989b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753136"
---
# <a name="allinternal"></a><span data-ttu-id="ca586-103">AllInternal</span><span class="sxs-lookup"><span data-stu-id="ca586-103">AllInternal</span></span>

<span data-ttu-id="ca586-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 如果电子邮件的所有收件人均为发件人组织的内部人员， **AllInternal** 元素的值为 **true**。</span><span class="sxs-lookup"><span data-stu-id="ca586-104">The **AllInternal** element evaluates to **true** if all recipients of an e-mail message are internal to the sender's organization.</span></span> 
  
```xml
<AllInternal/>
```

 <span data-ttu-id="ca586-105">**ProtectionRuleAllInternalType**</span><span class="sxs-lookup"><span data-stu-id="ca586-105">**ProtectionRuleAllInternalType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ca586-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ca586-106">Attributes and elements</span></span>

<span data-ttu-id="ca586-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ca586-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ca586-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="ca586-108">Attributes</span></span>

<span data-ttu-id="ca586-109">无。</span><span class="sxs-lookup"><span data-stu-id="ca586-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ca586-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ca586-110">Child elements</span></span>

<span data-ttu-id="ca586-111">无。</span><span class="sxs-lookup"><span data-stu-id="ca586-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ca586-112">父元素</span><span class="sxs-lookup"><span data-stu-id="ca586-112">Parent elements</span></span>

|<span data-ttu-id="ca586-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="ca586-113">**Element**</span></span>|<span data-ttu-id="ca586-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="ca586-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ca586-115">条件</span><span class="sxs-lookup"><span data-stu-id="ca586-115">Condition</span></span>](condition.md) <br/> |<span data-ttu-id="ca586-116">确定要执行该规则的操作部分必须满足的条件。</span><span class="sxs-lookup"><span data-stu-id="ca586-116">Identifies the condition that must be satisfied for the action part of the rule to be executed.</span></span>  <br/> |
|[<span data-ttu-id="ca586-117">和 (ProtectionRuleAndType)</span><span class="sxs-lookup"><span data-stu-id="ca586-117">And (ProtectionRuleAndType)</span></span>](and-protectionruleandtype.md) <br/> |<span data-ttu-id="ca586-118">指定所有子元素都必须匹配以使值为 **true**。</span><span class="sxs-lookup"><span data-stu-id="ca586-118">Specifies that all child elements must match to evaluate to **true**.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ca586-119">文本值</span><span class="sxs-lookup"><span data-stu-id="ca586-119">Text value</span></span>

<span data-ttu-id="ca586-120">**AllInternal** 元素必须为空。</span><span class="sxs-lookup"><span data-stu-id="ca586-120">The **AllInternal** element must be empty.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ca586-121">说明</span><span class="sxs-lookup"><span data-stu-id="ca586-121">Remarks</span></span>

<span data-ttu-id="ca586-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ca586-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ca586-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="ca586-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ca586-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="ca586-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ca586-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="ca586-125">Schema Name</span></span>  <br/> |<span data-ttu-id="ca586-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="ca586-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="ca586-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="ca586-127">Validation File</span></span>  <br/> |<span data-ttu-id="ca586-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ca586-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ca586-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="ca586-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="ca586-130">False</span><span class="sxs-lookup"><span data-stu-id="ca586-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ca586-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ca586-131">See also</span></span>

- [<span data-ttu-id="ca586-132">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="ca586-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

