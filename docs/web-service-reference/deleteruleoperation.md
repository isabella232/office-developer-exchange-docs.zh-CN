---
title: DeleteRuleOperation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteRuleOperation
api_type:
- schema
ms.assetid: c5e251af-f795-43cc-baaf-95d84475677c
description: DeleteRuleOperation 元素包含一个删除现有 "收件箱" 规则的操作。
ms.openlocfilehash: 6b17f7f99f1fd9b9889db00fdf55fba5eef5aba8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526919"
---
# <a name="deleteruleoperation"></a><span data-ttu-id="0c852-103">DeleteRuleOperation</span><span class="sxs-lookup"><span data-stu-id="0c852-103">DeleteRuleOperation</span></span>

<span data-ttu-id="0c852-104">**DeleteRuleOperation**元素包含一个删除现有 "收件箱" 规则的操作。</span><span class="sxs-lookup"><span data-stu-id="0c852-104">The **DeleteRuleOperation** element contains an operation to delete an existing Inbox rule.</span></span> 
  
- [<span data-ttu-id="0c852-105">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="0c852-105">UpdateInboxRules</span></span>](updateinboxrules.md)
- [<span data-ttu-id="0c852-106">Operations</span><span class="sxs-lookup"><span data-stu-id="0c852-106">Operations</span></span>](operations.md)
  
```XML
<DeleteRuleOperation>
    <RuleId/>
</DeleteRuleOperation>
```

 <span data-ttu-id="0c852-107">**DeleteRuleOperationType**</span><span class="sxs-lookup"><span data-stu-id="0c852-107">**DeleteRuleOperationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0c852-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0c852-108">Attributes and elements</span></span>

<span data-ttu-id="0c852-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0c852-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0c852-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="0c852-110">Attributes</span></span>

<span data-ttu-id="0c852-111">无。</span><span class="sxs-lookup"><span data-stu-id="0c852-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0c852-112">子元素</span><span class="sxs-lookup"><span data-stu-id="0c852-112">Child elements</span></span>

|<span data-ttu-id="0c852-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="0c852-113">**Element**</span></span>|<span data-ttu-id="0c852-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="0c852-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0c852-115">RuleId</span><span class="sxs-lookup"><span data-stu-id="0c852-115">RuleId</span></span>](ruleid.md) <br/> |<span data-ttu-id="0c852-116">指定要删除的规则的标识符。</span><span class="sxs-lookup"><span data-stu-id="0c852-116">Specifies the identifier of the rule to delete.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0c852-117">父元素</span><span class="sxs-lookup"><span data-stu-id="0c852-117">Parent elements</span></span>

|<span data-ttu-id="0c852-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="0c852-118">**Element**</span></span>|<span data-ttu-id="0c852-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="0c852-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0c852-120">操作</span><span class="sxs-lookup"><span data-stu-id="0c852-120">Operations</span></span>](operations.md) <br/> |<span data-ttu-id="0c852-121">包含规则的操作，可以在收件箱的一个数组。</span><span class="sxs-lookup"><span data-stu-id="0c852-121">Contains an array of rule operations that can be performed on an Inbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0c852-122">文本值</span><span class="sxs-lookup"><span data-stu-id="0c852-122">Text value</span></span>

<span data-ttu-id="0c852-123">无。</span><span class="sxs-lookup"><span data-stu-id="0c852-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0c852-124">说明</span><span class="sxs-lookup"><span data-stu-id="0c852-124">Remarks</span></span>

<span data-ttu-id="0c852-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0c852-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0c852-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="0c852-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0c852-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="0c852-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0c852-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="0c852-128">Schema Name</span></span>  <br/> |<span data-ttu-id="0c852-129">类型架构</span><span class="sxs-lookup"><span data-stu-id="0c852-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="0c852-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="0c852-130">Validation File</span></span>  <br/> |<span data-ttu-id="0c852-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0c852-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0c852-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="0c852-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="0c852-133">False</span><span class="sxs-lookup"><span data-stu-id="0c852-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0c852-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0c852-134">See also</span></span>

- [<span data-ttu-id="0c852-135">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="0c852-135">UpdateInboxRules</span></span>](updateinboxrules.md) 
- [<span data-ttu-id="0c852-136">SetRuleOperation</span><span class="sxs-lookup"><span data-stu-id="0c852-136">SetRuleOperation</span></span>](setruleoperation.md) 
- [<span data-ttu-id="0c852-137">CreateRuleOperation</span><span class="sxs-lookup"><span data-stu-id="0c852-137">CreateRuleOperation</span></span>](createruleoperation.md)
- [<span data-ttu-id="0c852-138">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="0c852-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

