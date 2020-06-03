---
title: 参数
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Argument
api_type:
- schema
ms.assetid: 15b0bfb8-2448-4ceb-aeac-965115e0fb72
description: Argument 元素指定操作的参数。
ms.openlocfilehash: 41e3b1d891610669b0cc93f3daf6e8ee98c48396
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464754"
---
# <a name="argument"></a><span data-ttu-id="0870f-103">参数</span><span class="sxs-lookup"><span data-stu-id="0870f-103">Argument</span></span>

<span data-ttu-id="0870f-104">**Argument**元素指定操作的参数。</span><span class="sxs-lookup"><span data-stu-id="0870f-104">The **Argument** element specifies arguments to the action.</span></span> 
  
```xml
<Argument Value=""/>
```

 <span data-ttu-id="0870f-105">**ProtectionRuleArgumentType**</span><span class="sxs-lookup"><span data-stu-id="0870f-105">**ProtectionRuleArgumentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0870f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0870f-106">Attributes and elements</span></span>

<span data-ttu-id="0870f-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0870f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0870f-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="0870f-108">Attributes</span></span>

|<span data-ttu-id="0870f-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="0870f-109">**Attribute**</span></span>|<span data-ttu-id="0870f-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="0870f-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0870f-111">**值**</span><span class="sxs-lookup"><span data-stu-id="0870f-111">**Value**</span></span> <br/> |<span data-ttu-id="0870f-112">一个非空字符串值，表示保护规则的操作部分的参数值。</span><span class="sxs-lookup"><span data-stu-id="0870f-112">A non-empty string value that represents the value of an argument to the action part of a protection rule.</span></span> <span data-ttu-id="0870f-113">此特性是必需的。</span><span class="sxs-lookup"><span data-stu-id="0870f-113">This attribute is required.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0870f-114">子元素</span><span class="sxs-lookup"><span data-stu-id="0870f-114">Child elements</span></span>

<span data-ttu-id="0870f-115">无。</span><span class="sxs-lookup"><span data-stu-id="0870f-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0870f-116">父元素</span><span class="sxs-lookup"><span data-stu-id="0870f-116">Parent elements</span></span>

|<span data-ttu-id="0870f-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="0870f-117">**Element**</span></span>|<span data-ttu-id="0870f-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="0870f-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0870f-119">Action （ProtectionRuleActionType）</span><span class="sxs-lookup"><span data-stu-id="0870f-119">Action (ProtectionRuleActionType)</span></span>](action-protectionruleactiontype.md) <br/> |<span data-ttu-id="0870f-120">确定当规则的条件部分匹配时，必须执行的操作。</span><span class="sxs-lookup"><span data-stu-id="0870f-120">Identifies what action must be executed if the condition part of the rule matches.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0870f-121">文本值</span><span class="sxs-lookup"><span data-stu-id="0870f-121">Text value</span></span>

<span data-ttu-id="0870f-122">无。</span><span class="sxs-lookup"><span data-stu-id="0870f-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0870f-123">说明</span><span class="sxs-lookup"><span data-stu-id="0870f-123">Remarks</span></span>

<span data-ttu-id="0870f-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0870f-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0870f-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="0870f-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0870f-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="0870f-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0870f-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="0870f-127">Schema Name</span></span>  <br/> |<span data-ttu-id="0870f-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="0870f-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="0870f-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="0870f-129">Validation File</span></span>  <br/> |<span data-ttu-id="0870f-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0870f-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0870f-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="0870f-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="0870f-132">False</span><span class="sxs-lookup"><span data-stu-id="0870f-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0870f-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0870f-133">See also</span></span>

- [<span data-ttu-id="0870f-134">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="0870f-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

