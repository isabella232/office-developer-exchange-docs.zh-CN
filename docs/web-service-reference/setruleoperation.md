---
title: SetRuleOperation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SetRuleOperation
api_type:
- schema
ms.assetid: 2106a85b-58fe-49be-b71d-4ca6aa66e060
description: SetRuleOperation 元素表示用于更新现有规则的操作。
ms.openlocfilehash: 96fba2f229003b8c729c36614e69655852a3aa8c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526331"
---
# <a name="setruleoperation"></a><span data-ttu-id="67767-103">SetRuleOperation</span><span class="sxs-lookup"><span data-stu-id="67767-103">SetRuleOperation</span></span>

<span data-ttu-id="67767-104">**SetRuleOperation**元素表示用于更新现有规则的操作。</span><span class="sxs-lookup"><span data-stu-id="67767-104">The **SetRuleOperation** element represents an operation to update an existing rule.</span></span> 
  
[<span data-ttu-id="67767-105">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="67767-105">UpdateInboxRules</span></span>](updateinboxrules.md)
  
[<span data-ttu-id="67767-106">Operations</span><span class="sxs-lookup"><span data-stu-id="67767-106">Operations</span></span>](operations.md)
  
```XML
<SetRuleOperation>
    <Rule/>
</SetRuleOperation>
```

 <span data-ttu-id="67767-107">**SetRuleOperationType**</span><span class="sxs-lookup"><span data-stu-id="67767-107">**SetRuleOperationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="67767-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="67767-108">Attributes and elements</span></span>

<span data-ttu-id="67767-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="67767-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="67767-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="67767-110">Attributes</span></span>

<span data-ttu-id="67767-111">无。</span><span class="sxs-lookup"><span data-stu-id="67767-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="67767-112">子元素</span><span class="sxs-lookup"><span data-stu-id="67767-112">Child elements</span></span>

|<span data-ttu-id="67767-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="67767-113">**Element**</span></span>|<span data-ttu-id="67767-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="67767-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="67767-115">规则 (RuleType)</span><span class="sxs-lookup"><span data-stu-id="67767-115">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="67767-116">代表用户邮箱中的规则。</span><span class="sxs-lookup"><span data-stu-id="67767-116">Represents a rule in a user's mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="67767-117">父元素</span><span class="sxs-lookup"><span data-stu-id="67767-117">Parent elements</span></span>

|<span data-ttu-id="67767-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="67767-118">**Element**</span></span>|<span data-ttu-id="67767-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="67767-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="67767-120">操作</span><span class="sxs-lookup"><span data-stu-id="67767-120">Operations</span></span>](operations.md) <br/> |<span data-ttu-id="67767-121">包含规则的操作，可以在收件箱的一个数组。</span><span class="sxs-lookup"><span data-stu-id="67767-121">Contains an array of rule operations that can be performed on an Inbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="67767-122">文本值</span><span class="sxs-lookup"><span data-stu-id="67767-122">Text value</span></span>

<span data-ttu-id="67767-123">无。</span><span class="sxs-lookup"><span data-stu-id="67767-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="67767-124">说明</span><span class="sxs-lookup"><span data-stu-id="67767-124">Remarks</span></span>

<span data-ttu-id="67767-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="67767-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="67767-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="67767-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="67767-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="67767-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="67767-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="67767-128">Schema Name</span></span>  <br/> |<span data-ttu-id="67767-129">类型架构</span><span class="sxs-lookup"><span data-stu-id="67767-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="67767-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="67767-130">Validation File</span></span>  <br/> |<span data-ttu-id="67767-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="67767-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="67767-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="67767-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="67767-133">False</span><span class="sxs-lookup"><span data-stu-id="67767-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="67767-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="67767-134">See also</span></span>



[<span data-ttu-id="67767-135">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="67767-135">UpdateInboxRules</span></span>](updateinboxrules.md)
  
[<span data-ttu-id="67767-136">DeleteRuleOperation</span><span class="sxs-lookup"><span data-stu-id="67767-136">DeleteRuleOperation</span></span>](deleteruleoperation.md)
  
[<span data-ttu-id="67767-137">CreateRuleOperation</span><span class="sxs-lookup"><span data-stu-id="67767-137">CreateRuleOperation</span></span>](createruleoperation.md)


- [<span data-ttu-id="67767-138">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="67767-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

